# URLClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLClassLoader

```
open class URLClassLoader : SecureClassLoader, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.lang.ClassLoader](../java/lang/ClassLoader.md) |||
| | ↳ | [java.security.SecureClassLoader](../java/security/SecureClassLoader.md) ||
| | | ↳ | [java.net.URLClassLoader](../java/net/URLClassLoader.md) |
| --- | --- | --- | --- |

This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories. Any URL that ends with a '/' is assumed to refer to a directory. Otherwise, the URL is assumed to refer to a JAR file which will be opened as needed.

The AccessControlContext of the thread that created the instance of URLClassLoader will be used when subsequently loading classes and resources.

The classes that are loaded are by default granted permission only to access the URLs specified when the URLClassLoader was created.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [URLClassLoader](../java/net/URLClassLoader.md))`(`urls:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>!`)` Constructs a new URLClassLoader for the specified URLs using the default delegation parent`ClassLoader`. |
| [URLClassLoader](../java/net/URLClassLoader.md))`(`urls:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>!`, `parent:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` Constructs a new URLClassLoader for the given URLs. |
| [URLClassLoader](../java/net/URLClassLoader.md))`(`urls:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>!`, `parent:` ` [ClassLoader](../java/lang/ClassLoader.md)!`, `factory:` ` [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md)!`)` Constructs a new URLClassLoader for the specified URLs, parent class loader, and URLStreamHandlerFactory. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/net/URLClassLoader.md))`()` Closes this URLClassLoader, so that it can no longer be used to load new classes or resources that are defined by this loader. |
| open [URL](../java/net/URL.md)! | [findResource](../java/net/URLClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds the resource with the specified name on the URL search path. |
| open [Enumeration](../java/util/Enumeration.md)\< [URL](../java/net/URL.md)!\>! | [findResources](../java/net/URLClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an Enumeration of URLs representing all of the resources on the URL search path having the specified name. |
| --- | --- |
| open [InputStream](../java/io/InputStream.md)! | [getResourceAsStream](../java/net/URLClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an input stream for reading the specified resource. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>! | [getURLs](../java/net/URLClassLoader.md))`()` Returns the search path of URLs for loading classes and resources. |
| openstatic [URLClassLoader](../java/net/URLClassLoader.md)! | [newInstance](../java/net/URLClassLoader.md))`(`urls:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>!`)` Creates a new instance of URLClassLoader for the specified URLs and default parent class loader. |
| --- | --- |
| openstatic [URLClassLoader](../java/net/URLClassLoader.md)! | [newInstance](../java/net/URLClassLoader.md))`(`urls:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>!`, `parent:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` Creates a new instance of URLClassLoader for the specified URLs and parent class loader. |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addURL](../java/net/URLClassLoader.md))`(`url:` ` [URL](../java/net/URL.md)!`)` Appends the specified URL to the list of URLs to search for classes and resources. |
| open [Package](../java/lang/Package.md)! | [definePackage](../java/net/URLClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `man:` ` [Manifest](../java/util/jar/Manifest.md)!`, `url:` ` [URL](../java/net/URL.md)!`)` Defines a new package by name in this ClassLoader. |
| open [Class](../java/lang/Class.md)\<\*\>! | [findClass](../java/net/URLClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds and loads the class with the specified name from the URL search path. |
| --- | --- |
| open [PermissionCollection](../java/security/PermissionCollection.md)! | [getPermissions](../java/net/URLClassLoader.md))`(`codesource:` ` [CodeSource](../java/security/CodeSource.md)!`)` Returns the permissions for the given codesource object. |

| Inherited functions ||
|---|---|
| From class [ClassLoader](../java/lang/ClassLoader.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAssertionStatus](../java/lang/ClassLoader.md))`()` <br /> Sets the default assertion status for this class loader to`false`and discards any package defaults or class assertion status settings associated with the class loader. This method is provided so that class loaders can be made to ignore any command line or persistent assertion status settings and "start with a clean slate." Android-note: AssertionStatuses are unsupported. This method is a no-op. <br /> | | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/lang/ClassLoader.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Converts an array of bytes into an instance of class`Class`. Before the`Class`can be used it must be resolved. This method is deprecated in favor of the version that takes a [binary name](../java/lang/ClassLoader.md) as its first argument, and is more secure. <br /> | | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Converts an array of bytes into an instance of class`Class`. Before the`Class`can be used it must be resolved. This method assigns a default [ProtectionDomain](../java/security/ProtectionDomain.md) to the newly defined class. The`ProtectionDomain`is effectively granted the same set of permissions returned when [Policy.getPolicy().getPermissions(new CodeSource(null, null))](../java/security/Policy.md))is invoked. The default protection domain is created on the first invocation of [defineClass](../java/lang/ClassLoader.md)), and re-used on subsequent invocations. To assign a specific`ProtectionDomain`to the class, use the [defineClass](../java/lang/ClassLoader.md))method that takes a`ProtectionDomain`as one of its arguments. This method defines a package in this class loader corresponding to the package of the`Class`(if such a package has not already been defined in this class loader). The name of the defined package is derived from the [binary name](../java/lang/ClassLoader.md) of the class specified by the byte array`b`. Other properties of the defined package are as specified by [Package](../java/lang/Package.md). <br /> | | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `protectionDomain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`)` <br /> Converts an array of bytes into an instance of class`Class`, with a given`ProtectionDomain`. If the given`ProtectionDomain`is`null`, then a default protection domain will be assigned to the class as specified in the documentation for[defineClass(java.lang.String,byte[],int,int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). Before the class can be used it must be resolved. The first class defined in a package determines the exact set of certificates that all subsequent classes defined in that package must contain. The set of certificates for a class is obtained from the [CodeSource](../java/security/CodeSource.md) within the`ProtectionDomain`of the class. Any classes added to that package must contain the same set of certificates or a`SecurityException`will be thrown. Note that if`name`is`null`, this check is not performed. You should always pass in the [binary name](../java/lang/ClassLoader.md) of the class you are defining as well as the bytes. This ensures that the class you are defining is indeed the class you think it is. This method defines a package in this class loader corresponding to the package of the`Class`(if such a package has not already been defined in this class loader). The name of the defined package is derived from the [binary name](../java/lang/ClassLoader.md) of the class specified by the byte array`b`. Other properties of the defined package are as specified by [Package](../java/lang/Package.md). <br /> | | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `protectionDomain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`)` <br /> Converts a [ByteBuffer](../java/nio/ByteBuffer.md) into an instance of class`Class`, with the given`ProtectionDomain`. If the given`ProtectionDomain`is`null`, then a default protection domain will be assigned to the class as specified in the documentation for[defineClass(java.lang.String,byte[],int,int)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). Before the class can be used it must be resolved. The rules about the first class defined in a package determining the set of certificates for the package, the restrictions on class names, and the defined package of the class are identical to those specified in the documentation for[defineClass(java.lang.String,byte[],int,int,java.security.ProtectionDomain)](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#defineClass(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.security.ProtectionDomain)). An invocation of this method of the form*cl* `.defineClass(`*name* `,`*bBuffer* `,`*pd* `)`yields exactly the same result as the statements ` ...` ` byte[] temp = new byte [bBuffer.`[remaining](../java/nio/Buffer.md))`()];` ` bBuffer.` [get](../java/nio/ByteBuffer.md))`(temp);` ` return ` [cl.defineClass](../java/lang/ClassLoader.md))`(name, temp, 0, temp.length, pd);` ` ` <br /> | | [Package](../java/lang/Package.md)! | [definePackage](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specTitle:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specVersion:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `specVendor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implTitle:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implVersion:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `implVendor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sealBase:` ` [URL](../java/net/URL.md)!`)` <br /> Defines a package by [name](../java/lang/ClassLoader.md) in this`ClassLoader`. [Package names](../java/lang/ClassLoader.md) must be unique within a class loader and cannot be redefined or changed once created. If a class loader wishes to define a package with specific properties, such as version information, then the class loader should call this`definePackage`method before calling`defineClass`. Otherwise, the [defineClass](../java/lang/ClassLoader.md))method will define a package in this class loader corresponding to the package of the newly defined class; the properties of this defined package are specified by [Package](../java/lang/Package.md). <br /> | | [Class](../java/lang/Class.md)<*>! | [findClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds the class with the specified [binary name](../java/lang/ClassLoader.md). This method should be overridden by class loader implementations that follow the delegation model for loading classes, and will be invoked by the #loadClass method after checking the parent class loader for the requested class. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findLibrary](../java/lang/ClassLoader.md))`(`libname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the absolute path name of a native library. The VM invokes this method to locate the native libraries that belong to classes loaded with this class loader. If this method returns`null`, the VM searches the library along the path specified as the "`java.library.path`" property. <br /> | | [Class](../java/lang/Class.md)<*>! | [findLoadedClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the class with the given [binary name](../java/lang/ClassLoader.md) if this loader has been recorded by the Java virtual machine as an initiating loader of a class with that [binary name](../java/lang/ClassLoader.md). Otherwise`null`is returned. <br /> | | [URL](../java/net/URL.md)! | [findResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds the resource with the given name. Class loader implementations should override this method. <br /> | | [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | [findResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns an enumeration of [URL](../java/net/URL.md) objects representing all the resources with the given name. Class loader implementations should override this method. <br /> | | [Class](../java/lang/Class.md)<*>! | [findSystemClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds a class with the specified [binary name](../java/lang/ClassLoader.md), loading it if necessary. This method loads the class through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))). The`Class`object returned might have more than one`ClassLoader`associated with it. Subclasses of`ClassLoader`need not usually invoke this method, because most class loaders need to override just [findClass(java.lang.String)](../java/lang/ClassLoader.md)). <br /> | | [Package](../java/lang/Package.md)! | [getPackage](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds a package by [name](../java/lang/ClassLoader.md) in this class loader and its ancestors. If this class loader defines a`Package`of the given name, the`Package`is returned. Otherwise, the ancestors of this class loader are searched recursively (parent by parent) for a`Package`of the given name. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Package](../java/lang/Package.md)!>! | [getPackages](../java/lang/ClassLoader.md))`()` <br /> Returns all of the`Package`s that have been defined by this class loader and its ancestors. The returned array may contain more than one`Package`object of the same package name, each defined by a different class loader in the class loader hierarchy. <br /> | | [ClassLoader](../java/lang/ClassLoader.md)! | [getParent](../java/lang/ClassLoader.md))`()` <br /> Returns the parent class loader for delegation. Some implementations may use`null`to represent the bootstrap class loader. This method will return`null`in such implementations if this class loader's parent is the bootstrap class loader. <br /> | | [URL](../java/net/URL.md)! | [getResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds the resource with the given name. A resource is some data (images, audio, text, etc) that can be accessed by class code in a way that is independent of the location of the code. The name of a resource is a '`/`'-separated path name thatf identifies the resource. <br /> | | [InputStream](../java/io/InputStream.md)! | [getResourceAsStream](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns an input stream for reading the specified resource. The search order is described in the documentation for [getResource(java.lang.String)](../java/lang/ClassLoader.md)). <br /> | | [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | [getResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds all the resources with the given name. A resource is some data (images, audio, text, etc) that can be accessed by class code in a way that is independent of the location of the code. The name of a resource is a`/`-separated path name that identifies the resource. <br /> | | [ClassLoader](../java/lang/ClassLoader.md)! | [getSystemClassLoader](../java/lang/ClassLoader.md))`()` <br /> Returns the system class loader. This is the default delegation parent for new`ClassLoader`instances, and is typically the class loader used to start the application. This method is first invoked early in the runtime's startup sequence, at which point it creates the system class loader. This class loader will be the context class loader for the main application thread (for example, the thread that invokes the`main`method of the main class). The default system class loader is an implementation-dependent instance of this class. <br /> | | [URL](../java/net/URL.md)! | [getSystemResource](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Find a resource of the specified name from the search path used to load classes. This method locates the resource through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))). <br /> | | [InputStream](../java/io/InputStream.md)! | [getSystemResourceAsStream](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Open for reading, a resource of the specified name from the search path used to load classes. This method locates the resource through the system class loader (see [getSystemClassLoader()](../java/lang/ClassLoader.md))). <br /> | | [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | [getSystemResources](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds all resources of the specified name from the search path used to load classes. The resources thus found are returned as an [Enumeration](../java/util/Enumeration.md) of objects. The search order is described in the documentation for [getSystemResource(java.lang.String)](../java/lang/ClassLoader.md)). <br /> | | [Class](../java/lang/Class.md)<*>! | [loadClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Loads the class with the specified [binary name](../java/lang/ClassLoader.md). This method searches for classes in the same manner as the [loadClass(java.lang.String,boolean)](../java/lang/ClassLoader.md))method. It is invoked by the Java virtual machine to resolve class references. Invoking this method is equivalent to invoking [loadClass(name,](../java/lang/ClassLoader.md)). <br /> | | [Class](../java/lang/Class.md)<*>! | [loadClass](../java/lang/ClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resolve:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Loads the class with the specified [binary name](../java/lang/ClassLoader.md). The default implementation of this method searches for classes in the following order: 1. Invoke [findLoadedClass(java.lang.String)](../java/lang/ClassLoader.md))to check if the class has already been loaded. 2. Invoke the [loadClass](../java/lang/ClassLoader.md))method on the parent class loader. If the parent is`null`the class loader built into the virtual machine is used, instead. 3. Invoke the [findClass(java.lang.String)](../java/lang/ClassLoader.md))method to find the class. <br /> If the class was found using the above steps, and the`resolve`flag is true, this method will then invoke the [resolveClass(java.lang.Class)](../java/lang/ClassLoader.md))method on the resulting`Class`object. Subclasses of`ClassLoader`are encouraged to override [findClass(java.lang.String)](../java/lang/ClassLoader.md)), rather than this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerAsParallelCapable](../java/lang/ClassLoader.md))`()` <br /> Registers the caller as`isRegisteredAsParallelCapable() parallel capable`. The registration succeeds if and only if all of the following conditions are met: 1. no instance of the caller has been created 2. all of the super classes (except class Object) of the caller are registered as parallel capable <br /> Note that once a class loader is registered as parallel capable, there is no way to change it back. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resolveClass](../java/lang/ClassLoader.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`)` <br /> Links the specified class. This (misleadingly named) method may be used by a class loader to link a class. If the class`c`has already been linked, then this method simply returns. Otherwise, the class is linked as described in the "Execution" chapter of The Java Language Specification. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClassAssertionStatus](../java/lang/ClassLoader.md))`(`className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the desired assertion status for the named top-level class in this class loader and any nested classes contained therein. This setting takes precedence over the class loader's default assertion status, and over any applicable per-package default. This method has no effect if the named class has already been initialized. (Once a class is initialized, its assertion status cannot change.) If the named class is not a top-level class, this invocation will have no effect on the actual assertion status of any class. Android-note: AssertionStatuses are unsupported. This method is a no-op. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultAssertionStatus](../java/lang/ClassLoader.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the default assertion status for this class loader. This setting determines whether classes loaded by this class loader and initialized in the future will have assertions enabled or disabled by default. This setting may be overridden on a per-package or per-class basis by invoking [setPackageAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md))or [setClassAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md)). Android-note: AssertionStatuses are unsupported. This method is a no-op. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPackageAssertionStatus](../java/lang/ClassLoader.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the package default assertion status for the named package. The package default assertion status determines the assertion status for classes initialized in the future that belong to the named package or any of its "subpackages". A subpackage of a package named p is any package whose name begins with "`p.`". For example,`javax.swing.text`is a subpackage of`javax.swing`, and both`java.util`and`java.lang.reflect`are subpackages of`java`. In the event that multiple package defaults apply to a given class, the package default pertaining to the most specific package takes precedence over the others. For example, if`javax.lang`and`javax.lang.reflect`both have package defaults associated with them, the latter package default applies to classes in`javax.lang.reflect`. Package defaults take precedence over the class loader's default assertion status, and may be overridden on a per-class basis by invoking [setClassAssertionStatus(java.lang.String,boolean)](../java/lang/ClassLoader.md)). Android-note: AssertionStatuses are unsupported. This method is a no-op. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSigners](../java/lang/ClassLoader.md))`(`c:` ` [Class](../java/lang/Class.md)<*>!`, `signers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> Sets the signers of a class. This should be invoked after defining a class. <br /> | ||
| From class [SecureClassLoader](../java/security/SecureClassLoader.md) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/security/SecureClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cs:` ` [CodeSource](../java/security/CodeSource.md)!`)` <br /> Converts an array of bytes into an instance of class Class, with an optional CodeSource. Before the class can be used it must be resolved. If a non-null CodeSource is supplied a ProtectionDomain is constructed and associated with the class being defined. <br /> <br /> | | [Class](../java/lang/Class.md)<*>! | [defineClass](../java/security/SecureClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `cs:` ` [CodeSource](../java/security/CodeSource.md)!`)` <br /> Converts a [ByteBuffer](../java/nio/ByteBuffer.md) into an instance of class`Class`, with an optional CodeSource. Before the class can be used it must be resolved. If a non-null CodeSource is supplied a ProtectionDomain is constructed and associated with the class being defined. <br /> <br /> | ||

## Public constructors

### URLClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URLClassLoader(urls: Array<URL!>!)
```

Constructs a new URLClassLoader for the specified URLs using the default delegation parent`ClassLoader`. The URLs will be searched in the order specified for classes and resources after first searching in the parent class loader. Any URL that ends with a '/' is assumed to refer to a directory. Otherwise, the URL is assumed to refer to a JAR file which will be downloaded and opened as needed.

If there is a security manager, this method first calls the security manager's`checkCreateClassLoader`method to ensure creation of a class loader is allowed.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urls` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>!:the URLs from which to load classes and resources |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkCreateClassLoader`method doesn't allow creation of a class loader. |
| `java.lang.NullPointerException` | if`urls`is`null`. |

**See Also**

- [java.lang.SecurityManager#checkCreateClassLoader](../java/lang/SecurityManager.md)) 

### URLClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URLClassLoader(
    urls: Array<URL!>!, 
    parent: ClassLoader!)
```

Constructs a new URLClassLoader for the given URLs. The URLs will be searched in the order specified for classes and resources after first searching in the specified parent class loader. Any URL that ends with a '/' is assumed to refer to a directory. Otherwise, the URL is assumed to refer to a JAR file which will be downloaded and opened as needed.

If there is a security manager, this method first calls the security manager's`checkCreateClassLoader`method to ensure creation of a class loader is allowed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urls` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>!:the URLs from which to load classes and resources |
| `parent` | [ClassLoader](../java/lang/ClassLoader.md)!:the parent class loader for delegation |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkCreateClassLoader`method doesn't allow creation of a class loader. |
| `java.lang.NullPointerException` | if`urls`is`null`. |

**See Also**

- [java.lang.SecurityManager#checkCreateClassLoader](../java/lang/SecurityManager.md)) 

### URLClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URLClassLoader(
    urls: Array<URL!>!, 
    parent: ClassLoader!, 
    factory: URLStreamHandlerFactory!)
```

Constructs a new URLClassLoader for the specified URLs, parent class loader, and URLStreamHandlerFactory. The parent argument will be used as the parent class loader for delegation. The factory argument will be used as the stream handler factory to obtain protocol handlers when creating new jar URLs.

If there is a security manager, this method first calls the security manager's`checkCreateClassLoader`method to ensure creation of a class loader is allowed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urls` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>!:the URLs from which to load classes and resources |
| `parent` | [ClassLoader](../java/lang/ClassLoader.md)!:the parent class loader for delegation |
| `factory` | [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md)!:the URLStreamHandlerFactory to use when creating URLs |
| --- | --- |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkCreateClassLoader`method doesn't allow creation of a class loader. |
| `java.lang.NullPointerException` | if`urls`is`null`. |

**See Also**

- [java.lang.SecurityManager#checkCreateClassLoader](../java/lang/SecurityManager.md))

## Public methods

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this URLClassLoader, so that it can no longer be used to load new classes or resources that are defined by this loader. Classes and resources defined by any of this loader's parents in the delegation hierarchy are still accessible. Also, any classes or resources that are already loaded, are still accessible.

In the case of jar: and file: URLs, it also closes any files that were opened by it. If another thread is loading a class when the`close`method is invoked, then the result of that load is undefined.

The method makes a best effort attempt to close all opened files, by catching [IOException](../java/io/IOException.md) s internally. Unchecked exceptions and errors are not caught. Calling close on an already closed loader has no effect.

<br />

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.io.IOException` | if closing any file opened by this class loader resulted in an IOException. Any such exceptions are caught internally. If only one is caught, then it is re-thrown. If more than one exception is caught, then the second and following exceptions are added as suppressed exceptions of the first one caught, which is then re-thrown. |
| --- | --- |
| `java.lang.SecurityException` | if a security manager is set, and it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("closeClassLoader")` |

### findResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findResource(name: String!): URL!
```

Finds the resource with the specified name on the URL search path.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the resource |

| Return ||
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [URL](../java/net/URL.md)! | a`URL`for the resource, or`null`if the resource could not be found, or if the loader is closed. |

### findResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findResources(name: String!): Enumeration<URL!>!
```

Returns an Enumeration of URLs representing all of the resources on the URL search path having the specified name.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the resource name |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [URL](../java/net/URL.md)!>! | an`Enumeration`of`URL`s If the loader is closed, the Enumeration will be empty. |

| Exceptions ||
|-----------------------|----------------------------|
| `java.io.IOException` | If I/O errors occur |
| `java.io.IOException` | if an I/O exception occurs |

### getResourceAsStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceAsStream(name: String!): InputStream!
```

Returns an input stream for reading the specified resource. If this loader is closed, then any resources opened by this method will be closed.

The search order is described in the documentation for [getResource(java.lang.String)](../java/lang/ClassLoader.md)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [InputStream](../java/io/InputStream.md)! | An input stream for reading the resource, or`null`if the resource could not be found |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If`name`is`null` |

### getURLs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getURLs(): Array<URL!>!
```

Returns the search path of URLs for loading classes and resources. This includes the original list of URLs specified to the constructor, along with any URLs subsequently appended by the addURL() method.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [URL](../java/net/URL.md)!>! | the search path of URLs for loading classes and resources. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(urls: Array<URL!>!): URLClassLoader!
```

Creates a new instance of URLClassLoader for the specified URLs and default parent class loader. If a security manager is installed, the`loadClass`method of the URLClassLoader returned by this method will invoke the`SecurityManager.checkPackageAccess`before loading the class.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urls` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>!:the URLs to search for classes and resources |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [URLClassLoader](../java/net/URLClassLoader.md)! | the resulting class loader |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`urls`is`null`. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    urls: Array<URL!>!, 
    parent: ClassLoader!
): URLClassLoader!
```

Creates a new instance of URLClassLoader for the specified URLs and parent class loader. If a security manager is installed, the`loadClass`method of the URLClassLoader returned by this method will invoke the`SecurityManager.checkPackageAccess`method before loading the class.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `urls` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [URL](../java/net/URL.md)!\>!:the URLs to search for classes and resources |
| `parent` | [ClassLoader](../java/lang/ClassLoader.md)!:the parent class loader for delegation |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [URLClassLoader](../java/net/URLClassLoader.md)! | the resulting class loader |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`urls`is`null`. |

## Protected methods

### addURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun addURL(url: URL!): Unit
```

Appends the specified URL to the list of URLs to search for classes and resources.

If the URL specified is`null`or is already in the list of URLs, or if this loader is closed, then invoking this method has no effect.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `url` | [URL](../java/net/URL.md)!:the URL to be added to the search path of URLs |

### definePackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun definePackage(
    name: String!, 
    man: Manifest!, 
    url: URL!
): Package!
```

Defines a new package by name in this ClassLoader. The attributes contained in the specified Manifest will be used to obtain package version and sealing information. For sealed packages, the additional URL specifies the code source URL from which the package was loaded.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the package name |
| `man` | [Manifest](../java/util/jar/Manifest.md)!:the Manifest containing package version and sealing information |
| `url` | [URL](../java/net/URL.md)!:the code source url for the package, or null if none |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Package](../java/lang/Package.md)! | the newly defined Package object |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the package name duplicates an existing package either in this class loader or one of its ancestors |

### findClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findClass(name: String!): Class<*>!
```

Finds and loads the class with the specified name from the URL search path. Any URLs referring to JAR files are loaded and opened as needed until the class is found.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the class |

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [Class](../java/lang/Class.md)<*>! | the resulting class |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------|
| `java.lang.ClassNotFoundException` | If the class could not be found |
| `java.lang.ClassNotFoundException` | if the class could not be found, or if the loader is closed. |
| `java.lang.NullPointerException` | if`name`is`null`. |
| --- | --- |

### getPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPermissions(codesource: CodeSource!): PermissionCollection!
```

Returns the permissions for the given codesource object. The implementation of this method first calls super.getPermissions and then adds permissions based on the URL of the codesource.

If the protocol of this URL is "jar", then the permission granted is based on the permission that is required by the URL of the Jar file.

If the protocol is "file" and there is an authority component, then permission to connect to and accept connections from that authority may be granted. If the protocol is "file" and the path specifies a file, then permission to read that file is granted. If protocol is "file" and the path is a directory, permission is granted to read all files and (recursively) all files and subdirectories contained in that directory.

If the protocol is not "file", then permission to connect to and accept connections from the URL's host is granted.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------|
| `codesource` | [CodeSource](../java/security/CodeSource.md)!:the codesource |

| Return ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [PermissionCollection](../java/security/PermissionCollection.md)! | the permissions granted to the codesource |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`codesource`is`null`. |
