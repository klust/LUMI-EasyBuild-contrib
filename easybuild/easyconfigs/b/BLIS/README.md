# BLIS instructions

-   [BLIS development and home page on GitHub](https://github.com/flame/blis)

-   [AMD's fork of BLIS home page](https://www.amd.com/en/developer/aocl/dense.html)

-   [AMD's GitHub with the BLIS fork](https://github.com/amd/blis/)

    -   [GitHub releases](https://github.com/amd/blis/releases)
  
  
## Notes

-   BLIS does not provide the ISAMIN etc. functions. They don't seem to be part of 
    the BLAS1 specifications either, unlike their ISAMAX etc. variants. 
    
    They do seem to be missed though when building ScaLAPACK with the Cray compiler.
    It is likely (but needs further investigation) that other compilers include them
    in their runtime libraries.
    
-   ILP64 variants are also provided. However, even though the non-ILP64 variants use
    32 bit integers in the BLAS function interfaces, they do use 64-bit integers internally.


## EasyBuild

-   [BLIS support in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/b/BLIS)

-   There is no support for BLIS in the CSCS repository.


### Version 3.1 for CPE 21.08

-   The EasyConfig file is a direct port from the EasyBuilders one

-   Some logic was added to select zen3 depending on the partition loaded to
    support cross-compiling.


### Version 3.2 for CPE 22.06 and 22.08 (archived)

-   Trivial port of the EasyConfig file for 3.1.


### Version 4.0 for CPE 22.12 (archived) and 23.03

-   Trivial port of the EasyConfig file for 4.0
  
-   Did restrict the number of threads for the tests though as not doing so 
    resulted in frequent errors when compiling on the login nodes.

-   Reworked the EasyConfig trying to save the test results in the installation
    which does not yet fully work, and storing license information with the 
    installation. We failed to store the test logs in the `easybuild` subdirectory.
    They are located in the `easybuild-extra-logs` subdirectory instead.
    
-   Created ILP64 versions.


### Version 4.2 for CPE 23.12/and 24.03

-   Trivial port of the EasyConfig file for 4.2

  
### Version 5.1 for CPE 25.03

-   The EasyConfig is s trivial port of the EasyConfig for 4.2 for 24.03, but we did
    change the name of the downloaded files.

-   For 26.03, we switched to EB6-compatible parameters and worked a bit on
    the sanity checks. Unfortunately, the version encoded in the `.pc`
    file is more than just `5.1.0` so we do not test to detect version errors from erroneous
    downloads or so.

-   Considered switching to 5.3 for 26.03. However, there is a switch to the
    CMake build process which is enforced for some tools and not for others,
    and we couldn't get libFLAME (which only supports CMake) to build. It is
    currently not clear if it is incompatible with BLIS built with configure
    or what is going on.
