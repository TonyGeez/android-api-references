# dalvik.system

# dalvik.system

## Interfaces

| [Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback) | Interface that defines the core validation mechanism when accessing zip file entry paths. |
| --- | --- |

## Classes

| [ApplicationRuntime](https://developer.android.com/reference/kotlin/dalvik/system/ApplicationRuntime) | Provides APIs to retrieve the information about the application loaded in the current runtime. |
| --- | --- |
| [BaseDexClassLoader](https://developer.android.com/reference/kotlin/dalvik/system/BaseDexClassLoader) | Base class for common functionality between various dex-based [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#) implementations. |
| [DelegateLastClassLoader](https://developer.android.com/reference/kotlin/dalvik/system/DelegateLastClassLoader) | A`ClassLoader`implementation that implements a**delegate last**lookup policy. |
| [DexClassLoader](https://developer.android.com/reference/kotlin/dalvik/system/DexClassLoader) | A class loader that loads classes from`.jar`and`.apk`files containing a`classes.dex`entry. |
| --- | --- |
| [DexFile](https://developer.android.com/reference/kotlin/dalvik/system/DexFile) | Loads DEX files. |
| [InMemoryDexClassLoader](https://developer.android.com/reference/kotlin/dalvik/system/InMemoryDexClassLoader) | A [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#) implementation that loads classes from a buffer containing a DEX file. |
| [PathClassLoader](https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader) | Provides a simple [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#) implementation that operates on a list of files and directories in the local file system, but does not attempt to load classes from the network. |
| --- | --- |
| [ZipPathValidator](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator) | Enables validation of zip file entry paths to prevent exploitation of the path traversal vulnerability, e. |
