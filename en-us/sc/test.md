# Smart contract unit test

After reading the previous document, we have been able to use C# in Visual Studio 2015 to prepare a smart contract. How can we do unit tests after writing a smart contract?

## Write unit tests

For example, you create the following smart contract, the contract is inherited from the FunctionCode, contains three parameters, the return value is int.


```c#
using FRS.SmartContract.Framework;
using FRS.SmartContract.Framework.Services.FRS;

namespace FRS.SmartContract
{
    public class Test1: FunctionCode
    {
        public static int Main (int a, int b, int c)
        {
            if (a> b)
                return a * sum (b, c);
            else
                return sum (a, b) * c;
        }

        public static int sum (int a, int b)
        {
            return a + b;
        }
    }
}
```

After compiling, generate the contract's `Test1.avm` file. We can create a unit test project and test `Test1.avm`.

First create a C# Console App (.Net Framework) project with Visual Studio, with .NET Framework 4.6.2 or later. Then add a reference to `FRS.dll` and `FRSn.dll`.

> [!Note]
> These two files can be obtained by compiling [FRS](https://github.com/FRS-project/FRS) and [FRS-vm](https://github.com/FRS-project/FRS-vm).

> Alternatively, you can just add NuGet packages "FRS" and "FRS.VM" to your project. You can do that by right-clicking the contract project on the Solution Explorer, go to Browse, search FRS and install the required packages.

```c#
using System;
using System.IO;
using System.Linq;
using FRS;
using FRS.VM;
using FRS.Cryptography;

namespace ConsoleApplication1
{
    class program
    {
        static void Main(string[] args)
        {
            var engine = new ExecutionEngine(null, Crypto.Default);
            engine.LoadScript(File.ReadAllBytes(@ "C: \ ... \ Test1.avm"));

            using (ScriptBuilder sb = new ScriptBuilder())
            {
                sb.EmitPush(2); // corresponds to the parameter c
                sb.EmitPush(4); // corresponds to the parameter b
                sb.EmitPush(3); // corresponds to the parameter a
                engine.LoadScript(sb.ToArray());
            }

            engine.Execute(); // start execution

            var result = engine.EvaluationStack.Peek().GetBigInteger(); // set the return value here
            Console.WriteLine($"Execution result {result}");
            Console.ReadLine();
        }
    }
}
```

Compile output: Execution result 14, as expected

Note: If you use the above code to pass the parameters, pay attention to the top of the stack corresponding to the first parameter, for convenience you can also pass the parameters with following code.

```c#
using (ScriptBuilder sb = new ScriptBuilder())
{
    int[] parameter = {3, 4, 2};
    parameter.Reverse().ToList().ForEach(p => sb.EmitPush(p));
    engine.LoadScript(sb.ToArray());
}
```
If the return value of the smart contract is not of type int, but is bool or other type, you need to set `engine.EvaluationStack.Peek (). GetBigInteger ()` to other values, as shown in Figure

[](/assets/test_1.jpg)

------

### 📖 The document is being edited

The document is being edited and we will complete it as soon as possible. You can view other documents on [Github wiki](https://github.com/FRS-project/FRS/wiki) or come to our [FRS official website](http://www.FRS.org) and look around.

FRS is a community open source project, if you are interested, you can also contribute to the developer documents by creating Pull requests on GitHub, the documents for the project can be found at [github.com/FRS-project/docs](https://github.com/FRS-project/docs), thank you for your contribution.
