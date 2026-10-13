# Wannier90

-  [Wannier website](http://www.wannier.org/)

-   [Wannier90 on GitHub](https://github.com/wannier-developers/wannier90)

    -   [GitHub releases](https://github.com/wannier-developers/wannier90/releases)


## General information

Wannier90 is an open-source code (released under GPLv2) for generating 
maximally-localized Wannier functions and using them to compute advanced 
electronic properties of materials with high efficiency and accuracy.

  * [Wannier user guide and tutorial](http://www.wannier.org/support/)

## Known Issues

  * There is a problem with the code version 3.1.0 and GCC 12/13 reported 
    [in the wannier GitHub as issue 521](https://github.com/wannier-developers/wannier90/issues/521)
    which may result in `wannier` program faults.

    For mitigating the issue develop code version (end of Jan 2025) is available with eb file:
    - Wannier90-24Jan2025-cpeGNU-24.03.eb  


## EasyBuild

-   [Wannier90 in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/w/Wannier90)

-   [Spack package wannier90](https://packages.spack.io/package.html?name=wannier90)


### Version 3.1.0

-   The EasyConfig is derived from the `Wannier90-3.1.0-foss-2022a.eb` EasyConfig.

-   For 26.03, we switched to EB6-compatible parameters.


### Version 4.0.1

-   As Wannier90 now uses CMake, we switched to the CMake build process which required some rewriting.

-   ISSUE: The pkg-config file does not pass the validation tests.

-   ISSUE: As soon as the `cray-mpich` module is unloaded, the BLAS libraries are not found anymore which
    is very strange. We needed to specify them explicitly.
