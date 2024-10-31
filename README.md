## Note
This C#  project implements Tencent-RTC's UserSig authentication, providing a secure server-side method for generating signatures to protect the keys from leakage.

![](https://cloudcache.intl.tencent-cloud.com/cms/backend-cms/12569f72920411ef810152540055f650.png)

## Integration
Integration is possible using both the package manager under Visual Studio Tools and the NuGet command line. In addition, you can download the source code for direct integration.
#### VS Integration

It is recommended to use Visual Studio 2017 and above. If the version is too low and does not support NuGet, use the source code integration directly.
In Visual Studio follow `Tools`->`NuGet Package Manager`->`Manage NuGet Packages for Solutions`, then search for `tls-sig-api-v2` to install.
#### NuGet command line integration

The project has been packaged and uploaded to the nuget.org package management repository, which can be installed directly using nuget.
```
PM> Install-Package tls-sig-api-v2
```
A variety of command line installation methods [here](https://www.nuget.org/packages/tls-sig-api-v2)view.

#### source code integration
Download `tls-sig-api-v2-cs/TLSSigAPIv2.cs` to the developer project directory, and manually download the dependencies[zlib.net](https://www.nuget.org/packages/zlib.net-mutliplatform/) development library，Call it according to the following sample code.

## Usage
``` c#
using tencentcloud;

TLSSigAPIv2 api = new TLSSigAPIv2(1400000000, "5bd2850fff3ecb11d7c805251c51ee463a25727bddc2385f3fa8bfee1bb93b5e");
string sig = api.GenSig("xiaojun");
System.Console.WriteLine(sig);
```
