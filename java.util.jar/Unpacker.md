# Pack200.Unpacker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Unpacker

```
interface Unpacker
```

| [java.util.jar.Pack200.Unpacker](../java/util/jar/Pack200.Unpacker.md) |

The unpacker engine converts the packed stream to a JAR file. An instance of the engine can be obtained using [newUnpacker](../java/util/jar/Pack200.md)).

Every JAR file produced by this engine will include the string "PACK200" as a zip file comment. This allows a deployer to detect if a JAR archive was packed and unpacked.

Note: Unless otherwise noted, passing a null argument to a constructor or method in this class will cause a [NullPointerException](../java/lang/NullPointerException.md) to be thrown.

This version of the unpacker is compatible with all previous versions.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFLATE_HINT](../java/util/jar/Pack200.Unpacker.md) Property indicating that the unpacker should ignore all transmitted values for DEFLATE_HINT, replacing them by the given value, [TRUE](../java/util/jar/Pack200.Unpacker.md) or [FALSE](../java/util/jar/Pack200.Unpacker.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FALSE](../java/util/jar/Pack200.Unpacker.md) The string "false", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP](../java/util/jar/Pack200.Unpacker.md) The string "keep", a possible value for certain properties. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROGRESS](../java/util/jar/Pack200.Unpacker.md) The unpacker's progress as a percentage, as periodically updated by the unpacker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TRUE](../java/util/jar/Pack200.Unpacker.md) The string "true", a possible value for certain properties. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](../java/util/jar/Pack200.Unpacker.md))`(`listener:` ` [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!`)` Registers a listener for PropertyChange events on the properties map. |
| abstract [SortedMap](../java/util/SortedMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [properties](../java/util/jar/Pack200.Unpacker.md))`()` Get the set of this engine's properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](../java/util/jar/Pack200.Unpacker.md))`(`listener:` ` [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!`)` Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](../java/util/jar/Pack200.Unpacker.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unpack](../java/util/jar/Pack200.Unpacker.md))`(`in:` ` [File](../java/io/File.md)!`, `out:` ` [JarOutputStream](../java/util/jar/JarOutputStream.md)!`)` Read a Pack200 archive, and write the encoded JAR to a JarOutputStream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unpack](../java/util/jar/Pack200.Unpacker.md))`(`in:` ` [InputStream](../java/io/InputStream.md)!`, `out:` ` [JarOutputStream](../java/util/jar/JarOutputStream.md)!`)` Read a Pack200 archive, and write the encoded JAR to a JarOutputStream. |

## Constants

### DEFLATE_HINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATE_HINT: String
```

Property indicating that the unpacker should ignore all transmitted values for DEFLATE_HINT, replacing them by the given value, [TRUE](../java/util/jar/Pack200.Unpacker.md) or [FALSE](../java/util/jar/Pack200.Unpacker.md). The default value is the special string [KEEP](../java/util/jar/Pack200.Unpacker.md), which asks the unpacker to preserve all transmitted deflation hints. 

 Value: "unpack.deflate.hint"

### FALSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FALSE: String
```

The string "false", a possible value for certain properties. 

 Value: "false"

**See Also**

- [#DEFLATE_HINT](../java/util/jar/Pack200.Unpacker.md) 

### KEEP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP: String
```

The string "keep", a possible value for certain properties. 

 Value: "keep"

**See Also**

- [#DEFLATE_HINT](../java/util/jar/Pack200.Unpacker.md) 

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

- [#DEFLATE_HINT](../java/util/jar/Pack200.Unpacker.md)

## Public methods

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. Applications that need to monitor progress of the unpacker can poll the value of the [PROGRESS](../java/util/jar/Pack200.Unpacker.md) property instead.*

Registers a listener for PropertyChange events on the properties map. This is typically used by applications to update a progress bar.

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!:An object to be invoked when a property is changed. |

**See Also**

- [#properties](../java/util/jar/Pack200.Unpacker.md))
- [#PROGRESS](../java/util/jar/Pack200.Unpacker.md) 

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
| [SortedMap](../java/util/SortedMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A sorted association of option key strings to option values. |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release.*

Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](../java/util/jar/Pack200.Unpacker.md)).

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](../java/beans/PropertyChangeListener.md)!:The PropertyChange listener to be removed. |

**See Also**

- [#addPropertyChangeListener](../java/util/jar/Pack200.Unpacker.md)) 

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
| `in` | [File](../java/io/File.md)!:a File. |
| `out` | [JarOutputStream](../java/util/jar/JarOutputStream.md)!:a JarOutputStream. |

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
| `in` | [InputStream](../java/io/InputStream.md)!:an InputStream. |
| `out` | [JarOutputStream](../java/util/jar/JarOutputStream.md)!:a JarOutputStream. |

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if an error is encountered. |
