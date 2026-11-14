Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystems

```
class FileSystems
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.file.FileSystems](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#) |

Factory methods for file systems. This class defines the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getDefault()` method to get the default file system and factory methods to construct other types of file systems.

The first invocation of any of the methods defined by this class causes the default `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider` to be loaded. The default provider, identified by the URI scheme "file", creates the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem` that provides access to the file systems accessible to the Java virtual machine. If the process of loading or initializing the default provider fails then an unspecified error is thrown.

The first invocation of the `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders()` method, by way of invoking any of the `newFileSystem` methods defined by this class, locates and loads all installed file system providers. Installed providers are loaded using the service-provider loading facility defined by the `https://developer.android.com/reference/kotlin/java/util/ServiceLoader.html#` class. Installed providers are loaded using the system class loader. If the system class loader cannot be found then the platform class loader is used. Providers are typically installed by placing them in a JAR file on the application class path, the JAR file contains a provider-configuration file named `java.nio.file.spi.FileSystemProvider` in the resource directory `META-INF/services`, and the file lists one or more fully-qualified names of concrete subclass of `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider` that have a zero argument constructor. The ordering that installed providers are located is implementation specific. If a provider is instantiated and its `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getScheme()` returns the same URI scheme of a provider that was previously instantiated then the most recently instantiated duplicate is discarded. URI schemes are compared without regard to case. During construction a provider may safely access files associated with the default provider but care needs to be taken to avoid circular loading of other installed providers. If circular loading of installed providers is detected then an unspecified error is thrown.

This class also defines factory methods that allow a `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` to be specified when locating a provider. As with installed providers, the provider classes are identified by placing the provider configuration file in the resource directory `META-INF/services`.

If a thread initiates the loading of the installed file system providers and another thread invokes a method that also attempts to load the providers then the method will block until the loading completes.

## Summary

| Public methods ||
|---|---|
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getDefault()()` Returns the default `FileSystem`. |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getFileSystem(java.net.URI)(uri: https://developer.android.com/reference/kotlin/java/net/URI.html#!)` Returns a reference to an existing `FileSystem`. |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap)(uri: https://developer.android.com/reference/kotlin/java/net/URI.html#!, env: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, *>!)` Constructs a new file system that is identified by a `https://developer.android.com/reference/kotlin/java/net/URI.html#` |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap,%20java.lang.ClassLoader)(uri: https://developer.android.com/reference/kotlin/java/net/URI.html#!, env: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, *>!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Constructs a new file system that is identified by a `https://developer.android.com/reference/kotlin/java/net/URI.html#` |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path)(path: https://developer.android.com/reference/kotlin/java/nio/file/Path!)` Constructs a new `FileSystem` to access the contents of a file as a file system. |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20java.lang.ClassLoader)(path: https://developer.android.com/reference/kotlin/java/nio/file/Path!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Constructs a new `FileSystem` to access the contents of a file as a file system. |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap)(path: https://developer.android.com/reference/kotlin/java/nio/file/Path!, env: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, *>!)` Constructs a new `FileSystem` to access the contents of a file as a file system. |
| static [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem)! | `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap,%20java.lang.ClassLoader)(path: https://developer.android.com/reference/kotlin/java/nio/file/Path!, env: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, *>!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Constructs a new `FileSystem` to access the contents of a file as a file system. |

## Public methods

### getDefault

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefault(): FileSystem!
```

Returns the default `FileSystem`. The default file system creates objects that provide access to the file systems accessible to the Java virtual machine. The *working directory* of the file system is the current user directory, named by the system property `user.dir`. This allows for interoperability with the `https://developer.android.com/reference/kotlin/java/io/File.html#` class.

The first invocation of any of the methods defined by this class locates the default `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider` object. Where the system property `java.nio.file.spi.DefaultFileSystemProvider` is not defined then the default provider is a system-default provider that is invoked to create the default file system.

If the system property `java.nio.file.spi.DefaultFileSystemProvider` is defined then it is taken to be a list of one or more fully-qualified names of concrete provider classes identified by the URI scheme `"file"`. Where the property is a list of more than one name then the names are separated by a comma. Each class is loaded, using the system class loader, and instantiated by invoking a one argument constructor whose formal parameter type is `FileSystemProvider`. The providers are loaded and instantiated in the order they are listed in the property. If this process fails or a provider's scheme is not equal to `"file"` then an unspecified error is thrown. URI schemes are normally compared without regard to case but for the default provider, the scheme is required to be `"file"`. The first provider class is instantiated by invoking it with a reference to the system-default provider. The second provider class is instantiated by invoking it with a reference to the first provider instance. The third provider class is instantiated by invoking it with a reference to the second instance, and so on. The last provider to be instantiated becomes the default provider; its `getFileSystem` method is invoked with the URI `"file:///"` to get a reference to the default file system.

Subsequent invocations of this method return the file system that was returned by the first invocation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | the default file system |

### getFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getFileSystem(uri: URI!): FileSystem!
```

Returns a reference to an existing `FileSystem`.

This method iterates over the `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders()` providers to locate the provider that is identified by the URI `https://developer.android.com/reference/kotlin/java/net/URI.html#getScheme()` of the given URI. URI schemes are compared without regard to case. The exact form of the URI is highly provider dependent. If found, the provider's `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getFileSystem(java.net.URI)` method is invoked to obtain a reference to the `FileSystem`.

Once a file system created by this provider is java.nio.file.FileSystem#close it is provider-dependent if this method returns a reference to the closed file system or throws `https://developer.android.com/reference/kotlin/java/nio/file/FileSystemNotFoundException`. If the provider allows a new file system to be created with the same URI as a file system it previously created then this method throws the exception if invoked after the file system is closed (and before a new instance is created by the #newFileSystem method).

If a security manager is installed then a provider implementation may require to check a permission before returning a reference to an existing file system. In the case of the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#getDefault()` file system, no permission check is required.

| Parameters ||
|---|---|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!: the URI to locate the file system |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | the reference to the file system |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pre-conditions for the `uri` parameter are not met |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission |
| `java.nio.file.FileSystemNotFoundException` | if the file system, identified by the URI, does not exist |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting the URI scheme is not installed |

### newFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(
    uri: URI!, 
    env: MutableMap<String!, *>!
): FileSystem!
```

Constructs a new file system that is identified by a `https://developer.android.com/reference/kotlin/java/net/URI.html#`

This method iterates over the `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders()` providers to locate the provider that is identified by the URI `https://developer.android.com/reference/kotlin/java/net/URI.html#getScheme()` of the given URI. URI schemes are compared without regard to case. The exact form of the URI is highly provider dependent. If found, the provider's `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap)` method is invoked to construct the new file system.

Once a file system is java.nio.file.FileSystem#close it is provider-dependent if the provider allows a new file system to be created with the same URI as a file system it previously created.

**Usage Example:** Suppose there is a provider identified by the scheme `"memory"` installed:

```kotlin
FileSystem fs = FileSystems.newFileSystem(URI.create("memory:///?name=logfs"),
                                             Map.of("capacity", "16G", "blockSize", "4k"));
  
```

| Parameters ||
|---|---|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!: the URI identifying the file system |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!: a map of provider specific properties to configure the file system; may be empty |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs creating the file system |
| `java.lang.IllegalArgumentException` | if the pre-conditions for the `uri` parameter are not met, or the `env` parameter does not contain properties required by the provider, or a property value is invalid |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission required by the file system provider implementation |
| `java.nio.file.FileSystemAlreadyExistsException` | if the file system has already been created |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting the URI scheme is not installed |

### newFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(
    uri: URI!, 
    env: MutableMap<String!, *>!, 
    loader: ClassLoader!
): FileSystem!
```

Constructs a new file system that is identified by a `https://developer.android.com/reference/kotlin/java/net/URI.html#`

This method first attempts to locate an installed provider in exactly the same manner as the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap)` method. If none of the installed providers support the URI scheme then an attempt is made to locate the provider using the given class loader. If a provider supporting the URI scheme is located then its `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap)` is invoked to construct the new file system.

| Parameters ||
|---|---|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!: the URI identifying the file system |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!: a map of provider specific properties to configure the file system; may be empty |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: the class loader to locate the provider or `null` to only attempt to locate an installed provider |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | an I/O error occurs creating the file system |
| `java.lang.IllegalArgumentException` | if the pre-conditions for the `uri` parameter are not met, or the `env` parameter does not contain properties required by the provider, or a property value is invalid |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission required by the file system provider implementation |
| `java.nio.file.FileSystemAlreadyExistsException` | if the URI scheme identifies an installed provider and the file system has already been created |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting the URI scheme is not found |
| `java.util.ServiceConfigurationError` | when an error occurs while loading a service provider |

### newFileSystem

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(path: Path!): FileSystem!
```

Constructs a new `FileSystem` to access the contents of a file as a file system.

This method makes use of specialized providers that create pseudo file systems where the contents of one or more files is treated as a file system.

This method first attempts to locate an installed provider in exactly the same manner as the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap,%20java.lang.ClassLoader)` method. If found, the provider's `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap)` method is invoked with an empty map to construct the new file system.

| Parameters ||
|---|---|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!: the path to the file |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting this file type cannot be located |
| `java.util.ServiceConfigurationError` | when an error occurs while loading a service provider |

### newFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(
    path: Path!, 
    loader: ClassLoader!
): FileSystem!
```

Constructs a new `FileSystem` to access the contents of a file as a file system.

This method makes use of specialized providers that create pseudo file systems where the contents of one or more files is treated as a file system.

This method first attempts to locate an installed provider in exactly the same manner as the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap,%20java.lang.ClassLoader)` method with an empty map. If none of the installed providers return a `FileSystem` then an attempt is made to locate the provider using the given class loader. If a provider returns a file system then the lookup terminates and the file system is returned.

| Parameters ||
|---|---|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!: the path to the file |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: the class loader to locate the provider or `null` to only attempt to locate an installed provider |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting this file type cannot be located |
| `java.util.ServiceConfigurationError` | when an error occurs while loading a service provider |

### newFileSystem

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(
    path: Path!, 
    env: MutableMap<String!, *>!
): FileSystem!
```

Constructs a new `FileSystem` to access the contents of a file as a file system.

This method makes use of specialized providers that create pseudo file systems where the contents of one or more files is treated as a file system.

This method first attempts to locate an installed provider in exactly the same manner as the `https://developer.android.com/reference/kotlin/java/nio/file/FileSystems#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap,%20java.lang.ClassLoader)` method. If found, the provider's `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap)` method is invoked to construct the new file system.

| Parameters ||
|---|---|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!: the path to the file |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!: a map of provider specific properties to configure the file system; may be empty |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting this file type cannot be located |
| `java.util.ServiceConfigurationError` | when an error occurs while loading a service provider |

### newFileSystem

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newFileSystem(
    path: Path!, 
    env: MutableMap<String!, *>!, 
    loader: ClassLoader!
): FileSystem!
```

Constructs a new `FileSystem` to access the contents of a file as a file system.

This method makes use of specialized providers that create pseudo file systems where the contents of one or more files is treated as a file system.

This method iterates over the `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders()` providers. It invokes, in turn, each provider's `https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap)` method. If a provider returns a file system then the iteration terminates and the file system is returned. If none of the installed providers return a `FileSystem` then an attempt is made to locate the provider using the given class loader. If a provider returns a file system, then the lookup terminates and the file system is returned.

| Parameters ||
|---|---|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!: the path to the file |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>!: a map of provider specific properties to configure the file system; may be empty |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: the class loader to locate the provider or `null` to only attempt to locate an installed provider |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem!` | a new file system |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission |
| `java.nio.file.ProviderNotFoundException` | if a provider supporting this file type cannot be located |
| `java.util.ServiceConfigurationError` | when an error occurs while loading a service provider |
