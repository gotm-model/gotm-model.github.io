+++
showonlyimage = false
draft = false
date = "2016-11-05T18:25:22+05:30"
title = "Windows"
weight = 0
authors = "Jorn Bruggeman"
+++

### Quick start

  1. **Get GOTM** It is easiest to 
[download the pre-built GOTM software for Windows (gotm.exe)](http://github.com/gotm-model/code/releases)
, provided with each stable release.
  2. **Get examples** 
[Download the example scenarios](http://github.com/gotm-model/cases/releases)
for your version of 
GOTM. You may run these scenarios to familiarize yourself with GOTM or to learn 
about ocean turbulence; 
[the example scenarios are discussed in detail on this web site](/examples/).
  3. **Run** To run a scenario, open a command prompt ("cmd"), cd to the 
scenario directory, and run GOTM by typing the full path to gotm.exe.
  4. **View results** GOTM produces output in NetCDF format (files with .nc 
extension). These can be read by many applications (e.g., MATLAB, R). If you 
need a stand-alone NetCDF viewer, we recommend 
[PyNcView](https://sourceforge.net/projects/pyncview). 

### Building from scratch

#### Prerequisites

  * a supported Fortran compiler. We regularly test the Intel Fortran compiler, 
which integrates with Visual Studio.~~, as well as the GNU Fortran compiler 
provided with the free 
[mingw-w64 compiler suite](http://mingw-w64.org).~~
  * [CMake ~~2.8.8~~ 3.0 or later](https://cmake.org)

#### Download the code

First, get the GOTM source code from GitHub. You can either download 
[the latest stable release of the code](http://github.com/gotm-model/code/releases) 
as a single zip file, or check out the very latest version ("developer's 
version") of the code from 
[GOTM's git repository](http://github.com/gotm-model/code)
. If you need the developer's 
version, a graphical git client such as 
[TortoiseGit](https://tortoisegit.org) 
can be used to obtain the source code from the Git repository. Note that 
TortoiseGit also requires 
[Git for Windows](https://git-for-windows.github.io) 
to be installed. After Git for Windows and TortoiseGit are installed, you 
obtain the developer's version of GOTM by right-clicking in Windows Explorer 
within the directory where you want to place the source code directory, and 
choosing "Git Clone...". In the window that appears, set "URL" to 
https://github.com/gotm-model/code.git, set "Directory" to the path where you 
want the source code (recommended: _CURRENT_DIRECTORY_\gotm-git) and click OK. 
This should download the latest code. 

#### Building

  1. Start "CMake (cmake-gui)" from the start menu.
  2. Click the "Browse Source..." button and select the directory with the GOTM 
source code. ~~This is the src directory at the root of the GOTM repository.~~
  3. Click the "Browse Build..." button and select a directory of your choice 
to build GOTM in - e.g. C:\Users\_USERNAME_\build\gotm. It is recommended to 
choose an empty (or new) directory for this purpose. **MinGW users**: some 
versions of CMake (e.g., 3.0.2) generate invalid makefiles if the build 
directory is on a remote server (i.e., a path starting with \\\\); to avoid 
problems, place it on a local or mounted network drive instead.
  4. Click the "Configure" button. This first time you do this, CMake asks you 
to select a build system generator. If you intend to use Intel Visual Fortran, 
select your version of Visual Studio and press OK (choose "Visual Studio 
_VERSION_ _YEAR_" - avoid the entries with IA64 and Win64 postfixes!). If you 
intend to use MinGW, choose "MinGW Makefiles".
  5. Now all configuration variables for the build system are listed and you 
can change them according to your preferences. After changing any variable, 
press the "Configure" button again - additional settings may appear.
  6. If all configuration variables are set correctly, and you have clicked the 
"Configure" button until no new (red-colored) configuration variables appear, 
press the 'Generate' button. If you previously selected Visual Studio as build 
system, this now creates the Visual Studio solution and projects in your chosen 
build directory. If you selected MinGW as build system, it will generate the 
make files.
  7. If you use Intel Fortran, open Visual Studio, and open the solution 
gotm.sln that CMake has created in the build directory chosen in CMake. To 
build and install GOTM, right-click the "INSTALL" project in the solution 
explorer, and choose "Build". If you use MinGW, open a command prompt (run 
"cmd") and cd to the build directory (not the src directory!) defined above. 
Then type and run "mingw32-make install".

After the build completes, the GOTM executable will be installed at 
%LOCALAPPDATA%\gotm\bin\gotm.exe (%APPDATA%\gotm\bin\gotm.exe on Windows XP). 
At this point you can continue with step 2 in the quick start instructions at 
the top of this page.
