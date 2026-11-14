# DelegateLastClassLoader

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DelegateLastClassLoader

```
class DelegateLastClassLoader : PathClassLoader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.lang.ClassLoader](../java.lang/ClassLoader.md) ||||
| | ↳ | [dalvik.system.BaseDexClassLoader](BaseDexClassLoader.md) |||
| | | ↳ | [dalvik.system.PathClassLoader](PathClassLoader.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [dalvik.system.DelegateLastClassLoader](DelegateLastClassLoader.md) |

A`ClassLoader`implementation that implements a**delegate last**lookup policy. For every class or resource this loader is requested to load, the following lookup order is employed:

- The boot classpath is always searched first
- Then, the list of`dex`files associated with this classloaders's`dexPath`is searched.
- Finally, this classloader will delegate to the specified`parent`.

<br />

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DelegateLastClassLoader](DelegateLastClassLoader.md))`(`dexPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parent:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Equivalent to calling [DelegateLastClassLoader(java.lang.String,java.lang.String,java.lang.ClassLoader,boolean)](DelegateLastClassLoader.md))with`librarySearchPath = null, delegateResourceLoading = true`. |
| [DelegateLastClassLoader](DelegateLastClassLoader.md))`(`dexPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `librarySearchPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parent:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Equivalent to calling [DelegateLastClassLoader(java.lang.String,java.lang.String,java.lang.ClassLoader,boolean)](DelegateLastClassLoader.md))with`delegateResourceLoading = true`. |
| [DelegateLastClassLoader](DelegateLastClassLoader.md))`(`dexPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `librarySearchPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `parent:` ` [ClassLoader](../java.lang/ClassLoader.md)?`, `delegateResourceLoading:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a`DelegateLastClassLoader`that operates on a given`dexPath`and a`librarySearchPath`. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URL](../java.net/URL.md)! | [getResource](DelegateLastClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [Enumeration](../java.util/Enumeration.md)\< [URL](../java.net/URL.md)!\>! | [getResources](DelegateLastClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Class](../java.lang/Class.md)\<\*\>! | [loadClass](DelegateLastClassLoader.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resolve:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

## Public constructors

### DelegateLastClassLoader

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DelegateLastClassLoader(
    dexPath: String!, 
    parent: ClassLoader!)
```

Equivalent to calling [DelegateLastClassLoader(java.lang.String,java.lang.String,java.lang.ClassLoader,boolean)](DelegateLastClassLoader.md))with`librarySearchPath = null, delegateResourceLoading = true`. 

### DelegateLastClassLoader

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DelegateLastClassLoader(
    dexPath: String!, 
    librarySearchPath: String!, 
    parent: ClassLoader!)
```

Equivalent to calling [DelegateLastClassLoader(java.lang.String,java.lang.String,java.lang.ClassLoader,boolean)](DelegateLastClassLoader.md))with`delegateResourceLoading = true`. 

### DelegateLastClassLoader

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DelegateLastClassLoader(
    dexPath: String, 
    librarySearchPath: String?, 
    parent: ClassLoader?, 
    delegateResourceLoading: Boolean)
```

Creates a`DelegateLastClassLoader`that operates on a given`dexPath`and a`librarySearchPath`. The`dexPath`should consist of one or more of the following, separated by`File.pathSeparator`, which is`":"`on Android.

- JAR/ZIP/APK files, possibly containing a "classes.dex" file as well as arbitrary resources.
- Raw ".dex" files (not inside a zip file).

Unlike [PathClassLoader](PathClassLoader.md), this classloader will attempt to locate classes (or resources) using the following lookup order.

- The boot classpath is always searched first.
- Then, the list of`dex`files contained in`dexPath`is searched./li\>
- Lastly, this classloader will delegate to the specified`parent`.

Note that this is in contrast to other standard classloaders that follow the delegation model. In those classloaders, the`parent`is always searched first.`librarySearchPath`specifies one more directories containing native library files, separated by`File.pathSeparator`.

<br />

| Parameters ||
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dexPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the list of jar/apk files containing classes and resources, delimited by`File.pathSeparator`, which defaults to`":"`on Android. This value cannot be`null`. |
| `librarySearchPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the list of directories containing native libraries, delimited by`File.pathSeparator`; may be`null`. |
| `parent` | [ClassLoader](../java.lang/ClassLoader.md)?:the parent class loader. May be`null`for the boot classloader. |
| --- | --- |
| `delegateResourceLoading` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to delegate resource loading to the parent if the resource is not found. This does not affect class loading delegation. |

## Public methods

### getResource

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResource(name: String!): URL!
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URL](../java.net/URL.md)! | `URL`object for reading the resource;`null`if the resource could not be found, a`URL`could not be constructed to locate the resource, the resource is in a package that is not opened unconditionally, or access to the resource is denied by the security manager. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If`name`is`null` |

### getResources

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResources(name: String!): Enumeration<URL!>!
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource name |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Enumeration](../java.util/Enumeration.md)< [URL](../java.net/URL.md)!>! | An enumeration of [URL](../java.net/URL.md) objects for the resource. If no resources could be found, the enumeration will be empty. Resources for which a`URL`cannot be constructed, are in a package that is not opened unconditionally, or access to the resource is denied by the security manager, are not returned in the enumeration. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.io.IOException` | If I/O errors occur |
| `java.lang.NullPointerException` | If`name`is`null` |

## Protected methods

### loadClass

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun loadClass(
    name: String!, 
    resolve: Boolean
): Class<*>!
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The [binary name](DelegateLastClassLoader.md) of the class |
| `resolve` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then resolve the class |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [Class](../java.lang/Class.md)<*>! | The resulting`Class`object |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.lang.ClassNotFoundException` | If the class could not be found |
