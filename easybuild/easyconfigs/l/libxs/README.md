# libxs technical information

LIBXS is a portable C library providing building blocks for memory operations, numerics, synchronization, and more — with a focus on performance and minimal dependencies. 
Originally developed as part of [LIBXSMM](../libxsmm/index.md).

-   [LIBXS manual](https://libxs.readthedocs.io/en/latest/)

-   [libxs on GitHub](https://github.com/hfp/libxs)

    -   [GitHub releases](https://github.com/hfp/libxs/releases)


## EasyBuild

Version 1.0.0 only appeared in June 2026, likely with the release of libxsmm 2.0.0, so 
when we started developing recipes for libxs, there was not much around.

-   No support in the EasyBuilders repository.

-   [Spack package libxs](https://packages.spack.io/package.html?name=libxs)


### Version 1.0.0

-   The EasyConfig is a LUST development, using information from the 
    [CP2K build script for libxs](https://github.com/cp2k/cp2k/blob/v2026.2/tools/toolchain/scripts/stage4/install_libxs.sh)
    and the [Spack package file](https://github.com/spack/spack-packages/blob/develop/repos/spack_repo/builtin/packages/libxs/package.py).


