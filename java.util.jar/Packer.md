# Pack200.Packer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Packer

```
interface Packer
```

| [java.util.jar.Pack200.Packer](../java/util/jar/Pack200.Packer.md) |

The packer engine applies various transformations to the input JAR file, making the pack stream highly compressible by a compressor such as gzip or zip. An instance of the engine can be obtained using [newPacker](Pack200.md)). The high degree of compression is achieved by using a number of techniques described in the JSR 200 specification. Some of the techniques are sorting, re-ordering and co-location of the constant pool.

The pack engine is initialized to an initial state as described by their properties below. The initial state can be manipulated by getting the engine properties (using [properties](../java/util/jar/Pack200.Packer.md))) and storing the modified properties on the map. The resource files will be passed through with no changes at all. The class files will not contain identical bytes, since the unpacker is free to change minor class file features such as constant pool order. However, the class files will be semantically identical, as specified in The Java™ Virtual Machine Specification.

By default, the packer does not change the order of JAR elements. Also, the modification time and deflation hint of each JAR element is passed unchanged. (Any other ZIP-archive information, such as extra attributes giving Unix file permissions, are lost.)

Note that packing and unpacking a JAR will in general alter the bytewise contents of classfiles in the JAR. This means that packing and unpacking will in general invalidate any digital signatures which rely on bytewise images of JAR elements. In order both to sign and to pack a JAR, you must first pack and unpack the JAR to "normalize" it, then compute signatures on the unpacked JAR elements, and finally repack the signed JAR. Both packing steps should use precisely the same options, and the segment limit may also need to be set to "-1", to prevent accidental variation of segment boundaries as class file sizes change slightly.

(Here's why this works: Any reordering the packer does of any classfile structures is idempotent, so the second packing does not change the orderings produced by the first packing. Also, the unpacker is guaranteed by the JSR 200 specification to produce a specific bytewise image for any given transmission ordering of archive elements.)

In order to maintain backward compatibility, the pack file's version is set to accommodate the class files present in the input JAR file. In other words, the pack file version will be the latest, if the class files are the latest and conversely the pack file version will be the oldest if the class file versions are also the oldest. For intermediate class file versions the corresponding pack file version will be used. For example: If the input JAR-files are solely comprised of 1.5 (or lesser) class files, a 1.5 compatible pack file is produced. This will also be the case for archives that have no class files. If the input JAR-files contains a 1.6 class file, then the pack file version will be set to 1.6.

Note: Unless otherwise noted, passing a null argument to a constructor or method in this class will cause a [NullPointerException](../java.lang/NullPointerException.md) to be thrown.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) When concatenated with a class attribute name, indicates the format of that attribute, using the layout language specified in the JSR 200 specification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CODE_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) When concatenated with a code attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFLATE_HINT](../java/util/jar/Pack200.Packer.md) If this property is set to [TRUE](../java/util/jar/Pack200.Packer.md) or [FALSE](../java/util/jar/Pack200.Packer.md), the packer will set the deflation hint accordingly in the output archive, and will not transmit the individual deflation hints of archive elements. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFORT](../java/util/jar/Pack200.Packer.md) If this property is set to a single decimal digit, the packer will use the indicated amount of effort in compressing the archive. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ERROR](../java/util/jar/Pack200.Packer.md) The string "error", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FALSE](../java/util/jar/Pack200.Packer.md) The string "false", a possible value for certain properties. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FIELD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) When concatenated with a field attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP](../java/util/jar/Pack200.Packer.md) The string "keep", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP_FILE_ORDER](../java/util/jar/Pack200.Packer.md) If this property is set to [TRUE](../java/util/jar/Pack200.Packer.md), the packer will transmit all elements in their original order within the source archive. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LATEST](../java/util/jar/Pack200.Packer.md) The string "latest", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METHOD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) When concatenated with a method attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MODIFICATION_TIME](../java/util/jar/Pack200.Packer.md) If this property is set to the special string [LATEST](../java/util/jar/Pack200.Packer.md), the packer will attempt to determine the latest modification time, among all the available entries in the original archive or the latest modification time of all the available entries in each segment. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASS](../java/util/jar/Pack200.Packer.md) The string "pass", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASS_FILE_PFX](../java/util/jar/Pack200.Packer.md) Indicates that a file should be passed through bytewise, with no compression. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROGRESS](../java/util/jar/Pack200.Packer.md) The unpacker's progress as a percentage, as periodically updated by the unpacker. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEGMENT_LIMIT](../java/util/jar/Pack200.Packer.md) This property is a numeral giving the estimated target size N (in bytes) of each archive segment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STRIP](../java/util/jar/Pack200.Packer.md) The string "strip", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TRUE](../java/util/jar/Pack200.Packer.md) The string "true", a possible value for certain properties. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [UNKNOWN_ATTRIBUTE](../java/util/jar/Pack200.Packer.md) Indicates the action to take when a class-file containing an unknown attribute is encountered. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](../java/util/jar/Pack200.Packer.md))`(`listener:` ` [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!`)` Registers a listener for PropertyChange events on the properties map. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pack](../java/util/jar/Pack200.Packer.md))`(`in:` ` [JarFile](JarFile.md)!`, `out:` ` [OutputStream](../java.io/OutputStream.md)!`)` Takes a JarFile and converts it into a Pack200 archive. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pack](../java/util/jar/Pack200.Packer.md))`(`in:` ` [JarInputStream](JarInputStream.md)!`, `out:` ` [OutputStream](../java.io/OutputStream.md)!`)` Takes a JarInputStream and converts it into a Pack200 archive. |
| --- | --- |
| abstract [SortedMap](../java.util/SortedMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [properties](../java/util/jar/Pack200.Packer.md))`()` Get the set of this engine's properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](../java/util/jar/Pack200.Packer.md))`(`listener:` ` [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!`)` Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](../java/util/jar/Pack200.Packer.md)). |

## Constants

### CLASS_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASS_ATTRIBUTE_PFX: String
```

When concatenated with a class attribute name, indicates the format of that attribute, using the layout language specified in the JSR 200 specification.

For example, the effect of this option is built in:`pack.class.attribute.SourceFile=RUH`.

The special strings [ERROR](../java/util/jar/Pack200.Packer.md), [STRIP](../java/util/jar/Pack200.Packer.md), and [PASS](../java/util/jar/Pack200.Packer.md) are also allowed, with the same meaning as [UNKNOWN_ATTRIBUTE](../java/util/jar/Pack200.Packer.md). This provides a way for users to request that specific attributes be refused, stripped, or passed bitwise (with no class compression).

Code like this might be used to support attributes for JCOV: 

```kotlin
<code>
      Map p = packer.properties();
      p.put(CODE_ATTRIBUTE_PFX+"CoverageTable",       "NH[PHHII]");
      p.put(CODE_ATTRIBUTE_PFX+"CharacterRangeTable", "NH[PHPOHIIH]");
      p.put(CLASS_ATTRIBUTE_PFX+"SourceID",           "RUH");
      p.put(CLASS_ATTRIBUTE_PFX+"CompilationID",      "RUH");
  </code>
```

Code like this might be used to strip debugging attributes: 

```kotlin
<code>
      Map p = packer.properties();
      p.put(CODE_ATTRIBUTE_PFX+"LineNumberTable",    STRIP);
      p.put(CODE_ATTRIBUTE_PFX+"LocalVariableTable", STRIP);
      p.put(CLASS_ATTRIBUTE_PFX+"SourceFile",        STRIP);
  </code>
```  

 Value: "pack.class.attribute."

### CODE_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ATTRIBUTE_PFX: String
```

When concatenated with a code attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.code.attribute.LocalVariableTable=NH[PHOHRUHRSHH]`. The special strings [ERROR](../java/util/jar/Pack200.Packer.md), [STRIP](../java/util/jar/Pack200.Packer.md), and [PASS](../java/util/jar/Pack200.Packer.md) are also allowed. 

 Value: "pack.code.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### DEFLATE_HINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATE_HINT: String
```

If this property is set to [TRUE](../java/util/jar/Pack200.Packer.md) or [FALSE](../java/util/jar/Pack200.Packer.md), the packer will set the deflation hint accordingly in the output archive, and will not transmit the individual deflation hints of archive elements.

If this property is set to the special string [KEEP](../java/util/jar/Pack200.Packer.md), the packer will attempt to determine an independent deflation hint for each available element of the input archive, and transmit this hint separately.

The default is [KEEP](../java/util/jar/Pack200.Packer.md), which preserves the input information, but may cause the transmitted archive to be larger than necessary.

It is up to the unpacker implementation to take action upon the hint to suitably compress the elements of the resulting unpacked jar.

The deflation hint of a ZIP or JAR element indicates whether the element was deflated or stored directly. 

 Value: "pack.deflate.hint"

### EFFORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFORT: String
```

If this property is set to a single decimal digit, the packer will use the indicated amount of effort in compressing the archive. Level 1 may produce somewhat larger size and faster compression speed, while level 9 will take much longer but may produce better compression.

The special value 0 instructs the packer to copy through the original JAR file directly, with no compression. The JSR 200 standard requires any unpacker to understand this special case as a pass-through of the entire archive.

The default is 5, investing a modest amount of time to produce reasonable compression. 

 Value: "pack.effort"

### ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: String
```

The string "error", a possible value for certain properties. 

 Value: "error"

**See Also**

- [#UNKNOWN_ATTRIBUTE](../java/util/jar/Pack200.Packer.md)
- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#FIELD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#METHOD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#CODE_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### FALSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FALSE: String
```

The string "false", a possible value for certain properties. 

 Value: "false"

**See Also**

- [#KEEP_FILE_ORDER](../java/util/jar/Pack200.Packer.md)
- [#DEFLATE_HINT](../java/util/jar/Pack200.Packer.md) 

### FIELD_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_ATTRIBUTE_PFX: String
```

When concatenated with a field attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.field.attribute.Deprecated=`. The special strings [ERROR](../java/util/jar/Pack200.Packer.md), [STRIP](../java/util/jar/Pack200.Packer.md), and [PASS](../java/util/jar/Pack200.Packer.md) are also allowed. 

 Value: "pack.field.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### KEEP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP: String
```

The string "keep", a possible value for certain properties. 

 Value: "keep"

**See Also**

- [#DEFLATE_HINT](../java/util/jar/Pack200.Packer.md)
- [#MODIFICATION_TIME](../java/util/jar/Pack200.Packer.md) 

### KEEP_FILE_ORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP_FILE_ORDER: String
```

If this property is set to [TRUE](../java/util/jar/Pack200.Packer.md), the packer will transmit all elements in their original order within the source archive.

If it is set to [FALSE](../java/util/jar/Pack200.Packer.md), the packer may reorder elements, and also remove JAR directory entries, which carry no useful information for Java applications. (Typically this enables better compression.)

The default is [TRUE](../java/util/jar/Pack200.Packer.md), which preserves the input information, but may cause the transmitted archive to be larger than necessary. 

 Value: "pack.keep.file.order"

### LATEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LATEST: String
```

The string "latest", a possible value for certain properties. 

 Value: "latest"

**See Also**

- [#MODIFICATION_TIME](../java/util/jar/Pack200.Packer.md) 

### METHOD_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_ATTRIBUTE_PFX: String
```

When concatenated with a method attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.method.attribute.Exceptions=NH[RCH]`. The special strings [ERROR](../java/util/jar/Pack200.Packer.md), [STRIP](../java/util/jar/Pack200.Packer.md), and [PASS](../java/util/jar/Pack200.Packer.md) are also allowed. 

 Value: "pack.method.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### MODIFICATION_TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODIFICATION_TIME: String
```

If this property is set to the special string [LATEST](../java/util/jar/Pack200.Packer.md), the packer will attempt to determine the latest modification time, among all the available entries in the original archive or the latest modification time of all the available entries in each segment. This single value will be transmitted as part of the segment and applied to all the entries in each segment, [SEGMENT_LIMIT](../java/util/jar/Pack200.Packer.md).

This can marginally decrease the transmitted size of the archive, at the expense of setting all installed files to a single date.

If this property is set to the special string [KEEP](../java/util/jar/Pack200.Packer.md), the packer transmits a separate modification time for each input element.

The default is [KEEP](../java/util/jar/Pack200.Packer.md), which preserves the input information, but may cause the transmitted archive to be larger than necessary.

It is up to the unpacker implementation to take action to suitably set the modification time of each element of its output file. 

 Value: "pack.modification.time"

**See Also**

- [#SEGMENT_LIMIT](../java/util/jar/Pack200.Packer.md) 

### PASS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PASS: String
```

The string "pass", a possible value for certain properties. 

 Value: "pass"

**See Also**

- [#UNKNOWN_ATTRIBUTE](../java/util/jar/Pack200.Packer.md)
- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#FIELD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#METHOD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#CODE_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### PASS_FILE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PASS_FILE_PFX: String
```

Indicates that a file should be passed through bytewise, with no compression. Multiple files may be specified by specifying additional properties with distinct strings appended, to make a family of properties with the common prefix.

There is no pathname transformation, except that the system file separator is replaced by the JAR file separator '/'.

The resulting file names must match exactly as strings with their occurrences in the JAR file.

If a property value is a directory name, all files under that directory will be passed also.

Examples: 

```kotlin
<code>Map p = packer.properties();
      p.put(PASS_FILE_PFX+0, "mutants/Rogue.class");
      p.put(PASS_FILE_PFX+1, "mutants/Wolverine.class");
      p.put(PASS_FILE_PFX+2, "mutants/Storm.class");
      # Pass all files in an entire directory hierarchy:
      p.put(PASS_FILE_PFX+3, "police/");
  </code>
```  

 Value: "pack.pass.file."

### PROGRESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROGRESS: String
```

The unpacker's progress as a percentage, as periodically updated by the unpacker. Values of 0 - 100 are normal, and -1 indicates a stall. Progress can be monitored by polling the value of this property.

At a minimum, the unpacker must set progress to 0 at the beginning of a packing operation, and to 100 at the end. 

 Value: "pack.progress"

### SEGMENT_LIMIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEGMENT_LIMIT: String
```

This property is a numeral giving the estimated target size N (in bytes) of each archive segment. If a single input file requires more than N bytes, it will be given its own archive segment.

As a special case, a value of -1 will produce a single large segment with all input files, while a value of 0 will produce one segment for each class. Larger archive segments result in less fragmentation and better compression, but processing them requires more memory.

The size of each segment is estimated by counting the size of each input file to be transmitted in the segment, along with the size of its name and other transmitted properties.

The default is -1, which means the packer will always create a single segment output file. In cases where extremely large output files are generated, users are strongly encouraged to use segmenting or break up the input file into smaller JARs.

A 10Mb JAR packed without this limit will typically pack about 10% smaller, but the packer may require a larger Java heap (about ten times the segment limit). 

 Value: "pack.segment.limit"

### STRIP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRIP: String
```

The string "strip", a possible value for certain properties. 

 Value: "strip"

**See Also**

- [#UNKNOWN_ATTRIBUTE](../java/util/jar/Pack200.Packer.md)
- [#CLASS_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#FIELD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#METHOD_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md)
- [#CODE_ATTRIBUTE_PFX](../java/util/jar/Pack200.Packer.md) 

### TRUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRUE: String
```

The string "true", a possible value for certain properties. 

 Value: "true"

**See Also**

- [#KEEP_FILE_ORDER](../java/util/jar/Pack200.Packer.md)
- [#DEFLATE_HINT](../java/util/jar/Pack200.Packer.md) 

### UNKNOWN_ATTRIBUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_ATTRIBUTE: String
```

Indicates the action to take when a class-file containing an unknown attribute is encountered. Possible values are the strings [ERROR](../java/util/jar/Pack200.Packer.md), [STRIP](../java/util/jar/Pack200.Packer.md), and [PASS](../java/util/jar/Pack200.Packer.md).

The string [ERROR](../java/util/jar/Pack200.Packer.md) means that the pack operation as a whole will fail, with an exception of type`IOException`. The string [STRIP](../java/util/jar/Pack200.Packer.md) means that the attribute will be dropped. The string [PASS](../java/util/jar/Pack200.Packer.md) means that the whole class-file will be passed through (as if it were a resource file) without compression, with a suitable warning. This is the default value for this property.

Examples: 

```kotlin
<code>Map p = pack200.getProperties();
      p.put(UNKNOWN_ATTRIBUTE, ERROR);
      p.put(UNKNOWN_ATTRIBUTE, STRIP);
      p.put(UNKNOWN_ATTRIBUTE, PASS);
  </code>
```  

 Value: "pack.unknown.attribute"

## Public methods

### addPropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. Applications that need to monitor progress of the packer can poll the value of the [PROGRESS](../java/util/jar/Pack200.Packer.md) property instead.*

Registers a listener for PropertyChange events on the properties map. This is typically used by applications to update a progress bar.

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!:An object to be invoked when a property is changed. |

**See Also**

- [#properties](../java/util/jar/Pack200.Packer.md))
- [#PROGRESS](../java/util/jar/Pack200.Packer.md) 

### pack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pack(
    in: JarFile!, 
    out: OutputStream!
): Unit
```

Takes a JarFile and converts it into a Pack200 archive.

Closes its input but not its output. (Pack200 archives are appendable.)

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------|
| `in` | [JarFile](JarFile.md)!:a JarFile |
| `out` | [OutputStream](../java.io/OutputStream.md)!:an OutputStream |

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if an error is encountered. |

### pack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pack(
    in: JarInputStream!, 
    out: OutputStream!
): Unit
```

Takes a JarInputStream and converts it into a Pack200 archive.

Closes its input but not its output. (Pack200 archives are appendable.)

The modification time and deflation hint attributes are not available, for the JAR manifest file and its containing directory.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `in` | [JarInputStream](JarInputStream.md)!:a JarInputStream |
| `out` | [OutputStream](../java.io/OutputStream.md)!:an OutputStream |

**See Also**

- [#MODIFICATION_TIME](../java/util/jar/Pack200.Packer.md)
- [#DEFLATE_HINT](../java/util/jar/Pack200.Packer.md)

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if an error is encountered. |

### properties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun properties(): SortedMap<String!, String!>!
```

Get the set of this engine's properties. This set is a "live view", so that changing its contents immediately affects the Packer engine, and changes from the engine (such as progress indications) are immediately visible in the map.

The property map may contain pre-defined implementation specific and default properties. Users are encouraged to read the information and fully understand the implications, before modifying pre-existing properties.

Implementation specific properties are prefixed with a package name associated with the implementor, beginning with com. or a similar prefix. All property names beginning with pack. and unpack. are reserved for use by this API.

Unknown properties may be ignored or rejected with an unspecified error, and invalid entries may cause an unspecified error to be thrown.

The returned map implements all optional [SortedMap](../java.util/SortedMap.md) operations

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [SortedMap](../java.util/SortedMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A sorted association of property key strings to property values. |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release.*

Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](../java/util/jar/Pack200.Packer.md)).

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](../java.beans/PropertyChangeListener.md)!:The PropertyChange listener to be removed. |

**See Also**

- [#addPropertyChangeListener](../java/util/jar/Pack200.Packer.md))
