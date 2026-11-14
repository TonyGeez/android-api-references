Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DexFile

```
class DexFile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [dalvik.system.DexFile](https://developer.android.com/reference/kotlin/dalvik/system/DexFile#) |

Loads DEX files. This class is meant for internal use and should not be used by applications. Applications should not instantiate this class. It will hurt performance in most cases and will lead to incorrect execution of bytecode in the worst case. Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **Non-static APIs will be removed in a future Android release**.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile.OptimizationInfo` Encapsulates information about the optimizations performed on a dex file. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#DexFile(java.io.File)(file: https://developer.android.com/reference/kotlin/java/io/File.html#!)` Opens a DEX file from a given File object. |
| `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#DexFile(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Opens a DEX file from a given filename. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#close()()` Closes the DEX file. |
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#entries()()` Enumerate the names of the classes in this DEX file. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#getName()()` Gets the name of the (already opened) DEX file. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#isDexOptNeeded(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns true if the VM believes that the apk/jar file is out of date and should be passed through "dexopt" again. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#loadClass(kotlin.String,%20java.lang.ClassLoader)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Loads a class. |
| static [DexFile](https://developer.android.com/reference/kotlin/dalvik/system/DexFile#)! | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#loadDex(kotlin.String,%20kotlin.String,%20kotlin.Int)(sourcePathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, outputPathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Open a DEX file, specifying the file in which the optimized DEX data should be written. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#toString()()` Returns a string representation of the object. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/dalvik/system/DexFile#finalize()()` Called when the class is finalized. |

## Public constructors

### DexFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DexFile(file: File!)
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Opens a DEX file from a given File object.

### DexFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DexFile(fileName: String!)
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Opens a DEX file from a given filename.

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Closes the DEX file.

This may not be able to release all of the resources. If classes from this DEX file are still resident, the DEX file can't be unmapped. In the case where we do not release all the resources, close is called again in the finalizer.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs during closing the file, which normally should not happen |

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun entries(): Enumeration<String!>!
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Enumerate the names of the classes in this DEX file.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an enumeration of names of classes contained in the DEX file, in the usual internal form (like "java/lang/String"). |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Gets the name of the (already opened) DEX file.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the file name |

### isDexOptNeeded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDexOptNeeded(fileName: String!): Boolean
```

**Deprecated:** *Use `Artd.getDexoptNeeded` instead.*

Returns true if the VM believes that the apk/jar file is out of date and should be passed through "dexopt" again.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the absolute path to the apk/jar file to examine. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if dexopt should be called on the file, false otherwise. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if fileName is not readable, not a file, or not present. |
| `java.io.IOException` | if fileName is not a valid apk/jar file or if problems occur while parsing it. |
| `java.lang.NullPointerException` | if fileName is null. |

### loadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadClass(
    name: String!, 
    loader: ClassLoader!
): Class<Any!>!
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Loads a class. Returns the class on success, or a `null` reference on failure.

If you are not calling this from a class loader, this is most likely not going to do what you want. Use `https://developer.android.com/reference/kotlin/java/lang/Class.html#forName(kotlin.String)` instead.

The method does not throw `https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException.html#` if the class isn't found because it isn't reasonable to throw exceptions wildly every time a class is not found in the first DEX file we look at.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the class name, which should look like "java/lang/String" |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: the class loader that tries to load the class (in most cases the caller of the method |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | the `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object representing the class, or `null` if the class cannot be loaded |

### loadDex

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun loadDex(
    sourcePathName: String!, 
    outputPathName: String!, 
    flags: Int
): DexFile!
```

**Deprecated:** *Applications should use one of the standard classloaders such as `https://developer.android.com/reference/kotlin/dalvik/system/PathClassLoader` instead. **This API will be removed in a future Android release**.*

Open a DEX file, specifying the file in which the optimized DEX data should be written. If the optimized form exists and appears to be current, it will be used; if not, the VM will attempt to regenerate it.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called when the class is finalized. Makes sure the DEX file is closed.

Note: dex2oat bypasses finalization during multi-process app image generation by dropping the java.lang.ref.FinalizerReference.head poimter before GC.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
| `java.io.IOException` | if an I/O error occurs during closing the file, which normally should not happen |
