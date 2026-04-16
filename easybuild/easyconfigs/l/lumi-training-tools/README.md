# lumi-trainig-tools technical documentation

-   mkfile tool:   

    -   It was originally a tool included with Solaris and can still be found in some
        BSD distributions.
  
    -   A simple version with one option less is available on the
        [GitHub repository vogelchr/mkfile](https://github.com/vogelchr/mkfile).
        Its command line options are different though so we avoid using it for now.

-   `lstopo` command

    -   It is part of [the `hwloc` libraries](https://www.open-mpi.org/projects/hwloc/) 
        which itself is a subproject of
        [Open MPI](https://www.open-mpi.org/).


## EasyConfigs

### Version 20240502 - Amsterdam 2-day LUST training in May 2024

-   Only includes the mkfile tool, but already uses a bundle for future
    extensions.

-   The Makefile that comes with `mkfile` is for the BSD make so we compiled
    with explicit commands using `CmdCp` and also modified the manual page a
    bit to fit better with our setup. 


### Version 20250422 - Riga 2-day training in April 2026

-   Now also includes `lstopo` extracted from `hwloc`.

    We do remove all components of `hwloc` that are not needed as we don't
    want users to start using that version of the `hwloc` library on LUMI.

    The build recipe for `lstopo` is only vaguely based on that for 
    [`hwloc` in the EasyBuilders repository](https://github.com/easybuilders/easybuild-easyconfigs/tree/develop/easybuild/easyconfigs/h/hwloc)
    as we needed mostly different options and wanted the hwloc libraries to
    be linked statically into `lstopo` so that we could remove those libraries.
