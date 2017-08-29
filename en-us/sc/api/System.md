# System Namespace

The System namespace is the API provided by the Smart Contract Execution Engine (FRSVM), which provides a way to access the execution environment of the smart contract.

| API | Description |
| ---------------------------------------- | -------------------------- |
| System.ExecutionEngine.GetScriptContainer | Get the script container for this smart contract (the first trigger) |
| System.ExecutionEngine.GetExecutingScriptHash | Get the scripthash of the executing smart contract  |
| System.ExecutionEngine.GetCallingScriptHash | Get the scripthash of the caller for this smart contract |
| System.ExecutionEngine.GetEntryScriptHash | Get the scripthash of the entry point for the smart contract (the starting point of the contract call chain) |

Note: The source code for the API above can be found under `FRS.VM` in the `src\FRS.VM\InteropService.cs` file.