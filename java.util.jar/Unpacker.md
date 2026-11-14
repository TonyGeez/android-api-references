# Pack200.Unpacker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Unpacker

```
interface Unpacker
```

| [java.util.jar.Pack200.Unpacker](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#) |

The unpacker engine converts the packed stream to a JAR file. An instance of the engine can be obtained using [newUnpacker](https://developer.android.com/reference/kotlin/java/util/jar/Pack200#newUnpacker()).

Every JAR file produced by this engine will include the string "PACK200" as a zip file comment. This allows a deployer to detect if a JAR archive was packed and unpacked.

Note: Unless otherwise noted, passing a null argument to a constructor or method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

This version of the unpacker is compatible with all previous versions.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#DEFLATE_HINT:kotlin.String) Property indicating that the unpacker should ignore all transmitted values for DEFLATE_HINT, replacing them by the given value, [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#TRUE:kotlin.String) or [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#FALSE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#FALSE:kotlin.String) The string "false", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#KEEP:kotlin.String) The string "keep", a possible value for certain properties. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#PROGRESS:kotlin.String) The unpacker's progress as a percentage, as periodically updated by the unpacker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#TRUE:kotlin.String) The string "true", a possible value for certain properties. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#addPropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!`)` Registers a listener for PropertyChange events on the properties map. |
| abstract [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [properties](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#properties())`()` Get the set of this engine's properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#removePropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!`)` Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#addPropertyChangeListener(java.beans.PropertyChangeListener)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unpack](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#unpack(java.io.File,%20java.util.jar.JarOutputStream))`(`in:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `out:` ` [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream)!`)` Read a Pack200 archive, and write the encoded JAR to a JarOutputStream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unpack](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#unpack(java.io.InputStream,%20java.util.jar.JarOutputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `out:` ` [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream)!`)` Read a Pack200 archive, and write the encoded JAR to a JarOutputStream. |

## Constants

### DEFLATE_HINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATE_HINT: String
```

Property indicating that the unpacker should ignore all transmitted values for DEFLATE_HINT, replacing them by the given value, [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#TRUE:kotlin.String) or [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#FALSE:kotlin.String). The default value is the special string [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#KEEP:kotlin.String), which asks the unpacker to preserve all transmitted deflation hints. 

 Value: "unpack.deflate.hint"

### FALSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FALSE: String
```

The string "false", a possible value for certain properties. 

 Value: "false"

**See Also**

- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#DEFLATE_HINT:kotlin.String) 

### KEEP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP: String
```

The string "keep", a possible value for certain properties. 

 Value: "keep"

**See Also**

- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#DEFLATE_HINT:kotlin.String) 

### PROGRESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROGRESS: String
```

The unpacker's progress as a percentage, as periodically updated by the unpacker. Values of 0 - 100 are normal, and -1 indicates a stall. Progress can be monitored by polling the value of this property.

At a minimum, the unpacker must set progress to 0 at the beginning of a packing operation, and to 100 at the end. 

 Value: "unpack.progress"

### TRUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRUE: String
```

The string "true", a possible value for certain properties. 

 Value: "true"

**See Also**

- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#DEFLATE_HINT:kotlin.String)

## Public methods

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. Applications that need to monitor progress of the unpacker can poll the value of the [PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#PROGRESS:kotlin.String) property instead.*

Registers a listener for PropertyChange events on the properties map. This is typically used by applications to update a progress bar.

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!:An object to be invoked when a property is changed. |

**See Also**

- [#properties](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#properties())
- [#PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#PROGRESS:kotlin.String) 

### properties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun properties(): SortedMap<String!, String!>!
```

Get the set of this engine's properties. This set is a "live view", so that changing its contents immediately affects the Packer engine, and changes from the engine (such as progress indications) are immediately visible in the map.

The property map may contain pre-defined implementation specific and default properties. Users are encouraged to read the information and fully understand the implications, before modifying pre-existing properties.

Implementation specific properties are prefixed with a package name associated with the implementor, beginning with com. or a similar prefix. All property names beginning with pack. and unpack. are reserved for use by this API.

Unknown properties may be ignored or rejected with an unspecified error, and invalid entries may cause an unspecified error to be thrown.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A sorted association of option key strings to option values. |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release.*

Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#addPropertyChangeListener(java.beans.PropertyChangeListener)).

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!:The PropertyChange listener to be removed. |

**See Also**

- [#addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker#addPropertyChangeListener(java.beans.PropertyChangeListener)) 

### unpack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unpack(
    in: File!, 
    out: JarOutputStream!
): Unit
```

Read a Pack200 archive, and write the encoded JAR to a JarOutputStream.

Does not close its output. (The output can accumulate more elements.)

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `in` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:a File. |
| `out` | [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream)!:a JarOutputStream. |

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if an error is encountered. |

### unpack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unpack(
    in: InputStream!, 
    out: JarOutputStream!
): Unit
```

Read a Pack200 archive, and write the encoded JAR to a JarOutputStream. The entire contents of the input stream will be read. It may be more efficient to read the Pack200 archive to a file and pass the File object, using the alternate method described below.

Closes its input but not its output. (The output can accumulate more elements.)

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an InputStream. |
| `out` | [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream)!:a JarOutputStream. |

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if an error is encountered. |
