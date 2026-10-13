# Libint (CP2K version) instructions

-   [Libint for CP2K on GitHub](https://github.com/cp2k/libint-cp2k)

    -   [GitHub releases](https://github.com/cp2k/libint-cp2k/releases)

-   [Regular Libint GitHub](https://github.com/evaleev/libint)

    -   [GitHub releases](https://github.com/evaleev/libint/releases)


## EasyBuild

-   [Libint-CP2K in the CSCS repository](https://github.com/eth-cscs/production/tree/master/easybuild/easyconfigs/l/Libint-CP2K)


### Version 2.6.0 for CP2K 9.1 and later

-   The EasyConfig is a direct port from the CSCS one.
  
-   Always update to the Boost version for the specific toolchain.


### Version 2.7.2.

-   Adapted using the EasyBuilders one as a guidance. It is an unusual version
    for CP2K.
    
-   Kept in 25.03 also due to uncertainties about compatibility of newer versions with
    CP2K. In fact, the CP2K authors still test with 2.6.0, but the EasyBuilders use
    2.7.2.


### Version 2.13.1

-   Libint has changed to a CMake build process. Also, it is not clear which options are exactly
    needed for CP2K. Therefore we decided to switch to a different approach and work with 
    downloads prepared specifically for CP2K by
    [analysing the CP2K build script for Libint](https://github.com/cp2k/cp2k/blob/v2026.2/tools/toolchain/scripts/stage3/install_libint.sh).

-   The `CMakeMake` EasyConfig is a LUST development evolved from the non-CMake one for 2.7.2 in 25.03.
