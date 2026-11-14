Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectInputStream

```
open class ObjectInputStream : InputStream, ObjectInput, ObjectStreamConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) ||
| | ↳ | [java.io.ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#) |

An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream.

ObjectOutputStream and ObjectInputStream can provide an application with persistent storage for graphs of objects when used with a FileOutputStream and FileInputStream respectively. ObjectInputStream is used to recover those objects previously serialized. Other uses include passing objects between hosts using a socket stream or for marshaling and unmarshaling arguments and parameters in a remote communication system.

ObjectInputStream ensures that the types of all objects in the graph created from the stream match the classes present in the Java Virtual Machine. Classes are loaded as required using the standard mechanisms.

Only objects that support the java.io.Serializable or java.io.Externalizable interface can be read from streams.

The method `readObject` is used to read an object from the stream. Java's safe casting should be used to get the desired type. In Java, strings and arrays are objects and are treated as objects during serialization. When read they need to be cast to the expected type.

Primitive data types can be read from the stream using the appropriate method on DataInput.

The default deserialization mechanism for objects restores the contents of each field to the value and type it had when it was written. Fields declared as transient or static are ignored by the deserialization process. References to other objects cause those objects to be read from the stream as necessary. Graphs of objects are restored correctly using a reference sharing mechanism. New objects are always allocated when deserializing, which prevents existing objects from being overwritten.

Reading an object is analogous to running the constructors of a new object. Memory is allocated for the object and initialized to zero (NULL). No-arg constructors are invoked for the non-serializable classes and then the fields of the serializable classes are restored from the stream starting with the serializable class closest to java.lang.object and finishing with the object's most specific class.

For example to read from a stream as written by the example in ObjectOutputStream: 

```kotlin
FileInputStream fis = new FileInputStream("t.tmp");
       ObjectInputStream ois = new ObjectInputStream(fis);
 
       int i = ois.readInt();
       String today = (String) ois.readObject();
       Date date = (Date) ois.readObject();
 
       ois.close();
  
```

Classes control how they are serialized by implementing either the java.io.Serializable or java.io.Externalizable interfaces.

Implementing the Serializable interface allows object serialization to save and restore the entire state of the object and it allows classes to evolve between the time the stream is written and the time it is read. It automatically traverses references between objects, saving and restoring entire graphs.

Serializable classes that require special handling during the serialization and deserialization process should implement the following methods:

```kotlin
private void writeObject(java.io.ObjectOutputStream stream)
      throws IOException;
  private void readObject(java.io.ObjectInputStream stream)
      throws IOException, ClassNotFoundException;
  private void readObjectNoData()
      throws ObjectStreamException;
  
```

The readObject method is responsible for reading and restoring the state of the object for its particular class using data written to the stream by the corresponding writeObject method. The method does not need to concern itself with the state belonging to its superclasses or subclasses. State is restored by reading data from the ObjectInputStream for the individual fields and making assignments to the appropriate fields of the object. Reading primitive data types is supported by DataInput.

Any attempt to read object data which exceeds the boundaries of the custom data written by the corresponding writeObject method will cause an OptionalDataException to be thrown with an eof field value of true. Non-object reads which exceed the end of the allotted data will reflect the end of data in the same way that they would indicate the end of the stream: bytewise reads will return -1 as the byte read or number of bytes read, and primitive reads will throw EOFExceptions. If there is no corresponding writeObject method, then the end of default serialized data marks the end of the allotted data.

Primitive and object read calls issued from within a readExternal method behave in the same manner--if the stream is already positioned at the end of data written by the corresponding writeExternal method, object reads will throw OptionalDataExceptions with eof set to true, bytewise reads will return -1, and primitive reads will throw EOFExceptions. Note that this behavior does not hold for streams written with the old `ObjectStreamConstants.PROTOCOL_VERSION_1` protocol, in which the end of data written by writeExternal methods is not demarcated, and hence cannot be detected.

The readObjectNoData method is responsible for initializing the state of the object for its particular class in the event that the serialization stream does not list the given class as a superclass of the object being deserialized. This may occur in cases where the receiving party uses a different version of the deserialized instance's class than the sending party, and the receiver's version extends classes that are not extended by the sender's version. This may also occur if the serialization stream has been tampered; hence, readObjectNoData is useful for initializing deserialized objects properly despite a "hostile" or incomplete source stream.

Serialization does not read or assign values to the fields of any object that does not implement the java.io.Serializable interface. Subclasses of Objects that are not serializable can be serializable. In this case the non-serializable class must have a no-arg constructor to allow its fields to be initialized. In this case it is the responsibility of the subclass to save and restore the state of the non-serializable class. It is frequently the case that the fields of that class are accessible (public, package, or protected) or that there are get and set methods that can be used to restore the state.

Any exception that occurs while deserializing an object will be caught by the ObjectInputStream and abort the reading process.

Implementing the Externalizable interface allows the object to assume complete control over the contents and format of the object's serialized form. The methods of the Externalizable interface, writeExternal and readExternal, are called to save and restore the objects state. When implemented by a class they can write and read their own state using all of the methods of ObjectOutput and ObjectInput. It is the responsibility of the objects to handle any versioning that occurs.

Enum constants are deserialized differently than ordinary serializable or externalizable objects. The serialized form of an enum constant consists solely of its name; field values of the constant are not transmitted. To deserialize an enum constant, ObjectInputStream reads the constant name from the stream; the deserialized constant is then obtained by calling the static method `Enum.valueOf(Class, String)` with the enum constant's base type and the received constant name as arguments. Like other serializable or externalizable objects, enum constants can function as the targets of back references appearing subsequently in the serialization stream. The process by which enum constants are deserialized cannot be customized: any class-specific readObject, readObjectNoData, and readResolve methods defined by enum types are ignored during deserialization. Similarly, any serialPersistentFields or serialVersionUID field declarations are also ignored--all enum types have a fixed serialVersionUID of 0L.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream.GetField` Provide access to the persistent fields read from the input stream. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_1:kotlin.Int` A Stream Protocol Version. All externalizable data is written in JDK 1.1 external data format after calling this method. This version is needed to write streams containing Externalizable data that can be read by pre-JDK 1.1.6 JVMs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#PROTOCOL_VERSION_2:kotlin.Int` A Stream Protocol Version. This protocol is written by JVM 1.2. Externalizable data is written in block data mode and is terminated with TC_ENDBLOCKDATA. Externalizable class descriptor flags has SC_BLOCK_DATA enabled. JVM 1.1.6 and greater can read this format change. Enables writing a nonSerializable class descriptor into the stream. The serialVersionUID of a nonSerializable class is set to 0L. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_BLOCK_DATA:kotlin.Byte` Bit mask for ObjectStreamClass flag. Indicates Externalizable data written in Block Data mode. Added for PROTOCOL_VERSION_2. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_ENUM:kotlin.Byte` Bit mask for ObjectStreamClass flag. Indicates class is an enum type. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_EXTERNALIZABLE:kotlin.Byte` Bit mask for ObjectStreamClass flag. Indicates class is Externalizable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_SERIALIZABLE:kotlin.Byte` Bit mask for ObjectStreamClass flag. Indicates class is Serializable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SC_WRITE_METHOD:kotlin.Byte` Bit mask for ObjectStreamClass flag. Indicates a Serializable class defines its own writeObject method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_MAGIC:kotlin.Short` Magic number that is written to the stream header. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#STREAM_VERSION:kotlin.Short` Version number that is written to the stream header. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ARRAY:kotlin.Byte` new Array. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BASE:kotlin.Byte` First tag value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATA:kotlin.Byte` Block of optional data. Byte following tag indicates number of bytes in this block data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_BLOCKDATALONG:kotlin.Byte` long Block data. The long following the tag indicates the number of bytes in this block data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASS:kotlin.Byte` Reference to Class. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_CLASSDESC:kotlin.Byte` new Class Descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENDBLOCKDATA:kotlin.Byte` End of optional block data blocks for an object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_ENUM:kotlin.Byte` new Enum constant. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_EXCEPTION:kotlin.Byte` Exception during write. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_LONGSTRING:kotlin.Byte` Long string. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_MAX:kotlin.Byte` Last tag value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_NULL:kotlin.Byte` Null object reference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_OBJECT:kotlin.Byte` new Object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_PROXYCLASSDESC:kotlin.Byte` new Proxy Class Descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_REFERENCE:kotlin.Byte` Reference to an object already written into the stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_RESET:kotlin.Byte` Reset stream context. All handles written into stream are reset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#TC_STRING:kotlin.Byte` new String. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#baseWireHandle:kotlin.Int` First wire handle to be assigned. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#ObjectInputStream(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!)` Creates an ObjectInputStream that reads from the specified InputStream. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#ObjectInputStream()()` Provide a way for subclasses that are completely reimplementing ObjectInputStream to not have to allocate private data just used by this implementation of ObjectInputStream. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#available()()` Returns the number of bytes that can be read without blocking. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#close()()` Closes the input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#defaultReadObject()()` Read the non-static and non-transient fields of the current class from this stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#read()()` Reads a byte of data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(buf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads into an array of bytes. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readBoolean()()` Reads in a boolean. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readByte()()` Reads an 8 bit byte. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readChar()()` Reads a 16 bit char. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readDouble()()` Reads a 64 bit double. |
| open [ObjectInputStream.GetField](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream.GetField)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readFields()()` Reads the persistent fields from the stream and makes them available by name. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readFloat()()` Reads a 32 bit float. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readFully(kotlin.ByteArray)(buf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads bytes, blocking until all bytes are read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readFully(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(buf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads bytes, blocking until all bytes are read. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readInt()()` Reads a 32 bit int. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readLine()()` Reads in a line that has been terminated by a \\n, \\r, \\r\\n or EOF. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readLong()()` Reads a 64 bit long. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readObject()()` Read an object from the ObjectInputStream. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readShort()()` Reads a 16 bit short. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readUTF()()` Reads a String in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readUnshared()()` Reads an "unshared" object from the ObjectInputStream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readUnsignedByte()()` Reads an unsigned 8 bit byte. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readUnsignedShort()()` Reads an unsigned 16 bit short. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#registerValidation(java.io.ObjectInputValidation,%20kotlin.Int)(obj: https://developer.android.com/reference/kotlin/java/io/ObjectInputValidation!, prio: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Register an object to be validated before the graph is returned. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#skipBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Skips bytes. |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#enableResolveObject(kotlin.Boolean)(enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable the stream to allow objects read from the stream to be replaced. |
| open [ObjectStreamClass](https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readClassDescriptor()()` Read a class descriptor from the serialization stream. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readObjectOverride()()` This method is called by trusted subclasses of ObjectOutputStream that constructed ObjectOutputStream using the protected no-arg constructor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readStreamHeader()()` The readStreamHeader method is provided to allow subclasses to read and verify their own stream headers. |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#resolveClass(java.io.ObjectStreamClass)(desc: https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass!)` Load the local class equivalent of the specified stream class description. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#resolveObject(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` This method will allow trusted subclasses of ObjectInputStream to substitute one object for another during deserialization. |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>! | `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#resolveProxyClass(kotlin.Array)(interfaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Returns a proxy class that implements the interfaces named in a proxy class descriptor; subclasses may implement this method to read custom data from the stream along with the descriptors for dynamic proxy classes, allowing them to use an alternate loading mechanism for the interfaces and the proxy class. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/InputStream` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int)(readlimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the current position in this input stream. A subsequent call to the `reset` method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The `readlimit` arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated. The general contract of `mark` is that, if the method `markSupported` returns `true`, the stream somehow remembers all the bytes read after the call to `mark` and stands ready to supply those same bytes again if and whenever the method `reset` is called. However, the stream is not required to remember any data at all if more than `readlimit` bytes are read from the stream before `reset` is called. Marking a closed stream should not have any effect on the stream. The `mark` method of `InputStream` does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#markSupported()()` Tests if this input stream supports the `mark` and `reset` methods. Whether or not `mark` and `reset` are supported is an invariant property of a particular input stream instance. The `markSupported` method of `InputStream` returns `false`. <br /> | | `https://developer.android.com/reference/kotlin/java/io/InputStream!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream()()` Returns a new `InputStream` that reads no bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `available()`, `read()`, `read(byte[])`, `read(byte[], int, int)`, `readAllBytes()`, `readNBytes(byte[], int, int)`, `readNBytes(int)`, `skip(long)`, `skipNBytes(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` method does nothing, and the `reset()` method throws `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Reads some number of bytes from the input stream and stores them into the buffer array `b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown. If the length of `b` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at the end of the file, the value `-1` is returned; otherwise, at least one byte is read and stored into `b`. The first byte read is stored into element `b[0]`, the next one into `b[1]`, and so on. The number of bytes read is, at most, equal to the length of `b`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[0]` through `b[`*k* `-1]`, leaving elements `b[`*k* `]` through `b[b.length-1]` unaffected. The `read(b)` method for class `InputStream` has the same effect as: ```kotlin <code>read(b, 0, b.length) </code> ``` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes()()` Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads the requested number of bytes from the input stream into the given byte array. This method blocks until `len` bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before `len` bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If `len` is zero, then no bytes are read and `0` is returned; otherwise, there is an attempt to read up to `len` bytes. The first byte read is stored into element `b[off]`, the next one in to `b[off+1]`, and so on. The number of bytes read is, at most, equal to `len`. Let *k* be the number of bytes actually read; these bytes will be stored in elements `b[off]` through `b[off+`*k* `-1]`, leaving elements `b[off+`*k* `]` through `b[off+len-1]` unaffected. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of `b` have been updated with data from the input stream. Consequently the input stream and `b` may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int)(len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If `len` is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to `len` bytes are read from the stream. Fewer than `len` bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by `len`. Therefore, the method may be safely called with very large values of `len` provided sufficient memory is available. The behavior for the case where the input stream is *asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#reset()()` Repositions this stream to the position at the time the `mark` method was last called on this input stream. The general contract of `reset` is: - If the method `markSupported` returns `true`, then: - If the method `mark` has not been called since the stream was created, or the number of bytes read from the stream since `mark` was last called is larger than the argument to `mark` at that last call, then an `IOException` might be thrown. - If such an `IOException` is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to `mark` (or since the start of the file, if `mark` has not been called) will be resupplied to subsequent callers of the `read` method, followed by any bytes that otherwise would have been the next input data as of the time of the call to `reset`. - If the method `markSupported` returns `false`, then: - The call to `reset` may throw an `IOException`. - If an `IOException` is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the `read` method depend on the particular type of the input stream. The method `reset` for class `InputStream` does nothing except throw an `IOException`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards `n` bytes of data from this input stream. The `skip` method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly `0`. This may result from any of a number of conditions; reaching end of file before `n` bytes have been skipped is only one possibility. The actual number of bytes skipped is returned. If `n` is negative, the `skip` method for class `InputStream` always returns 0, and no bytes are skipped. Subclasses may handle the negative value differently. The `skip` method implementation of this class creates a byte array and then repeatedly reads into it until `n` bytes have been read or the end of the stream has been reached. Subclasses are encouraged to provide a more efficient implementation of this method. For instance, the implementation may depend on the ability to seek. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips over and discards exactly `n` bytes of data from this input stream. If `n` is zero, then no bytes are skipped. If `n` is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an `EOFException` is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream!)` Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is *asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants` |---|---| | `https://developer.android.com/reference/kotlin/java/io/SerializablePermission!` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBCLASS_IMPLEMENTATION_PERMISSION:java.io.SerializablePermission` Enable overriding of readObject and writeObject. <br /> | | `https://developer.android.com/reference/kotlin/java/io/SerializablePermission!` | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamConstants#SUBSTITUTION_PERMISSION:java.io.SerializablePermission` Enable substitution of one object for another during serialization/deserialization. <br /> | ||

## Public constructors

### ObjectInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ObjectInputStream(in: InputStream!)
```

Creates an ObjectInputStream that reads from the specified InputStream. A serialization stream header is read from the stream and verified. This constructor will block until the corresponding ObjectOutputStream has written and flushed the header.

If a security manager is installed, this constructor will check for the "enableSubclassImplementation" SerializablePermission when invoked directly or indirectly by the constructor of a subclass which overrides the ObjectInputStream.readFields or ObjectInputStream.readUnshared methods.

| Parameters ||
|---|---|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!: input stream to read from |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs while reading stream header |
| `java.io.StreamCorruptedException` | if the stream header is incorrect |
| `java.lang.NullPointerException` | if `in` is `null` |
| `java.lang.SecurityException` | if untrusted subclass illegally overrides security-sensitive methods |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#ObjectInputStream()`
- `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readFields()`
- `https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#ObjectOutputStream(java.io.OutputStream)`

## Protected constructors

### ObjectInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ObjectInputStream()
```

Provide a way for subclasses that are completely reimplementing ObjectInputStream to not have to allocate private data just used by this implementation of ObjectInputStream.

If there is a security manager installed, this method first calls the security manager's `checkPermission` method with the `SerializablePermission("enableSubclassImplementation")` permission to ensure it's ok to enable subclassing.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs while creating this stream |
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method denies enabling subclassing. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/SerializablePermission`

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun available(): Int
```

Returns the number of bytes that can be read without blocking.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of available bytes. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there are I/O errors while reading from the underlying `InputStream` |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes the input stream. Must be called to release any resources associated with the stream.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error has occurred. |

### defaultReadObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun defaultReadObject(): Unit
```

Read the non-static and non-transient fields of the current class from this stream. This may only be called from the readObject method of the class being deserialized. It will throw the NotActiveException if it is called otherwise.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.NotActiveException` | if the stream is not currently reading objects. |
| `java.lang.ClassNotFoundException` | if the class of a serialized object could not be found. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads a byte of data. This method will block if no input is available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the byte read, or -1 if the end of the stream is reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error has occurred. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads into an array of bytes. This method will block until some input is available. Consider using java.io.DataInputStream.readFully to read exactly 'length' bytes.

| Parameters ||
|---|---|
| `b` | the buffer into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes read |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of bytes read, -1 is returned when the end of the stream is reached. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error has occurred. |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, `len` is negative, or `len` is greater than `b.length - off` |
| `java.lang.NullPointerException` | If `b` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/DataInputStream#readFully(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`

### readBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readBoolean(): Boolean
```

Reads in a boolean.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the boolean read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readByte(): Byte
```

Reads an 8 bit byte.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the 8 bit byte read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readChar(): Char
```

Reads a 16 bit char.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the 16 bit char read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readDouble(): Double
```

Reads a 64 bit double.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the 64 bit double read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFields(): ObjectInputStream.GetField!
```

Reads the persistent fields from the stream and makes them available by name.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream.GetField!` | the `GetField` object representing the persistent fields of the object being deserialized |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.NotActiveException` | if the stream is not currently reading objects. |
| `java.lang.ClassNotFoundException` | if the class of a serialized object could not be found. |

### readFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFloat(): Float
```

Reads a 32 bit float.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the 32 bit float read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFully(buf: ByteArray!): Unit
```

Reads bytes, blocking until all bytes are read.

| Parameters ||
|---|---|
| `b` | the buffer into which the data is read. |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |
| `java.lang.NullPointerException` | if `b` is `null`. |

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFully(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Reads bytes, blocking until all bytes are read.

| Parameters ||
|---|---|
| `b` | the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes to read |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer into which the data is read |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |
| `java.lang.IndexOutOfBoundsException` | if `off` is negative, `len` is negative, or `len` is greater than `b.length - off`. |
| `java.lang.NullPointerException` | if `b` is `null`. |

### readInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readInt(): Int
```

Reads a 32 bit int.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the 32 bit integer read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readLine(): String!
```

**Deprecated:** *This method does not properly convert bytes to characters. see DataInputStream for the details and alternatives.*

Reads in a line that has been terminated by a \\n, \\r, \\r\\n or EOF.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a String copy of the line. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there are I/O errors while reading from the underlying `InputStream` |

### readLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readLong(): Long
```

Reads a 64 bit long.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the read 64 bit long. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readObject(): Any!
```

Read an object from the ObjectInputStream. The class of the object, the signature of the class, and the values of the non-transient and non-static fields of the class and all of its supertypes are read. Default deserializing for a class can be overridden using the writeObject and readObject methods. Objects referenced by this object are read transitively so that a complete equivalent graph of objects is reconstructed by readObject.

The root object is completely restored when all of its fields and the objects it references are completely restored. At this point the object validation callbacks are executed in order based on their registered priorities. The callbacks are registered by objects (in the readObject special methods) as they are individually restored.

Exceptions are thrown for problems with the InputStream and for classes that should not be deserialized. All exceptions are fatal to the InputStream and leave it in an indeterminate state; it is up to the caller to ignore or recover the stream state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the object read from the stream |

| Exceptions ||
|---|---|
| `java.io.IOException` | Any of the usual Input/Output related exceptions. |
| `java.lang.ClassNotFoundException` | Class of a serialized object cannot be found. |
| `java.io.InvalidClassException` | Something is wrong with a class used by serialization. |
| `java.io.OptionalDataException` | Primitive data was found in the stream instead of objects. |
| `java.io.StreamCorruptedException` | Control information in the stream is inconsistent. |

### readShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readShort(): Short
```

Reads a 16 bit short.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the 16 bit short read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readUTF(): String!
```

Reads a String in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the String. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | if this stream reaches the end before reading all the bytes. |
| `java.io.IOException` | if there are I/O errors while reading from the underlying `InputStream` |
| `java.io.UTFDataFormatException` | if read bytes do not represent a valid modified UTF-8 encoding of a string |

### readUnshared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readUnshared(): Any!
```

Reads an "unshared" object from the ObjectInputStream. This method is identical to readObject, except that it prevents subsequent calls to readObject and readUnshared from returning additional references to the deserialized instance obtained via this call. Specifically:

- If readUnshared is called to deserialize a back-reference (the stream representation of an object which has been written previously to the stream), an ObjectStreamException will be thrown.
- If readUnshared returns successfully, then any subsequent attempts to deserialize back-references to the stream handle deserialized by readUnshared will cause an ObjectStreamException to be thrown.

Deserializing an object via readUnshared invalidates the stream handle associated with the returned object. Note that this in itself does not always guarantee that the reference returned by readUnshared is unique; the deserialized object may define a readResolve method which returns an object visible to other parties, or readUnshared may return a Class object or enum constant obtainable elsewhere in the stream or through external means. If the deserialized object defines a readResolve method and the invocation of that method returns an array, then readUnshared returns a shallow clone of that array; this guarantees that the returned array object is unique and cannot be obtained a second time from an invocation of readObject or readUnshared on the ObjectInputStream, even if the underlying data stream has been manipulated.

<br />

ObjectInputStream subclasses which override this method can only be constructed in security contexts possessing the "enableSubclassImplementation" SerializablePermission; any attempt to instantiate such a subclass without this permission will cause a SecurityException to be thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | reference to deserialized object |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs during deserialization |
| `java.io.ObjectStreamException` | if object to deserialize has already appeared in stream |
| `java.io.OptionalDataException` | if primitive data is next in stream |
| `java.io.StreamCorruptedException` | if control information in the stream is inconsistent |
| `java.lang.ClassNotFoundException` | if class of an object to deserialize cannot be found |

### readUnsignedByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readUnsignedByte(): Int
```

Reads an unsigned 8 bit byte.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the 8 bit byte read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### readUnsignedShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readUnsignedShort(): Int
```

Reads an unsigned 16 bit short.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the 16 bit short read. |

| Exceptions ||
|---|---|
| `java.io.EOFException` | If end of file is reached. |
| `java.io.IOException` | If other I/O error has occurred. |

### registerValidation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerValidation(
    obj: ObjectInputValidation!, 
    prio: Int
): Unit
```

Register an object to be validated before the graph is returned. While similar to resolveObject these validations are called after the entire graph has been reconstituted. Typically, a readObject method will register the object with the stream so that when all of the objects are restored a final set of validations can be performed.

| Parameters ||
|---|---|
| `obj` | [ObjectInputValidation](https://developer.android.com/reference/kotlin/java/io/ObjectInputValidation)!: the object to receive the validation callback. |
| `prio` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): controls the order of callbacks;zero is a good default. Use higher numbers to be called back earlier, lower numbers for later callbacks. Within a priority, callbacks are processed in no particular order. |

| Exceptions ||
|---|---|
| `java.io.InvalidObjectException` | The validation object is null. |
| `java.io.NotActiveException` | The stream is not currently reading objects so it is invalid to register a callback. |

### skipBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skipBytes(len: Int): Int
```

Skips bytes.

| Parameters ||
|---|---|
| `n` | the number of bytes to be skipped. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to be skipped |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of bytes skipped. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error has occurred. |

## Protected methods

### enableResolveObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun enableResolveObject(enable: Boolean): Boolean
```

Enable the stream to allow objects read from the stream to be replaced. When enabled, the resolveObject method is called for every object being deserialized.

If *enable* is true, and there is a security manager installed, this method first calls the security manager's `checkPermission` method with the `SerializablePermission("enableSubstitution")` permission to ensure it's ok to enable the stream to allow objects read from the stream to be replaced.

| Parameters ||
|---|---|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true for enabling use of `resolveObject` for every object being deserialized |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the previous setting before this method was invoked |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method denies enabling the stream to allow objects read from the stream to be replaced. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/SerializablePermission`

### readClassDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun readClassDescriptor(): ObjectStreamClass!
```

Read a class descriptor from the serialization stream. This method is called when the ObjectInputStream expects a class descriptor as the next item in the serialization stream. Subclasses of ObjectInputStream may override this method to read in class descriptors that have been written in non-standard formats (by subclasses of ObjectOutputStream which have overridden the `writeClassDescriptor` method). By default, this method reads class descriptors according to the format defined in the Object Serialization specification.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass!` | the class descriptor read |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error has occurred. |
| `java.lang.ClassNotFoundException` | If the Class of a serialized object used in the class descriptor representation cannot be found |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#writeClassDescriptor(java.io.ObjectStreamClass)`

### readObjectOverride

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun readObjectOverride(): Any!
```

This method is called by trusted subclasses of ObjectOutputStream that constructed ObjectOutputStream using the protected no-arg constructor. The subclass is expected to provide an override method with the modifier "final".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the Object read from the stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if I/O errors occurred while reading from the underlying stream |
| `java.io.OptionalDataException` | Primitive data was found in the stream instead of objects. |
| `java.lang.ClassNotFoundException` | Class definition of a serialized object cannot be found. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#ObjectInputStream()`
- `https://developer.android.com/reference/kotlin/java/io/ObjectInputStream#readObject()`

### readStreamHeader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun readStreamHeader(): Unit
```

The readStreamHeader method is provided to allow subclasses to read and verify their own stream headers. It reads and verifies the magic number and version number.

| Exceptions ||
|---|---|
| `java.io.IOException` | if there are I/O errors while reading from the underlying `InputStream` |
| `java.io.StreamCorruptedException` | if control information in the stream is inconsistent |

### resolveClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun resolveClass(desc: ObjectStreamClass!): Class<*>!
```

Load the local class equivalent of the specified stream class description. Subclasses may implement this method to allow classes to be fetched from an alternate source.

The corresponding method in `ObjectOutputStream` is `annotateClass`. This method will be invoked only once for each unique class in the stream. This method can be implemented by subclasses to use an alternate loading mechanism but must return a `Class` object. Once returned, if the class is not an array class, its serialVersionUID is compared to the serialVersionUID of the serialized class, and if there is a mismatch, the deserialization fails and an `https://developer.android.com/reference/kotlin/java/io/InvalidClassException` is thrown.

The default implementation of this method in `ObjectInputStream` returns the result of calling

```kotlin
Class.forName(desc.getName(), false, loader)
  
```
where `loader` is determined as follows: if there is a method on the current thread's stack whose declaring class was defined by a user-defined class loader (and was not a generated to implement reflective invocations), then `loader` is class loader corresponding to the closest such method to the currently executing frame; otherwise, `loader` is `null`. If this call results in a `ClassNotFoundException` and the name of the passed `ObjectStreamClass` instance is the Java language keyword for a primitive type or void, then the `Class` object representing that primitive type or void will be returned (e.g., an `ObjectStreamClass` with the name `"int"` will be resolved to `Integer.TYPE`). Otherwise, the `ClassNotFoundException` will be thrown to the caller of this method.

| Parameters ||
|---|---|
| `desc` | [ObjectStreamClass](https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass)!: an instance of class `ObjectStreamClass` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!` | a `Class` object corresponding to `desc` |

| Exceptions ||
|---|---|
| `java.io.IOException` | any of the usual Input/Output exceptions. |
| `java.lang.ClassNotFoundException` | if class of a serialized object cannot be found. |

### resolveObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun resolveObject(obj: Any!): Any!
```

This method will allow trusted subclasses of ObjectInputStream to substitute one object for another during deserialization. Replacing objects is disabled until enableResolveObject is called. The enableResolveObject method checks that the stream requesting to resolve object can be trusted. Every reference to serializable objects is passed to resolveObject. To insure that the private state of objects is not unintentionally exposed only trusted streams may use resolveObject.

This method is called after an object has been read but before it is returned from readObject. The default resolveObject method just returns the same object.

When a subclass is replacing objects it must insure that the substituted object is compatible with every field where the reference will be stored. Objects whose type is not a subclass of the type of the field or array element abort the serialization by raising an exception and the object is not be stored.

This method is called only once when each object is first encountered. All subsequent references to the object will be redirected to the new object.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: object to be substituted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the substituted object |

| Exceptions ||
|---|---|
| `java.io.IOException` | Any of the usual Input/Output exceptions. |

### resolveProxyClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun resolveProxyClass(interfaces: Array<String!>!): Class<*>!
```

Returns a proxy class that implements the interfaces named in a proxy class descriptor; subclasses may implement this method to read custom data from the stream along with the descriptors for dynamic proxy classes, allowing them to use an alternate loading mechanism for the interfaces and the proxy class.

This method is called exactly once for each unique proxy class descriptor in the stream.

The corresponding method in `ObjectOutputStream` is `annotateProxyClass`. For a given subclass of `ObjectInputStream` that overrides this method, the `annotateProxyClass` method in the corresponding subclass of `ObjectOutputStream` must write any data or objects read by this method.

The default implementation of this method in `ObjectInputStream` returns the result of calling `Proxy.getProxyClass` with the list of `Class` objects for the interfaces that are named in the `interfaces` parameter. The `Class` object for each interface name `i` is the value returned by calling

```kotlin
Class.forName(i, false, loader)
  
```
where `loader` is that of the first non-`null` class loader up the execution stack, or `null` if no non-`null` class loaders are on the stack (the same class loader choice used by the `resolveClass` method). Unless any of the resolved interfaces are non-public, this same value of `loader` is also the class loader passed to `Proxy.getProxyClass`; if non-public interfaces are present, their class loader is passed instead (if more than one non-public interface class loader is encountered, an `IllegalAccessError` is thrown). If `Proxy.getProxyClass` throws an `IllegalArgumentException`, `resolveProxyClass` will throw a `ClassNotFoundException` containing the `IllegalArgumentException`.

| Parameters ||
|---|---|
| `interfaces` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the list of interface names that were deserialized in the proxy class descriptor |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!` | a proxy class for the specified interfaces |

| Exceptions ||
|---|---|
| `java.io.IOException` | any exception thrown by the underlying `InputStream` |
| `java.lang.ClassNotFoundException` | if the proxy class or any of the named interfaces could not be found |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream#annotateProxyClass(java.lang.Class)`
