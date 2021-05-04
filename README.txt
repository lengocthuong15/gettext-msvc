This was forked from kahrl/gettext-msvc
Add support for Visual Studio 2019
================================================================
Visual Studio 2019 solution for gettext-0.19.4 and libiconv-1.14
================================================================

This lets you build libintl (from gettext) and libiconv with Visual Studio 2013.
(These two libraries are just enough to build Minetest with gettext support.)

Notes:

- I already included the source code in the repo and a pre-built binaries for Release x64

- There is a problem with VS2019 and the fix is on libiconv-1.14\config.h, I comment out: #define mbstate_t int

- Output will be: libintl.dll, libintl.lib, libiconv.dll, libiconv.lib.

- 32 bit and 64 bit builds are both supported.


Instructions
============

1. Open gettext.sln in Visual Studio 2019

2. Select a configuration (Release or Debug) and a platform (Win32 or x64)
   and click BUILD -> Build Solution.


Acknowledgements
================

A lot of this is based on the solution files provided at

    https://github.com/winlibs/gettext
    https://github.com/winlibs/libiconv
