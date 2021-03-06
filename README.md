# caeplugin-ThermalDesktop
An Pointwise CAE plugin that exports a ThermalDesktop grid.

![ThermalDesktop][Logo]

## Solver Attributes

### WideFormat

Set `true` to export using wide column format. Type `Boolean`. Default `true`.

### ShellThickness

The default PSHELL thickness. Type `Real`. Default `0.0`.

### ShellOrientation

The default PSHELL orientation. Type `enum(NormalsOut|NormalsIn)`. Default `NormalsOut`.

## Limitations

Only the `Unspecified` BC and VC physical types are supported.


## Building the Plugin

This plugin was created using version 1.0 R7 of the Pointwise CAE Plugin SDK.
However, it should build properly with newer versions of the SDK.

To build the ThermalDesktop plugin you must integrate this source code into 
your local PluginSDK installation by following these steps.

* Download and install the [Pointwise Plugin SDK][SDKdownload].
* Configure and validate the SDK following the [SDK's instructions][SDKdocs].
* Create a ThermalDesktop plugin project using the mkplugin script: `mkplugin -uns -cpp ThermalDesktop`
* Replace the project's generated files with the files from this repository.
* Follow the platform specific instuctions below.

### Building the Plugin with Microsoft Visual Studio

* Open the Plugin SDK Visual Studio solution file.
 * For VS2008 open `PluginSDK\PluginSDK.sln`
 * For VS2012 open `PluginSDK\PluginSDK_vs2012.sln`
* Add the existing CaeUnsThermalDesktop project file to the solution *Plugins* folder.
 * For VS2008 add `PluginSDK\src\plugins\CaeUnsThermalDesktop\CaeUnsThermalDesktop.vcproj`
 * For VS2012 add `PluginSDK\src\plugins\CaeUnsThermalDesktop\CaeUnsThermalDesktop.vcxproj`

### Building the Plugin with Mac OS/X and Linux

* Nothing more needs to be done.


## Disclaimer
Plugins are freely provided. They are not supported products of
Pointwise, Inc. Some plugins have been written and contributed by third
parties outside of Pointwise's control.

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, POINTWISE DISCLAIMS
ALL WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED
TO, IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
PURPOSE, WITH REGARD TO THESE SCRIPTS. TO THE MAXIMUM EXTENT PERMITTED
BY APPLICABLE LAW, IN NO EVENT SHALL POINTWISE BE LIABLE TO ANY PARTY
FOR ANY SPECIAL, INCIDENTAL, INDIRECT, OR CONSEQUENTIAL DAMAGES
WHATSOEVER (INCLUDING, WITHOUT LIMITATION, DAMAGES FOR LOSS OF BUSINESS
INFORMATION, OR ANY OTHER PECUNIARY LOSS) ARISING OUT OF THE USE OF OR
INABILITY TO USE THESE SCRIPTS EVEN IF POINTWISE HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES AND REGARDLESS OF THE FAULT OR NEGLIGENCE OF
POINTWISE.

[Logo]: https://raw.github.com/dbgarlisch/CaeUnsThermalDesktop/master/logo_thermaldesktop.png  "ThermalDesktop Logo"
[SDKdocs]: http://www.pointwise.com/plugins
[SDKdownload]: http://www.pointwise.com/plugins/#sdk_downloads
