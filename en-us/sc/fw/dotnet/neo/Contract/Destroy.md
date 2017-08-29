# Contract.Destroy Method ()

Destruction of smart contracts. The smart contract published to the blockchain cannot be destroyed from outside, thus if the contract needs to be destryed, the logic needs to be written during development.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern void Destroy()
```

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         var height = Blockchain.GetHeight();
         var block = Blockchain.GetBlock(height);
         if (block.Timestamp > 1514736000) // Beijing time 2018-1-1
         {
             FRS.SmartContract.Framework.Services.FRS.Contract.Destroy();
         }
     }
}
```



[Back](../Account.md)
