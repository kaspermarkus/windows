# GPII for Windows

Contains platform-specific components of the GPII architecture for Windows. See http://gpii.net/ for overall details of the GPII
project. 

# Windows Installation Instructions

## GPII end-users
We provide an official graphical GPII installer (.msi). This is linked from the [http://gpii.net](GPII website)

## For devopers

### Dependencies

* Git
 * Install GitHub for Windows - it includes the command line Msysgit which you run as "Git Shell".
 * Or, for advanced developers, use Cygwin for a full Unix-like environment on Windows

* Node.js
 * GPII is dependent on node.js and is currently tested and stable with node.js 4.2.x (the long term support)
 * nodejs can be found here: https://nodejs.org/en/download/. Download and follow the installation instructions.

* node-gyp dependencies
 * The dependencies are described here: https://github.com/nodejs/node-gyp#installation
 * you dont need to actually install node-gyp, as this will be done as part of GPII, but you should install the dependencies (such as VisualStudio Express 2013, Python, etc).

* Other:
 * Windows 7, 64bit, has a bug with high-contrast mode. If you're running this Windows version, you'll need to install the hotfix linked from this Microsoft support page (http://support.microsoft.com/kb/2516889) (x64 only).

### Building the GPII Personalization Framework on Windows
* Open up a git compatible command prompt (e.g. git shell)
* Create a GPII directory
 * `mkdir \gpii` (or wherever you prefer)
 * `cd \gpii`
* Clone the GPII Windows repository
 * `git clone git://github.com/GPII/windows.git`
 * `cd windows`
* Install dependencies of the framework
 * `npm install`
* Make sure grunt is installed:
 * `npm install grunt`
 * `npm install -g grunt-cli`
* Build everything, incl. getting the universal (cross platform code):
 * `grunt build`

### Starting the GPII Personalization framework

From the command prompt, inside the windows folder of the GPII (eg. C:\GPII\windows\), type the following:
* `start.cmd`

### Installing the USB and RFID listeners
* Use the Windows installer found here: https://github.com/OpenDirective/GPII-windows/releases/tag/Listeners_V1.3.0
* OR build the binaries by following the installation instructions http://github.com/windows/UsbUserListener/README.txt

### Additional Windows Configuration and comments:
* Increasing the buffor size for the command line (useful for bugreporting)
 * Open a command line and right-click on the command line's window.
 * In the context menu that pops up, select the "Layout" tab.
 * In the layout tab, change the "Height" of the "Screen Buffer Size" to a much higher number, e.g. 900. Then click OK to confirm the change.
 * As a result of this, most of the DOS windows that pop up when you start GPII will "store" more logging lines. These logging lines can be copied and pasted into bug reports. For guidance on how to copy those logging lines, see Microsoft's article To copy text from a command prompt window.


