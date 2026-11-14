# ObjectStreamConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamConstants

```
interface ObjectStreamConstants
```

| [java.io.ObjectStreamConstants](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#) |

| Known Direct Subclasses [ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream), [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) |-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. | | [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Constants written into the Object Serialization Stream.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_1](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_1:kotlin.Int) A Stream Protocol Version. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_2](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_2:kotlin.Int) A Stream Protocol Version. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_BLOCK_DATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_BLOCK_DATA:kotlin.Byte) Bit mask for ObjectStreamClass flag. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_ENUM](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_ENUM:kotlin.Byte) Bit mask for ObjectStreamClass flag. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_EXTERNALIZABLE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_EXTERNALIZABLE:kotlin.Byte) Bit mask for ObjectStreamClass flag. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_SERIALIZABLE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_SERIALIZABLE:kotlin.Byte) Bit mask for ObjectStreamClass flag. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_WRITE_METHOD](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_WRITE_METHOD:kotlin.Byte) Bit mask for ObjectStreamClass flag. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_MAGIC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_MAGIC:kotlin.Short) Magic number that is written to the stream header. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_VERSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_VERSION:kotlin.Short) Version number that is written to the stream header. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ARRAY](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ARRAY:kotlin.Byte) new Array. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BASE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BASE:kotlin.Byte) First tag value. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATA:kotlin.Byte) Block of optional data. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATALONG](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATALONG:kotlin.Byte) long Block data. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASS](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASS:kotlin.Byte) Reference to Class. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASSDESC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASSDESC:kotlin.Byte) new Class Descriptor. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENDBLOCKDATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENDBLOCKDATA:kotlin.Byte) End of optional block data blocks for an object. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENUM](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENUM:kotlin.Byte) new Enum constant. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_EXCEPTION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_EXCEPTION:kotlin.Byte) Exception during write. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_LONGSTRING](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_LONGSTRING:kotlin.Byte) Long string. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_MAX](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_MAX:kotlin.Byte) Last tag value. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_NULL](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_NULL:kotlin.Byte) Null object reference. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_OBJECT](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_OBJECT:kotlin.Byte) new Object. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_PROXYCLASSDESC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_PROXYCLASSDESC:kotlin.Byte) new Proxy Class Descriptor. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_REFERENCE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_REFERENCE:kotlin.Byte) Reference to an object already written into the stream. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_RESET](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_RESET:kotlin.Byte) Reset stream context. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_STRING](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_STRING:kotlin.Byte) new String. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [baseWireHandle](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#baseWireHandle:kotlin.Int) First wire handle to be assigned. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission)! | [SUBCLASS_IMPLEMENTATION_PERMISSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBCLASS_IMPLEMENTATION_PERMISSION:java.io.SerializablePermission) Enable overriding of readObject and writeObject. |
| static [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission)! | [SUBSTITUTION_PERMISSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBSTITUTION_PERMISSION:java.io.SerializablePermission) Enable substitution of one object for another during serialization/deserialization. |

## Constants

### PROTOCOL_VERSION_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_VERSION_1: Int
```

A Stream Protocol Version.

All externalizable data is written in JDK 1.1 external data format after calling this method. This version is needed to write streams containing Externalizable data that can be read by pre-JDK 1.1.6 JVMs. 

 Value: 1

**See Also**

- [java.io.ObjectOutputStream#useProtocolVersion(int)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#useProtocolVersion(kotlin.Int)) 

### PROTOCOL_VERSION_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_VERSION_2: Int
```

A Stream Protocol Version.

This protocol is written by JVM 1.2. Externalizable data is written in block data mode and is terminated with TC_ENDBLOCKDATA. Externalizable class descriptor flags has SC_BLOCK_DATA enabled. JVM 1.1.6 and greater can read this format change. Enables writing a nonSerializable class descriptor into the stream. The serialVersionUID of a nonSerializable class is set to 0L. 

 Value: 2

**See Also**

- [java.io.ObjectOutputStream#useProtocolVersion(int)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#useProtocolVersion(kotlin.Int))
- [#SC_BLOCK_DATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_BLOCK_DATA:kotlin.Byte) 

### SC_BLOCK_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_BLOCK_DATA: Byte
```

Bit mask for ObjectStreamClass flag. Indicates Externalizable data written in Block Data mode. Added for PROTOCOL_VERSION_2. 

 Value: 8

**See Also**

- [#PROTOCOL_VERSION_2](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_2:kotlin.Int) 

### SC_ENUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_ENUM: Byte
```

Bit mask for ObjectStreamClass flag. Indicates class is an enum type. 

 Value: 16

### SC_EXTERNALIZABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_EXTERNALIZABLE: Byte
```

Bit mask for ObjectStreamClass flag. Indicates class is Externalizable. 

 Value: 4

### SC_SERIALIZABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_SERIALIZABLE: Byte
```

Bit mask for ObjectStreamClass flag. Indicates class is Serializable. 

 Value: 2

### SC_WRITE_METHOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_WRITE_METHOD: Byte
```

Bit mask for ObjectStreamClass flag. Indicates a Serializable class defines its own writeObject method. 

 Value: 1

### STREAM_MAGIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_MAGIC: Short
```

Magic number that is written to the stream header. 

 Value: -21267

### STREAM_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_VERSION: Short
```

Version number that is written to the stream header. 

 Value: 5

### TC_ARRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_ARRAY: Byte
```

new Array. 

 Value: 117

### TC_BASE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_BASE: Byte
```

First tag value. 

 Value: 112

### TC_BLOCKDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_BLOCKDATA: Byte
```

Block of optional data. Byte following tag indicates number of bytes in this block data. 

 Value: 119

### TC_BLOCKDATALONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_BLOCKDATALONG: Byte
```

long Block data. The long following the tag indicates the number of bytes in this block data. 

 Value: 122

### TC_CLASS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_CLASS: Byte
```

Reference to Class. 

 Value: 118

### TC_CLASSDESC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_CLASSDESC: Byte
```

new Class Descriptor. 

 Value: 114

### TC_ENDBLOCKDATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_ENDBLOCKDATA: Byte
```

End of optional block data blocks for an object. 

 Value: 120

### TC_ENUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_ENUM: Byte
```

new Enum constant. 

 Value: 126

### TC_EXCEPTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_EXCEPTION: Byte
```

Exception during write. 

 Value: 123

### TC_LONGSTRING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_LONGSTRING: Byte
```

Long string. 

 Value: 124

### TC_MAX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_MAX: Byte
```

Last tag value. 

 Value: 126

### TC_NULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_NULL: Byte
```

Null object reference. 

 Value: 112

### TC_OBJECT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_OBJECT: Byte
```

new Object. 

 Value: 115

### TC_PROXYCLASSDESC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_PROXYCLASSDESC: Byte
```

new Proxy Class Descriptor. 

 Value: 125

### TC_REFERENCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_REFERENCE: Byte
```

Reference to an object already written into the stream. 

 Value: 113

### TC_RESET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_RESET: Byte
```

Reset stream context. All handles written into stream are reset. 

 Value: 121

### TC_STRING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TC_STRING: Byte
```

new String. 

 Value: 116

### baseWireHandle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val baseWireHandle: Int
```

First wire handle to be assigned. 

 Value: 8257536

## Properties

### SUBCLASS_IMPLEMENTATION_PERMISSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS_IMPLEMENTATION_PERMISSION: SerializablePermission!
```

Enable overriding of readObject and writeObject. 
**See Also**

- [java.io.ObjectOutputStream#writeObjectOverride(Object)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeObjectOverride(kotlin.Any))
- [java.io.ObjectInputStream#readObjectOverride()](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readObjectOverride()) 

### SUBSTITUTION_PERMISSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSTITUTION_PERMISSION: SerializablePermission!
```

Enable substitution of one object for another during serialization/deserialization. 
**See Also**

- [java.io.ObjectOutputStream#enableReplaceObject(boolean)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#enableReplaceObject(kotlin.Boolean))
- [java.io.ObjectInputStream#enableResolveObject(boolean)](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#enableResolveObject(kotlin.Boolean))
