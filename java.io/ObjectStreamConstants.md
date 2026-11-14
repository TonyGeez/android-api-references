# ObjectStreamConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamConstants

```
interface ObjectStreamConstants
```

| [java.io.ObjectStreamConstants](../java/io/ObjectStreamConstants.md) |

| Known Direct Subclasses [ObjectInputStream](../java/io/ObjectInputStream.md), [ObjectOutputStream](../java/io/ObjectOutputStream.md) |-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [ObjectInputStream](../java/io/ObjectInputStream.md) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. | | [ObjectOutputStream](../java/io/ObjectOutputStream.md) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Constants written into the Object Serialization Stream.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_1](../java/io/ObjectStreamConstants.md) A Stream Protocol Version. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_2](../java/io/ObjectStreamConstants.md) A Stream Protocol Version. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_BLOCK_DATA](../java/io/ObjectStreamConstants.md) Bit mask for ObjectStreamClass flag. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_ENUM](../java/io/ObjectStreamConstants.md) Bit mask for ObjectStreamClass flag. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_EXTERNALIZABLE](../java/io/ObjectStreamConstants.md) Bit mask for ObjectStreamClass flag. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_SERIALIZABLE](../java/io/ObjectStreamConstants.md) Bit mask for ObjectStreamClass flag. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_WRITE_METHOD](../java/io/ObjectStreamConstants.md) Bit mask for ObjectStreamClass flag. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_MAGIC](../java/io/ObjectStreamConstants.md) Magic number that is written to the stream header. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_VERSION](../java/io/ObjectStreamConstants.md) Version number that is written to the stream header. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ARRAY](../java/io/ObjectStreamConstants.md) new Array. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BASE](../java/io/ObjectStreamConstants.md) First tag value. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATA](../java/io/ObjectStreamConstants.md) Block of optional data. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATALONG](../java/io/ObjectStreamConstants.md) long Block data. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASS](../java/io/ObjectStreamConstants.md) Reference to Class. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASSDESC](../java/io/ObjectStreamConstants.md) new Class Descriptor. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENDBLOCKDATA](../java/io/ObjectStreamConstants.md) End of optional block data blocks for an object. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENUM](../java/io/ObjectStreamConstants.md) new Enum constant. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_EXCEPTION](../java/io/ObjectStreamConstants.md) Exception during write. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_LONGSTRING](../java/io/ObjectStreamConstants.md) Long string. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_MAX](../java/io/ObjectStreamConstants.md) Last tag value. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_NULL](../java/io/ObjectStreamConstants.md) Null object reference. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_OBJECT](../java/io/ObjectStreamConstants.md) new Object. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_PROXYCLASSDESC](../java/io/ObjectStreamConstants.md) new Proxy Class Descriptor. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_REFERENCE](../java/io/ObjectStreamConstants.md) Reference to an object already written into the stream. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_RESET](../java/io/ObjectStreamConstants.md) Reset stream context. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_STRING](../java/io/ObjectStreamConstants.md) new String. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [baseWireHandle](../java/io/ObjectStreamConstants.md) First wire handle to be assigned. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [SerializablePermission](../java/io/SerializablePermission.md)! | [SUBCLASS_IMPLEMENTATION_PERMISSION](../java/io/ObjectStreamConstants.md) Enable overriding of readObject and writeObject. |
| static [SerializablePermission](../java/io/SerializablePermission.md)! | [SUBSTITUTION_PERMISSION](../java/io/ObjectStreamConstants.md) Enable substitution of one object for another during serialization/deserialization. |

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

- [java.io.ObjectOutputStream#useProtocolVersion(int)](../java/io/ObjectOutputStream.md)) 

### PROTOCOL_VERSION_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_VERSION_2: Int
```

A Stream Protocol Version.

This protocol is written by JVM 1.2. Externalizable data is written in block data mode and is terminated with TC_ENDBLOCKDATA. Externalizable class descriptor flags has SC_BLOCK_DATA enabled. JVM 1.1.6 and greater can read this format change. Enables writing a nonSerializable class descriptor into the stream. The serialVersionUID of a nonSerializable class is set to 0L. 

 Value: 2

**See Also**

- [java.io.ObjectOutputStream#useProtocolVersion(int)](../java/io/ObjectOutputStream.md))
- [#SC_BLOCK_DATA](../java/io/ObjectStreamConstants.md) 

### SC_BLOCK_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SC_BLOCK_DATA: Byte
```

Bit mask for ObjectStreamClass flag. Indicates Externalizable data written in Block Data mode. Added for PROTOCOL_VERSION_2. 

 Value: 8

**See Also**

- [#PROTOCOL_VERSION_2](../java/io/ObjectStreamConstants.md) 

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

- [java.io.ObjectOutputStream#writeObjectOverride(Object)](../java/io/ObjectOutputStream.md))
- [java.io.ObjectInputStream#readObjectOverride()](../java/io/ObjectInputStream.md)) 

### SUBSTITUTION_PERMISSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSTITUTION_PERMISSION: SerializablePermission!
```

Enable substitution of one object for another during serialization/deserialization. 
**See Also**

- [java.io.ObjectOutputStream#enableReplaceObject(boolean)](../java/io/ObjectOutputStream.md))
- [java.io.ObjectInputStream#enableResolveObject(boolean)](../java/io/ObjectInputStream.md))
