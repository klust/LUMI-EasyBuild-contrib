# libvori instructions

-   [libvori web site](https://brehm-research.de/libvori.php)

Note that the `CMakeLists.txt` file looks pretty terrible; this code seems to assume 
gcc is the only compiler people use!


## EasyBuild

-   [libvori in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/l/libvori)

-   [libvbori support in the CSCS repository](https://github.com/eth-cscs/production/tree/master/easybuild/easyconfigs/l/libvori)


### libvori 210412 for CP2K 9.1

-   The EasyConfig is a direct port of the CSCS one.


### libvori 220621 for CP2K 2022.1, 2023.1, 2024.x, 2025.x and 2026.x

-   Trivial port of the previous EasyConfig

-   Cleaned up a bit for 25.03.

-   Switched to EB6-compatible parameters for 26.03.

-   For 26.03 we build both a static and shared library, and it turned out that we needed
    to enable PIC ourselves as the CMake recipe didn't do so, so the building of the shared
    library failed.
