# ObjectOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectOutputStream

```
open class ObjectOutputStream : OutputStream, ObjectOutput, ObjectStreamConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) ||
| | ↳ | [java.io.ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#) |

An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. The objects can be read (reconstituted) using an ObjectInputStream. Persistent storage of objects can be accomplished by using a file for the stream. If the stream is a network socket stream, the objects can be reconstituted on another host or in another process.

Only objects that support the java.io.Serializable interface can be written to streams. The class of each serializable object is encoded including the class name and signature of the class, the values of the object's fields and arrays, and the closure of any other objects referenced from the initial objects.

The method writeObject is used to write an object to the stream. Any object, including Strings and arrays, is written with writeObject. Multiple objects or primitives can be written to the stream. The objects must be read back from the corresponding ObjectInputstream with the same types and in the same order as they were written.

Primitive data types can also be written to the stream using the appropriate methods from DataOutput. Strings can also be written using the writeUTF method.

The default serialization mechanism for an object writes the class of the object, the class signature, and the values of all non-transient and non-static fields. References to other objects (except in transient or static fields) cause those objects to be written also. Multiple references to a single object are encoded using a reference sharing mechanism so that graphs of objects can be restored to the same shape as when the original was written.

For example to write an object that can be read by the example in ObjectInputStream: 

```kotlin
FileOutputStream fos = new FileOutputStream("t.tmp");
       ObjectOutputStream oos = new ObjectOutputStream(fos);
 
       oos.writeInt(12345);
       oos.writeObject("Today");
       oos.writeObject(new Date());
 
       oos.close();
  
```

Classes that require special handling during the serialization and deserialization process must implement special methods with these exact signatures: 

```kotlin
private void readObject(java.io.ObjectInputStream stream)
      throws IOException, ClassNotFoundException;
  private void writeObject(java.io.ObjectOutputStream stream)
      throws IOException
  private void readObjectNoData()
      throws ObjectStreamException;
  
```

The writeObject method is responsible for writing the state of the object for its particular class so that the corresponding readObject method can restore it. The method does not need to concern itself with the state belonging to the object's superclasses or subclasses. State is saved by writing the individual fields to the ObjectOutputStream using the writeObject method or by using the methods for primitive data types supported by DataOutput.

Serialization does not write out the fields of any object that does not implement the java.io.Serializable interface. Subclasses of Objects that are not serializable can be serializable. In this case the non-serializable class must have a no-arg constructor to allow its fields to be initialized. In this case it is the responsibility of the subclass to save and restore the state of the non-serializable class. It is frequently the case that the fields of that class are accessible (public, package, or protected) or that there are get and set methods that can be used to restore the state.

Serialization of an object can be prevented by implementing writeObject and readObject methods that throw the NotSerializableException. The exception will be caught by the ObjectOutputStream and abort the serialization process.

Implementing the Externalizable interface allows the object to assume complete control over the contents and format of the object's serialized form. The methods of the Externalizable interface, writeExternal and readExternal, are called to save and restore the objects state. When implemented by a class they can write and read their own state using all of the methods of ObjectOutput and ObjectInput. It is the responsibility of the objects to handle any versioning that occurs.

Enum constants are serialized differently than ordinary serializable or externalizable objects. The serialized form of an enum constant consists solely of its name; field values of the constant are not transmitted. To serialize an enum constant, ObjectOutputStream writes the string returned by the constant's name method. Like other serializable or externalizable objects, enum constants can function as the targets of back references appearing subsequently in the serialization stream. The process by which enum constants are serialized cannot be customized; any class-specific writeObject and writeReplace methods defined by enum types are ignored during serialization. Similarly, any serialPersistentFields or serialVersionUID field declarations are also ignored--all enum types have a fixed serialVersionUID of 0L.

Primitive data, excluding serializable fields and externalizable data, is written to the ObjectOutputStream in block-data records. A block data record is composed of a header and data. The block data header consists of a marker and the number of bytes to follow the header. Consecutive primitive data writes are merged into one block-data record. The blocking factor used for a block-data record will be 1024 bytes. Each block-data record will be filled up to 1024 bytes, or be written whenever there is a termination of block-data mode. Calls to the ObjectOutputStream methods writeObject, defaultWriteObject and writeFields initially terminate any existing block-data record.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [PutField](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream.PutField) Provide programmatic access to the persistent fields to be written to ObjectOutput. |

| Inherited constants ||
|---|---|
| From class [ObjectStreamConstants](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants) |--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_1](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_1:kotlin.Int) <br /> A Stream Protocol Version. All externalizable data is written in JDK 1.1 external data format after calling this method. This version is needed to write streams containing Externalizable data that can be read by pre-JDK 1.1.6 JVMs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_VERSION_2](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_2:kotlin.Int) <br /> A Stream Protocol Version. This protocol is written by JVM 1.2. Externalizable data is written in block data mode and is terminated with TC_ENDBLOCKDATA. Externalizable class descriptor flags has SC_BLOCK_DATA enabled. JVM 1.1.6 and greater can read this format change. Enables writing a nonSerializable class descriptor into the stream. The serialVersionUID of a nonSerializable class is set to 0L. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_BLOCK_DATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_BLOCK_DATA:kotlin.Byte) <br /> Bit mask for ObjectStreamClass flag. Indicates Externalizable data written in Block Data mode. Added for PROTOCOL_VERSION_2. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_ENUM](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_ENUM:kotlin.Byte) <br /> Bit mask for ObjectStreamClass flag. Indicates class is an enum type. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_EXTERNALIZABLE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_EXTERNALIZABLE:kotlin.Byte) <br /> Bit mask for ObjectStreamClass flag. Indicates class is Externalizable. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_SERIALIZABLE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_SERIALIZABLE:kotlin.Byte) <br /> Bit mask for ObjectStreamClass flag. Indicates class is Serializable. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SC_WRITE_METHOD](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_WRITE_METHOD:kotlin.Byte) <br /> Bit mask for ObjectStreamClass flag. Indicates a Serializable class defines its own writeObject method. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_MAGIC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_MAGIC:kotlin.Short) <br /> Magic number that is written to the stream header. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [STREAM_VERSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_VERSION:kotlin.Short) <br /> Version number that is written to the stream header. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ARRAY](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ARRAY:kotlin.Byte) <br /> new Array. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BASE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BASE:kotlin.Byte) <br /> First tag value. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATA:kotlin.Byte) <br /> Block of optional data. Byte following tag indicates number of bytes in this block data. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_BLOCKDATALONG](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATALONG:kotlin.Byte) <br /> long Block data. The long following the tag indicates the number of bytes in this block data. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASS](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASS:kotlin.Byte) <br /> Reference to Class. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_CLASSDESC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASSDESC:kotlin.Byte) <br /> new Class Descriptor. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENDBLOCKDATA](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENDBLOCKDATA:kotlin.Byte) <br /> End of optional block data blocks for an object. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_ENUM](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENUM:kotlin.Byte) <br /> new Enum constant. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_EXCEPTION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_EXCEPTION:kotlin.Byte) <br /> Exception during write. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_LONGSTRING](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_LONGSTRING:kotlin.Byte) <br /> Long string. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_MAX](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_MAX:kotlin.Byte) <br /> Last tag value. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_NULL](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_NULL:kotlin.Byte) <br /> Null object reference. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_OBJECT](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_OBJECT:kotlin.Byte) <br /> new Object. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_PROXYCLASSDESC](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_PROXYCLASSDESC:kotlin.Byte) <br /> new Proxy Class Descriptor. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_REFERENCE](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_REFERENCE:kotlin.Byte) <br /> Reference to an object already written into the stream. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_RESET](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_RESET:kotlin.Byte) <br /> Reset stream context. All handles written into stream are reset. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TC_STRING](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_STRING:kotlin.Byte) <br /> new String. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [baseWireHandle](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#baseWireHandle:kotlin.Int) <br /> First wire handle to be assigned. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#ObjectOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`)` Creates an ObjectOutputStream that writes to the specified OutputStream. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#ObjectOutputStream())`()` Provide a way for subclasses that are completely reimplementing ObjectOutputStream to not have to allocate private data just used by this implementation of ObjectOutputStream. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#close())`()` Closes the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [defaultWriteObject](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#defaultWriteObject())`()` Write the non-static and non-transient fields of the current class to this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#flush())`()` Flushes the stream. |
| open [ObjectOutputStream.PutField](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream.PutField)! | [putFields](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#putFields())`()` Retrieve the object used to buffer persistent fields to be written to the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#reset())`()` Reset will disregard the state of any objects already written to the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [useProtocolVersion](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#useProtocolVersion(kotlin.Int))`(`version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify stream protocol version to use when writing the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#write(kotlin.ByteArray))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes an array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a sub array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#write(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBoolean](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeBoolean(kotlin.Boolean))`(`val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Writes a boolean. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeByte](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeByte(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an 8 bit byte. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeBytes(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes a String as a sequence of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeChar](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeChar(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a 16 bit char. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeChars](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeChars(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes a String as a sequence of chars. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDouble](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeDouble(kotlin.Double))`(`val:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Writes a 64 bit double. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeFields](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeFields())`()` Write the buffered fields to the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeFloat](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeFloat(kotlin.Float))`(`val:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Writes a 32 bit float. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeInt](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeInt(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a 32 bit int. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeLong](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeLong(kotlin.Long))`(`val:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes a 64 bit long. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeObject](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeObject(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Write the specified object to the ObjectOutputStream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeShort](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeShort(kotlin.Int))`(`val:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a 16 bit short. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeUTF](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeUTF(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Primitive data write of this String in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeUnshared](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeUnshared(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Writes an "unshared" object to the ObjectOutputStream. |

| Protected methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [annotateClass](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#annotateClass(java.lang.Class))`(`cl:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Subclasses may implement this method to allow class data to be stored in the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [annotateProxyClass](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#annotateProxyClass(java.lang.Class))`(`cl:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Subclasses may implement this method to store custom data in the stream along with descriptors for dynamic proxy classes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drain](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#drain())`()` Drain any buffered data in ObjectOutputStream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enableReplaceObject](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#enableReplaceObject(kotlin.Boolean))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable the stream to do replacement of objects in the stream. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [replaceObject](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#replaceObject(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` This method will allow trusted subclasses of ObjectOutputStream to substitute one object for another during serialization. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeClassDescriptor](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeClassDescriptor(java.io.ObjectStreamClass))`(`desc:` ` [ObjectStreamClass](https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass)!`)` Write the specified class descriptor to the ObjectOutputStream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeObjectOverride](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeObjectOverride(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Method used by subclasses to override the default writeObject method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeStreamHeader](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeStreamHeader())`()` The writeStreamHeader method is provided so subclasses can append or prepend their own header to the stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Inherited properties ||
|---|---|
| From class [ObjectStreamConstants](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants) |----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission)! | [SUBCLASS_IMPLEMENTATION_PERMISSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBCLASS_IMPLEMENTATION_PERMISSION:java.io.SerializablePermission) <br /> Enable overriding of readObject and writeObject. <br /> | | [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission)! | [SUBSTITUTION_PERMISSION](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBSTITUTION_PERMISSION:java.io.SerializablePermission) <br /> Enable substitution of one object for another during serialization/deserialization. <br /> | ||

## Public constructors

### ObjectOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ObjectOutputStream(out: OutputStream!)
```

Creates an ObjectOutputStream that writes to the specified OutputStream. This constructor writes the serialization stream header to the underlying stream; callers may wish to flush the stream immediately to ensure that constructors for receiving ObjectInputStreams will not block when reading the header.

If a security manager is installed, this constructor will check for the "enableSubclassImplementation" SerializablePermission when invoked directly or indirectly by the constructor of a subclass which overrides the ObjectOutputStream.putFields or ObjectOutputStream.writeUnshared methods.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!:output stream to write to |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while writing stream header |
| `java.lang.SecurityException` | if untrusted subclass illegally overrides security-sensitive methods |
| `java.lang.NullPointerException` | if`out`is`null` |

**See Also**

- [java.io.ObjectOutputStream#ObjectOutputStream()](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#ObjectOutputStream())
- [java.io.ObjectOutputStream#putFields()](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#putFields())
- [java.io.ObjectInputStream#ObjectInputStream(InputStream)](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#ObjectInputStream(java.io.InputStream))

## Protected constructors

### ObjectOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ObjectOutputStream()
```

Provide a way for subclasses that are completely reimplementing ObjectOutputStream to not have to allocate private data just used by this implementation of ObjectOutputStream.

If there is a security manager installed, this method first calls the security manager's`checkPermission`method with a`SerializablePermission("enableSubclassImplementation")`permission to ensure it's ok to enable subclassing.

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies enabling subclassing. |
| `java.io.IOException` | if an I/O error occurs while creating this stream |

**See Also**

- [java.io.SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission)

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the stream. This method must be called to release any resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error has occurred. |

### defaultWriteObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun defaultWriteObject(): Unit
```

Write the non-static and non-transient fields of the current class to this stream. This may only be called from the writeObject method of the class being serialized. It will throw the NotActiveException if it is called otherwise.

| Exceptions ||
|-----------------------|-------------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying`OutputStream` |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes the stream. This will write any buffered output bytes and flush through to the underlying stream.

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### putFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putFields(): ObjectOutputStream.PutField!
```

Retrieve the object used to buffer persistent fields to be written to the stream. The fields will be written to the stream when writeFields method is called.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ObjectOutputStream.PutField](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream.PutField)! | an instance of the class Putfield that holds the serializable fields |

| Exceptions ||
|-----------------------|---------------------|
| `java.io.IOException` | if I/O errors occur |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset will disregard the state of any objects already written to the stream. The state is reset to be the same as a new ObjectOutputStream. The current point in the stream is marked as reset so the corresponding ObjectInputStream will be reset at the same point. Objects previously written to the stream will not be referred to as already being in the stream. They will be written to the stream again.

| Exceptions ||
|-----------------------|----------------------------------------------------|
| `java.io.IOException` | if reset() is invoked while serializing an object. |

### useProtocolVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun useProtocolVersion(version: Int): Unit
```

Specify stream protocol version to use when writing the stream.

This routine provides a hook to enable the current version of Serialization to write in a format that is backwards compatible to a previous version of the stream format.

Every effort will be made to avoid introducing additional backwards incompatibilities; however, sometimes there is no other alternative.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):use ProtocolVersion from java.io.ObjectStreamConstants. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalStateException` | if called after any objects have been serialized. |
| `java.lang.IllegalArgumentException` | if invalid version is passed in. |
| `java.io.IOException` | if I/O errors occur |

**See Also**

- [java.io.ObjectStreamConstants#PROTOCOL_VERSION_1](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_1:kotlin.Int)
- [java.io.ObjectStreamConstants#PROTOCOL_VERSION_2](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_2:kotlin.Int) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(buf: ByteArray!): Unit
```

Writes an array of bytes. This method will block until the bytes are actually written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | the data to be written |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes a sub array of bytes.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | the data to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes that are written |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(val: Int): Unit
```

Writes a byte. This method will block until the byte is actually written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | the byte |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written to the stream |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### writeBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeBoolean(val: Boolean): Unit
```

Writes a boolean.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `v` | the boolean to be written. |
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the boolean to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeByte(val: Int): Unit
```

Writes an 8 bit byte.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `v` | the byte value to be written. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeBytes(str: String!): Unit
```

Writes a String as a sequence of bytes.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `s` | the string of bytes to be written. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String of bytes to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeChar(val: Int): Unit
```

Writes a 16 bit char.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `v` | the`char`value to be written. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the char value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeChars(str: String!): Unit
```

Writes a String as a sequence of chars.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `s` | the string value to be written. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String of chars to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeDouble(val: Double): Unit
```

Writes a 64 bit double.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `v` | the`double`value to be written. |
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the double value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeFields(): Unit
```

Write the buffered fields to the stream.

| Exceptions ||
|------------------------------|-------------------------------------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |
| `java.io.NotActiveException` | Called when a classes writeObject method was not called to write the state of the object. |

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeFloat(val: Float): Unit
```

Writes a 32 bit float.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `v` | the`float`value to be written. |
| `val` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the float value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeInt(val: Int): Unit
```

Writes a 32 bit int.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------|
| `v` | the`int`value to be written. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeLong(val: Long): Unit
```

Writes a 64 bit long.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `v` | the`long`value to be written. |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the long value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeObject(obj: Any!): Unit
```

Write the specified object to the ObjectOutputStream. The class of the object, the signature of the class, and the values of the non-transient and non-static fields of the class and all of its supertypes are written. Default serialization for a class can be overridden using the writeObject and the readObject methods. Objects referenced by this object are written transitively so that a complete equivalent graph of objects can be reconstructed by an ObjectInputStream.

Exceptions are thrown for problems with the OutputStream and for classes that should not be serialized. All exceptions are fatal to the OutputStream, which is left in an indeterminate state, and it is up to the caller to ignore or recover the stream state.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to be written |

| Exceptions ||
|------------------------------------|-------------------------------------------------------------------------------------|
| `java.io.InvalidClassException` | Something is wrong with a class used by serialization. |
| `java.io.NotSerializableException` | Some object to be serialized does not implement the java.io.Serializable interface. |
| `java.io.IOException` | Any exception thrown by the underlying OutputStream. |

### writeShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeShort(val: Int): Unit
```

Writes a 16 bit short.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `v` | the`short`value to be written. |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the short value to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeUTF(str: String!): Unit
```

Primitive data write of this String in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format. Note that there is a significant difference between writing a String into the stream as primitive data or as an Object. A String instance written by writeObject is written into the stream as a String initially. Future writeObject() calls write references to the string into the stream.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------|
| `s` | the string value to be written. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String to be written |

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### writeUnshared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeUnshared(obj: Any!): Unit
```

Writes an "unshared" object to the ObjectOutputStream. This method is identical to writeObject, except that it always writes the given object as a new, unique object in the stream (as opposed to a back-reference pointing to a previously serialized instance). Specifically:

- An object written via writeUnshared is always serialized in the same manner as a newly appearing object (an object that has not been written to the stream yet), regardless of whether or not the object has been written previously.
- If writeObject is used to write an object that has been previously written with writeUnshared, the previous writeUnshared operation is treated as if it were a write of a separate object. In other words, ObjectOutputStream will never generate back-references to object data written by calls to writeUnshared.

While writing an object via writeUnshared does not in itself guarantee a unique reference to the object when it is deserialized, it allows a single object to be defined multiple times in a stream, so that multiple calls to readUnshared by the receiver will not conflict. Note that the rules described above only apply to the base-level object written with writeUnshared, and not to any transitively referenced sub-objects in the object graph to be serialized.

<br />

ObjectOutputStream subclasses which override this method can only be constructed in security contexts possessing the "enableSubclassImplementation" SerializablePermission; any attempt to instantiate such a subclass without this permission will cause a SecurityException to be thrown.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:object to write to stream |

| Exceptions ||
|------------------------------------|------------------------------------------------------------------------------------------|
| `java.io.NotSerializableException` | if an object in the graph to be serialized does not implement the Serializable interface |
| `java.io.InvalidClassException` | if a problem exists with the class of an object to be serialized |
| `java.io.IOException` | if an I/O error occurs during serialization |

## Protected methods

### annotateClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun annotateClass(cl: Class<*>!): Unit
```

Subclasses may implement this method to allow class data to be stored in the stream. By default this method does nothing. The corresponding method in ObjectInputStream is resolveClass. This method is called exactly once for each unique class in the stream. The class name and signature will have already been written to the stream. This method may make free use of the ObjectOutputStream to save any representation of the class it deems suitable (for example, the bytes of the class file). The resolveClass method in the corresponding subclass of ObjectInputStream must read and use any data or objects written by annotateClass.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `cl` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:the class to annotate custom data for |

| Exceptions ||
|-----------------------|------------------------------------------------------|
| `java.io.IOException` | Any exception thrown by the underlying OutputStream. |

### annotateProxyClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun annotateProxyClass(cl: Class<*>!): Unit
```

Subclasses may implement this method to store custom data in the stream along with descriptors for dynamic proxy classes.

This method is called exactly once for each unique proxy class descriptor in the stream. The default implementation of this method in`ObjectOutputStream`does nothing.

The corresponding method in`ObjectInputStream`is`resolveProxyClass`. For a given subclass of`ObjectOutputStream`that overrides this method, the`resolveProxyClass`method in the corresponding subclass of`ObjectInputStream`must read any data or objects written by`annotateProxyClass`.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------|
| `cl` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:the proxy class to annotate custom data for |

| Exceptions ||
|-----------------------|------------------------------------------------------|
| `java.io.IOException` | any exception thrown by the underlying`OutputStream` |

**See Also**

- [java.io.ObjectInputStream#resolveProxyClass(String[])](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#resolveProxyClass(kotlin.Array)) 

### drain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun drain(): Unit
```

Drain any buffered data in ObjectOutputStream. Similar to flush but does not propagate the flush to the underlying stream.

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |

### enableReplaceObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun enableReplaceObject(enable: Boolean): Boolean
```

Enable the stream to do replacement of objects in the stream. When enabled, the replaceObject method is called for every object being serialized.

If`enable`is true, and there is a security manager installed, this method first calls the security manager's`checkPermission`method with a`SerializablePermission("enableSubstitution")`permission to ensure it's ok to enable the stream to do replacement of objects in the stream.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):boolean parameter to enable replacement of objects |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the previous setting before this method was invoked |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies enabling the stream to do replacement of objects in the stream. |

**See Also**

- [java.io.SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission) 

### replaceObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun replaceObject(obj: Any!): Any!
```

This method will allow trusted subclasses of ObjectOutputStream to substitute one object for another during serialization. Replacing objects is disabled until enableReplaceObject is called. The enableReplaceObject method checks that the stream requesting to do replacement can be trusted. The first occurrence of each object written into the serialization stream is passed to replaceObject. Subsequent references to the object are replaced by the object returned by the original call to replaceObject. To ensure that the private state of objects is not unintentionally exposed, only trusted streams may use replaceObject.

The ObjectOutputStream.writeObject method takes a parameter of type Object (as opposed to type Serializable) to allow for cases where non-serializable objects are replaced by serializable ones.

When a subclass is replacing objects it must insure that either a complementary substitution must be made during deserialization or that the substituted object is compatible with every field where the reference will be stored. Objects whose type is not a subclass of the type of the field or array element abort the serialization by raising an exception and the object is not be stored.

This method is called only once when each object is first encountered. All subsequent references to the object will be redirected to the new object. This method should return the object to be substituted or the original object.

Null can be returned as the object to be substituted, but may cause NullReferenceException in classes that contain references to the original object since they may be expecting an object instead of null.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to be replaced |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the alternate object that replaced the specified one |

| Exceptions ||
|-----------------------|------------------------------------------------------|
| `java.io.IOException` | Any exception thrown by the underlying OutputStream. |

### writeClassDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun writeClassDescriptor(desc: ObjectStreamClass!): Unit
```

Write the specified class descriptor to the ObjectOutputStream. Class descriptors are used to identify the classes of objects written to the stream. Subclasses of ObjectOutputStream may override this method to customize the way in which class descriptors are written to the serialization stream. The corresponding method in ObjectInputStream,`readClassDescriptor`, should then be overridden to reconstitute the class descriptor from its custom stream representation. By default, this method writes class descriptors according to the format defined in the Object Serialization specification.

Note that this method will only be called if the ObjectOutputStream is not using the old serialization stream format (set by calling ObjectOutputStream's`useProtocolVersion`method). If this serialization stream is using the old format (`PROTOCOL_VERSION_1`), the class descriptor will be written internally in a manner that cannot be overridden or customized.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `desc` | [ObjectStreamClass](https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass)!:class descriptor to write to the stream |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

**See Also**

- [java.io.ObjectInputStream#readClassDescriptor()](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readClassDescriptor())
- [#useProtocolVersion(int)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#useProtocolVersion(kotlin.Int))
- [java.io.ObjectStreamConstants#PROTOCOL_VERSION_1](https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_1:kotlin.Int) 

### writeObjectOverride

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun writeObjectOverride(obj: Any!): Unit
```

Method used by subclasses to override the default writeObject method. This method is called by trusted subclasses of ObjectInputStream that constructed ObjectInputStream using the protected no-arg constructor. The subclass is expected to provide an override method with the modifier "final".

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:object to be written to the underlying stream |

| Exceptions ||
|-----------------------|----------------------------------------------------------------|
| `java.io.IOException` | if there are I/O errors while writing to the underlying stream |

**See Also**

- <https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#ObjectOutputStream()>
- [#writeObject(Object)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeObject(kotlin.Any)) 

### writeStreamHeader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun writeStreamHeader(): Unit
```

The writeStreamHeader method is provided so subclasses can append or prepend their own header to the stream. It writes the magic number and version to the stream.

| Exceptions ||
|-----------------------|------------------------------------------------------------|
| `java.io.IOException` | if I/O errors occur while writing to the underlying stream |
