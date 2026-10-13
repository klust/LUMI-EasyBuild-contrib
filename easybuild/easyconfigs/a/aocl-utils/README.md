# AOCL-Utils

  - [AOCL-Utils web page](https://www.amd.com/en/developer/aocl/utils.html)
    

## EasyBuild

-   There is no support in the EasyBuilders repository
-   There is no support in the CSCS repository


### Version 4.2 for CPE 23.12 and 24.03

- Created for LUMI


### Version 5.1 for 25.03 and 26.03

-   Trivial port of the EasyConfig for 4.2 for 24.03, but changed the name
    of the source files.

-   For 26.03, we switched to EB6-compatible parameters and added more 
    extensive sanity checks.

-   Considered switching to 5.3 for 26.03. However, there is a switch to the
    CMake build process which is enforced for some tools and not for others,
    and we couldn't get libFLAME (which only supports CMake) to build. It is
    currently not clear if it is incompatible with BLIS built with configure
    or what is going on.
