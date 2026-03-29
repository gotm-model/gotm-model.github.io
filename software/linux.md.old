+++
showonlyimage = false
draft = false
date = "2016-11-05T18:25:22+05:30"
title = "Linux/Mac"
weight = 0
authors = "Karsten Bolding"
+++

### Overview

  1. **Get GOTM** For now we do not provide pre-compiled versions of GOTM for Linux and Mac. The main reason being that all pre-requisites for building locally are readily available on these platforms - notably a working Fortran compiler. So please follow the instructions below for three different ways to build GOTM - of increasing complexity.
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

#### Command line version of CMake

For a fast - and simple - configuration the following can be used.

   1. Create and enter a build directory - e.g. /tmp/gotmbuild/
   2. cmake ~/GOTM/code -DGOTM_USE_FABM=off - do NOT include FABM~~
   3. cmake ~/GOTM/code -DGOTM_USE_BASE=on - do include FABM
   4. make _or_ cmake --build .
   5. ./gotm -c

```
kb@orca ~/TT/build $ ./gotm -c
 ------------------------------------------------------------------------
 GOTM version:   v5.3-122-g9d840387 (cmake branch)
 NetCDF version: 4.7.0 of May  1 2019 11:13:47 $
 ------------------------------------------------------------------------
 Compiler: Intel 19.0.0.20190117
 ------------------------------------------------------------------------
```

   ~~2. cmake ~/GOTM/code/src -DGOTM_USE_FABM=false - do NOT include FABM~~
   ~~3. cmake ~/GOTM/code/src -DFABM_BASE=~/FABM/fabm - do include FABM~~


Adjust the path to the GOTM ~~(and FABM)~~ source code.

#### The GUI version of CMake

  1. Start "CMake (cmake-gui)".
  2. Click the "Browse Source..." button and select the directory with the GOTM 
source code. ~~This is the src directory at the root of the GOTM repository.~~
  3. Click the "Browse Build..." button and select a directory of your choice 
to build GOTM in - e.g. /home/_USERNAME_/build/gotm. It is recommended to 
choose an empty (or new) directory for this purpose. 
  4. Click the "Configure" button. This first time you do this, CMake asks you 
to select a build system generator.
  5. Now all configuration variables for the build system are listed and you 
can change them according to your preferences. After changing any variable, 
press the "Configure" button again - additional settings may appear.
  6. If all configuration variables are set correctly, and you have clicked the 
"Configure" button until no new (red-colored) configuration variables appear, 
press the 'Generate' button.
  7. If no erros occur a Makefile has been generated in the selected build directory. 
Open a Terminal and enter this directory and type *make*.


#### The provided configure/build scripts

Text in *italics* are commands and text in **bold** are variables.

In the following it is assumed the GOTM ~~and FABM~~ source code is cloned to **GOTM_BASE** ~~and FABM_BASE ~~. Default values are:
* **GOTM_BASE** = *$HOME/GOTM/code*
~~* **FABM_BASE** = *$HOME/FABM/code*~~

##### Configuring
The first step is to create a *build directory* and change to it: * *mkdir -p $HOME/build/gotm/ && cd $HOME/build/gotm*

Executing the script *$GOTM_BASE/scripts/linux/gotm_configure.sh* will generate a Make-based build system in a sub-directory named after the compiler used - default is *gfortran*.

This step must be completed without any errors before advancing to the actual compilation.

##### Building/installing
Executing the script *$GOTM_BASE/scripts/linux/gotm_build.sh* will compile GOTM according to the configuration carried out in the previous step.

A manual build can also be done like:
* *cd $HOME/build/gotm/<compiler> && make install*

CMake *installs* the generated executable and libraries in an *install_directory* - default i **$HOME/local**.
To test if the compilation has been succesful - try:
* *$HOME/local/bin/gotm -c*

For furher use of GOTM it is a big advantage to add **$HOME/local/bin** to the **PATH**.

The scripts used above for configuration and compilation have some documentation included and it should be relative easy to adjust to specific need and taste.

#### After a successful build

After the build completes, the GOTM executable will be installed in /home/_USERNAME_/local/bin/gotm (default) or a user configurable destination.
At this point you can continue with step 2 in the quick start instructions at the top of this page.
