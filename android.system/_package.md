# android.system

# android.system

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [Int64Ref](Int64Ref.md) | A signed 64bit integer reference suitable for passing to lower-level system calls. |
| --- | --- |
| [Os](Os.md) | Access to low-level system functionality. |
| [OsConstants](OsConstants.md) | Constants and helper functions for use with [Os](Os.md). |
| [StructCmsghdr](StructCmsghdr.md) | Corresponds to C's`struct cmsghdr`. |
| --- | --- |
| [StructDlInfo](StructDlInfo.md) | Corresponds to C's`struct Dl_info`. |
| [StructMsghdr](StructMsghdr.md) | Corresponds to C's`struct msghdr` |
| [StructPollfd](StructPollfd.md) | Used as an in/out parameter to [Os.poll](Os.md)). |
| --- | --- |
| [StructStat](StructStat.md) | File information returned by [Os.fstat](Os.md)), [Os.lstat](Os.md)), and [Os.stat](Os.md)). |
| [StructStatVfs](StructStatVfs.md) | File information returned by [Os.fstatvfs](Os.md))and [Os.statvfs](Os.md)). |
| [StructTimespec](StructTimespec.md) | Corresponds to C's`struct timespec`from`<time.h>`. |
| --- | --- |
| [StructTimeval](StructTimeval.md) | Corresponds to C's`struct timeval`from`sys/time.h`. |
| [StructUtsname](StructUtsname.md) | Information returned by [Os.uname](Os.md)). |
| [SystemCleaner](SystemCleaner.md) | Java. |
| --- | --- |
| [VmSocketAddress](VmSocketAddress.md) | A virtio-vsock address [VmSocketAddress](VmSocketAddress.md). |

## Exceptions

| [ErrnoException](ErrnoException.md) | A checked exception thrown when [Os](Os.md) methods fail. |
| --- | --- |
