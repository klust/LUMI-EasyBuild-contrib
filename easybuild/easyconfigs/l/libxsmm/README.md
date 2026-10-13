# libxsmm instructions

-   [libxsmm on ReadTheDocs](https://libxsmm.readthedocs.io/en/latest/)

-   [libxsmm on GitHub](https://github.com/libxsmm/libxsmm)

    -   [GitHub releases](https://github.com/libxsmm/libxsmm/releases)

-   [Alternative fork of libxsmm on GitHub](https://github.com/hfp/libxsmm)


## EasyBuild

-   [libxsmm in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/l/libxsmm)

-   [libxsmm in the CSCS repository](https://github.com/eth-cscs/production/tree/master/easybuild/easyconfigs/l/libxsmm)


### libxsmm 1.17 for cpeGNU 21.08 and later

-   The EasyConfig is a direct port of the CSCS one.

-   Added license info for the 25.03 and later versions.

-   Switched to EB6-compatible parameters for 26.03.


### libxsmm 29Dec22 for CPE 22.08 and later

-   Created for PyFR as it requires a recent version of libxsmm but no release
    exists. Use the date of the commit as the version.


### libxsmm 2.0.0 for 26.03

-   The EasyConfig is a remake of the one for 1.17, now using a CMake build process.

-   Options used are based on the [build recipe for CP2K 2026.2](https://github.com/cp2k/cp2k/blob/v2026.2/tools/toolchain/scripts/stage4/install_libxsmm.sh),
    but we generate both static and shared libraries as before.
