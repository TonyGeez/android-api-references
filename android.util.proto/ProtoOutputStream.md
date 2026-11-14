# ProtoOutputStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtoOutputStream

Kotlin| [Java](https://developer.android.com/reference/android/util/proto/ProtoOutputStream "View this page in Java") 

```
class ProtoOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.util.proto.ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#) |

Class to write to a protobuf stream.

This API is not as convenient or type safe as the standard protobuf classes. If possible, the best recommended library is to use protobuf lite. However, in environments (such as the Android platform itself), a more memory efficient version is necessary.

Each write method takes an ID code from the protoc generated classes and the value to write. To make a nested object, call [start(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#start(kotlin.Long))and then [end(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#end(kotlin.Long))when you are done.

The ID codes have type information embedded into them, so if you call the incorrect function you will get an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#).

To retrieve the encoded protobuf stream, call [getBytes()](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes()). stream as the top-level objects are finished.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long) Bit mask for selecting the field count when reading a field id that is used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) Repeated packed field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long) Repeated field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int) Bit offset for building a field id to be used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long) Single field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long) Unknown field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_ID_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_ID_SHIFT:kotlin.Int) Number of bits to shift the field number to form a tag. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_BOOL](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_BOOL:kotlin.Long) Field type code for bool fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_BYTES](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_BYTES:kotlin.Long) Field type code for bytes fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_DOUBLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_DOUBLE:kotlin.Long) Field type code for double fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_ENUM](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_ENUM:kotlin.Long) Field type code for enum fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_FIXED32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_FIXED32:kotlin.Long) Field type code for fixed32 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_FIXED64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_FIXED64:kotlin.Long) Field type code for fixed64 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_FLOAT:kotlin.Long) Field type code for float fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_INT32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_INT32:kotlin.Long) Field type code for int32 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_INT64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_INT64:kotlin.Long) Field type code for int64 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_MASK:kotlin.Long) Mask for the field types stored in a fieldId. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_MESSAGE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_MESSAGE:kotlin.Long) Field type code for message fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_SFIXED32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_SFIXED32:kotlin.Long) Field type code for sfixed32 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_SFIXED64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_SFIXED64:kotlin.Long) Field type code for sfixed64 fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_SHIFT:kotlin.Int) Position of the field type in a (long) fieldId. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_SINT32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_SINT32:kotlin.Long) Field type code for sint32 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_SINT64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_SINT64:kotlin.Long) Field type code for sint64 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_STRING:kotlin.Long) Field type code for string fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_UINT32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_UINT32:kotlin.Long) Field type code for uint32 fields. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FIELD_TYPE_UINT64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_TYPE_UINT64:kotlin.Long) Field type code for uint64 fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_END_GROUP](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_END_GROUP:kotlin.Int) End group wire type code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_FIXED32](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_FIXED32:kotlin.Int) Fixed32 wire type code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_FIXED64](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_FIXED64:kotlin.Int) Fixed64 wire type code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_LENGTH_DELIMITED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_LENGTH_DELIMITED:kotlin.Int) Length delimited wire type code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_MASK:kotlin.Int) Mask to select the wire type from a tag. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_START_GROUP](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_START_GROUP:kotlin.Int) Start group wire type code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIRE_TYPE_VARINT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#WIRE_TYPE_VARINT:kotlin.Int) Varint wire type code. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#ProtoOutputStream())`()` Construct a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#) with the default chunk size. |
| [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#ProtoOutputStream(kotlin.Int))`(`chunkSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a [with the given chunk size.](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes()) |
| [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#ProtoOutputStream(java.io.OutputStream))`(`stream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)`)` Construct a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#) that sits on top of an [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#). |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkFieldId](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#checkFieldId(kotlin.Long,%20kotlin.Long))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `expectedFlags:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Validates that the fieldId provided is of the type and count from expectedType. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#dump(kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Dump debugging data about the buffers with the given log tag. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#end(kotlin.Long))`(`token:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` End the object started by start() that returned token. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#flush())`()` Write remaining data to the output stream. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getBytes](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes())`()` Finish the encoding of the data, and return a byte\[\] with the protobuf formatted data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFieldCountString](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getFieldCountString(kotlin.Long))`(`fieldCount:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Get the developer-usable name of a field count. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getFieldIdString](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getFieldIdString(kotlin.Long))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Get a debug string for a fieldId. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFieldTypeString](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getFieldTypeString(kotlin.Long))`(`fieldType:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Get the developer-usable name of a field type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRawSize](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getRawSize())`()` Returns the total size of the data that has been written, after full protobuf encoding has occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getWireTypeString](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getWireTypeString(kotlin.Int))`(`wireType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the developer-usable name of a wire type. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [makeFieldId](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#makeFieldId(kotlin.Int,%20kotlin.Long))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fieldFlags:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Combine a fieldId (the field keys in the proto file) and the field flags. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [makeToken](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#makeToken(kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`tagSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeated:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `depth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objectId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make a token. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [start](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#start(kotlin.Long))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Start a sub object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [token2String](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#token2String(kotlin.Long))`(`token:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Return a debugging string of a token. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Boolean))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Write a boolean value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.ByteArray))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Write a byte\[\] value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Double))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Write a value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Float))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Write a value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write a value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.String))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Write a string value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))`(`fieldId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Write a value for the given fieldId. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTag](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#writeTag(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wireType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write an individual field tag by hand. |

## Constants

### FIELD_COUNT_MASK

```
static val FIELD_COUNT_MASK: Long
```

Bit mask for selecting the field count when reading a field id that is used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. 

 Value: 16492674416640L

**See Also**

- [#FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int)
- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long)
- [#FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long)
- [#FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long)
- [#FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) 

### FIELD_COUNT_PACKED

```
static val FIELD_COUNT_PACKED: Long
```

Repeated packed field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. 

 Value: 5497558138880L

**See Also**

- [#FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int)
- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long)
- [#FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long)
- [#FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long) 

### FIELD_COUNT_REPEATED

```
static val FIELD_COUNT_REPEATED: Long
```

Repeated field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. 

 Value: 2199023255552L

**See Also**

- [#FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int)
- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long)
- [#FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long)
- [#FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) 

### FIELD_COUNT_SHIFT

```
static val FIELD_COUNT_SHIFT: Int
```

Bit offset for building a field id to be used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`. 

 Value: 40

**See Also**

- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long)
- [#FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long)
- [#FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long)
- [#FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) 

### FIELD_COUNT_SINGLE

```
static val FIELD_COUNT_SINGLE: Long
```

Single field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. 

 Value: 1099511627776L

**See Also**

- [#FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int)
- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_UNKNOWN](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_UNKNOWN:kotlin.Long)
- [#FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long)
- [#FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) 

### FIELD_COUNT_UNKNOWN

```
static val FIELD_COUNT_UNKNOWN: Long
```

Unknown field count, encoded into a field id used with a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#)`.write(...)`method. 

 Value: 0L

**See Also**

- [#FIELD_COUNT_SHIFT](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SHIFT:kotlin.Int)
- [#FIELD_COUNT_MASK](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_MASK:kotlin.Long)
- [#FIELD_COUNT_SINGLE](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_SINGLE:kotlin.Long)
- [#FIELD_COUNT_REPEATED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_REPEATED:kotlin.Long)
- [#FIELD_COUNT_PACKED](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#FIELD_COUNT_PACKED:kotlin.Long) 

### FIELD_ID_SHIFT

```
static val FIELD_ID_SHIFT: Int
```

Number of bits to shift the field number to form a tag. 

```kotlin
// Reading a field number from a tag.
  int fieldNumber = tag >>> FIELD_ID_SHIFT;
 
  // Building a tag from a field number and a wire type.
  int tag = (fieldNumber << FIELD_ID_SHIFT) | wireType;
  
```

<br />

 Value: 3

**See Also**

### FIELD_TYPE_BOOL

```
static val FIELD_TYPE_BOOL: Long
```

Field type code for bool fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, boolean)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Boolean))method. 

 Value: 34359738368L

### FIELD_TYPE_BYTES

```
static val FIELD_TYPE_BYTES: Long
```

Field type code for bytes fields. Used to build constants in generated code for use with the[ProtoOutputStream.write(long, byte[])](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.ByteArray))method. 

 Value: 51539607552L

### FIELD_TYPE_DOUBLE

```
static val FIELD_TYPE_DOUBLE: Long
```

Field type code for double fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, double)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Double))method. 

 Value: 4294967296L

### FIELD_TYPE_ENUM

```
static val FIELD_TYPE_ENUM: Long
```

Field type code for enum fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 60129542144L

### FIELD_TYPE_FIXED32

```
static val FIELD_TYPE_FIXED32: Long
```

Field type code for fixed32 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 30064771072L

### FIELD_TYPE_FIXED64

```
static val FIELD_TYPE_FIXED64: Long
```

Field type code for fixed64 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))method. 

 Value: 25769803776L

### FIELD_TYPE_FLOAT

```
static val FIELD_TYPE_FLOAT: Long
```

Field type code for float fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, float)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Float))method. 

 Value: 8589934592L

### FIELD_TYPE_INT32

```
static val FIELD_TYPE_INT32: Long
```

Field type code for int32 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 21474836480L

### FIELD_TYPE_INT64

```
static val FIELD_TYPE_INT64: Long
```

Field type code for int64 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))method. 

 Value: 12884901888L

### FIELD_TYPE_MASK

```
static val FIELD_TYPE_MASK: Long
```

Mask for the field types stored in a fieldId. Leaves a whole byte for future expansion, even though there are currently only 17 types. 

 Value: 1095216660480L

### FIELD_TYPE_MESSAGE

```
static val FIELD_TYPE_MESSAGE: Long
```

Field type code for message fields. Used to build constants in generated code for use with the [ProtoOutputStream.start(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#start(kotlin.Long))method. 

 Value: 47244640256L

### FIELD_TYPE_SFIXED32

```
static val FIELD_TYPE_SFIXED32: Long
```

Field type code for sfixed32 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 64424509440L

### FIELD_TYPE_SFIXED64

```
static val FIELD_TYPE_SFIXED64: Long
```

Field type code for sfixed64 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))method. 

 Value: 68719476736L

### FIELD_TYPE_SHIFT

```
static val FIELD_TYPE_SHIFT: Int
```

Position of the field type in a (long) fieldId. 

 Value: 32

### FIELD_TYPE_SINT32

```
static val FIELD_TYPE_SINT32: Long
```

Field type code for sint32 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 73014444032L

### FIELD_TYPE_SINT64

```
static val FIELD_TYPE_SINT64: Long
```

Field type code for sint64 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))method. 

 Value: 77309411328L

### FIELD_TYPE_STRING

```
static val FIELD_TYPE_STRING: Long
```

Field type code for string fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, String)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.String))method. 

 Value: 38654705664L

### FIELD_TYPE_UINT32

```
static val FIELD_TYPE_UINT32: Long
```

Field type code for uint32 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, int)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Int))method. 

 Value: 55834574848L

### FIELD_TYPE_UINT64

```
static val FIELD_TYPE_UINT64: Long
```

Field type code for uint64 fields. Used to build constants in generated code for use with the [ProtoOutputStream.write(long, long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#write(kotlin.Long,%20kotlin.Long))method. 

 Value: 17179869184L

### WIRE_TYPE_END_GROUP

```
static val WIRE_TYPE_END_GROUP: Int
```

End group wire type code. 

 Value: 4

**See Also**

### WIRE_TYPE_FIXED32

```
static val WIRE_TYPE_FIXED32: Int
```

Fixed32 wire type code. 

 Value: 5

**See Also**

### WIRE_TYPE_FIXED64

```
static val WIRE_TYPE_FIXED64: Int
```

Fixed64 wire type code. 

 Value: 1

**See Also**

### WIRE_TYPE_LENGTH_DELIMITED

```
static val WIRE_TYPE_LENGTH_DELIMITED: Int
```

Length delimited wire type code. 

 Value: 2

**See Also**

### WIRE_TYPE_MASK

```
static val WIRE_TYPE_MASK: Int
```

Mask to select the wire type from a tag. 

```kotlin
// Reading a wire type from a tag.
  int wireType = tag & WIRE_TYPE_MASK;
 
  // Building a tag from a field number and a wire type.
  int tag = (fieldNumber << FIELD_ID_SHIFT) | wireType;
  
```

<br />

 Value: 7

**See Also**

### WIRE_TYPE_START_GROUP

```
static val WIRE_TYPE_START_GROUP: Int
```

Start group wire type code. 

 Value: 3

**See Also**

### WIRE_TYPE_VARINT

```
static val WIRE_TYPE_VARINT: Int
```

Varint wire type code. 

 Value: 0

**See Also**

## Public constructors

### ProtoOutputStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtoOutputStream()
```

Construct a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#) with the default chunk size.

This is for an in-memory proto. The caller should use [getBytes()](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes())for the result. 

### ProtoOutputStream

```
ProtoOutputStream(chunkSize: Int)
```

Construct a [with the given chunk size.](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes()) 

### ProtoOutputStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtoOutputStream(stream: OutputStream)
```

Construct a [ProtoOutputStream](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#) that sits on top of an [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#).

The [flush()](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#flush())method must be called when done writing to flush any remaining data, although data \*may\* be written at intermediate points within the writing as well.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `stream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#):This value cannot be`null`. |

## Public methods

### checkFieldId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun checkFieldId(
    fieldId: Long, 
    expectedFlags: Long
): Int
```

Validates that the fieldId provided is of the type and count from expectedType.

The type must match exactly to pass this check.

The count must match according to this truth table to pass the check: expectedFlags UNKNOWN SINGLE REPEATED PACKED fieldId UNKNOWN true false false false SINGLE x true false false REPEATED x false true false PACKED x false true true

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The raw ID of that field. |

| Exceptions ||
|---|----------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) if it is not. |

### dump

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(tag: String): Unit
```

Dump debugging data about the buffers with the given log tag.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### end

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun end(token: Long): Unit
```

End the object started by start() that returned token.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The token returned from [start(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#start(kotlin.Long)) |

### flush

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flush(): Unit
```

Write remaining data to the output stream. If there is no output stream, this function does nothing. Any currently open objects (i.e. ones that have not had [end(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#end(kotlin.Long))called for them will not be written). Whether this writes objects that are closed if there are remaining open objects is undefined (current implementation does not write it, future ones will). For now, can either call [getBytes()](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#getBytes())or [flush()](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#flush()), but not both. 

### getBytes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBytes(): ByteArray
```

Finish the encoding of the data, and return a byte\[\] with the protobuf formatted data.

After this call, do not call any of the write\* functions. The behavior is undefined.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getFieldCountString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFieldCountString(fieldCount: Long): String?
```

Get the developer-usable name of a field count.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getFieldIdString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFieldIdString(fieldId: Long): String
```

Get a debug string for a fieldId.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getFieldTypeString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFieldTypeString(fieldType: Long): String?
```

Get the developer-usable name of a field type.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fieldType` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is android.util.proto.ProtoStream.FIELD_TYPE_UNKNOWN, android.util.proto.ProtoStream.FIELD_TYPE_DOUBLE, android.util.proto.ProtoStream.FIELD_TYPE_FLOAT, android.util.proto.ProtoStream.FIELD_TYPE_INT64, android.util.proto.ProtoStream.FIELD_TYPE_UINT64, android.util.proto.ProtoStream.FIELD_TYPE_INT32, android.util.proto.ProtoStream.FIELD_TYPE_FIXED64, android.util.proto.ProtoStream.FIELD_TYPE_FIXED32, android.util.proto.ProtoStream.FIELD_TYPE_BOOL, android.util.proto.ProtoStream.FIELD_TYPE_STRING, android.util.proto.ProtoStream.FIELD_TYPE_MESSAGE, android.util.proto.ProtoStream.FIELD_TYPE_BYTES, android.util.proto.ProtoStream.FIELD_TYPE_UINT32, android.util.proto.ProtoStream.FIELD_TYPE_ENUM, android.util.proto.ProtoStream.FIELD_TYPE_SFIXED32, android.util.proto.ProtoStream.FIELD_TYPE_SFIXED64, android.util.proto.ProtoStream.FIELD_TYPE_SINT32, or android.util.proto.ProtoStream.FIELD_TYPE_SINT64 |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getRawSize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawSize(): Int
```

Returns the total size of the data that has been written, after full protobuf encoding has occurred.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the uncompressed buffer size |

### getWireTypeString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getWireTypeString(wireType: Int): String?
```

Get the developer-usable name of a wire type.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wireType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is android.util.proto.ProtoStream.WIRE_TYPE_VARINT, android.util.proto.ProtoStream.WIRE_TYPE_FIXED64, android.util.proto.ProtoStream.WIRE_TYPE_LENGTH_DELIMITED, android.util.proto.ProtoStream.WIRE_TYPE_START_GROUP, android.util.proto.ProtoStream.WIRE_TYPE_END_GROUP, or android.util.proto.ProtoStream.WIRE_TYPE_FIXED32 |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### makeFieldId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun makeFieldId(
    id: Int, 
    fieldFlags: Long
): Long
```

Combine a fieldId (the field keys in the proto file) and the field flags. Mostly useful for testing because the generated code contains the fieldId constants. 

### makeToken

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun makeToken(
    tagSize: Int, 
    repeated: Boolean, 
    depth: Int, 
    objectId: Int, 
    offset: Int
): Long
```

Make a token. Bits 61-63 - tag size (So we can go backwards later if the object had not data) - 3 bits, max value 7, max value needed 5 Bit 60 - true if the object is repeated (lets us require endObject or endRepeatedObject) Bits 59-51 - depth (For error checking) - 9 bits, max value 512, when checking, value is masked (if we really are more than 512 levels deep) Bits 32-50 - objectId (For error checking) - 19 bits, max value 524,288. that's a lot of objects. IDs will wrap because of the overflow, and only the tokens are compared. Bits 0-31 - offset of interest for the object. 

### start

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(fieldId: Long): Long
```

Start a sub object.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The token to call [end(long)](https://developer.android.com/reference/kotlin/android/util/proto/ProtoOutputStream#end(kotlin.Long))with. |

### token2String

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun token2String(token: Long): String
```

Return a debugging string of a token.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: Boolean
): Unit
```

Write a boolean value for the given fieldId.

If the field is not a bool field, an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) will be thrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The value. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: ByteArray?
): Unit
```

Write a byte\[\] value for the given fieldId.

If the field is not a bytes or object field, an exception will be thrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:The value. This value may be`null`. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: Double
): Unit
```

Write a value for the given fieldId.

Will automatically convert for the following field types, and throw an exception for others: double, float, int32, int64, uint32, uint64, sint32, sint64, fixed32, fixed64, sfixed32, sfixed64, bool, enum.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The value. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: Float
): Unit
```

Write a value for the given fieldId.

Will automatically convert for the following field types, and throw an exception for others: double, float, int32, int64, uint32, uint64, sint32, sint64, fixed32, fixed64, sfixed32, sfixed64, bool, enum.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: Int
): Unit
```

Write a value for the given fieldId.

Will automatically convert for the following field types, and throw an exception for others: double, float, int32, int64, uint32, uint64, sint32, sint64, fixed32, fixed64, sfixed32, sfixed64, bool, enum.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: String?
): Unit
```

Write a string value for the given fieldId.

If the field is not a string field, an exception will be thrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The value. This value may be`null`. |

### write

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(
    fieldId: Long, 
    val: Long
): Unit
```

Write a value for the given fieldId.

Will automatically convert for the following field types, and throw an exception for others: double, float, int32, int64, uint32, uint64, sint32, sint64, fixed32, fixed64, sfixed32, sfixed64, bool, enum.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fieldId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The field identifier constant from the generated class. |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The value. |

### writeTag

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeTag(
    id: Int, 
    wireType: Int
): Unit
```

Write an individual field tag by hand. See [Protobuf Encoding](https://developers.google.com/protocol-buffers/docs/encoding) for details on the structure of how tags and data are written.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wireType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is android.util.proto.ProtoStream.WIRE_TYPE_VARINT, android.util.proto.ProtoStream.WIRE_TYPE_FIXED64, android.util.proto.ProtoStream.WIRE_TYPE_LENGTH_DELIMITED, android.util.proto.ProtoStream.WIRE_TYPE_START_GROUP, android.util.proto.ProtoStream.WIRE_TYPE_END_GROUP, or android.util.proto.ProtoStream.WIRE_TYPE_FIXED32 |
