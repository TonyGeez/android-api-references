# Pack200.Packer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Packer

```
interface Packer
```

| [java.util.jar.Pack200.Packer](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#) |

The packer engine applies various transformations to the input JAR file, making the pack stream highly compressible by a compressor such as gzip or zip. An instance of the engine can be obtained using [newPacker](https://developer.android.com/reference/kotlin/java/util/jar/Pack200#newPacker()). The high degree of compression is achieved by using a number of techniques described in the JSR 200 specification. Some of the techniques are sorting, re-ordering and co-location of the constant pool.

The pack engine is initialized to an initial state as described by their properties below. The initial state can be manipulated by getting the engine properties (using [properties](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#properties())) and storing the modified properties on the map. The resource files will be passed through with no changes at all. The class files will not contain identical bytes, since the unpacker is free to change minor class file features such as constant pool order. However, the class files will be semantically identical, as specified in The Java™ Virtual Machine Specification.

By default, the packer does not change the order of JAR elements. Also, the modification time and deflation hint of each JAR element is passed unchanged. (Any other ZIP-archive information, such as extra attributes giving Unix file permissions, are lost.)

Note that packing and unpacking a JAR will in general alter the bytewise contents of classfiles in the JAR. This means that packing and unpacking will in general invalidate any digital signatures which rely on bytewise images of JAR elements. In order both to sign and to pack a JAR, you must first pack and unpack the JAR to "normalize" it, then compute signatures on the unpacked JAR elements, and finally repack the signed JAR. Both packing steps should use precisely the same options, and the segment limit may also need to be set to "-1", to prevent accidental variation of segment boundaries as class file sizes change slightly.

(Here's why this works: Any reordering the packer does of any classfile structures is idempotent, so the second packing does not change the orderings produced by the first packing. Also, the unpacker is guaranteed by the JSR 200 specification to produce a specific bytewise image for any given transmission ordering of archive elements.)

In order to maintain backward compatibility, the pack file's version is set to accommodate the class files present in the input JAR file. In other words, the pack file version will be the latest, if the class files are the latest and conversely the pack file version will be the oldest if the class file versions are also the oldest. For intermediate class file versions the corresponding pack file version will be used. For example: If the input JAR-files are solely comprised of 1.5 (or lesser) class files, a 1.5 compatible pack file is produced. This will also be the case for archives that have no class files. If the input JAR-files contains a 1.6 class file, then the pack file version will be set to 1.6.

Note: Unless otherwise noted, passing a null argument to a constructor or method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String) When concatenated with a class attribute name, indicates the format of that attribute, using the layout language specified in the JSR 200 specification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CODE_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CODE_ATTRIBUTE_PFX:kotlin.String) When concatenated with a code attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#DEFLATE_HINT:kotlin.String) If this property is set to [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String) or [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FALSE:kotlin.String), the packer will set the deflation hint accordingly in the output archive, and will not transmit the individual deflation hints of archive elements. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFORT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#EFFORT:kotlin.String) If this property is set to a single decimal digit, the packer will use the indicated amount of effort in compressing the archive. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String) The string "error", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FALSE:kotlin.String) The string "false", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FIELD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FIELD_ATTRIBUTE_PFX:kotlin.String) When concatenated with a field attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP:kotlin.String) The string "keep", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEEP_FILE_ORDER](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP_FILE_ORDER:kotlin.String) If this property is set to [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String), the packer will transmit all elements in their original order within the source archive. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LATEST](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#LATEST:kotlin.String) The string "latest", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METHOD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#METHOD_ATTRIBUTE_PFX:kotlin.String) When concatenated with a method attribute name, indicates the format of that attribute. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MODIFICATION_TIME](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#MODIFICATION_TIME:kotlin.String) If this property is set to the special string [LATEST](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#LATEST:kotlin.String), the packer will attempt to determine the latest modification time, among all the available entries in the original archive or the latest modification time of all the available entries in each segment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) The string "pass", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASS_FILE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS_FILE_PFX:kotlin.String) Indicates that a file should be passed through bytewise, with no compression. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PROGRESS:kotlin.String) The unpacker's progress as a percentage, as periodically updated by the unpacker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEGMENT_LIMIT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#SEGMENT_LIMIT:kotlin.String) This property is a numeral giving the estimated target size N (in bytes) of each archive segment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String) The string "strip", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String) The string "true", a possible value for certain properties. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [UNKNOWN_ATTRIBUTE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#UNKNOWN_ATTRIBUTE:kotlin.String) Indicates the action to take when a class-file containing an unknown attribute is encountered. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#addPropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!`)` Registers a listener for PropertyChange events on the properties map. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pack](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#pack(java.util.jar.JarFile,%20java.io.OutputStream))`(`in:` ` [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile)!`, `out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Takes a JarFile and converts it into a Pack200 archive. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pack](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#pack(java.util.jar.JarInputStream,%20java.io.OutputStream))`(`in:` ` [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream)!`, `out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Takes a JarInputStream and converts it into a Pack200 archive. |
| abstract [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [properties](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#properties())`()` Get the set of this engine's properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#removePropertyChangeListener(java.beans.PropertyChangeListener))`(`listener:` ` [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!`)` Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#addPropertyChangeListener(java.beans.PropertyChangeListener)). |

## Constants

### CLASS_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASS_ATTRIBUTE_PFX: String
```

When concatenated with a class attribute name, indicates the format of that attribute, using the layout language specified in the JSR 200 specification.

For example, the effect of this option is built in:`pack.class.attribute.SourceFile=RUH`.

The special strings [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String), [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String), and [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) are also allowed, with the same meaning as [UNKNOWN_ATTRIBUTE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#UNKNOWN_ATTRIBUTE:kotlin.String). This provides a way for users to request that specific attributes be refused, stripped, or passed bitwise (with no class compression).

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

When concatenated with a code attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.code.attribute.LocalVariableTable=NH[PHOHRUHRSHH]`. The special strings [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String), [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String), and [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) are also allowed. 

 Value: "pack.code.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String) 

### DEFLATE_HINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATE_HINT: String
```

If this property is set to [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String) or [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FALSE:kotlin.String), the packer will set the deflation hint accordingly in the output archive, and will not transmit the individual deflation hints of archive elements.

If this property is set to the special string [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP:kotlin.String), the packer will attempt to determine an independent deflation hint for each available element of the input archive, and transmit this hint separately.

The default is [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP:kotlin.String), which preserves the input information, but may cause the transmitted archive to be larger than necessary.

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

- [#UNKNOWN_ATTRIBUTE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#UNKNOWN_ATTRIBUTE:kotlin.String)
- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String)
- [#FIELD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FIELD_ATTRIBUTE_PFX:kotlin.String)
- [#METHOD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#METHOD_ATTRIBUTE_PFX:kotlin.String)
- [#CODE_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CODE_ATTRIBUTE_PFX:kotlin.String) 

### FALSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FALSE: String
```

The string "false", a possible value for certain properties. 

 Value: "false"

**See Also**

- [#KEEP_FILE_ORDER](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP_FILE_ORDER:kotlin.String)
- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#DEFLATE_HINT:kotlin.String) 

### FIELD_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_ATTRIBUTE_PFX: String
```

When concatenated with a field attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.field.attribute.Deprecated=`. The special strings [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String), [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String), and [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) are also allowed. 

 Value: "pack.field.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String) 

### KEEP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP: String
```

The string "keep", a possible value for certain properties. 

 Value: "keep"

**See Also**

- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#DEFLATE_HINT:kotlin.String)
- [#MODIFICATION_TIME](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#MODIFICATION_TIME:kotlin.String) 

### KEEP_FILE_ORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP_FILE_ORDER: String
```

If this property is set to [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String), the packer will transmit all elements in their original order within the source archive.

If it is set to [FALSE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FALSE:kotlin.String), the packer may reorder elements, and also remove JAR directory entries, which carry no useful information for Java applications. (Typically this enables better compression.)

The default is [TRUE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#TRUE:kotlin.String), which preserves the input information, but may cause the transmitted archive to be larger than necessary. 

 Value: "pack.keep.file.order"

### LATEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LATEST: String
```

The string "latest", a possible value for certain properties. 

 Value: "latest"

**See Also**

- [#MODIFICATION_TIME](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#MODIFICATION_TIME:kotlin.String) 

### METHOD_ATTRIBUTE_PFX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_ATTRIBUTE_PFX: String
```

When concatenated with a method attribute name, indicates the format of that attribute. For example, the effect of this option is built in:`pack.method.attribute.Exceptions=NH[RCH]`. The special strings [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String), [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String), and [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) are also allowed. 

 Value: "pack.method.attribute."

**See Also**

- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String) 

### MODIFICATION_TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODIFICATION_TIME: String
```

If this property is set to the special string [LATEST](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#LATEST:kotlin.String), the packer will attempt to determine the latest modification time, among all the available entries in the original archive or the latest modification time of all the available entries in each segment. This single value will be transmitted as part of the segment and applied to all the entries in each segment, [SEGMENT_LIMIT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#SEGMENT_LIMIT:kotlin.String).

This can marginally decrease the transmitted size of the archive, at the expense of setting all installed files to a single date.

If this property is set to the special string [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP:kotlin.String), the packer transmits a separate modification time for each input element.

The default is [KEEP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP:kotlin.String), which preserves the input information, but may cause the transmitted archive to be larger than necessary.

It is up to the unpacker implementation to take action to suitably set the modification time of each element of its output file. 

 Value: "pack.modification.time"

**See Also**

- [#SEGMENT_LIMIT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#SEGMENT_LIMIT:kotlin.String) 

### PASS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PASS: String
```

The string "pass", a possible value for certain properties. 

 Value: "pass"

**See Also**

- [#UNKNOWN_ATTRIBUTE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#UNKNOWN_ATTRIBUTE:kotlin.String)
- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String)
- [#FIELD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FIELD_ATTRIBUTE_PFX:kotlin.String)
- [#METHOD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#METHOD_ATTRIBUTE_PFX:kotlin.String)
- [#CODE_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CODE_ATTRIBUTE_PFX:kotlin.String) 

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

- [#UNKNOWN_ATTRIBUTE](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#UNKNOWN_ATTRIBUTE:kotlin.String)
- [#CLASS_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CLASS_ATTRIBUTE_PFX:kotlin.String)
- [#FIELD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#FIELD_ATTRIBUTE_PFX:kotlin.String)
- [#METHOD_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#METHOD_ATTRIBUTE_PFX:kotlin.String)
- [#CODE_ATTRIBUTE_PFX](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#CODE_ATTRIBUTE_PFX:kotlin.String) 

### TRUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRUE: String
```

The string "true", a possible value for certain properties. 

 Value: "true"

**See Also**

- [#KEEP_FILE_ORDER](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#KEEP_FILE_ORDER:kotlin.String)
- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#DEFLATE_HINT:kotlin.String) 

### UNKNOWN_ATTRIBUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_ATTRIBUTE: String
```

Indicates the action to take when a class-file containing an unknown attribute is encountered. Possible values are the strings [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String), [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String), and [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String).

The string [ERROR](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#ERROR:kotlin.String) means that the pack operation as a whole will fail, with an exception of type`IOException`. The string [STRIP](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#STRIP:kotlin.String) means that the attribute will be dropped. The string [PASS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PASS:kotlin.String) means that the whole class-file will be passed through (as if it were a resource file) without compression, with a suitable warning. This is the default value for this property.

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

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release. Applications that need to monitor progress of the packer can poll the value of the [PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PROGRESS:kotlin.String) property instead.*

Registers a listener for PropertyChange events on the properties map. This is typically used by applications to update a progress bar.

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!:An object to be invoked when a property is changed. |

**See Also**

- [#properties](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#properties())
- [#PROGRESS](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#PROGRESS:kotlin.String) 

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
| `in` | [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile)!:a JarFile |
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:an OutputStream |

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
| `in` | [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream)!:a JarInputStream |
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:an OutputStream |

**See Also**

- [#MODIFICATION_TIME](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#MODIFICATION_TIME:kotlin.String)
- [#DEFLATE_HINT](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#DEFLATE_HINT:kotlin.String)

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

The returned map implements all optional [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#) operations

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | A sorted association of property key strings to property values. |

### removePropertyChangeListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePropertyChangeListener(listener: PropertyChangeListener!): Unit
```

**Deprecated:** *The dependency on`PropertyChangeListener`creates a significant impediment to future modularization of the Java platform. This method will be removed in a future release.*

Remove a listener for PropertyChange events, added by the [addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#addPropertyChangeListener(java.beans.PropertyChangeListener)).

The default implementation of this method does nothing and has no side-effects.

**WARNING:** This method is omitted from the interface declaration in all subset Profiles of Java SE that do not include the`java.beans`package.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PropertyChangeListener](https://developer.android.com/reference/kotlin/java/beans/PropertyChangeListener.html#)!:The PropertyChange listener to be removed. |

**See Also**

- [#addPropertyChangeListener](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer#addPropertyChangeListener(java.beans.PropertyChangeListener))
