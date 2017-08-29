# Blockchain.GetAccount Method (byte[])

Returns an account (address) based on the hash of the contract scripthash.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Account GetAccount(byte[] script_hash)
```

Parameters: Scripthash as a byte array of length 20.

Return Value: [Account](../Account.md).

## Example

```c#
public class Contract1: FunctionCode
{
    public static void Main()
    {
        byte[] scriptHash = {36, 23, 241, 177, 228, 54, 109, 223, 27, 237, 139, 54, 207, 38, 132, 101, 172, 3, 10, 73};
        Account acc = Blockchain.GetAccount(scriptHash);
    }
}
```
The scripthash can be obtained in advanced and passed as a parameter into smart contracts. The following code uses the SDK to convert an address into scripthash.

```c#
Static void Main(string[] args)
{
    byte[] scriptHash = FRS.Wallets.Wallet.ToScriptHash("AK4if54jXjSiJBs6jkfZjxAastauJtjjse").ToArray();
}
```



[Back](../Blockchain.md)
