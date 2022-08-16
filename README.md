Kotlin Linux Template
A basic template for developing Linux programs using
Kotlin Native. This templates uses
Kotlin 1.4.10, and covers the following Kotlin Native Linux targets:


linuxArm32Hfp (supports ARM v7 CPU)

linuxArm64 (supports ARM v8 CPU)

linuxX64 (supports AMD64 based CPUs)

It is important to note that a Kotlin Native Linux binary will only work on a supported CPU, where the device is
running a Linux distribution that bundles glibc (Ubuntu, Debian, Linux Mint etc),
NOT Musl Libc (eg Alpine Linux). Currently there is an unresolved issue in the Kotlin
issue tracker on running binaries on Alpine Linux.

Gradle Tasks
Use the runLinux_appDebugExecutableLinuxX64, or runLinux_appReleaseExecutableLinuxX64 Gradle task to run a Linux
X64 program. Binaries for other targets must be run manually outside of Gradle. To generate a Linux debug binary
(contains debugging information) use one of the following Gradle tasks:

linkLinux_appDebugExecutableLinuxX64
linkLinux_appDebugExecutableLinuxArm32
linkLinux_appDebugExecutableLinuxArm64

To generate a Linux release binary (stripped of debugging information) use one of the following Grade tasks:

linkLinux_appReleaseExecutableLinuxX64
linkLinux_appReleaseExecutableLinuxArm32
linkLinux_appReleaseExecutableLinuxArm64

Build artifacts can be removed by running the clean Gradle task.
