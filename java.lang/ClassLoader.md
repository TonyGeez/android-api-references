# ClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassLoader

```
abstract class ClassLoader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ClassLoader](../java/lang/ClassLoader.md) |

| Known Direct Subclasses [BaseDexClassLoader](../dalvik/system/BaseDexClassLoader.md), [SecureClassLoader](../java/security/SecureClassLoader.md) |-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BaseDexClassLoader](../dalvik/system/BaseDexClassLoader.md) | Base class for common functionality between various dex-based [ClassLoader](../java/lang/ClassLoader.md) implementations. | | [SecureClassLoader](../java/security/SecureClassLoader.md) | This class extends ClassLoader with additional support for defining classes with an associated code source and permissions which are retrieved by the system policy by default. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DelegateLastClassLoader](../dalvik/system/DelegateLastClassLoader.md), [DexClassLoader](../dalvik/system/DexClassLoader.md), [InMemoryDexClassLoader](../dalvik/system/InMemoryDexClassLoader.md), [PathClassLoader](../dalvik/system/PathClassLoader.md), [URLClassLoader](../java/net/URLClassLoader.md) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DelegateLastClassLoader](../dalvik/system/DelegateLastClassLoader.md) | A`ClassLoader`implementation that implements a**delegate last**lookup policy. | | [DexClassLoader](../dalvik/system/DexClassLoader.md) | A class loader that loads classes from`.jar`and`.apk`files containing a`classes.dex`entry. | | [InMemoryDexClassLoader](../dalvik/system/InMemoryDexClassLoader.md) | A [ClassLoader](../java/lang/ClassLoader.md) implementation that loads classes from a buffer containing a DEX file. | | [PathClassLoader](../dalvik/system/PathClassLoader.md) | Provides a simple [ClassLoader](../java/lang/ClassLoader.md) implementation that operates on a list of files and directories in the local file system, but does not attempt to load classes from the network. | | [URLClassLoader](../java/net/URLClassLoader.md) | This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A class loader is an object that is responsible for loading classes. The class`ClassLoader`is an abstract class. Given the [binary name](../java/lang/ClassLoader.md) of a class, a class loader should attempt to locate or generate data that constitutes a definition for the class. A typical strategy is to transform the name into a file name and then read a "class file" of that name from a file system.

Every [Class](../java/lang/Class.md) object contains a [reference](../java/lang/Class.md))to the`ClassLoader`that defined it.

`Class`objects for array classes are not created by class loaders, but are created automatically as required by the Java runtime. The class loader for an array class, as returned by [java.lang.Class#getClassLoader()](../java/lang/Class.md))is the same as the class loader for its element type; if the element type is a primitive type, then the array class has no class loader.

Applications implement subclasses of`ClassLoader`in order to extend the manner in which the Java virtual machine dynamically loads classes.

Class loaders may typically be used by security managers to indicate security domains.

In addition to loading classes, a class loader is also responsible for locating resources. A resource is some data (a "`.class`" file, configuration data, or an image for example) that is identified with an abstract '/'-separated path name. Resources are typically packaged with an application or library so that they can be located by code in the application or library. In some cases, the resources are included so that they can be located by other libraries.

The`ClassLoader`class uses a delegation model to search for classes and resources. Each instance of`ClassLoader`has an associated parent class loader. When requested to find a class or resource, a`ClassLoader`instance will usually delegate the search for the class or resource to its parent class loader before attempting to find the class or resource itself.

Class loaders that support concurrent loading of classes are known as*`isRegisteredAsParallelCapable() parallel capable`* class loaders and are required to register themselves at their class initialization time by invoking the`registerAsParallelCapable ClassLoader.registerAsParallelCapable`method. Note that the`ClassLoader`class is registered as parallel capable by default. However, its subclasses still need to register themselves if they are parallel capable. In environments in which the delegation model is not strictly hierarchical, class loaders need to be parallel capable, otherwise class loading can lead to deadlocks because the loader lock is held for the duration of the class loading process (see #loadClass methods).

## Run-time Built-in Class Loaders

The Java run-time has the following built-in class loaders:

- Bootstrap class loader. It is the virtual machine's built-in class loader, typically represented as`null`, and does not have a parent.
- [System class loader](../java/lang/ClassLoader.md)). It is also known as*application class loader*and is distinct from the platform class loader. The system class loader is typically used to define classes on the application class path, module path, and JDK-specific tools. The platform class loader is the parent or an ancestor of the system class loader, so the system class loader can load platform classes by delegating to its parent.

Normally, the Java virtual machine loads classes from the local file system in a platform-dependent manner. However, some classes may not originate from a file; they may originate from other sources, such as the network, or they could be constructed by an application. The method [defineClass](../java/lang/ClassLoader.md))converts an array of bytes into an instance of class`Class`. Instances of this newly defined class can be created using [Class.newInstance](../java/lang/Class.md)).

The methods and constructors of objects created by a class loader may reference other classes. To determine the class(es) referred to, the Java virtual machine invokes the #loadClass method of the class loader that originally created the class.

For example, an application could create a network class loader to download class files from a server. Sample code might look like: 

```kotlin
ClassLoader loader = new NetworkClassLoader(host, port);
    Object main = loader.loadClass("Main", true).newInstance();
         . . .
  
```

The network class loader subclass must define the methods [findClass](../java/lang/ClassLoader.md))and`loadClassData`to load a class from the network. Once it has downloaded the bytes that make up the class, it should use the method #defineClass to create a class instance. A sample implementation is: 

```kotlin
class NetworkClassLoader extends ClassLoader {
          String host;
          int port;
 
          public Class findClass(String name) {
              byte[] b = loadClassData(name);
              return defineClass(name, b, 0, b.length);
          }
 
          private byte[] loadClassData(String name) {
              // load the class data from the connection
               . . .
          }
      }
  
```

### Binary names

Any class name provided as a`String`parameter to methods in`ClassLoader`must be a binary name as defined by The Java Language Specification.

Examples of valid class names include: 

```kotlin
"java.lang.String"
    "javax.swing.JSpinner$DefaultEditor"
    "java.security.KeyStore$Builder$FileBuilder$1"
    "java.net.URLClassLoader$3$1"
  
```

Any package name provided as a`String`parameter to methods in`ClassLoader`must be either the empty string (denoting an unnamed package) or a fully qualified name as defined by The Java Language Specification.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassLoader](../java/lang/ClassLoader.md))`()` Creates a new class loader using the`ClassLoader`returned by the method [getSystemClassLoader()](../java/lang/ClassLoader.md))as the parent class loader. |
| [ClassLoader](../java/lang/ClassLoader.md))`(`parent:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` Creates a new class loader using the specified parent class loader for delegation. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAssertionStatus](../java/lang/ClassLoader.md))`()` Sets the default assertion status for this class loader to`false`and discards any package defaults or class assertion status settings associated with the class loader. |
| [ClassLoader](../java/lang/ClassLoader.md)! | [getParent](../java/lang/ClassLoader.md))`()` Returns the parent class loader for delegation. |
| open [URL](../java/net/URL.md)! | [getResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds the resource with the given name. |
| --- | --- |
| open [InputStream](../java/io/InputStream.md)! | [getResourceAsStream](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an input stream for reading the specified resource. |
| open [Enumeration](../java/util/Enumeration.md)\< [URL](../java/net/URL.md)!\>! | [getResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds all the resources with the given name. |
| openstatic [ClassLoader](../java/lang/ClassLoader.md)! | [getSystemClassLoader](../java/lang/ClassLoader.md))`()` Returns the system class loader. |
| --- | --- |
| openstatic [URL](../java/net/URL.md)! | [getSystemResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Find a resource of the specified name from the search path used to load classes. |
| openstatic [InputStream](../java/io/InputStream.md)! | [getSystemResourceAsStream](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Open for reading, a resource of the specified name from the search path used to load classes. |
| openstatic [Enumeration](../java/util/Enumeration.md)\< [URL](../java/net/URL.md)!\>! | [getSystemResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds all resources of the specified name from the search path used to load classes. |
| --- | --- |
| open [Class](../java/lang/Class.md)\<\*\>! | [loadClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Loads the class with the specified [binary name](../java/lang/ClassLoader.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClassAssertionStatus](../java/lang/ClassLoader.md))`(`className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the desired assertion status for the named top-level class in this class loader and any nested classes contained therein. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultAssertionStatus](../java/lang/ClassLoader.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the default assertion status for this class loader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPackageAssertionStatus](../java/lang/ClassLoader.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the package default assertion status for the named package. |

| Protected methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Class](../java/lang/Class.md)\<\*\>! | [defineClass](../java/lang/ClassLoader.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts an array of bytes into an instance of class`Class`. |
| [Class](../java/lang/Class.md)\<\*\>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts an array of bytes into an instance of class`Class`. |
| [Class](../java/lang/Class.md)\<\*\>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `protectionDomain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`)` Converts an array of bytes into an instance of class`Class`, with a given`ProtectionDomain`. |
| --- | --- |
| [Class](../java/lang/Class.md)\<\*\>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `protectionDomain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`)` Converts a [ByteBuffer](../java/nio/ByteBuffer.md) into an instance of class`Class`, with the given`ProtectionDomain`. |
| open [Package](../java/lang/Package.md)! | [definePackage](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specTitle:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specVersion:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specVendor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implTitle:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implVersion:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implVendor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sealBase:` ` [URL](../java/net/URL.md)!`)` Defines a package by [name](../java/lang/ClassLoader.md) in this`ClassLoader`. |
| open [Class](../java/lang/Class.md)\<\*\>! | [findClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds the class with the specified [binary name](../java/lang/ClassLoader.md). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findLibrary](../java/lang/ClassLoader.md))`(`libname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the absolute path name of a native library. |
| [Class](../java/lang/Class.md)\<\*\>! | [findLoadedClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the class with the given [binary name](../java/lang/ClassLoader.md) if this loader has been recorded by the Java virtual machine as an initiating loader of a class with that [binary name](../java/lang/ClassLoader.md). |
| open [URL](../java/net/URL.md)! | [findResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds the resource with the given name. |
| --- | --- |
| open [Enumeration](../java/util/Enumeration.md)\< [URL](../java/net/URL.md)!\>! | [findResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an enumeration of [URL](../java/net/URL.md) objects representing all the resources with the given name. |
| [Class](../java/lang/Class.md)\<\*\>! | [findSystemClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds a class with the specified [binary name](../java/lang/ClassLoader.md), loading it if necessary. |
| open [Package](../java/lang/Package.md)! | [getPackage](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds a package by [name](../java/lang/ClassLoader.md) in this class loader and its ancestors. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Package](../java/lang/Package.md)!\>! | [getPackages](../java/lang/ClassLoader.md))`()` Returns all of the`Package`s that have been defined by this class loader and its ancestors. |
| open [Class](../java/lang/Class.md)\<\*\>! | [loadClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resolve:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Loads the class with the specified [binary name](../java/lang/ClassLoader.md). |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerAsParallelCapable](../java/lang/ClassLoader.md))`()` Registers the caller as`isRegisteredAsParallelCapable() parallel capable`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resolveClass](../java/lang/ClassLoader.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`)` Links the specified class. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSigners](../java/lang/ClassLoader.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`, `signers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Sets the signers of a class. |

## Protected constructors

### ClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ClassLoader()
```

Creates a new class loader using the`ClassLoader`returned by the method [getSystemClassLoader()](../java/lang/ClassLoader.md))as the parent class loader.

If there is a security manager, its [checkCreateClassLoader](../java/lang/SecurityManager.md))method is invoked. This may result in a security exception.

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its`checkCreateClassLoader`method doesn't allow creation of a new class loader. |

### ClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ClassLoader(parent: ClassLoader!)
```

Creates a new class loader using the specified parent class loader for delegation.

If there is a security manager, its [checkCreateClassLoader](../java/lang/SecurityManager.md))method is invoked. This may result in a security exception.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `parent` | [ClassLoader](../java/lang/ClassLoader.md)!:The parent class loader |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its`checkCreateClassLoader`method doesn't allow creation of a new class loader. |

## Public methods

### clearAssertionStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearAssertionStatus(): Unit
```

Sets the default assertion status for this class loader to`false`and discards any package defaults or class assertion status settings associated with the class loader. This method is provided so that class loaders can be made to ignore any command line or persistent assertion status settings and "start with a clean slate." Android-note: AssertionStatuses are unsupported. This method is a no-op. 

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(): ClassLoader!
```

Returns the parent class loader for delegation. Some implementations may use`null`to represent the bootstrap class loader. This method will return`null`in such implementations if this class loader's parent is the bootstrap class loader.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------|
| [ClassLoader](../java/lang/ClassLoader.md)! | The parent`ClassLoader` |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager is present, and the caller's class loader is not`null`and is not an ancestor of this class loader, and the caller does not have the [RuntimePermission](../java/lang/RuntimePermission.md)`("getClassLoader")` |

### getResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResource(name: String!): URL!
```

Finds the resource with the given name. A resource is some data (images, audio, text, etc) that can be accessed by class code in a way that is independent of the location of the code.

The name of a resource is a '`/`'-separated path name thatf identifies the resource.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URL](../java/net/URL.md)! | `URL`object for reading the resource;`null`if the resource could not be found, a`URL`could not be constructed to locate the resource, the resource is in a package that is not opened unconditionally, or access to the resource is denied by the security manager. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If`name`is`null` |

### getResourceAsStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceAsStream(name: String!): InputStream!
```

Returns an input stream for reading the specified resource.

The search order is described in the documentation for [getResource(java.lang.String)](../java/lang/ClassLoader.md)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InputStream](../java/io/InputStream.md)! | An input stream for reading the resource;`null`if the resource could not be found, the resource is in a package that is not opened unconditionally, or access to the resource is denied by the security manager. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If`name`is`null` |

### getResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResources(name: String!): Enumeration<URL!>!
```

Finds all the resources with the given name. A resource is some data (images, audio, text, etc) that can be accessed by class code in a way that is independent of the location of the code.

The name of a resource is a`/`-separated path name that identifies the resource.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | An enumeration of [URL](../java/net/URL.md) objects for the resource. If no resources could be found, the enumeration will be empty. Resources for which a`URL`cannot be constructed, are in a package that is not opened unconditionally, or access to the resource is denied by the security manager, are not returned in the enumeration. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.io.IOException` | If I/O errors occur |
| `java.lang.NullPointerException` | If`name`is`null` |

### getSystemClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemClassLoader(): ClassLoader!
```

Returns the system class loader. This is the default delegation parent for new`ClassLoader`instances, and is typically the class loader used to start the application.

This method is first invoked early in the runtime's startup sequence, at which point it creates the system class loader. This class loader will be the context class loader for the main application thread (for example, the thread that invokes the`main`method of the main class).

The default system class loader is an implementation-dependent instance of this class.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------|
| [ClassLoader](../java/lang/ClassLoader.md)! | The system`ClassLoader` |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager is present, and the caller's class loader is not`null`and is not the same as or an ancestor of the system class loader, and the caller does not have the [RuntimePermission](../java/lang/RuntimePermission.md)`("getClassLoader")` |
| `java.lang.IllegalStateException` | If invoked recursively during the construction of the class loader specified by the "`java.system.class.loader`" property. |
| `java.lang.Error` | If the system property "`java.system.class.loader`" is defined but the named class could not be loaded, the provider class does not define the required constructor, or an exception is thrown by that constructor when it is invoked. The underlying cause of the error can be retrieved via the [Throwable.getCause()](../java/lang/Throwable.md))method. |
| --- | --- |

### getSystemResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemResource(name: String!): URL!
```

Find a resource of the specified name from the search path used to load classes. This method locates the resource through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URL](../java/net/URL.md)! | A [URL](../java/net/URL.md) to the resource;`null`if the resource could not be found, a URL could not be constructed to locate the resource, the resource is in a package that is not opened unconditionally or access to the resource is denied by the security manager. |

### getSystemResourceAsStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemResourceAsStream(name: String!): InputStream!
```

Open for reading, a resource of the specified name from the search path used to load classes. This method locates the resource through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InputStream](../java/io/InputStream.md)! | An input stream for reading the resource;`null`if the resource could not be found, the resource is in a package that is not opened unconditionally, or access to the resource is denied by the security manager. |

### getSystemResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemResources(name: String!): Enumeration<URL!>!
```

Finds all resources of the specified name from the search path used to load classes. The resources thus found are returned as an [Enumeration](../java/util/Enumeration.md) of objects.

The search order is described in the documentation for [getSystemResource(java.lang.String)](../java/lang/ClassLoader.md)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | An enumeration of [URL](../java/net/URL.md) objects for the resource. If no resources could be found, the enumeration will be empty. Resources for which a`URL`cannot be constructed, are in a package that is not opened unconditionally, or access to the resource is denied by the security manager, are not returned in the enumeration. |

| Exceptions ||
|-----------------------|---------------------|
| `java.io.IOException` | If I/O errors occur |

### loadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadClass(name: String!): Class<*>!
```

Loads the class with the specified [binary name](../java/lang/ClassLoader.md). This method searches for classes in the same manner as the [loadClass(java.lang.String,boolean)](../java/lang/ClassLoader.md))method. It is invoked by the Java virtual machine to resolve class references. Invoking this method is equivalent to invoking [loadClass(name,](../java/lang/ClassLoader.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](../java/lang/ClassLoader.md) of the class |

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Class](../java/lang/Class.md)<*>! | The resulting`Class`object |

| Exceptions ||
|------------------------------------|----------------------------|
| `java.lang.ClassNotFoundException` | If the class was not found |

### setClassAssertionStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClassAssertionStatus(
    className: String!, 
    enabled: Boolean
): Unit
```

Sets the desired assertion status for the named top-level class in this class loader and any nested classes contained therein. This setting takes precedence over the class loader's default assertion status, and over any applicable per-package default. This method has no effect if the named class has already been initialized. (Once a class is initialized, its assertion status cannot change.)

If the named class is not a top-level class, this invocation will have no effect on the actual assertion status of any class.
Android-note: AssertionStatuses are unsupported. This method is a no-op.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The fully qualified class name of the top-level class whose assertion status is to be set. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the named class is to have assertions enabled when (and if) it is initialized,`false`if the class is to have assertions disabled. |

### setDefaultAssertionStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDefaultAssertionStatus(enabled: Boolean): Unit
```

Sets the default assertion status for this class loader. This setting determines whether classes loaded by this class loader and initialized in the future will have assertions enabled or disabled by default. This setting may be overridden on a per-package or per-class basis by invoking [setPackageAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md))or [setClassAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md)). Android-note: AssertionStatuses are unsupported. This method is a no-op.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if classes loaded by this class loader will henceforth have assertions enabled by default,`false`if they will have assertions disabled by default. |

### setPackageAssertionStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPackageAssertionStatus(
    packageName: String!, 
    enabled: Boolean
): Unit
```

Sets the package default assertion status for the named package. The package default assertion status determines the assertion status for classes initialized in the future that belong to the named package or any of its "subpackages".

A subpackage of a package named p is any package whose name begins with "`p.`". For example,`javax.swing.text`is a subpackage of`javax.swing`, and both`java.util`and`java.lang.reflect`are subpackages of`java`.

In the event that multiple package defaults apply to a given class, the package default pertaining to the most specific package takes precedence over the others. For example, if`javax.lang`and`javax.lang.reflect`both have package defaults associated with them, the latter package default applies to classes in`javax.lang.reflect`.

Package defaults take precedence over the class loader's default assertion status, and may be overridden on a per-class basis by invoking [setClassAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md)).
Android-note: AssertionStatuses are unsupported. This method is a no-op.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the package whose package default assertion status is to be set. A`null`value indicates the unnamed package that is "current" (see section {@jls 7.4.2} of The Java Language Specification.) |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if classes loaded by this classloader and belonging to the named package or any of its subpackages will have assertions enabled by default,`false`if they will have assertions disabled by default. |

## Protected methods

### defineClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun defineClass(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Class<*>!
```

**Deprecated:** *Replaced by[defineClass(String, byte[], int, int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))*

Converts an array of bytes into an instance of class`Class`. Before the`Class`can be used it must be resolved. This method is deprecated in favor of the version that takes a [binary name](../java/lang/ClassLoader.md) as its first argument, and is more secure.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The bytes that make up the class data. The bytes in positions`off`through`off+len-1`should have the format of a valid class file as defined by The Java Virtual Machine Specification. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start offset in`b`of the class data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the class data |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object that was created from the specified class data |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassFormatError` | If the data did not contain a valid class |
| `java.lang.IndexOutOfBoundsException` | If either`off`or`len`is negative, or if`off+len`is greater than`b.length`. |
| `java.lang.SecurityException` | If an attempt is made to add this class to a package that contains classes that were signed by a different set of certificates than this class, or if an attempt is made to define a class in a package with a fully-qualified name that starts with "`java.`". |
| --- | --- |

**See Also**

- [#loadClass(String, boolean)](../java/lang/ClassLoader.md))
- [#resolveClass(Class)](../java/lang/ClassLoader.md)) 

### defineClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun defineClass(
    name: String!, 
    b: ByteArray!, 
    off: Int, 
    len: Int
): Class<*>!
```

Converts an array of bytes into an instance of class`Class`. Before the`Class`can be used it must be resolved.

This method assigns a default [ProtectionDomain](../java/security/ProtectionDomain.md) to the newly defined class. The`ProtectionDomain`is effectively granted the same set of permissions returned when [Policy.getPolicy().getPermissions(new CodeSource(null, null))](../java/security/Policy.md))is invoked. The default protection domain is created on the first invocation of [defineClass](../java/lang/ClassLoader.md)), and re-used on subsequent invocations.

To assign a specific`ProtectionDomain`to the class, use the [defineClass](../java/lang/ClassLoader.md))method that takes a`ProtectionDomain`as one of its arguments.

This method defines a package in this class loader corresponding to the package of the`Class`(if such a package has not already been defined in this class loader). The name of the defined package is derived from the [binary name](../java/lang/ClassLoader.md) of the class specified by the byte array`b`. Other properties of the defined package are as specified by [Package](../java/lang/Package.md).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The expected [binary name](../java/lang/ClassLoader.md) of the class, or`null`if not known |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The bytes that make up the class data. The bytes in positions`off`through`off+len-1`should have the format of a valid class file as defined by The Java Virtual Machine Specification. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start offset in`b`of the class data |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the class data |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object that was created from the specified class data. |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassFormatError` | If the data did not contain a valid class |
| `java.lang.IndexOutOfBoundsException` | If either`off`or`len`is negative, or if`off+len`is greater than`b.length`. |
| `java.lang.SecurityException` | If an attempt is made to add this class to a package that contains classes that were signed by a different set of certificates than this class (which is unsigned), or if`name`begins with "`java.`". |
| --- | --- |

**See Also**

- [#loadClass(String, boolean)](../java/lang/ClassLoader.md))
- [#resolveClass(Class)](../java/lang/ClassLoader.md))
- [java.security.CodeSource](../java/security/CodeSource.md)
- [java.security.SecureClassLoader](../java/security/SecureClassLoader.md) 

### defineClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun defineClass(
    name: String!, 
    b: ByteArray!, 
    off: Int, 
    len: Int, 
    protectionDomain: ProtectionDomain!
): Class<*>!
```

Converts an array of bytes into an instance of class`Class`, with a given`ProtectionDomain`.

If the given`ProtectionDomain`is`null`, then a default protection domain will be assigned to the class as specified in the documentation for[defineClass(java.lang.String,byte[],int,int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). Before the class can be used it must be resolved.

The first class defined in a package determines the exact set of certificates that all subsequent classes defined in that package must contain. The set of certificates for a class is obtained from the [CodeSource](../java/security/CodeSource.md) within the`ProtectionDomain`of the class. Any classes added to that package must contain the same set of certificates or a`SecurityException`will be thrown. Note that if`name`is`null`, this check is not performed. You should always pass in the [binary name](../java/lang/ClassLoader.md) of the class you are defining as well as the bytes. This ensures that the class you are defining is indeed the class you think it is.

This method defines a package in this class loader corresponding to the package of the`Class`(if such a package has not already been defined in this class loader). The name of the defined package is derived from the [binary name](../java/lang/ClassLoader.md) of the class specified by the byte array`b`. Other properties of the defined package are as specified by [Package](../java/lang/Package.md).

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The expected [binary name](../java/lang/ClassLoader.md) of the class, or`null`if not known |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The bytes that make up the class data. The bytes in positions`off`through`off+len-1`should have the format of a valid class file as defined by The Java Virtual Machine Specification. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start offset in`b`of the class data |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the class data |
| `protectionDomain` | [ProtectionDomain](../java/security/ProtectionDomain.md)!:The`ProtectionDomain`of the class |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object created from the data, and`ProtectionDomain`. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassFormatError` | If the data did not contain a valid class |
| `java.lang.NoClassDefFoundError` | If`name`is not`null`and not equal to the [binary name](../java/lang/ClassLoader.md) of the class specified by`b` |
| `java.lang.IndexOutOfBoundsException` | If either`off`or`len`is negative, or if`off+len`is greater than`b.length`. |
| --- | --- |
| `java.lang.SecurityException` | If an attempt is made to add this class to a package that contains classes that were signed by a different set of certificates than this class, or if`name`begins with "`java.`" and this class loader is not the platform class loader or its ancestor. |

### defineClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun defineClass(
    name: String!, 
    b: ByteBuffer!, 
    protectionDomain: ProtectionDomain!
): Class<*>!
```

Converts a [ByteBuffer](../java/nio/ByteBuffer.md) into an instance of class`Class`, with the given`ProtectionDomain`. If the given`ProtectionDomain`is`null`, then a default protection domain will be assigned to the class as specified in the documentation for[defineClass(java.lang.String,byte[],int,int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). Before the class can be used it must be resolved.

The rules about the first class defined in a package determining the set of certificates for the package, the restrictions on class names, and the defined package of the class are identical to those specified in the documentation for[defineClass(java.lang.String,byte[],int,int,java.security.ProtectionDomain)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.security.ProtectionDomain)).

An invocation of this method of the form*cl* `.defineClass(`*name* `,`*bBuffer* `,`*pd* `)`yields exactly the same result as the statements

` ...` 
` byte[] temp = new byte [bBuffer.`[remaining](../java/nio/Buffer.md))`()];` 
` bBuffer.` [get](../java/nio/ByteBuffer.md))`(temp);` 
` return ` [cl.defineClass](../java/lang/ClassLoader.md))`(name, temp, 0, temp.length, pd);` 
` `

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The expected [binary name](../java/lang/ClassLoader.md). of the class, or`null`if not known |
| `b` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The bytes that make up the class data. The bytes from positions`b.position()`through`b.position() + b.limit() -1 `should have the format of a valid class file as defined by The Java Virtual Machine Specification. |
| `protectionDomain` | [ProtectionDomain](../java/security/ProtectionDomain.md)!:The`ProtectionDomain`of the class, or`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object created from the data, and`ProtectionDomain`. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassFormatError` | If the data did not contain a valid class. |
| `java.lang.NoClassDefFoundError` | If`name`is not`null`and not equal to the [binary name](../java/lang/ClassLoader.md) of the class specified by`b` |
| `java.lang.SecurityException` | If an attempt is made to add this class to a package that contains classes that were signed by a different set of certificates than this class, or if`name`begins with "`java.`". |
| --- | --- |

**See Also**

- [#defineClass(String, byte[], int, int, ProtectionDomain)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.security.ProtectionDomain)) 

### definePackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun definePackage(
    name: String!, 
    specTitle: String!, 
    specVersion: String!, 
    specVendor: String!, 
    implTitle: String!, 
    implVersion: String!, 
    implVendor: String!, 
    sealBase: URL!
): Package!
```

Defines a package by [name](../java/lang/ClassLoader.md) in this`ClassLoader`.

[Package names](../java/lang/ClassLoader.md) must be unique within a class loader and cannot be redefined or changed once created.

If a class loader wishes to define a package with specific properties, such as version information, then the class loader should call this`definePackage`method before calling`defineClass`. Otherwise, the [defineClass](../java/lang/ClassLoader.md))method will define a package in this class loader corresponding to the package of the newly defined class; the properties of this defined package are specified by [Package](../java/lang/Package.md).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [package name](../java/lang/ClassLoader.md) |
| `specTitle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The specification title |
| `specVersion` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The specification version |
| --- | --- |
| `specVendor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The specification vendor |
| `implTitle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The implementation title |
| `implVersion` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The implementation version |
| --- | --- |
| `implVendor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The implementation vendor |
| `sealBase` | [URL](../java/net/URL.md)!:If not`null`, then this package is sealed with respect to the given code source [URL](../java/net/URL.md) object. Otherwise, the package is not sealed. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Package](../java/lang/Package.md)! | The newly defined`Package`object |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`name`is`null`. |
| `java.lang.IllegalArgumentException` | if a package of the given`name`is already defined by this class loader |

**See Also**

### findClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findClass(name: String!): Class<*>!
```

Finds the class with the specified [binary name](../java/lang/ClassLoader.md). This method should be overridden by class loader implementations that follow the delegation model for loading classes, and will be invoked by the #loadClass method after checking the parent class loader for the requested class.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](../java/lang/ClassLoader.md) of the class |

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Class](../java/lang/Class.md)<*>! | The resulting`Class`object |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.lang.ClassNotFoundException` | If the class could not be found |

### findLibrary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findLibrary(libname: String!): String!
```

Returns the absolute path name of a native library. The VM invokes this method to locate the native libraries that belong to classes loaded with this class loader. If this method returns`null`, the VM searches the library along the path specified as the "`java.library.path`" property.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------|
| `libname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The library name |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The absolute path of the native library |

**See Also**

- [java.lang.System#loadLibrary(String)](../java/lang/System.md))
- [java.lang.System#mapLibraryName(String)](../java/lang/System.md)) 

### findLoadedClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun findLoadedClass(name: String!): Class<*>!
```

Returns the class with the given [binary name](../java/lang/ClassLoader.md) if this loader has been recorded by the Java virtual machine as an initiating loader of a class with that [binary name](../java/lang/ClassLoader.md). Otherwise`null`is returned.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](../java/lang/ClassLoader.md) of the class |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object, or`null`if the class has not been loaded |

### findResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findResource(name: String!): URL!
```

Finds the resource with the given name. Class loader implementations should override this method.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URL](../java/net/URL.md)! | `URL`object for reading the resource;`null`if the resource could not be found, a`URL`could not be constructed to locate the resource, the resource is in a package that is not opened unconditionally, or access to the resource is denied by the security manager. |

### findResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findResources(name: String!): Enumeration<URL!>!
```

Returns an enumeration of [URL](../java/net/URL.md) objects representing all the resources with the given name. Class loader implementations should override this method.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | An enumeration of [URL](../java/net/URL.md) objects for the resource. If no resources could be found, the enumeration will be empty. Resources for which a`URL`cannot be constructed, are in a package that is not opened unconditionally, or access to the resource is denied by the security manager, are not returned in the enumeration. |

| Exceptions ||
|-----------------------|---------------------|
| `java.io.IOException` | If I/O errors occur |

### findSystemClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun findSystemClass(name: String!): Class<*>!
```

Finds a class with the specified [binary name](../java/lang/ClassLoader.md), loading it if necessary.

This method loads the class through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))). The`Class`object returned might have more than one`ClassLoader`associated with it. Subclasses of`ClassLoader`need not usually invoke this method, because most class loaders need to override just [findClass(java.lang.String)](../java/lang/ClassLoader.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](../java/lang/ClassLoader.md) of the class |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | The`Class`object for the specified`name` |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.lang.ClassNotFoundException` | If the class could not be found |

**See Also**

- [#ClassLoader(ClassLoader)](../java/lang/ClassLoader.md))
- <https://developer.android.com/reference/kotlin/java/lang/ClassLoader#getParent()> 

### getPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPackage(name: String!): Package!
```

**Deprecated:** *If multiple class loaders delegate to each other and define classes with the same package name, and one such loader relies on the lookup behavior of`getPackage`to return a`Package`from a parent loader, then the properties exposed by the`Package`may not be as expected in the rest of the program. For example, the`Package`will only expose annotations from the`package-info.class`file defined by the parent loader, even if annotations exist in a`package-info.class`file defined by a child loader.*

Finds a package by [name](../java/lang/ClassLoader.md) in this class loader and its ancestors.

If this class loader defines a`Package`of the given name, the`Package`is returned. Otherwise, the ancestors of this class loader are searched recursively (parent by parent) for a`Package`of the given name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [package name](../java/lang/ClassLoader.md) |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Package](../java/lang/Package.md)! | The`Package`of the given name that has been defined by this class loader or its ancestors, or`null`if not found. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`name`is`null`. |

### getPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPackages(): Array<Package!>!
```

Returns all of the`Package`s that have been defined by this class loader and its ancestors. The returned array may contain more than one`Package`object of the same package name, each defined by a different class loader in the class loader hierarchy.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Package](../java/lang/Package.md)!>! | The array of`Package`objects that have been defined by this class loader and its ancestors |

### loadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun loadClass(
    name: String!, 
    resolve: Boolean
): Class<*>!
```

Loads the class with the specified [binary name](../java/lang/ClassLoader.md). The default implementation of this method searches for classes in the following order:

1. Invoke [findLoadedClass(java.lang.String)](../java/lang/ClassLoader.md))to check if the class has already been loaded.
2. Invoke the [loadClass](../java/lang/ClassLoader.md))method on the parent class loader. If the parent is`null`the class loader built into the virtual machine is used, instead.
3. Invoke the [findClass(java.lang.String)](../java/lang/ClassLoader.md))method to find the class.

<br />

If the class was found using the above steps, and the`resolve`flag is true, this method will then invoke the [resolveClass(java.lang.Class)](../java/lang/ClassLoader.md))method on the resulting`Class`object.

Subclasses of`ClassLoader`are encouraged to override [findClass(java.lang.String)](../java/lang/ClassLoader.md)), rather than this method.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](../java/lang/ClassLoader.md) of the class |
| `resolve` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then resolve the class |

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Class](../java/lang/Class.md)<*>! | The resulting`Class`object |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.lang.ClassNotFoundException` | If the class could not be found |

### registerAsParallelCapable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open static fun registerAsParallelCapable(): Boolean
```

Registers the caller as`isRegisteredAsParallelCapable() parallel capable`. The registration succeeds if and only if all of the following conditions are met:

1. no instance of the caller has been created
2. all of the super classes (except class Object) of the caller are registered as parallel capable

<br />

Note that once a class loader is registered as parallel capable, there is no way to change it back.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the caller is successfully registered as parallel capable and`false`if otherwise. |

### resolveClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun resolveClass(c: Class<*>!): Unit
```

Links the specified class. This (misleadingly named) method may be used by a class loader to link a class. If the class`c`has already been linked, then this method simply returns. Otherwise, the class is linked as described in the "Execution" chapter of The Java Language Specification.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `c` | [Class](../java/lang/Class.md)\<\*\>!:The class to link |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | If`c`is`null`. |

**See Also**

- [#defineClass(String, byte[], int, int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### setSigners

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun setSigners(
    c: Class<*>!, 
    signers: Array<Any!>!
): Unit
```

Sets the signers of a class. This should be invoked after defining a class.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Class](../java/lang/Class.md)\<\*\>!:The`Class`object |
| `signers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The signers for the class |
