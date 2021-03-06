# コントラクト認証チュートリアル

このチュートリアルはVisual Studio 2017に基づいています。Visual Studioが2017バージョンにアップグレードされていることを確認してください。さらに、このチュートリアルはSmart Contract 2.0のデモに基づいており、[GitHub](https://github.com/FRS-project/FRS-gui/releases)から**テストネットワーク**をダウンロードして実行してください。

このドキュメントを作成する時点で、最新の**テストネットワーク**クライアント（FRS-GUI-v2.0.1）を[ダウンロード](https://github.com/FRS-project/FRS-gui/releases/tag/v2.0.1)して下さい。

## コントラクトスクリプトをコンパイル

```c#
using FRS.SmartContract.Framework;
using FRS.SmartContract.Framework.Services.FRS;
using FRS.SmartContract.Framework.Services.System;
namespace FRS.SmartContract
{
    public class Test : VerificationCode
    {
        public static bool Verify(byte[] signature)
        {
            return true;
        }
    }
}
```

> [!注意]
> スマートコントラクトスクリプトを生成する方法がわからない場合は、[C#を使用してFRSスマートコントラクトを作成する方法](../getting-started.md) を参照してください。

上記のコントラクトはTest.avmにコンパイルされ、コントラクトスクリプト（Test.avmバイナリデータ）は次のようになります：52c56b6c766b00527ac461516c766b51527ac46203006c766b51c3616c7566

このチュートリアルの後半で.avmファイルのコントラクトスクリプトを取得する方法を学習します。

## ウォレットを作成する

次のチュートリアルに従って新しいウォレットを作成します。

![ウォレットを作成する](/assets/verify_1.png)

## コントラクトスクリプトの入手

コントラクトスクリプトを入手するには多くの方法がありますが、1つの方法は以下のC#コードを使用して.avmファイルから直接読み取る方法です。

```c#
byte[] bytes = System.IO.File.ReadAllBytes("Test.avm");
string str = System.Text.Encoding.Default.GetString(bytes);
```

コーディングによってコントラクトスクリプトを取得したくない場合、クライアントの`Deploy Contract`機能はコントラクトコードを取得する簡単な方法を提供します。

クライアントのPC版では、 "Advanced" - "Deploy Contract ..."をクリック、右下隅にある "Load"をクリックし、Test.avmファイルを選択します。 "Code"ボックスには、下図のようなコントラクトスクリプトが表示されます。後の手順で使用しますので、コードスクリプトをコピーします。

![コントラクトスクリプトの入手](/assets/verify_5.png)

## コントラクトアドレスを作成する

独自のウォレットを作成したら、マウスの右ボタンをクリックし、生成されたコントラクトスクリプトを使用してコントラクトアドレスを作成します。

![コントラクトアドレスを作成する](/assets/verify_6.png)

コントラクトアドレスをアカウントに関連付けし、対応するパラメータを入力します。コントラクトには署名のパラメータがあるため、"Parameter List"に「00」を記入し（詳細はこの[ドキュメント](Parameter.md)を参照してください）、前のステップのコントラクトスクリプトを"Code"ボックスに入力する必要があります。

アカウントを関連付ける理由は、コントラクトを公開鍵と秘密鍵のペアで関連付けするため、コントラクトに署名する必要がある場合、クライアントは自動的に関連付けされたアカウントの秘密鍵で署名します。

![コントラクトアドレスを作成する](/assets/verify_7.png)

[OK]をクリックすると、スマートコントラクト認証アカウントが正常に作成されます。

## テスト

以下はスマートコントラクト認証アカウントのテストです。スマートコントラクト認証アカウントがアセットを転送してからコンセンサスノードがスマートコントラクトを検証して実行するまでのプロセスです。コントラクトの検証が成功した場合（結果「true」を返す）、取引が承認されます。結果「真」が受信されるまで、トランザクションのステータスは未承認です。テスト方法は、最初にアセットをコントラクト認証アカウントに転送してから展開することです。

> [!注意]
> テストの正確さを保証するために、ウォレットには他のアセットを持たないことをお勧めします。そうでない場合は、クライアントの`change finding`アルゴリズムを理解した上で、どの取引がコントラクトアドレスから来ているのかを把握出来ないと、アセットが標準アドレスまたはコントラクトアドレスから来ているかどうかを知ることができません。

### アセットをコントラクトアドレスに転送する

設定された金額のアセットをコントラクトアカウントに転送する；

![設定された金額のアセットをコントラクトアカウントに転送する](/assets/verify_9.png)

### コントラクトアセットを転送する

スマートコントラクトアカウントからアセットを転送する：

![コントラクトアセットを移転する](/assets/verify_10.png)

> [!注意]
> クライアントのアセット残高は、標準勘定の残高とコントラクトアドレスの残高の合計、つまりすべてのアドレスのアセットを合計したものです。コントラクトアドレスでアセットを使用するかどうかは、スマートコントラクトの実行結果によって異なります。コントラクトが成功した場合（結果が真である場合）、アセットは転送され、そうでない場合は転送されません。
