# Release schedule

## arm-none-eabi-gcc & aarch64-none-elf-gcc

The [Arm GNU Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads/)
release cycle is about two releases per year.

The **xPack GNU Arm & AArch64 Embedded GCC** release schedule generally follows the
upstream releases.

Currently the Arm site does not provide a notification mechanism when new releases are 
available, so please post a message to the project 
[Discussions](https://github.com/xpack-dev-tools/arm-none-eabi-gcc-xpack/discussions) 
if you discover a new release.

## gcc, mingw-w64-gcc, riscv-none-elf-gcc

The GNU GCC project has a complex [release cycle](https://gcc.gnu.org/releases.html).

The **xPack GCC** release schedule generally follows the original GNU releases, including
the backports, with one release per year, around September.

The initial X.1.0 release comes in the first half of the year, and is skipped, 
waiting for, X.2.0, which comes a few months later. 
At the same time updates for the previous 3 major versions (like
(X-1).3.0, (X-2).4.0, (X-3).5.0) are released.

The Apple Silicon macOS binaries require a patch, usualy copied from the
HomeBrew [gcc](https://github.com/Homebrew/homebrew-core/blob/master/Formula/gcc.rb)
package using the Iain Sandoe's [forks](https://github.com/iains?tab=repositories).

## clang 

LLVM is released on a time based schedule, with major releases roughly every 6 months. 
In between major releases there may be dot releases
[Annual Release Schedule](https://llvm.org/docs/HowToReleaseLLVM.html).

The **xPack clang** project follows the official
[LLVM clang](https://github.com/llvm/llvm-project/releases/) releases,
but only the final patch of each version is released (like 16.0.6).
The rule is to wait for the new upstream release (like X.0.0), and
release the previous one (X-1.0.[567]).

For Windows builds, wait for
[llvm-mingw releases](https://github.com/mstorsjo/llvm-mingw/releases).

For macOS builds, wait for 
[HomeBrew](https://github.com/Homebrew/homebrew-core/blob/master/Formula/l/llvm.rb).

In order to spot possible issues, test builds should be performed
as soon as a new dot version become available (like X.0.1),
without making releases.

## cmake

The Kitware cmake project has no fixed release cycle, with multiple
[releases](https://github.com/Kitware/CMake/releases) per year.

The **xPack cmake** project is generally one minor release behind the upstream
releases, trying to capture the latest patch of a previous minor version;
a possible rule of thumb would be to wait for 3.x.**3**, before releasing 3.x-1.y.

## meson-build

The mson build project has no fixed release cycle, with multiple
[releases](https://github.com/mesonbuild/meson/releases/) per year.

The **xPack meson** project is generally one minor release behind the upstream
releases. In practical terms, when the minor release number changes, it awaits 
a few more weeks to get the latest patch release.

## openocd

In the past, the OpenOCD had no release schedule, and very rare
[releases](https://github.com/openocd-org/openocd/releases).

The **xPack OpenOCD** project also has no schedules, and releases are done on an
as-needed basis. As a general rule, it is planned to follow the upstream
releases and add releases from the repo HEAD from time to time.

## qemu-arm & qemu-riscv

The QEMU project has occasional [releases](https://github.com/qemu/qemu/tags).

The **xPack QEMU Arm & RISC-V** release schedule generally follows the original
upstream releases.

## windows-build-tools

The main tool is GNU make, which has no release schedule.

The **xPack Windows Build Tools** project generally follows the make release.

## wine

The WineHQ [release cycle](https://dl.winehq.org/wine/source/)
is one stable major release per year, with 2-3 patch releases. 
The development release cycle is about two weeks.

The **xPack wine** project generally plans to follow the final patch of the
stable release (like X.0.2).

## patchelf

The NixOS PatchELF has occasional
[releases](https://github.com/NixOS/patchelf/releases/).

The **xPack NixOS PatchELF** project generally follows the upstream
releases, but with a
few weeks filter, which means that releases that are overridden in
a few weeks may be skipped.

## other

For the other packages (bison, flex, m4, patchelf, pkg-config, realpath, sed), 
the upstream releases are very rare, and releases will be occasional.
