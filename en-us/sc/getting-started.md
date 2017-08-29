---
typora-root-url: ..\..
---

### How to use C# to write an FRS smart contract

We currently recommend C# for developing smart contracts (though we support or plan to support Java, Kotlin, Go, C/C++, Python, JavaScript and other programming languages)

This section contains a short tutorial that guides you in configuring the C# development environment for FRS smart contracts and gives you an idea of ​​how to create a smart contract project and how to compile it.

   > [!Note]
   > At present, all the projects have been upgraded to the Visual Studio 2017 version, if you want to use Visual Studio 2015 to create intelligent contracts can refer to [how to use C # to write FRSs intelligent contract for VS2015](getting-started-2015.md)

## Development Tools

### 1. Visual Studio 2017

If you have already installed Visual Studio 2017 on your computer and checked for .NET Cross-Platform Development at the time of installation, you can skip this section.

Download and install:

[Visual Studio download address](https://www.visualstudio.com/products/visual-studio-community-vs)

The installation process is very simple, follow the operation prompts step-by-step, it should be noted that you need to check the installation of `.NET Core cross-platform development`, otherwise you will not be able to open FRS-vm project in step #3. The installation takes about ten minutes or up to an hour.

![install net core cross-platform development toolset](/assets/install_core_cross_platform_development_toolset.png)

### 2. FRSContractPlugin

Installation method:

Open Visual Studio 2017, open Tools, click on Extensions and Updates, click on the Online tab on the left side of the window, search FRS in the search box on the top right corner of the window, download the FRSContractPlugin (this step requires internet access).

![download and install FRS smart contract plugin](/assets/download_and_install_smart_contract_plugin.png)

### 3. FRS-compiler

Installation and configuration steps:

Download the [FRS-compiler](https://github.com/FRS-project/FRS-compiler) project on Github, open the solution with Visual Studio 2017, publish the FRSn project,

![publish FRS compiler msil project](/assets/publish_FRS_compiler_msil_project.png)

![publish and profile settings](/assets/publish_and_profile_settings.png)


After the release is successful, the FRSn.exe file is generated in `bin\Release\PublishOutput`.

We now need to add this directory to our execution path. The PATH is the system variable that your operating system uses to locate needed executables from the command line or Terminal window.

**Windows 10 and Windows 8:**

  In Search, search for and then select: System (Control Panel)
  Click the Advanced system settings link.
  Click Environment Variables. In the section System Variables, find the PATH environment variable and select it. Click Edit. If the PATH environment variable does not exist, click New.
  In the Edit System Variable (or New System Variable) window, specify the value of the PATH environment variable. Click OK. Close all remaining windows by clicking OK.

**Windows 7:**

  From the desktop, right click the Computer icon.
  Choose Properties from the context menu.
  Click the Advanced system settings link.
  Click Environment Variables. In the section System Variables, find the PATH environment variable and select it. Click Edit. If the PATH environment variable does not exist, click New.
  In the Edit System Variable (or New System Variable) window, specify the value of the PATH environment variable. Click OK. Close all remaining windows by clicking OK.

![edit environmental variables](/assets/edit_environmental_variables.png)

Now run Command or PowerShell, and enter FRSn.exe. If there is no error and the output shows the version number (as shown) the environment variable configuration is successful

![powershell enviornment variabled updated correctly](/assets/powershell_enviornment_variabled_updated_correctly.png)


NOTE. Windows 7 SP1 users might encounter an error "Unhandled Exception: System.DllNotFoundException: Unable to load DLL 'api-ms-win-core-console-l2-1-0.dll': The specified module could not be found". The required 'api-ms-win-core-console-l2-1-0.dll' file is only found in Windows 8 or later versions. This error can be resolved by obtaining a copy of 'api-ms-win-core-console-l2-1-0.dll' and putting it in the directory C:\Windows\System32.

## Create project

After the above installation configuration is successful, you can create an FRSContract project in Visual Studio 2017.

![new smart contract project](/assets/new_smart_contract_project.png)

Once you create a project, it will automatically generate a C# file, the default class inherited from the FunctionCode, as shown in the following:

![smart contract function code](/assets/smart_contract_function_code.png)


## Compile the Project

Everything is now ready to add the entry method that defines the smart contract:

```c#
public class Contract1: FunctionCode
{
    public static void Main ()// Note that the main method to capitalize
    {
        
    }
}
```

After you compiled it successfully, you will see` SmartContract1.avm` in the `bin/Debug` directory, which is the file that is generated as the FRS smart contract.

![compile smart contract](/assets/compile_smart_contract.png)


Now that you have completed the configuration of the FRS smart contract development environment, please refer to the [FRS smart contract tutorial](tutorial.md)
