# DFT-D4 information


-   [DFT-D4 home page](https://www.chemie.uni-bonn.de/pctc/mulliken-center/software/dftd4)

-   [DFT-D4 on GitHub](https://github.com/dftd4/dftd4)

    -   [GitHub releases](https://github.com/dftd4/dftd4/releases)


## EasyBuild

-   [Support in the EasyBuilders repository under a different name: DFT-D4 rather than DFTD4](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/d/DFT-D4)

-   There is no support in the CSCS repository


### Version 3.4.0

-   The EasyConfig is mostly a LUST development


### Version 3.7.0

-   Port of the 3.4.0 version, but a patch was needed.


### Version 4.0.2

-   With this version, a new dependency comes in: mctc-lib.


### Version 4.2.0

-   The EasyConfig is a straightforward update of the one for 4.0.2 in 25.03,
    but we switched to EB6-compatible parameters.

-   We tried to build a cpeCray version, using the mctc-lib that fails in one test,
    but there are many issues:

    -   The Meson build system does not support the Cray Fortran compiler. It supports
        several compilers that haven't been available for years, including the PathScale
        compiler, a company that was bought by Cray even before the merger with HPE, but
        does not support Cray Fortran.

    -   We did manage to configure the program with CMake instead. However, compilation
        fails as the code does things that are not supported by Cray Fortran.

    The conclusion should be that DFTD4 is incompatible with Cray Fortran and hence cannot
    be used as an optional module in VASP when VASP is compiled with the Cray Fortran
    compiler as is needed for the GPU version.
