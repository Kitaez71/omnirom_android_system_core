# omnirom/android_system_core for android 5.1
The system/ directory is intended for pieces of the world that are the
core of the embedded linux platform at the heart of Android.  These
essential bits are required for basic booting, operation, and debugging.

They should not depend on libraries outside of system/... (some of them
do currently -- they need to be updated or changed) and they should not
be required for the simulator build.

The license for all these pieces should be clean (Apache2, BSD, or MIT).

Currently system/bluetooth/... and system/extra/... have some pieces
with GPL/LGPL licensed code.

Assorted Issues:

- pppd depends on libutils for logging
- pppd depends on libcrypt/libcrypto
- init, linker, debuggerd, toolbox, usbd depend on libcutils
- should probably rename bionic to libc
