# dalvik.system

# dalvik.system

## Interfaces

| [Callback](../dalvik/system/ZipPathValidator.Callback.md) | Interface that defines the core validation mechanism when accessing zip file entry paths. |
| --- | --- |

## Classes

| [ApplicationRuntime](ApplicationRuntime.md) | Provides APIs to retrieve the information about the application loaded in the current runtime. |
| --- | --- |
| [BaseDexClassLoader](BaseDexClassLoader.md) | Base class for common functionality between various dex-based [ClassLoader](../java.lang/ClassLoader.md) implementations. |
| [DelegateLastClassLoader](DelegateLastClassLoader.md) | A`ClassLoader`implementation that implements a**delegate last**lookup policy. |
| [DexClassLoader](DexClassLoader.md) | A class loader that loads classes from`.jar`and`.apk`files containing a`classes.dex`entry. |
| --- | --- |
| [DexFile](DexFile.md) | Loads DEX files. |
| [InMemoryDexClassLoader](InMemoryDexClassLoader.md) | A [ClassLoader](../java.lang/ClassLoader.md) implementation that loads classes from a buffer containing a DEX file. |
| [PathClassLoader](PathClassLoader.md) | Provides a simple [ClassLoader](../java.lang/ClassLoader.md) implementation that operates on a list of files and directories in the local file system, but does not attempt to load classes from the network. |
| --- | --- |
| [ZipPathValidator](ZipPathValidator.md) | Enables validation of zip file entry paths to prevent exploitation of the path traversal vulnerability, e. |
