Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Os

```
class Os
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.Os](../android/system/Os.md) |

Access to low-level system functionality. Most of these are system calls. Most users will want to use higher-level APIs where available, but this class provides access to the underlying primitives used to implement the higher-level APIs.

The corresponding constants can be found in `https://developer.android.com/reference/kotlin/android/system/OsConstants`.

## Summary

| Public methods ||
|---|---|
| static [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#accept(java.io.FileDescriptor,%20java.net.InetSocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, peerAddress: https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#!)` See [accept(2)](http://man7.org/linux/man-pages/man2/accept.2.html). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#access(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [access(2)](http://man7.org/linux/man-pages/man2/access.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#bind(java.io.FileDescriptor,%20java.net.InetAddress,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, address: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [bind(2)](http://man7.org/linux/man-pages/man2/bind.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#bind(java.io.FileDescriptor,%20java.net.SocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, address: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)` See [bind(2)](http://man7.org/linux/man-pages/man2/bind.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#chmod(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [chmod(2)](http://man7.org/linux/man-pages/man2/chmod.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#chown(kotlin.String,%20kotlin.Int,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [chown(2)](http://man7.org/linux/man-pages/man2/chown.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#close(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [close(2)](http://man7.org/linux/man-pages/man2/close.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#connect(java.io.FileDescriptor,%20java.net.InetAddress,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, address: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [connect(2)](http://man7.org/linux/man-pages/man2/connect.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#connect(java.io.FileDescriptor,%20java.net.SocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, address: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)` See [connect(2)](http://man7.org/linux/man-pages/man2/connect.2.html). |
| --- | --- |
| static [StructDlInfo](../android/system/StructDlInfo.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#dladdr(kotlin.Long)(addr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [dladdr(3)](https://man7.org/linux/man-pages/man3/dladdr.3.html) |
| static [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#dup(java.io.FileDescriptor)(oldFd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [dup(2)](http://man7.org/linux/man-pages/man2/dup.2.html). |
| static [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#dup2(java.io.FileDescriptor,%20kotlin.Int)(oldFd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, newFd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [dup2(2)](http://man7.org/linux/man-pages/man2/dup2.2.html). |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/system/Os#environ()()` See [environ(3)](http://man7.org/linux/man-pages/man3/environ.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#execv(kotlin.String,%20kotlin.Array)(filename: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, argv: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` See [exec(3)](https://man7.org/linux/man-pages/man3/execv.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#execve(kotlin.String,%20kotlin.Array,%20kotlin.Array)(filename: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, argv: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, envp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` See [execve(2)](http://man7.org/linux/man-pages/man2/execve.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#fchmod(java.io.FileDescriptor,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [fchmod(2)](http://man7.org/linux/man-pages/man2/fchmod.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#fchown(java.io.FileDescriptor,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [fchown(2)](http://man7.org/linux/man-pages/man2/fchown.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#fcntlInt(java.io.FileDescriptor,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, cmd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [fcntl(2)](http://man7.org/linux/man-pages/man2/fcntl.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#fdatasync(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [fdatasync(2)](http://man7.org/linux/man-pages/man2/fdatasync.2.html). |
| static [StructStat](../android/system/StructStat.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#fstat(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [fstat(2)](http://man7.org/linux/man-pages/man2/fstat.2.html). |
| static [StructStatVfs](../android/system/StructStatVfs.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#fstatvfs(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [fstatvfs(2)](http://man7.org/linux/man-pages/man2/fstatvfs.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#fsync(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [fsync(2)](http://man7.org/linux/man-pages/man2/fsync.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#ftruncate(java.io.FileDescriptor,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [ftruncate(2)](http://man7.org/linux/man-pages/man2/ftruncate.2.html). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#gai_strerror(kotlin.Int)(error: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [gai_strerror(3)](http://man7.org/linux/man-pages/man3/gai_strerror.3.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#getegid()()` See [getegid(2)](http://man7.org/linux/man-pages/man2/getegid.2.html). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#getenv(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [getenv(3)](http://man7.org/linux/man-pages/man3/getenv.3.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#geteuid()()` See [geteuid(2)](http://man7.org/linux/man-pages/man2/geteuid.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#getgid()()` See [getgid(2)](http://man7.org/linux/man-pages/man2/getgid.2.html). |
| static [SocketAddress](../java/net/SocketAddress.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#getpeername(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [getpeername(2)](http://man7.org/linux/man-pages/man2/getpeername.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#getpid()()` See [getpid(2)](http://man7.org/linux/man-pages/man2/getpid.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#getppid()()` See [getppid(2)](http://man7.org/linux/man-pages/man2/getppid.2.html). |
| static [SocketAddress](../java/net/SocketAddress.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#getsockname(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [getsockname(2)](http://man7.org/linux/man-pages/man2/getsockname.2.html). |
| static [StructTimeval](../android/system/StructTimeval.md) | `https://developer.android.com/reference/kotlin/android/system/Os#getsockoptTimeval(java.io.FileDescriptor,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [getsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#gettid()()` See [gettid(2)](http://man7.org/linux/man-pages/man2/gettid.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#getuid()()` See [getuid(2)](http://man7.org/linux/man-pages/man2/getuid.2.html). |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#getxattr(kotlin.String,%20kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [getxattr(2)](http://man7.org/linux/man-pages/man2/getxattr.2.html) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#if_indextoname(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [if_indextoname(3)](http://man7.org/linux/man-pages/man3/if_indextoname.3.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#if_nametoindex(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [if_nametoindex(3)](http://man7.org/linux/man-pages/man3/if_nametoindex.3.html). |
| static [InetAddress](../java/net/InetAddress.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#inet_pton(kotlin.Int,%20kotlin.String)(family: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [inet_pton(3)](http://man7.org/linux/man-pages/man3/inet_pton.3.html). |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#isatty(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [isatty(3)](http://man7.org/linux/man-pages/man3/isatty.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#kill(kotlin.Int,%20kotlin.Int)(pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, signal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [kill(2)](http://man7.org/linux/man-pages/man2/kill.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#lchown(kotlin.String,%20kotlin.Int,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [lchown(2)](http://man7.org/linux/man-pages/man2/lchown.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#link(kotlin.String,%20kotlin.String)(oldPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, newPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [link(2)](http://man7.org/linux/man-pages/man2/link.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#listen(java.io.FileDescriptor,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, backlog: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [listen(2)](http://man7.org/linux/man-pages/man2/listen.2.html). |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/system/Os#listxattr(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [listxattr(2)](http://man7.org/linux/man-pages/man2/listxattr.2.html) |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#lseek(java.io.FileDescriptor,%20kotlin.Long,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, whence: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [lseek(2)](http://man7.org/linux/man-pages/man2/lseek.2.html). |
| static [StructStat](../android/system/StructStat.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#lstat(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [lstat(2)](http://man7.org/linux/man-pages/man2/lstat.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#madvise(kotlin.Long,%20kotlin.Long,%20kotlin.Int)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, advice: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [madvise(2)](http://man7.org/linux/man-pages/man2/madvise.2.html). |
| --- | --- |
| static [FileDescriptor](../java/io/FileDescriptor.md) | `https://developer.android.com/reference/kotlin/android/system/Os#memfd_create(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [memfd_create(2)](http://man7.org/linux/man-pages/man2/memfd_create.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#mincore(kotlin.Long,%20kotlin.Long,%20kotlin.ByteArray)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, vector: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` See [mincore(2)](http://man7.org/linux/man-pages/man2/mincore.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#mkdir(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [mkdir(2)](http://man7.org/linux/man-pages/man2/mkdir.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#mkfifo(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [mkfifo(3)](http://man7.org/linux/man-pages/man3/mkfifo.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#mlock(kotlin.Long,%20kotlin.Long)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [mlock(2)](http://man7.org/linux/man-pages/man2/mlock.2.html). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#mmap(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20java.io.FileDescriptor,%20kotlin.Long)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, prot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [mmap(2)](http://man7.org/linux/man-pages/man2/mmap.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#msync(kotlin.Long,%20kotlin.Long,%20kotlin.Int)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [msync(2)](http://man7.org/linux/man-pages/man2/msync.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#munlock(kotlin.Long,%20kotlin.Long)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [munlock(2)](http://man7.org/linux/man-pages/man2/munlock.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#munmap(kotlin.Long,%20kotlin.Long)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [munmap(2)](http://man7.org/linux/man-pages/man2/munmap.2.html). |
| --- | --- |
| static [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#open(kotlin.String,%20kotlin.Int,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [open(2)](http://man7.org/linux/man-pages/man2/open.2.html). |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FileDescriptor](../java/io/FileDescriptor.md)!\>! | `https://developer.android.com/reference/kotlin/android/system/Os#pipe()()` See [pipe(2)](http://man7.org/linux/man-pages/man2/pipe.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#poll(kotlin.Array,%20kotlin.Int)(fds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/system/StructPollfd!>!, timeoutMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [poll(2)](http://man7.org/linux/man-pages/man2/poll.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#posix_fallocate(java.io.FileDescriptor,%20kotlin.Long,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [posix_fallocate(3)](http://man7.org/linux/man-pages/man3/posix_fallocate.3.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#prctl(kotlin.Int,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long)(option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arg2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, arg3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, arg4: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, arg5: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [prctl(2)](http://man7.org/linux/man-pages/man2/prctl.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#pread(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [pread(2)](http://man7.org/linux/man-pages/man2/pread.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#pread(java.io.FileDescriptor,%20java.nio.ByteBuffer,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [pread(2)](http://man7.org/linux/man-pages/man2/pread.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#pwrite(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [pwrite(2)](http://man7.org/linux/man-pages/man2/pwrite.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#pwrite(java.io.FileDescriptor,%20java.nio.ByteBuffer,%20kotlin.Long)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [pwrite(2)](http://man7.org/linux/man-pages/man2/pwrite.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#read(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [read(2)](http://man7.org/linux/man-pages/man2/read.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#read(java.io.FileDescriptor,%20java.nio.ByteBuffer)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` See [read(2)](http://man7.org/linux/man-pages/man2/read.2.html). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#readlink(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [readlink(2)](http://man7.org/linux/man-pages/man2/readlink.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#readv(java.io.FileDescriptor,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.IntArray)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!, offsets: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, byteCounts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` See [readv(2)](http://man7.org/linux/man-pages/man2/readv.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#recvfrom(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.net.InetSocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcAddress: https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#!)` See [recvfrom(2)](http://man7.org/linux/man-pages/man2/recvfrom.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#recvfrom(java.io.FileDescriptor,%20java.nio.ByteBuffer,%20kotlin.Int,%20java.net.InetSocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcAddress: https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#!)` See [recvfrom(2)](http://man7.org/linux/man-pages/man2/recvfrom.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#recvmsg(java.io.FileDescriptor,%20android.system.StructMsghdr,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, msg: https://developer.android.com/reference/kotlin/android/system/StructMsghdr, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [recvmsg(2)](http://man7.org/linux/man-pages/man2/recvmsg.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#remove(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [remove(3)](http://man7.org/linux/man-pages/man3/remove.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#removexattr(kotlin.String,%20kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [removexattr(2)](http://man7.org/linux/man-pages/man2/removexattr.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#rename(kotlin.String,%20kotlin.String)(oldPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, newPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [rename(2)](http://man7.org/linux/man-pages/man2/rename.2.html). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sendfile(java.io.FileDescriptor,%20java.io.FileDescriptor,%20android.system.Int64Ref,%20kotlin.Long)(outFd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, inFd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, offset: https://developer.android.com/reference/kotlin/android/system/Int64Ref!, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` See [sendfile(2)](http://man7.org/linux/man-pages/man2/sendfile.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sendmsg(java.io.FileDescriptor,%20android.system.StructMsghdr,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, msg: https://developer.android.com/reference/kotlin/android/system/StructMsghdr, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [sendmsg(2)](http://man7.org/linux/man-pages/man2/sendmsg.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sendto(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, inetAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sendto(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.net.SocketAddress)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, address: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#?)` See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sendto(java.io.FileDescriptor,%20java.nio.ByteBuffer,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, inetAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setegid(kotlin.Int)(egid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [setegid(2)](http://man7.org/linux/man-pages/man2/setegid.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setenv(kotlin.String,%20kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, overwrite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` See [setenv(3)](http://man7.org/linux/man-pages/man3/setenv.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#seteuid(kotlin.Int)(euid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [seteuid(2)](http://man7.org/linux/man-pages/man2/seteuid.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setgid(kotlin.Int)(gid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [setgid(2)](http://man7.org/linux/man-pages/man2/setgid.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setsid()()` See [setsid(2)](http://man7.org/linux/man-pages/man2/setsid.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setsockoptInt(java.io.FileDescriptor,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [setsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setsockoptTimeval(java.io.FileDescriptor,%20kotlin.Int,%20kotlin.Int,%20android.system.StructTimeval)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://developer.android.com/reference/kotlin/android/system/StructTimeval)` See [setsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setuid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [setuid(2)](http://man7.org/linux/man-pages/man2/setuid.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#setxattr(kotlin.String,%20kotlin.String,%20kotlin.ByteArray,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [setxattr(2)](http://man7.org/linux/man-pages/man2/setxattr.2.html) |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#shutdown(java.io.FileDescriptor,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, how: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [shutdown(2)](http://man7.org/linux/man-pages/man2/shutdown.2.html). |
| static [FileDescriptor](../java/io/FileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#socket(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(domain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [socket(2)](http://man7.org/linux/man-pages/man2/socket.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#socketpair(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.io.FileDescriptor,%20java.io.FileDescriptor)(domain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fd1: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, fd2: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [socketpair(2)](http://man7.org/linux/man-pages/man2/socketpair.2.html). |
| --- | --- |
| static [StructStat](../android/system/StructStat.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#stat(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [stat(2)](http://man7.org/linux/man-pages/man2/stat.2.html). |
| static [StructStatVfs](../android/system/StructStatVfs.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#statvfs(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [statvfs(2)](http://man7.org/linux/man-pages/man2/statvfs.2.html). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#strerror(kotlin.Int)(errno: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [strerror(2)](http://man7.org/linux/man-pages/man3/strerror.3.html). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/system/Os#strsignal(kotlin.Int)(signal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [strsignal(3)](http://man7.org/linux/man-pages/man3/strsignal.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#symlink(kotlin.String,%20kotlin.String)(oldPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, newPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [symlink(2)](http://man7.org/linux/man-pages/man2/symlink.2.html). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#sysconf(kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [sysconf(3)](http://man7.org/linux/man-pages/man3/sysconf.3.html). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#tcdrain(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!)` See [tcdrain(3)](http://man7.org/linux/man-pages/man3/tcdrain.3.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#tcsendbreak(java.io.FileDescriptor,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, duration: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [tcsendbreak(3)](http://man7.org/linux/man-pages/man3/tcsendbreak.3.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#umask(kotlin.Int)(mask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [umask(2)](http://man7.org/linux/man-pages/man2/umask.2.html). |
| --- | --- |
| static [StructUtsname](../android/system/StructUtsname.md)! | `https://developer.android.com/reference/kotlin/android/system/Os#uname()()` See [uname(2)](http://man7.org/linux/man-pages/man2/uname.2.html). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#unsetenv(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` See [unsetenv(3)](http://man7.org/linux/man-pages/man3/unsetenv.3.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#write(java.io.FileDescriptor,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, byteOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` See [write(2)](http://man7.org/linux/man-pages/man2/write.2.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#write(java.io.FileDescriptor,%20java.nio.ByteBuffer)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` See [write(2)](http://man7.org/linux/man-pages/man2/write.2.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/system/Os#writev(java.io.FileDescriptor,%20kotlin.Array,%20kotlin.IntArray,%20kotlin.IntArray)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, buffers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!, offsets: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, byteCounts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` See [writev(2)](http://man7.org/linux/man-pages/man2/writev.2.html). |

## Public methods

### accept

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun accept(
    fd: FileDescriptor!, 
    peerAddress: InetSocketAddress!
): FileDescriptor!
```

See [accept(2)](http://man7.org/linux/man-pages/man2/accept.2.html).

### access

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun access(
    path: String!, 
    mode: Int
): Boolean
```

See [access(2)](http://man7.org/linux/man-pages/man2/access.2.html).

### bind

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun bind(
    fd: FileDescriptor!, 
    address: InetAddress!, 
    port: Int
): Unit
```

See [bind(2)](http://man7.org/linux/man-pages/man2/bind.2.html).

### bind

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun bind(
    fd: FileDescriptor, 
    address: SocketAddress
): Unit
```

See [bind(2)](http://man7.org/linux/man-pages/man2/bind.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `address` | [SocketAddress](../java/net/SocketAddress.md): This value cannot be `null`. |

### chmod

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun chmod(
    path: String!, 
    mode: Int
): Unit
```

See [chmod(2)](http://man7.org/linux/man-pages/man2/chmod.2.html).

### chown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun chown(
    path: String!, 
    uid: Int, 
    gid: Int
): Unit
```

See [chown(2)](http://man7.org/linux/man-pages/man2/chown.2.html).

### close

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun close(fd: FileDescriptor!): Unit
```

See [close(2)](http://man7.org/linux/man-pages/man2/close.2.html).

### connect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun connect(
    fd: FileDescriptor!, 
    address: InetAddress!, 
    port: Int
): Unit
```

See [connect(2)](http://man7.org/linux/man-pages/man2/connect.2.html).

### connect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun connect(
    fd: FileDescriptor, 
    address: SocketAddress
): Unit
```

See [connect(2)](http://man7.org/linux/man-pages/man2/connect.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `address` | [SocketAddress](../java/net/SocketAddress.md): This value cannot be `null`. |

### dladdr

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun dladdr(addr: Long): StructDlInfo!
```

See [dladdr(3)](https://man7.org/linux/man-pages/man3/dladdr.3.html)

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/system/StructDlInfo!` | null if the underlying native `dladdr` call fails. |

### dup

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun dup(oldFd: FileDescriptor!): FileDescriptor!
```

See [dup(2)](http://man7.org/linux/man-pages/man2/dup.2.html).

### dup2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun dup2(
    oldFd: FileDescriptor!, 
    newFd: Int
): FileDescriptor!
```

See [dup2(2)](http://man7.org/linux/man-pages/man2/dup2.2.html).

### environ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun environ(): Array<String!>!
```

See [environ(3)](http://man7.org/linux/man-pages/man3/environ.3.html).

### execv

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun execv(
    filename: String!, 
    argv: Array<String!>!
): Unit
```

See [exec(3)](https://man7.org/linux/man-pages/man3/execv.3.html).

### execve

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun execve(
    filename: String!, 
    argv: Array<String!>!, 
    envp: Array<String!>!
): Unit
```

See [execve(2)](http://man7.org/linux/man-pages/man2/execve.2.html).

### fchmod

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fchmod(
    fd: FileDescriptor!, 
    mode: Int
): Unit
```

See [fchmod(2)](http://man7.org/linux/man-pages/man2/fchmod.2.html).

### fchown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fchown(
    fd: FileDescriptor!, 
    uid: Int, 
    gid: Int
): Unit
```

See [fchown(2)](http://man7.org/linux/man-pages/man2/fchown.2.html).

### fcntlInt

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fcntlInt(
    fd: FileDescriptor, 
    cmd: Int, 
    arg: Int
): Int
```

See [fcntl(2)](http://man7.org/linux/man-pages/man2/fcntl.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |

### fdatasync

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fdatasync(fd: FileDescriptor!): Unit
```

See [fdatasync(2)](http://man7.org/linux/man-pages/man2/fdatasync.2.html).

### fstat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fstat(fd: FileDescriptor!): StructStat!
```

See [fstat(2)](http://man7.org/linux/man-pages/man2/fstat.2.html).

### fstatvfs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fstatvfs(fd: FileDescriptor!): StructStatVfs!
```

See [fstatvfs(2)](http://man7.org/linux/man-pages/man2/fstatvfs.2.html).

### fsync

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fsync(fd: FileDescriptor!): Unit
```

See [fsync(2)](http://man7.org/linux/man-pages/man2/fsync.2.html).

### ftruncate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ftruncate(
    fd: FileDescriptor!, 
    length: Long
): Unit
```

See [ftruncate(2)](http://man7.org/linux/man-pages/man2/ftruncate.2.html).

### gai_strerror

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun gai_strerror(error: Int): String!
```

See [gai_strerror(3)](http://man7.org/linux/man-pages/man3/gai_strerror.3.html).

### getegid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getegid(): Int
```

See [getegid(2)](http://man7.org/linux/man-pages/man2/getegid.2.html).

### getenv

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getenv(name: String!): String!
```

See [getenv(3)](http://man7.org/linux/man-pages/man3/getenv.3.html).

### geteuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun geteuid(): Int
```

See [geteuid(2)](http://man7.org/linux/man-pages/man2/geteuid.2.html).

### getgid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getgid(): Int
```

See [getgid(2)](http://man7.org/linux/man-pages/man2/getgid.2.html).

### getpeername

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getpeername(fd: FileDescriptor!): SocketAddress!
```

See [getpeername(2)](http://man7.org/linux/man-pages/man2/getpeername.2.html).

### getpid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getpid(): Int
```

See [getpid(2)](http://man7.org/linux/man-pages/man2/getpid.2.html).

### getppid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getppid(): Int
```

See [getppid(2)](http://man7.org/linux/man-pages/man2/getppid.2.html).

### getsockname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getsockname(fd: FileDescriptor!): SocketAddress!
```

See [getsockname(2)](http://man7.org/linux/man-pages/man2/getsockname.2.html).

### getsockoptTimeval

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getsockoptTimeval(
    fd: FileDescriptor, 
    level: Int, 
    option: Int
): StructTimeval
```

See [getsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html).

Only for use with `option` values that return a `struct timeval` such as `https://developer.android.com/reference/kotlin/android/system/OsConstants#SO_RCVTIMEO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/system/OsConstants#SO_SNDTIMEO:kotlin.Int`. Use with other options may throw an `IllegalArgumentException` or return junk values.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/system/StructTimeval` | This value cannot be `null`. |

### gettid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun gettid(): Int
```

See [gettid(2)](http://man7.org/linux/man-pages/man2/gettid.2.html).

### getuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getuid(): Int
```

See [getuid(2)](http://man7.org/linux/man-pages/man2/getuid.2.html).

### getxattr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getxattr(
    path: String!, 
    name: String!
): ByteArray!
```

See [getxattr(2)](http://man7.org/linux/man-pages/man2/getxattr.2.html)

### if_indextoname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun if_indextoname(index: Int): String!
```

See [if_indextoname(3)](http://man7.org/linux/man-pages/man3/if_indextoname.3.html).

### if_nametoindex

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun if_nametoindex(name: String!): Int
```

See [if_nametoindex(3)](http://man7.org/linux/man-pages/man3/if_nametoindex.3.html).

### inet_pton

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun inet_pton(
    family: Int, 
    address: String!
): InetAddress!
```

See [inet_pton(3)](http://man7.org/linux/man-pages/man3/inet_pton.3.html).

### isatty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isatty(fd: FileDescriptor!): Boolean
```

See [isatty(3)](http://man7.org/linux/man-pages/man3/isatty.3.html).

### kill

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun kill(
    pid: Int, 
    signal: Int
): Unit
```

See [kill(2)](http://man7.org/linux/man-pages/man2/kill.2.html).

### lchown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lchown(
    path: String!, 
    uid: Int, 
    gid: Int
): Unit
```

See [lchown(2)](http://man7.org/linux/man-pages/man2/lchown.2.html).

### link

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun link(
    oldPath: String!, 
    newPath: String!
): Unit
```

See [link(2)](http://man7.org/linux/man-pages/man2/link.2.html).

### listen

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun listen(
    fd: FileDescriptor!, 
    backlog: Int
): Unit
```

See [listen(2)](http://man7.org/linux/man-pages/man2/listen.2.html).

### listxattr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun listxattr(path: String!): Array<String!>!
```

See [listxattr(2)](http://man7.org/linux/man-pages/man2/listxattr.2.html)

### lseek

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lseek(
    fd: FileDescriptor!, 
    offset: Long, 
    whence: Int
): Long
```

See [lseek(2)](http://man7.org/linux/man-pages/man2/lseek.2.html).

### lstat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lstat(path: String!): StructStat!
```

See [lstat(2)](http://man7.org/linux/man-pages/man2/lstat.2.html).

### madvise

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun madvise(
    address: Long, 
    byteCount: Long, 
    advice: Int
): Unit
```

See [madvise(2)](http://man7.org/linux/man-pages/man2/madvise.2.html).

### memfd_create

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun memfd_create(
    name: String, 
    flags: Int
): FileDescriptor
```

See [memfd_create(2)](http://man7.org/linux/man-pages/man2/memfd_create.2.html).

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#` | This value cannot be `null`. |

### mincore

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mincore(
    address: Long, 
    byteCount: Long, 
    vector: ByteArray!
): Unit
```

See [mincore(2)](http://man7.org/linux/man-pages/man2/mincore.2.html).

### mkdir

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mkdir(
    path: String!, 
    mode: Int
): Unit
```

See [mkdir(2)](http://man7.org/linux/man-pages/man2/mkdir.2.html).

### mkfifo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mkfifo(
    path: String!, 
    mode: Int
): Unit
```

See [mkfifo(3)](http://man7.org/linux/man-pages/man3/mkfifo.3.html).

### mlock

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mlock(
    address: Long, 
    byteCount: Long
): Unit
```

See [mlock(2)](http://man7.org/linux/man-pages/man2/mlock.2.html).

### mmap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mmap(
    address: Long, 
    byteCount: Long, 
    prot: Int, 
    flags: Int, 
    fd: FileDescriptor!, 
    offset: Long
): Long
```

See [mmap(2)](http://man7.org/linux/man-pages/man2/mmap.2.html).

### msync

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun msync(
    address: Long, 
    byteCount: Long, 
    flags: Int
): Unit
```

See [msync(2)](http://man7.org/linux/man-pages/man2/msync.2.html).

### munlock

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun munlock(
    address: Long, 
    byteCount: Long
): Unit
```

See [munlock(2)](http://man7.org/linux/man-pages/man2/munlock.2.html).

### munmap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun munmap(
    address: Long, 
    byteCount: Long
): Unit
```

See [munmap(2)](http://man7.org/linux/man-pages/man2/munmap.2.html).

### open

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun open(
    path: String!, 
    flags: Int, 
    mode: Int
): FileDescriptor!
```

See [open(2)](http://man7.org/linux/man-pages/man2/open.2.html).

### pipe

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pipe(): Array<FileDescriptor!>!
```

See [pipe(2)](http://man7.org/linux/man-pages/man2/pipe.2.html).

### poll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun poll(
    fds: Array<StructPollfd!>!, 
    timeoutMs: Int
): Int
```

See [poll(2)](http://man7.org/linux/man-pages/man2/poll.2.html).

Note that in Lollipop this could throw an `ErrnoException` with `EINTR`. In later releases, the implementation will automatically just restart the system call with an appropriately reduced timeout.

### posix_fallocate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun posix_fallocate(
    fd: FileDescriptor!, 
    offset: Long, 
    length: Long
): Unit
```

See [posix_fallocate(3)](http://man7.org/linux/man-pages/man3/posix_fallocate.3.html).

### prctl

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun prctl(
    option: Int, 
    arg2: Long, 
    arg3: Long, 
    arg4: Long, 
    arg5: Long
): Int
```

See [prctl(2)](http://man7.org/linux/man-pages/man2/prctl.2.html).

### pread

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pread(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int, 
    offset: Long
): Int
```

See [pread(2)](http://man7.org/linux/man-pages/man2/pread.2.html).

### pread

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pread(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!, 
    offset: Long
): Int
```

See [pread(2)](http://man7.org/linux/man-pages/man2/pread.2.html).

### pwrite

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pwrite(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int, 
    offset: Long
): Int
```

See [pwrite(2)](http://man7.org/linux/man-pages/man2/pwrite.2.html).

### pwrite

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pwrite(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!, 
    offset: Long
): Int
```

See [pwrite(2)](http://man7.org/linux/man-pages/man2/pwrite.2.html).

### read

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun read(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int
): Int
```

See [read(2)](http://man7.org/linux/man-pages/man2/read.2.html).

### read

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun read(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!
): Int
```

See [read(2)](http://man7.org/linux/man-pages/man2/read.2.html).

### readlink

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun readlink(path: String!): String!
```

See [readlink(2)](http://man7.org/linux/man-pages/man2/readlink.2.html).

### readv

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun readv(
    fd: FileDescriptor!, 
    buffers: Array<Any!>!, 
    offsets: IntArray!, 
    byteCounts: IntArray!
): Int
```

See [readv(2)](http://man7.org/linux/man-pages/man2/readv.2.html).

### recvfrom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun recvfrom(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int, 
    flags: Int, 
    srcAddress: InetSocketAddress!
): Int
```

See [recvfrom(2)](http://man7.org/linux/man-pages/man2/recvfrom.2.html).

### recvfrom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun recvfrom(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!, 
    flags: Int, 
    srcAddress: InetSocketAddress!
): Int
```

See [recvfrom(2)](http://man7.org/linux/man-pages/man2/recvfrom.2.html).

### recvmsg

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun recvmsg(
    fd: FileDescriptor, 
    msg: StructMsghdr, 
    flags: Int
): Int
```

See [recvmsg(2)](http://man7.org/linux/man-pages/man2/recvmsg.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `msg` | [StructMsghdr](../android/system/StructMsghdr.md): This value cannot be `null`. |

### remove

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun remove(path: String!): Unit
```

See [remove(3)](http://man7.org/linux/man-pages/man3/remove.3.html).

### removexattr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun removexattr(
    path: String!, 
    name: String!
): Unit
```

See [removexattr(2)](http://man7.org/linux/man-pages/man2/removexattr.2.html).

### rename

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun rename(
    oldPath: String!, 
    newPath: String!
): Unit
```

See [rename(2)](http://man7.org/linux/man-pages/man2/rename.2.html).

### sendfile

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendfile(
    outFd: FileDescriptor!, 
    inFd: FileDescriptor!, 
    offset: Int64Ref!, 
    byteCount: Long
): Long
```

See [sendfile(2)](http://man7.org/linux/man-pages/man2/sendfile.2.html).

### sendmsg

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendmsg(
    fd: FileDescriptor, 
    msg: StructMsghdr, 
    flags: Int
): Int
```

See [sendmsg(2)](http://man7.org/linux/man-pages/man2/sendmsg.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `msg` | [StructMsghdr](../android/system/StructMsghdr.md): This value cannot be `null`. |

### sendto

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendto(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int, 
    flags: Int, 
    inetAddress: InetAddress!, 
    port: Int
): Int
```

See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html).

### sendto

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendto(
    fd: FileDescriptor, 
    bytes: ByteArray, 
    byteOffset: Int, 
    byteCount: Int, 
    flags: Int, 
    address: SocketAddress?
): Int
```

See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html).

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |
| `address` | [SocketAddress](../java/net/SocketAddress.md)?: This value may be `null`. |
| --- | --- |

### sendto

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendto(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!, 
    flags: Int, 
    inetAddress: InetAddress!, 
    port: Int
): Int
```

See [sendto(2)](http://man7.org/linux/man-pages/man2/sendto.2.html).

### setegid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setegid(egid: Int): Unit
```

**Deprecated:** *Android Applications do not have sufficient privileges to call this method.*

See [setegid(2)](http://man7.org/linux/man-pages/man2/setegid.2.html).

### setenv

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setenv(
    name: String!, 
    value: String!, 
    overwrite: Boolean
): Unit
```

See [setenv(3)](http://man7.org/linux/man-pages/man3/setenv.3.html).

### seteuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun seteuid(euid: Int): Unit
```

**Deprecated:** *Android Applications do not have sufficient privileges to call this method.*

See [seteuid(2)](http://man7.org/linux/man-pages/man2/seteuid.2.html).

### setgid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setgid(gid: Int): Unit
```

**Deprecated:** *Android Applications do not have sufficient privileges to call this method.*

See [setgid(2)](http://man7.org/linux/man-pages/man2/setgid.2.html).

### setsid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setsid(): Int
```

See [setsid(2)](http://man7.org/linux/man-pages/man2/setsid.2.html).

### setsockoptInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setsockoptInt(
    fd: FileDescriptor!, 
    level: Int, 
    option: Int, 
    value: Int
): Unit
```

See [setsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html).

### setsockoptTimeval

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setsockoptTimeval(
    fd: FileDescriptor, 
    level: Int, 
    option: Int, 
    value: StructTimeval
): Unit
```

See [setsockopt(2)](http://man7.org/linux/man-pages/man2/setsockopt.2.html).

Only for use with `option` values that take a `struct timeval` such as `https://developer.android.com/reference/kotlin/android/system/OsConstants#SO_RCVTIMEO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/system/OsConstants#SO_SNDTIMEO:kotlin.Int`. Use with other options is likely to cause incorrect behavior.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md): This value cannot be `null`. |
| `value` | [StructTimeval](../android/system/StructTimeval.md): This value cannot be `null`. |

### setuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setuid(uid: Int): Unit
```

**Deprecated:** *Android Applications do not have sufficient privileges to call this method.*

See [setuid(2)](http://man7.org/linux/man-pages/man2/setuid.2.html).

### setxattr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setxattr(
    path: String!, 
    name: String!, 
    value: ByteArray!, 
    flags: Int
): Unit
```

See [setxattr(2)](http://man7.org/linux/man-pages/man2/setxattr.2.html)

### shutdown

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun shutdown(
    fd: FileDescriptor!, 
    how: Int
): Unit
```

See [shutdown(2)](http://man7.org/linux/man-pages/man2/shutdown.2.html).

### socket

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun socket(
    domain: Int, 
    type: Int, 
    protocol: Int
): FileDescriptor!
```

See [socket(2)](http://man7.org/linux/man-pages/man2/socket.2.html).

### socketpair

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun socketpair(
    domain: Int, 
    type: Int, 
    protocol: Int, 
    fd1: FileDescriptor!, 
    fd2: FileDescriptor!
): Unit
```

See [socketpair(2)](http://man7.org/linux/man-pages/man2/socketpair.2.html).

### stat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stat(path: String!): StructStat!
```

See [stat(2)](http://man7.org/linux/man-pages/man2/stat.2.html).

### statvfs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun statvfs(path: String!): StructStatVfs!
```

See [statvfs(2)](http://man7.org/linux/man-pages/man2/statvfs.2.html).

### strerror

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun strerror(errno: Int): String!
```

See [strerror(2)](http://man7.org/linux/man-pages/man3/strerror.3.html).

### strsignal

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun strsignal(signal: Int): String!
```

See [strsignal(3)](http://man7.org/linux/man-pages/man3/strsignal.3.html).

### symlink

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun symlink(
    oldPath: String!, 
    newPath: String!
): Unit
```

See [symlink(2)](http://man7.org/linux/man-pages/man2/symlink.2.html).

### sysconf

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sysconf(name: Int): Long
```

See [sysconf(3)](http://man7.org/linux/man-pages/man3/sysconf.3.html).

### tcdrain

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun tcdrain(fd: FileDescriptor!): Unit
```

See [tcdrain(3)](http://man7.org/linux/man-pages/man3/tcdrain.3.html).

### tcsendbreak

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun tcsendbreak(
    fd: FileDescriptor!, 
    duration: Int
): Unit
```

See [tcsendbreak(3)](http://man7.org/linux/man-pages/man3/tcsendbreak.3.html).

### umask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun umask(mask: Int): Int
```

See [umask(2)](http://man7.org/linux/man-pages/man2/umask.2.html).

### uname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun uname(): StructUtsname!
```

See [uname(2)](http://man7.org/linux/man-pages/man2/uname.2.html).

### unsetenv

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsetenv(name: String!): Unit
```

See [unsetenv(3)](http://man7.org/linux/man-pages/man3/unsetenv.3.html).

### write

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun write(
    fd: FileDescriptor!, 
    bytes: ByteArray!, 
    byteOffset: Int, 
    byteCount: Int
): Int
```

See [write(2)](http://man7.org/linux/man-pages/man2/write.2.html).

### write

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun write(
    fd: FileDescriptor!, 
    buffer: ByteBuffer!
): Int
```

See [write(2)](http://man7.org/linux/man-pages/man2/write.2.html).

### writev

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun writev(
    fd: FileDescriptor!, 
    buffers: Array<Any!>!, 
    offsets: IntArray!, 
    byteCounts: IntArray!
): Int
```

See [writev(2)](http://man7.org/linux/man-pages/man2/writev.2.html).
