# Smart Contract Example - HelloWorld

```c#
public class HelloWorld : FunctionCode
{
    public static void Main()
    {
        Storage.Put(Storage.CurrentContext, "Hello", "World");
    }
}
```

The Storage class is a static class that manipulates the private contract storage. The `Storage.Put()` method allows you to store data in the private storage area in key-value format. For details, refer to [Storage](../fw/dotnet/FRS/Storage.md).

Please refer to [Github](https://github.com/FRS-project/examples) for complete examples.
