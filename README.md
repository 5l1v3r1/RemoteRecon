# RemoteRecon
Remote Recon and Collection

RemoteRecon provides the ability to execute post-exploitation capabilities against a remote host, without having to expose your complete toolkit/agent. Often times as operator's we need to compromise a host, just so we can keylog or screenshot (or some other miniscule task) against a person/host of interest. Why should you have to push over beacon, empire, innuendo, or a custom RAT to the target? This increases the footprint that you have in the target environment, thus increasing your chances of getting caught. 

RemoteRecon utilizes the registry for data storage, with WMI as an internal C2 channel. All commands are executed in a asynchronous, push and pull manner. Meaning that you will send commands via the powershell controller and then retrieve the results of that command via the registry. All results will be displayed in the local console, except for the screenshot command. 

### Current Capabilities
PowerShell

Screenshot

Token Impersonation

Inject ReflectiveDll (Must Export the ReflectiveLoader function from Stephen Fewer)

Keylogger

### Improvements, Additions, ToDo's:

Dynamically Load and execute .NET assemblies

Mimikatz

Support non reflective dll's for injection


### Build Dependecies

The RemoteRecon.ps1 script already contains a fully weaponized JS payload for the Agent. The payload will only be updated as the code base changes. 

If you wish to make changes to the codebase on your own, there are a few depencies required.

1. Visual Studio 2015+
2. Windows 7 and .NET SDK
3. Windows 8.1 SDK
4. mscorlib.tlh (This is included in the project but there are instances where intellisense can't seem to find it [shrug])
5. .NET 3.5 & 4
6. James Forshaw's [DotNetToJScript project](https://github.com/tyranid/DotNetToJScript)
7. Fody/Costura Nuget [package](https://github.com/Fody/Costura). Package and embed any extra dependencies in .NET. 


### Credit

Thanks to these individuals for their contributions via code or knowledge :)

#### [ambray](https://github.com/ambray) <- He has a cool RE/ASM course too
#### [tifkin](https://twitter.com/tifkin_)
#### [mattifestation](https://twitter.com/mattifestation)
#### [subtee](https://twitter.com/subTee)
#### [harmj0y](https://twitter.com/harmj0y)


#### For a more in-depth guide, please visit this [post]()
