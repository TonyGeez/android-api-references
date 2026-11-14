Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# System

```
class System
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.System](System.md) |

The `System` class contains several useful class fields and methods. It cannot be instantiated.

Among the facilities provided by the `System` class are standard input, standard output, and error output streams; access to externally defined properties and environment variables; a means of loading files and libraries; and a utility method for quickly copying a portion of an array.

## Summary

| Public methods ||
|---|---|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#arraycopy(kotlin.Any,%20kotlin.Int,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int)(src: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, srcPos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dest: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, destPos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copies an array from the specified source array, beginning at the specified position, to the specified position of the destination array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/System#clearProperty(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Removes the system property indicated by the specified key. |
| static [Console](../java.io/Console.md)? | `https://developer.android.com/reference/kotlin/java/lang/System#console()()` Returns the unique `https://developer.android.com/reference/kotlin/java/io/Console.html#` object associated with the current Java virtual machine, if any. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#currentTimeMillis()()` Returns the current time in milliseconds. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#exit(kotlin.Int)(status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Terminates the currently running Java Virtual Machine. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#gc()()` Runs the garbage collector. |
| --- | --- |
| static [Properties](../java.util/Properties.md) | `https://developer.android.com/reference/kotlin/java/lang/System#getProperties()()` Determines the current system properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the system property indicated by the specified key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, def: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Gets the system property indicated by the specified key. |
| --- | --- |
| static [SecurityManager](SecurityManager.md)? | `https://developer.android.com/reference/kotlin/java/lang/System#getSecurityManager()()` Always returns `null` in Android |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/System#getenv()()` Returns an unmodifiable string map view of the current system environment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/System#getenv(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the value of the specified environment variable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#identityHashCode(kotlin.Any)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns the same hash code for the given object as would be returned by the default method hashCode(), whether or not the given object's class overrides hashCode(). |
| static [Channel](../java.nio.channels/Channel.md)? | `https://developer.android.com/reference/kotlin/java/lang/System#inheritedChannel()()` Returns the channel inherited from the entity that created this Java virtual machine. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#lineSeparator()()` Returns the system-dependent line separator string. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#load(kotlin.String)(filename: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Loads the native library specified by the filename argument. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#loadLibrary(kotlin.String)(libname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Loads the native library specified by the `libname` argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#mapLibraryName(kotlin.String)(libname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Maps a library name into a platform-specific string representing a native library. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#nanoTime()()` Returns the current value of the running Java Virtual Machine's high-resolution time source, in nanoseconds. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#runFinalization()()` Runs the finalization methods of any objects pending finalization. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#runFinalizersOnExit(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable finalization on exit; doing so specifies that the finalizers of all objects that have finalizers that have not yet been automatically invoked are to be run before the Java runtime exits. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#setErr(java.io.PrintStream)(err: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#?)` Reassigns the "standard" error output stream. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#setIn(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?)` Reassigns the "standard" input stream. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#setOut(java.io.PrintStream)(out: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#?)` Reassigns the "standard" output stream. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#setProperties(java.util.Properties)(props: https://developer.android.com/reference/kotlin/java/util/Properties.html#?)` Attempts to set all system properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/System#setProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Sets the system property indicated by the specified key. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/System#setSecurityManager(java.lang.SecurityManager)(s: https://developer.android.com/reference/kotlin/java/lang/SecurityManager?)` Throws `SecurityException` (except in case `sm == null`). |
| --- | --- |

| Properties ||
|---|---|
| static [PrintStream](../java.io/PrintStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/System#err:java.io.PrintStream` The "standard" error output stream. |
| static [InputStream](../java.io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/System#in:java.io.InputStream` The "standard" input stream. |
| static [PrintStream](../java.io/PrintStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/System#out:java.io.PrintStream` The "standard" output stream. |
| --- | --- |

## Public methods

### arraycopy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun arraycopy(
    src: Any, 
    srcPos: Int, 
    dest: Any, 
    destPos: Int, 
    length: Int
): Unit
```

Copies an array from the specified source array, beginning at the specified position, to the specified position of the destination array. A subsequence of array components are copied from the source array referenced by `src` to the destination array referenced by `dest`. The number of components copied is equal to the `length` argument. The components at positions `srcPos` through `srcPos+length-1` in the source array are copied into positions `destPos` through `destPos+length-1`, respectively, of the destination array.

If the `src` and `dest` arguments refer to the same array object, then the copying is performed as if the components at positions `srcPos` through `srcPos+length-1` were first copied to a temporary array with `length` components and then the contents of the temporary array were copied into positions `destPos` through `destPos+length-1` of the destination array.

If `dest` is `null`, then a `NullPointerException` is thrown.

If `src` is `null`, then a `NullPointerException` is thrown and the destination array is not modified.

Otherwise, if any of the following is true, an `ArrayStoreException` is thrown and the destination is not modified:

- The `src` argument refers to an object that is not an array.
- The `dest` argument refers to an object that is not an array.
- The `src` argument and `dest` argument refer to arrays whose component types are different primitive types.
- The `src` argument refers to an array with a primitive component type and the `dest` argument refers to an array with a reference component type.
- The `src` argument refers to an array with a reference component type and the `dest` argument refers to an array with a primitive component type.

Otherwise, if any of the following is true, an `IndexOutOfBoundsException` is thrown and the destination is not modified:

- The `srcPos` argument is negative.
- The `destPos` argument is negative.
- The `length` argument is negative.
- `srcPos+length` is greater than `src.length`, the length of the source array.
- `destPos+length` is greater than `dest.length`, the length of the destination array.

Otherwise, if any actual component of the source array from position `srcPos` through `srcPos+length-1` cannot be converted to the component type of the destination array by assignment conversion, an `ArrayStoreException` is thrown. In this case, let ***k*** be the smallest nonnegative integer less than length such that `src[srcPos+`*k* `]` cannot be converted to the component type of the destination array; when the exception is thrown, source array components from positions `srcPos` through `srcPos+`*k* `-1` will already have been copied to destination array positions `destPos` through `destPos+`*k* `-1` and no other positions of the destination array will have been modified. (Because of the restrictions already itemized, this paragraph effectively applies only to the situation where both arrays have component types that are reference types.)

| Parameters ||
|---|---|
| `src` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the source array. |
| `srcPos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): starting position in the source array. |
| `dest` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the destination array. |
| --- | --- |
| `destPos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): starting position in the destination data. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of array elements to be copied. |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if an element in the `src` array could not be stored into the `dest` array because of a type mismatch. |
| `java.lang.IndexOutOfBoundsException` | if copying would cause access of data outside array bounds. |
| `java.lang.NullPointerException` | if either `src` or `dest` is `null`. |
| --- | --- |

### clearProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clearProperty(key: String): String?
```

Removes the system property indicated by the specified key.

First, if a security manager exists, its `SecurityManager.checkPermission` method is called with a `PropertyPermission(key, "write")` permission. This may result in a SecurityException being thrown. If no exception is thrown, the specified property is removed.

<br />

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the system property to be removed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the previous string value of the system property, or `null` if there was no property with that key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `key` is empty. |
| `java.lang.NullPointerException` | if `key` is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its `checkPropertyAccess` method doesn't allow access to the specified system property. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#setProperty(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/util/Properties.html#`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertiesAccess()`

### console

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun console(): Console?
```

Returns the unique `https://developer.android.com/reference/kotlin/java/io/Console.html#` object associated with the current Java virtual machine, if any.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Console.html#?` | The system console, if any, otherwise null. |

### currentTimeMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun currentTimeMillis(): Long
```

Returns the current time in milliseconds. Note that while the unit of time of the return value is a millisecond, the granularity of the value depends on the underlying operating system and may be larger. For example, many operating systems measure time in units of tens of milliseconds.

See the description of the class `Date` for a discussion of slight discrepancies that may arise between "computer time" and coordinated universal time (UTC).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the difference, measured in milliseconds, between the current time and midnight, January 1, 1970 UTC. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Date.html#`

### exit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun exit(status: Int): Unit
```

Terminates the currently running Java Virtual Machine. The argument serves as a status code; by convention, a nonzero status code indicates abnormal termination.

This method calls the `exit` method in class `Runtime`. This method never returns normally.

The call `System.exit(n)` is effectively equivalent to the call:

```kotlin
Runtime.getRuntime().exit(n)
  
```

| Parameters ||
|---|---|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): exit status. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkExit` method doesn't allow exit with the specified status. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#exit(kotlin.Int)`

### gc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun gc(): Unit
```

Runs the garbage collector.

Calling the `gc` method suggests that the Java Virtual Machine expend effort toward recycling unused objects in order to make the memory they currently occupy available for quick reuse. When control returns from the method call, the Java Virtual Machine has made a best effort to reclaim space from all discarded objects.

The call `System.gc()` is effectively equivalent to the call:

```kotlin
Runtime.getRuntime().gc()
  
```
At API level 34 and lower, this does nothing unless it is preceded or followed by a runFinalization call. Runtime.getRuntime().gc() always attempts to reclaim space.

Calling this indiscriminately is likely to severely degrade performance. Intended primarily for testing.
**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#gc()`

### getProperties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getProperties(): Properties
```

Determines the current system properties.

The following properties are always provided by the Dalvik VM:

<br />

| **Name** | **Meaning** | **Example** |
| --- | --- | --- |
| file.separator | `https://developer.android.com/reference/kotlin/java/io/File.html#separator:kotlin.String` | `/` |
| java.class.path | System class path | `.` |
| java.class.version | (Not useful on Android) | `50.0` |
| --- | --- | --- |
| java.compiler | (Not useful on Android) | Empty |
| java.ext.dirs | (Not useful on Android) | Empty |
| java.home | Location of the VM on the file system | `/apex/com.android.art/` |
| --- | --- | --- |
| java.io.tmpdir | Location of a temporary directory. The location varies by application. See java.io.File#createTempFile | `/data/user/0/com.android.app/cache` |
| java.library.path | Search path for JNI libraries | `/system/lib:/system_ext/lib` |
| java.vendor | Human-readable VM vendor | `The Android Project` |
| --- | --- | --- |
| java.vendor.url | URL for VM vendor's web site | `http://www.android.com/` |
| java.version | (Not useful on Android) | `0` |
| java.specification.version | VM libraries version | `0.9` |
| --- | --- | --- |
| java.specification.vendor | VM libraries vendor | `The Android Project` |
| java.specification.name | VM libraries name | `Dalvik Core Library` |
| java.vm.version | VM implementation version | `1.2.0` |
| --- | --- | --- |
| java.vm.vendor | VM implementation vendor | `The Android Project` |
| java.vm.name | VM implementation name | `Dalvik` |
| java.vm.specification.version | VM specification version | `0.9` |
| --- | --- | --- |
| java.vm.specification.vendor | VM specification vendor | `The Android Project` |
| java.vm.specification.name | VM specification name | `Dalvik Virtual Machine Specification` |
| line.separator | The system line separator | `\n` |
| --- | --- | --- |
| os.arch | OS architecture | `aarch64` |
| os.name | OS (kernel) name | `Linux` |
| os.version | OS (kernel) version | `5.10.98-g6ea688a79989` |
| --- | --- | --- |
| path.separator | See `https://developer.android.com/reference/kotlin/java/io/File.html#pathSeparator:kotlin.String` | `:` |
| user.dir | Base of non-absolute paths | `/` |
| user.home | (Not useful on Android) | Empty |
| --- | --- | --- |
| user.name | (Not useful on Android) | Empty |

Multiple paths in a system property value are separated by the path separator character of the platform.

Note that even if the security manager does not permit the `getProperties` operation, it may choose to permit the `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String)` operation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Properties.html#` | the system properties |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPropertiesAccess` method doesn't allow access to the system properties. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#setProperties(java.util.Properties)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertiesAccess()`
- `https://developer.android.com/reference/kotlin/java/util/Properties.html#`

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getProperty(key: String): String?
```

Gets the system property indicated by the specified key.

First, if there is a security manager, its `checkPropertyAccess` method is called with the key as its argument. This may result in a SecurityException.

If there is no current set of system properties, a set of system properties is first created and initialized in the same manner as for the `getProperties` method.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the system property. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the string value of the system property, or `null` if there is no property with that key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `key` is empty. |
| `java.lang.NullPointerException` | if `key` is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its `checkPropertyAccess` method doesn't allow access to the specified system property. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#setProperty(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertyAccess(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/System#getProperties()`

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getProperty(
    key: String, 
    def: String?
): String?
```

Gets the system property indicated by the specified key.

First, if there is a security manager, its `checkPropertyAccess` method is called with the `key` as its argument.

If there is no current set of system properties, a set of system properties is first created and initialized in the same manner as for the `getProperties` method.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the system property. |
| `def` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the string value of the system property, or the default value if there is no property with that key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `key` is empty. |
| `java.lang.NullPointerException` | if `key` is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its `checkPropertyAccess` method doesn't allow access to the specified system property. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#setProperty(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkPropertyAccess(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/System#getProperties()`

### getSecurityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSecurityManager(): SecurityManager?
```

Always returns `null` in Android

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/SecurityManager?` | `null` in Android |

### getenv

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getenv(): MutableMap<String!, String!>
```

Returns an unmodifiable string map view of the current system environment. The environment is a system-dependent mapping from names to values which is passed from parent to child processes.

If the system does not support environment variables, an empty map is returned.

The returned map will never contain null keys or values. Attempting to query the presence of a null key or value will throw a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException`. Attempting to query the presence of a key or value which is not of type `https://developer.android.com/reference/kotlin/java/lang/String` will throw a `https://developer.android.com/reference/kotlin/java/lang/ClassCastException`.

The returned map and its collection views may not obey the general contract of the `https://developer.android.com/reference/kotlin/java/lang/Object#equals(kotlin.Any)` and `https://developer.android.com/reference/kotlin/java/lang/Object#hashCode()` methods.

The returned map is typically case-sensitive on all platforms.

If a security manager exists, its java.lang.SecurityManager#checkPermission method is called with a `` `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`("getenv.*") `` permission. This may result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException` being thrown.

When passing information to a Java subprocess, [system properties](System.md) are generally preferred over environment variables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | the environment as a map of variable names to values |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkPermission method doesn't allow access to the process environment |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#getenv(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#environment()`

### getenv

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getenv(name: String): String?
```

Gets the value of the specified environment variable. An environment variable is a system-dependent external named value.

If a security manager exists, its java.lang.SecurityManager#checkPermission method is called with a `` `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`("getenv."+name) `` permission. This may result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException` being thrown. If no exception is thrown the value of the variable `name` is returned.

*System properties* and *environment variables* are both conceptually mappings between names and values. Both mechanisms can be used to pass user-defined information to a Java process. Environment variables have a more global effect, because they are visible to all descendants of the process which defines them, not just the immediate Java subprocess. They can have subtly different semantics, such as case insensitivity, on different operating systems. For these reasons, environment variables are more likely to have unintended side effects. It is best to use system properties where possible. Environment variables should be used when a global effect is desired, or when an external system interface requires an environment variable (such as `PATH`).

On UNIX systems the alphabetic case of `name` is typically significant, while on Microsoft Windows systems it is typically not. For example, the expression `System.getenv("FOO").equals(System.getenv("foo"))` is likely to be true on Microsoft Windows.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the environment variable |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the string value of the variable, or `null` if the variable is not defined in the system environment |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `name` is `null` |
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkPermission method doesn't allow access to the environment variable `name` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#getenv()`
- `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#environment()`

### identityHashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun identityHashCode(x: Any?): Int
```

Returns the same hash code for the given object as would be returned by the default method hashCode(), whether or not the given object's class overrides hashCode(). The hash code for the null reference is zero.

| Parameters ||
|---|---|
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: object for which the hashCode is to be calculated |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hashCode |

### inheritedChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun inheritedChannel(): Channel?
```

Returns the channel inherited from the entity that created this Java virtual machine.

This method returns the channel obtained by invoking the `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider.html#inheritedChannel()` method of the system-wide default `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider.html#` object.

In addition to the network-oriented channels described in `https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider.html#inheritedChannel()`, this method may return other kinds of channels in the future.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/Channel.html#?` | The inherited channel, if any, otherwise null. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is present and it does not permit access to the channel. |

### lineSeparator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lineSeparator(): String
```

Returns the system-dependent line separator string. It always returns the same value - the initial value of the [system property](System.md)) `line.separator`.

On UNIX systems, it returns `"\n"`; on Microsoft Windows systems it returns `"\r\n"`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the system-dependent line separator string |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun load(filename: String): Unit
```

Loads the native library specified by the filename argument. The filename argument must be an absolute path name. If the filename argument, when stripped of any platform-specific library prefix, path, and file extension, indicates a library whose name is, for example, L, and a native library called L is statically linked with the VM, then the JNI_OnLoad_L function exported by the library is invoked rather than attempting to load a dynamic library. A filename matching the argument does not have to exist in the file system. See the JNI Specification for more details. Otherwise, the filename argument is mapped to a native library image in an implementation-dependent manner.

The call `System.load(name)` is effectively equivalent to the call:

```kotlin
Runtime.getRuntime().load(name)
  
```

| Parameters ||
|---|---|
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the file to load. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `filename` is `null` |
| `java.lang.SecurityException` | if a security manager exists and its `checkLink` method doesn't allow loading of the specified dynamic library |
| `java.lang.UnsatisfiedLinkError` | if either the filename is not an absolute path name, the native library is not statically linked with the VM, or the library cannot be mapped to a native library image by the host system. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#load(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkLink(kotlin.String)`

### loadLibrary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun loadLibrary(libname: String): Unit
```

Loads the native library specified by the `libname` argument. The `libname` argument must not contain any platform specific prefix, file extension or path. If a native library called `libname` is statically linked with the VM, then the JNI_OnLoad_`libname` function exported by the library is invoked. See the JNI Specification for more details. Otherwise, the libname argument is loaded from a system library location and mapped to a native library image in an implementation- dependent manner.

The call `System.loadLibrary(name)` is effectively equivalent to the call

```kotlin
Runtime.getRuntime().loadLibrary(name)
  
```

| Parameters ||
|---|---|
| `libname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the library. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `libname` is `null` |
| `java.lang.SecurityException` | if a security manager exists and its `checkLink` method doesn't allow loading of the specified dynamic library |
| `java.lang.UnsatisfiedLinkError` | if either the libname argument contains a file path, the native library is not statically linked with the VM, or the library cannot be mapped to a native library image by the host system. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#loadLibrary(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkLink(kotlin.String)`

### mapLibraryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mapLibraryName(libname: String): String
```

Maps a library name into a platform-specific string representing a native library.

| Parameters ||
|---|---|
| `libname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the library. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a platform-dependent native library name. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `libname` is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#loadLibrary(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/ClassLoader#findLibrary(kotlin.String)`

### nanoTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nanoTime(): Long
```

Returns the current value of the running Java Virtual Machine's high-resolution time source, in nanoseconds.

This method can only be used to measure elapsed time and is not related to any other notion of system or wall-clock time. The value returned represents nanoseconds since some fixed but arbitrary *origin* time (perhaps in the future, so values may be negative). The same origin is used by all invocations of this method in an instance of a Java virtual machine; other virtual machine instances are likely to use a different origin.

This method provides nanosecond precision, but not necessarily nanosecond resolution (that is, how frequently the value changes) - no guarantees are made except that the resolution is at least as good as that of `https://developer.android.com/reference/kotlin/java/lang/System#currentTimeMillis()`.

Differences in successive calls that span greater than approximately 292 years (263 nanoseconds) will not correctly compute elapsed time due to numerical overflow.

The values returned by this method become meaningful only when the difference between two such values, obtained within the same instance of a Java virtual machine, is computed.

For example, to measure how long some code takes to execute:

```kotlin
<code>long startTime = System.nanoTime();
  // ... the code being measured ...
  long estimatedTime = System.nanoTime() - startTime;</code>
```

To compare two nanoTime values

```kotlin
<code>long t0 = System.nanoTime();
  ...
  long t1 = System.nanoTime();</code>
```
one should use `t1 - t0 < 0`, not `t1 < t0`, because of the possibility of numerical overflow.

The value returned by this method does not account for elapsed time during deep sleep. For timekeeping facilities available on Android see `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current value of the running Java Virtual Machine's high-resolution time source, in nanoseconds |

### runFinalization

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun runFinalization(): Unit
```

Runs the finalization methods of any objects pending finalization.

Calling this method suggests that the Java Virtual Machine expend effort toward running the `finalize` methods of objects that have been found to be discarded but whose `finalize` methods have not yet been run. When control returns from the method call, the Java Virtual Machine has made a best effort to complete all outstanding finalizations.

The call `System.runFinalization()` is effectively equivalent to the call:

```kotlin
Runtime.getRuntime().runFinalization()
  
```
**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#runFinalization()`

### runFinalizersOnExit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun runFinalizersOnExit(value: Boolean): Unit
```

**Deprecated:** *This method is inherently unsafe. It may result in finalizers being called on live objects while other threads are concurrently manipulating those objects, resulting in erratic behavior or deadlock.*

Enable or disable finalization on exit; doing so specifies that the finalizers of all objects that have finalizers that have not yet been automatically invoked are to be run before the Java runtime exits. By default, finalization on exit is disabled.

If there is a security manager, its `checkExit` method is first called with 0 as its argument to ensure the exit is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicating enabling or disabling of finalization |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkExit` method doesn't allow the exit. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Runtime#exit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Runtime#gc()`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkExit(kotlin.Int)`

### setErr

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setErr(err: PrintStream?): Unit
```

Reassigns the "standard" error output stream.

First, if there is a security manager, its `checkPermission` method is called with a `RuntimePermission("setIO")` permission to see if it's ok to reassign the "standard" error output stream.

| Parameters ||
|---|---|
| `err` | [PrintStream](../java.io/PrintStream.md)?: the new standard error output stream. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow reassigning of the standard error output stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`

### setIn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setIn(in: InputStream?): Unit
```

Reassigns the "standard" input stream.

First, if there is a security manager, its `checkPermission` method is called with a `RuntimePermission("setIO")` permission to see if it's ok to reassign the "standard" input stream.

<br />

| Parameters ||
|---|---|
| `in` | [InputStream](../java.io/InputStream.md)?: the new standard input stream. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow reassigning of the standard input stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`

### setOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setOut(out: PrintStream?): Unit
```

Reassigns the "standard" output stream.

First, if there is a security manager, its `checkPermission` method is called with a `RuntimePermission("setIO")` permission to see if it's ok to reassign the "standard" output stream.

| Parameters ||
|---|---|
| `out` | [PrintStream](../java.io/PrintStream.md)?: the new standard output stream |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow reassigning of the standard output stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission`

### setProperties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setProperties(props: Properties?): Unit
```

Attempts to set all system properties. Copies all properties from `p` and discards system properties that are read only and cannot be modified. See #getProperty for a list of such properties.

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setProperty(
    key: String, 
    value: String?
): String?
```

Sets the system property indicated by the specified key.

First, if a security manager exists, its `SecurityManager.checkPermission` method is called with a `PropertyPermission(key, "write")` permission. This may result in a SecurityException being thrown. If no exception is thrown, the specified property is set to the given value.

<br />

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the system property. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the value of the system property. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the previous value of the system property, or `null` if it did not have one. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `key` is empty. |
| `java.lang.NullPointerException` | if `key` or `value` is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow setting of the specified property. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#`

### setSecurityManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setSecurityManager(s: SecurityManager?): Unit
```

Throws `SecurityException` (except in case `sm == null`).

Security managers do *not* provide a secure environment for executing untrusted code and are unsupported on Android. Untrusted code cannot be safely isolated within a single VM on Android, so this method *always* throws a `SecurityException` when passed a non-null SecurityManager

| Parameters ||
|---|---|
| `s` | [SecurityManager](SecurityManager.md)?: a security manager |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | always, unless `sm == null` |

## Properties

### err

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val err: PrintStream!
```

The "standard" error output stream. This stream is already open and ready to accept output data.

Typically this stream corresponds to display output or another output destination specified by the host environment or user. By convention, this output stream is used to display error messages or other information that should come to the immediate attention of a user even if the principal output stream, the value of the variable `out`, has been redirected to a file or other destination that is typically not continuously monitored.

### in

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val in: InputStream!
```

The "standard" input stream. This stream is already open and ready to supply input data. Typically this stream corresponds to keyboard input or another input source specified by the host environment or user.

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val out: PrintStream!
```

The "standard" output stream. This stream is already open and ready to accept output data. Typically this stream corresponds to display output or another output destination specified by the host environment or user.

For simple stand-alone Java applications, a typical way to write a line of output data is:

```kotlin
System.out.println(data)
  
```

See the `println` methods in class `PrintStream`.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println()`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.CharArray)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Double)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.Any)`
- `https://developer.android.com/reference/kotlin/java/io/PrintStream.html#println(kotlin.String)`
