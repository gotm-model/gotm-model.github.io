## Short guide on how to compile GOTM

The following prerequisites must be fulfilled before compilation is started

1. The source code for GOTM and [FABM](www.fabm.net) must have been cloned from Git repositories. The actual cloning will depend on the platform and Git-utilities used. Further informtion is provide [here](https://help.github.com/articles/cloning-a-repository/#platform-linux)
2. A Fortran compiler supporting at least Fortran 2003 must be avaialble
   * On Linux [gfortran](https://gcc.gnu.org/fortran/) versions including and above 4.7 have been tested and the [Intel Fortran compiler](https://software.intel.com/en-us/fortran-compilers).
   * On Windows the [Intel Fortran compiler](https://software.intel.com/en-us/fortran-compilers) configured with VisualStudio is working.
3. [NetCDF](http://www.unidata.ucar.edu/software/netcdf)
   * On Linux/Mac GOTM and NetCDF must be compiled with the same Fortran compiler
   * On Windows NetCDF is provided in the repository - compatible with the Intel Fortran compiler
4. [CMake](www.cmake.org) must be installed. CMake is used to configure the compilation and generate native build systems - i.e. Make-based systems on Linux/Mac and VisualStudio on Windows (which must also be installed and configured with the ortran compiler)

Only when the above 4 points are checked it makes sense to proceed.

#### On Linux/Unix/Mac

#### On Windows
