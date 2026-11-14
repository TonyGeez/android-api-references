Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Parcel

Kotlin | [Java](Parcel.md)
| --- | --- |

```
class Parcel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Parcel](Parcel.md) |

Container for a message (data and object references) that can be sent through an IBinder. A Parcel can contain both flattened data that will be unflattened on the other side of the IPC (using the various methods here for writing specific types, or the general Parcelable interface), and references to live IBinder objects that will result in the other side receiving a proxy IBinder connected with the original IBinder in the Parcel.

Parcel is **not** a general-purpose serialization mechanism. This class (and the corresponding Parcelable API for placing arbitrary objects into a Parcel) is designed as a high-performance IPC transport. As such, it is not appropriate to place any Parcel data in to persistent storage: changes in the underlying implementation of any of the data in the Parcel can render older data unreadable.

The bulk of the Parcel API revolves around reading and writing data of various types. There are six major classes of such functions available.

### Primitives

The most basic data functions are for writing and reading primitive data types: writeByte, readByte, writeDouble, readDouble, writeFloat, readFloat, writeInt, readInt, writeLong, readLong, writeString, readString. Most other data operations are built on top of these. The given data is written and read using the endianess of the host CPU.

### Primitive Arrays

There are a variety of methods for reading and writing raw arrays of primitive objects, which generally result in writing a 4-byte length followed by the primitive data items. The methods for reading can either read the data into an existing array, or create and return a new array. These available types are:

- writeBooleanArray, readBooleanArray, createBooleanArray
- writeByteArray, writeByteArray, readByteArray, createByteArray
- writeCharArray, readCharArray, createCharArray
- writeDoubleArray, readDoubleArray, createDoubleArray
- writeFloatArray, readFloatArray, createFloatArray
- writeIntArray, readIntArray, createIntArray
- writeLongArray, readLongArray, createLongArray
- writeStringArray, readStringArray, createStringArray.
- writeSparseBooleanArray, readSparseBooleanArray.

### Parcelables

The Parcelable protocol provides an extremely efficient (but low-level) protocol for objects to write and read themselves from Parcels. You can use the direct methods writeParcelable and readParcelable or writeParcelableArray and readParcelableArray to write or read. These methods write both the class type and its data to the Parcel, allowing that class to be reconstructed from the appropriate class loader when later reading.

There are also some methods that provide a more efficient way to work with Parcelables: writeTypedObject, writeTypedArray, #writeTypedList, readTypedObject, createTypedArray and createTypedArrayList. These methods do not write the class information of the original object: instead, the caller of the read function must know what type to expect and pass in the appropriate `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` instead to properly construct the new object and read its data. (To more efficient write and read a single Parcelable object that is not null, you can directly call writeToParcel and createFromParcel yourself.)

### Bundles

A special type-safe container, called Bundle, is available for key/value maps of heterogeneous values. This has many optimizations for improved performance when reading and writing data, and its type-safe API avoids difficult to debug type errors when finally marshalling the data contents into a Parcel. The methods to use are writeBundle, readBundle, and readBundle.

### Active Objects

An unusual feature of Parcel is the ability to read and write active objects. For these objects the actual contents of the object is not written, rather a special token referencing the object is written. When reading the object back from the Parcel, you do not get a new instance of the object, but rather a handle that operates on the exact same object that was originally written. There are two forms of active objects available.

Binder objects are a core facility of Android's general cross-process communication system. The IBinder interface describes an abstract protocol with a Binder object. Any such interface can be written in to a Parcel, and upon reading you will receive either the original object implementing that interface or a special proxy implementation that communicates calls back to the original object. The methods to use are writeStrongBinder, writeStrongInterface, readStrongBinder, writeBinderArray, readBinderArray, createBinderArray, #writeInterfaceArray(T\[\]), #readInterfaceArray(T\[\],java.util.function.Function), createInterfaceArray, writeBinderList, readBinderList, createBinderArrayList, writeInterfaceList, readInterfaceList, createInterfaceArrayList.

FileDescriptor objects, representing raw Linux file descriptor identifiers, can be written and ParcelFileDescriptor objects returned to operate on the original file descriptor. The returned file descriptor is a dup of the original file descriptor: the object and fd is different, but operating on the same underlying file stream, with the same position, etc. The methods to use are writeFileDescriptor, readFileDescriptor.

### Parcelable Containers

A final class of methods are for writing and reading standard Java containers of arbitrary types. These all revolve around the writeValue and readValue methods which define the types of objects allowed. The container methods are writeArray, readArray, writeList, readList, readArrayList, writeMap, readMap, writeSparseArray, readSparseArray.

### Restricted Parcelable Containers

A final class of methods are for reading standard Java containers of restricted types. These methods replace methods for reading containers of arbitrary types from previous section starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. The pairing writing methods are still the same from previous section. These methods accepts additional `clazz` parameters as the required types. The Restricted Parcelable container methods are readArray, readList, readArrayList, readMap, readSparseArray.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | appendFrom <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IBinder](IBinder.md)!\>? | createBinderArray <br /> |
| [ArrayList](../java.util/ArrayList.md)\< [IBinder](IBinder.md)!\>? | createBinderArrayList Read and return a new ArrayList containing IBinder objects from the parcel that was written with writeBinderList at the current dataPosition(). |
| --- | --- |
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)? | createBooleanArray <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | createByteArray Read and return a byte\[\] object from the parcel. |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)? | createCharArray <br /> |
| --- | --- |
| [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)? | createDoubleArray <br /> |
| T? | createFixedArray Read and return a new multi-dimensional array of typed parcelables from a parcel. |
| T? | createFixedArray Read and return a new multi-dimensional array from a parcel. |
| --- | --- |
| T? | createFixedArray Read and return a new multi-dimensional array of typed interfaces from a parcel. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)? | createFloatArray <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | createIntArray <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | createInterfaceArray Read and return a new array of T (IInterface) from the parcel. |
| [ArrayList](../java.util/ArrayList.md)\<T\>? | createInterfaceArrayList Read and return a new ArrayList containing T (IInterface) objects from the parcel that was written with writeInterfaceList at the current dataPosition(). |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | createLongArray <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | createStringArray <br /> |
| [ArrayList](../java.util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | createStringArrayList Read and return a new ArrayList containing String objects from the parcel that was written with writeStringList at the current dataPosition(). |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | createTypedArray Read and return a new array containing a particular object type from the parcel at the current dataPosition(). |
| --- | --- |
| [ArrayList](../java.util/ArrayList.md)\<T\>? | createTypedArrayList Read and return a new ArrayList containing a particular object type from the parcel that was written with #writeTypedList at the current dataPosition(). |
| [ArrayMap](../android.util/ArrayMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, T\>? | createTypedArrayMap Read into a new `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#` with string keys items containing a particular object type that were written with writeTypedArrayMap at the current dataPosition(). |
| [SparseArray](../android.util/SparseArray.md)\<T\>? | createTypedSparseArray Read into a new `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` items containing a particular object type that were written with writeTypedSparseArray at the current dataPosition(). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | dataAvail Returns the amount of data remaining to be read from the parcel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | dataCapacity Returns the total amount of space in the parcel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | dataPosition Returns the current position in the parcel data. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | dataSize Returns the total amount of data contained in the parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | enforceInterface Read the header written by writeInterfaceToken and verify it matches the interface name in question. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | enforceNoDataAvail Verify there are no bytes left to be read on the Parcel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFileDescriptors Report whether the parcel contains any marshalled file descriptors. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFileDescriptors Report whether the parcel contains any marshalled file descriptors in the range defined by `offset` and `length`. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | marshall Returns the raw bytes of the parcel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | marshall Writes the raw bytes of the parcel to a buffer. |
| static [Parcel](Parcel.md) | obtain Retrieve a new Parcel object from the pool. |
| static [Parcel](Parcel.md) | obtain Retrieve a new Parcel object from the pool for use with a specific binder. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>? | readArray Read and return a new Object array from the parcel at the current dataPosition(). |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | readArray Same as readArray but accepts `clazz` parameter as the type required for each item. |
| [ArrayList](../java.util/ArrayList.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>? | readArrayList Read and return a new ArrayList object from the parcel at the current dataPosition(). |
| --- | --- |
| [ArrayList](../java.util/ArrayList.md)\<T\>? | readArrayList Same as readArrayList but accepts `clazz` parameter as the type required for each item. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readBinderArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readBinderList Read into the given List items IBinder objects that were written with writeBinderList at the current dataPosition(). |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | readBlob Read a blob of data from the parcel and return it as a byte array. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | readBoolean Read a boolean value from the parcel at the current dataPosition(). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readBooleanArray <br /> |
| --- | --- |
| [Bundle](Bundle.md)? | readBundle Read and return a new Bundle object from the parcel at the current dataPosition(). |
| [Bundle](Bundle.md)? | readBundle Read and return a new Bundle object from the parcel at the current dataPosition(), using the given class loader to initialize the class loader of the Bundle for later retrieval of Parcelable objects. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | readByte Read a byte value from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readByteArray Read a byte\[\] object from the parcel and copy it into the given byte array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readCharArray <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | readDouble Read a double precision floating point value from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readDoubleArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readException Special function for reading an exception result from the header of a parcel, to be used after receiving the result of a transaction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readException Throw an exception with the given message. |
| --- | --- |
| [ParcelFileDescriptor](ParcelFileDescriptor.md)! | readFileDescriptor Read a FileDescriptor from the parcel at the current dataPosition(). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFixedArray Read a new multi-dimensional array from a parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFixedArray Read a new multi-dimensional array of typed parcelables from a parcel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFixedArray Read a new multi-dimensional array of typed interfaces from a parcel. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | readFloat Read a floating point value from the parcel at the current dataPosition(). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFloatArray <br /> |
| --- | --- |
| [HashMap](../java.util/HashMap.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>? | readHashMap Please use readBundle instead (whose data must have been written with writeBundle. |
| [HashMap](../java.util/HashMap.md)\<K, V\>? | readHashMap Same as readHashMap but accepts `clazzKey` and `clazzValue` parameter as the types required for each key and value pair. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | readInt Read an integer value from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readIntArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readInterfaceArray Read an array of T (IInterface) from a parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readInterfaceList Read into the given List items IInterface objects that were written with writeInterfaceList at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readList Read into an existing List object from the parcel at the current dataPosition(), using the given class loader to load any enclosed Parcelables. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readList Same as readList but accepts `clazz` parameter as the type required for each item. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | readLong Read a long integer value from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readLongArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readMap Please use readBundle instead (whose data must have been written with writeBundle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readMap Same as readMap but accepts `clazzKey` and `clazzValue` parameter as the types required for each key and value pair. |
| --- | --- |
| T? | readParcelable Read and return a new Parcelable from the parcel. |
| T? | readParcelable Same as readParcelable but accepts `clazz` parameter as the type required for each item. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Parcelable](Parcelable.md)!\>? | readParcelableArray Read and return a new Parcelable array from the parcel. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | readParcelableArray Same as readParcelableArray but accepts `clazz` parameter as the type required for each item. |
| [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<\*\>? | readParcelableCreator Read and return a Parcelable. |
| [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>? | readParcelableCreator Same as readParcelableCreator but accepts `clazz` parameter as the required type. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | readParcelableList Read the list of `Parcelable` objects at the current data position into the given `list`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | readParcelableList Same as readParcelableList but accepts `clazz` parameter as the type required for each item. |
| [PersistableBundle](PersistableBundle.md)? | readPersistableBundle Read and return a new Bundle object from the parcel at the current dataPosition(). |
| --- | --- |
| [PersistableBundle](PersistableBundle.md)? | readPersistableBundle Read and return a new Bundle object from the parcel at the current dataPosition(), using the given class loader to initialize the class loader of the Bundle for later retrieval of Parcelable objects. |
| [Serializable](../java.io/Serializable.md)? | readSerializable Read and return a new Serializable object from the parcel. |
| T? | readSerializable Same as readSerializable but accepts `loader` and `clazz` parameters. |
| --- | --- |
| [Size](../android.util/Size.md) | readSize Read a Size from the parcel at the current dataPosition(). |
| [SizeF](../android.util/SizeF.md) | readSizeF Read a SizeF from the parcel at the current dataPosition(). |
| [SparseArray](../android.util/SparseArray.md)\<T\>? | readSparseArray Read and return a new SparseArray object from the parcel at the current dataPosition(). |
| --- | --- |
| [SparseArray](../android.util/SparseArray.md)\<T\>? | readSparseArray Same as readSparseArray but accepts `clazz` parameter as the type required for each item. |
| [SparseBooleanArray](../android.util/SparseBooleanArray.md)? | readSparseBooleanArray Read and return a new SparseBooleanArray object from the parcel at the current dataPosition(). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | readString Read a string value from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readStringArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readStringList Read into the given List items String objects that were written with writeStringList at the current dataPosition(). |
| [IBinder](IBinder.md)! | readStrongBinder Read an object from the parcel at the current dataPosition(). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readTypedArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readTypedList Read into the given List items containing a particular object type that were written with #writeTypedList at the current dataPosition(). |
| T? | readTypedObject Read and return a typed Parcelable object from a parcel. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | readValue Read a typed object from a parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | recycle Put a Parcel object back into the pool. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDataCapacity Change the capacity (current available space) of the parcel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDataPosition Move the current read/write position in the parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDataSize Change the amount of data in the parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPropagateAllowBlocking This method is used by the AIDL compiler for system components. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unmarshall Fills the raw bytes of this Parcel with the supplied data. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unmarshall Fills the raw bytes of this Parcel with data from the supplied buffer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeArray Flatten an Object array into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBinderArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBinderList Flatten a List containing IBinder objects into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBlob Write a blob of data into the parcel at the current dataPosition, growing dataCapacity if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBlob Write a blob of data into the parcel at the current dataPosition, growing dataCapacity if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBoolean Write a boolean value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBooleanArray <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeBundle Flatten a Bundle into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeByte Write a byte value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeByteArray Write a byte array into the parcel at the current dataPosition, growing dataCapacity if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeByteArray Write a byte array into the parcel at the current dataPosition, growing dataCapacity if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeCharArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeDouble Write a double precision floating point value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeDoubleArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeException Special function for writing an exception result at the header of a parcel, to be used when returning an exception from a transaction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeFileDescriptor Write a FileDescriptor into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeFixedArray Flatten a homogeneous multi-dimensional array with fixed-size. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeFloat Write a floating point value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeFloatArray <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeInt Write an integer value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeIntArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeInterfaceArray Flatten a homogeneous array containing an IInterface type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeInterfaceList Flatten a `List` containing T (IInterface) objects into this parcel at the current position. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeInterfaceToken Store or read an IBinder interface token in the parcel at the current dataPosition. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeList Flatten a List into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeLong Write a long integer value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeLongArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeMap Please use writeBundle instead. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeNoException Special function for writing information at the front of the Parcel indicating that no exception occurred. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeParcelable Flatten the name of the class of the Parcelable and its contents into the parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeParcelableArray Write a heterogeneous array of Parcelable objects into the Parcel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeParcelableCreator Flatten the name of the class of the Parcelable into this Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeParcelableList Flatten a `List` containing arbitrary `Parcelable` objects into this parcel at the current position. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writePersistableBundle Flatten a PersistableBundle into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeSerializable Write a generic serializable object in to a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeSize Flatten a Size into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeSizeF Flatten a SizeF into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeSparseArray Flatten a generic SparseArray into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeSparseBooleanArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeString Write a string value into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeStringArray <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeStringList Flatten a List containing String objects into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeStrongBinder Write an object into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeStrongInterface Write an object into the parcel at the current dataPosition(), growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedArray Flatten a homogeneous array containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedArrayMap Flatten an `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#` with string keys containing a particular object type into the parcel at the current dataPosition() and growing dataCapacity() if needed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedList Flatten a List containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedList Flatten a List containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedObject Flatten the Parcelable object into the parcel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeTypedSparseArray Flatten a `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` containing a particular object type into the parcel at the current dataPosition() and growing dataCapacity() if needed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeValue Flatten a generic object in to a parcel. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/os/Parcel#STRING_CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### appendFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendFrom(
    parcel: Parcel!, 
    offset: Int, 
    length: Int
): Unit
```

### createBinderArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createBinderArray(): Array<IBinder!>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/IBinder!>?` | This value may be `null`. |

### createBinderArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createBinderArrayList(): ArrayList<IBinder!>?
```

Read and return a new ArrayList containing IBinder objects from the parcel that was written with writeBinderList at the current dataPosition(). Returns null if the previously written list object was null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/os/IBinder!>?` | A newly created ArrayList containing strings with the same data as those that were previously written. |

**See Also**

- writeBinderList

### createBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createBooleanArray(): BooleanArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?` | This value may be `null`. |

### createByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createByteArray(): ByteArray?
```

Read and return a byte\[\] object from the parcel.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### createCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createCharArray(): CharArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html?` | This value may be `null`. |

### createDoubleArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createDoubleArray(): DoubleArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?` | This value may be `null`. |

### createFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!, S : Parcelable!> createFixedArray(
    cls: Class<T>, 
    c: Parcelable.Creator<S>, 
    vararg dimensions: Int
): T?
```

Read and return a new multi-dimensional array of typed parcelables from a parcel. Returns null if the previously written array object is null. If you want to read IInterface values, use createFixedArray. For values of other types use createFixedArray.

| Parameters ||
|---|---|
| `cls` | [Class](../java.lang/Class.md)\<T\>: the Class object for the target array type. (e.g. Foo\[\]\[\].class). This value cannot be `null`. |
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<S\>: This value cannot be `null`. |
| `dimensions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an array of int representing length of each dimension. This value cannot be `null`. |
| --- | --- |

### createFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> createFixedArray(
    cls: Class<T>, 
    vararg dimensions: Int
): T?
```

Read and return a new multi-dimensional array from a parcel. Returns null if the previously written array object is null. If you want to read Parcelable or IInterface values, use createFixedArray or createFixedArray.

| Parameters ||
|---|---|
| `cls` | [Class](../java.lang/Class.md)\<T\>: the Class object for the target array type. (e.g. int\[\]\[\].class). This value cannot be `null`. |
| `dimensions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an array of int representing length of each dimension. This value cannot be `null`. |

**See Also**

- writeTypedArray
- createBooleanArray
- createByteArray
- createCharArray
- createIntArray
- createLongArray
- createFloatArray
- createDoubleArray
- createBinderArray
- createInterfaceArray
- createTypedArray

### createFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!, S : IInterface!> createFixedArray(
    cls: Class<T>, 
    asInterface: Function<IBinder!, S>, 
    vararg dimensions: Int
): T?
```

Read and return a new multi-dimensional array of typed interfaces from a parcel. Returns null if the previously written array object is null. If you want to read Parcelable values, use createFixedArray. For values of other types use createFixedArray.

| Parameters ||
|---|---|
| `cls` | [Class](../java.lang/Class.md)\<T\>: the Class object for the target array type. (e.g. IFoo\[\]\[\].class). This value cannot be `null`. |
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, S\>: This value cannot be `null`. |
| `dimensions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an array of int representing length of each dimension. This value cannot be `null`. |
| --- | --- |

### createFloatArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createFloatArray(): FloatArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?` | This value may be `null`. |

### createIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createIntArray(): IntArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | This value may be `null`. |

### createInterfaceArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> createInterfaceArray(
    newArray: IntFunction<Array<T>!>, 
    asInterface: Function<IBinder!, T>
): Array<T>?
```

Read and return a new array of T (IInterface) from the parcel.

| Parameters ||
|---|---|
| `newArray` | [IntFunction](../java.util.function/IntFunction.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>!\>: a function to create an array of T with a given length. This value cannot be `null`. |
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, T\>: a function to convert IBinder object into T (IInterface). This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | the IInterface array of type T. This value may be `null`. |

### createInterfaceArrayList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> createInterfaceArrayList(asInterface: Function<IBinder!, T>): ArrayList<T>?
```

Read and return a new ArrayList containing T (IInterface) objects from the parcel that was written with writeInterfaceList at the current dataPosition(). Returns null if the previously written list object was null.

| Parameters ||
|---|---|
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` | A newly created ArrayList containing T (IInterface) |

**See Also**

- writeInterfaceList

### createLongArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createLongArray(): LongArray?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?` | This value may be `null`. |

### createStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createStringArray(): Array<String!>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | This value may be `null`. |

### createStringArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createStringArrayList(): ArrayList<String!>?
```

Read and return a new ArrayList containing String objects from the parcel that was written with writeStringList at the current dataPosition(). Returns null if the previously written list object was null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | A newly created ArrayList containing strings with the same data as those that were previously written. |

**See Also**

- writeStringList

### createTypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> createTypedArray(c: Parcelable.Creator<T>): Array<T>?
```

Read and return a new array containing a particular object type from the parcel at the current dataPosition(). Returns null if the previously written array was null. The array *must* have previously been written via writeTypedArray with the same object type.

| Parameters ||
|---|---|
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | A newly created array containing objects with the same data as those that were previously written. |

**See Also**

- writeTypedArray

### createTypedArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> createTypedArrayList(c: Parcelable.Creator<T>): ArrayList<T>?
```

Read and return a new ArrayList containing a particular object type from the parcel that was written with #writeTypedList at the current dataPosition(). Returns null if the previously written list object was null. The list *must* have previously been written via #writeTypedList with the same object type.

| Parameters ||
|---|---|
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` | A newly created ArrayList containing objects with the same data as those that were previously written. |

**See Also**

### createTypedArrayMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> createTypedArrayMap(creator: Parcelable.Creator<T>): ArrayMap<String!, T>?
```

Read into a new `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#` with string keys items containing a particular object type that were written with writeTypedArrayMap at the current dataPosition(). The list *must* have previously been written via writeTypedArrayMap with the same object type.

| Parameters ||
|---|---|
| `creator` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: The creator to use when for instantiation. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, T>?` | A newly created `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#` containing objects with the same data as those that were previously written. This value may be `null`. |

**See Also**

- writeTypedArrayMap

### createTypedSparseArray

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> createTypedSparseArray(creator: Parcelable.Creator<T>): SparseArray<T>?
```

Read into a new `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` items containing a particular object type that were written with writeTypedSparseArray at the current dataPosition(). The list *must* have previously been written via writeTypedSparseArray with the same object type.

| Parameters ||
|---|---|
| `creator` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: The creator to use when for instantiation. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<T>?` | A newly created `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` containing objects with the same data as those that were previously written. This value may be `null`. |

**See Also**

- writeTypedSparseArray

### dataAvail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dataAvail(): Int
```

Returns the amount of data remaining to be read from the parcel. That is, dataSize-dataPosition.

### dataCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dataCapacity(): Int
```

Returns the total amount of space in the parcel. This is always \>= dataSize. The difference between it and dataSize() is the amount of room left until the parcel needs to re-allocate its data buffer.

### dataPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dataPosition(): Int
```

Returns the current position in the parcel data. Never more than dataSize.

### dataSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dataSize(): Int
```

Returns the total amount of data contained in the parcel.

### enforceInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enforceInterface(interfaceName: String): Unit
```

Read the header written by writeInterfaceToken and verify it matches the interface name in question. If the wrong interface type is present, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown. When used over binder, this exception should propagate to the caller.

| Parameters ||
|---|---|
| `interfaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### enforceNoDataAvail

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enforceNoDataAvail(): Unit
```

Verify there are no bytes left to be read on the Parcel.

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | If the current position hasn't reached the end of the Parcel. When used over binder, this exception should propagate to the caller. |

### hasFileDescriptors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFileDescriptors(): Boolean
```

Report whether the parcel contains any marshalled file descriptors. WARNING: Parcelable definitions change over time. Unless you define a Parcelable yourself OR the Parcelable explicitly guarantees that it would never include such objects, you should not expect the return value to stay the same, and your code should continue to work even if the return value changes.

### hasFileDescriptors

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFileDescriptors(
    offset: Int, 
    length: Int
): Boolean
```

Report whether the parcel contains any marshalled file descriptors in the range defined by `offset` and `length`. WARNING: Parcelable definitions change over time. Unless you define a Parcelable yourself OR the Parcelable explicitly guarantees that it would never include such objects, you should not expect the return value to stay the same, and your code should continue to work even if the return value changes.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset from which the range starts. Should be between 0 and dataSize. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The length of the range. Should be between 0 and dataSize - `offset`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether there are file descriptors or not. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the parameters are out of the permitted ranges. |

### marshall

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun marshall(): ByteArray!
```

Returns the raw bytes of the parcel.

The data you retrieve here **must not** be placed in any kind of persistent storage (on local disk, across a network, etc). For that, you should use standard serialization or another kind of general serialization mechanism. The Parcel marshalled representation is highly optimized for local IPC, and as such does not attempt to maintain compatibility with data created in different versions of the platform.

### marshall

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun marshall(buffer: ByteBuffer): Unit
```

Writes the raw bytes of the parcel to a buffer.

The data you retrieve here **must not** be placed in any kind of persistent storage (on local disk, across a network, etc). For that, you should use standard serialization or another kind of general serialization mechanism. The Parcel marshalled representation is highly optimized for local IPC, and as such does not attempt to maintain compatibility with data created in different versions of the platform.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md): The ByteBuffer to write the data to. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.nio.BufferOverflowException` | if the buffer is too small. |
| `java.nio.ReadOnlyBufferException` | if the buffer is read-only. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun obtain(): Parcel
```

Retrieve a new Parcel object from the pool.

| Return ||
|---|---|
| Parcel | This value cannot be `null`. |

### obtain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun obtain(binder: IBinder): Parcel
```

Retrieve a new Parcel object from the pool for use with a specific binder. Associate this parcel with a binder object. This marks the parcel as being prepared for a transaction on this specific binder object. Based on this, the format of the wire binder protocol may change. For future compatibility, it is recommended to use this for all Parcels.

| Parameters ||
|---|---|
| `binder` | [IBinder](IBinder.md): This value cannot be `null`. |

| Return ||
|---|---|
| Parcel | This value cannot be `null`. |

### readArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readArray(loader: ClassLoader?): Array<Any!>?
```

**Deprecated:** *Use the type-safer version readArray starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use createTypedArray if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read and return a new Object array from the parcel at the current dataPosition(). Returns null if the previously written array was null. The given class loader will be used to load any enclosed Parcelables.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readArray(
    loader: ClassLoader?, 
    clazz: Class<T>
): Array<T>?
```

Same as readArray but accepts `clazz` parameter as the type required for each item.

**Warning:** if the list contains items implementing the Parcelable interface, the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readArray instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readArrayList(loader: ClassLoader?): ArrayList<Any!>?
```

**Deprecated:** *Use the type-safer version readArrayList starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use createTypedArrayList if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read and return a new ArrayList object from the parcel at the current dataPosition(). Returns null if the previously written list object was null. The given class loader will be used to load any enclosed Parcelables.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readArrayList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readArrayList(
    loader: ClassLoader?, 
    clazz: Class<out T>
): ArrayList<T>?
```

Same as readArrayList but accepts `clazz` parameter as the type required for each item.

**Warning:** if the list contains items implementing the Parcelable interface, the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readArrayList instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<out T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readBinderArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBinderArray(val: Array<IBinder!>): Unit
```

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IBinder](IBinder.md)!\>: This value cannot be `null`. |

### readBinderList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBinderList(list: MutableList<IBinder!>): Unit
```

Read into the given List items IBinder objects that were written with writeBinderList at the current dataPosition().

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IBinder](IBinder.md)!\>: This value cannot be `null`. |

**See Also**

- writeBinderList

### readBlob

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBlob(): ByteArray?
```

Read a blob of data from the parcel and return it as a byte array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

**See Also**

- writeBlob

### readBoolean

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBoolean(): Boolean
```

Read a boolean value from the parcel at the current dataPosition().

### readBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBooleanArray(val: BooleanArray): Unit
```

| Parameters ||
|---|---|
| `val` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): This value cannot be `null`. |

### readBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBundle(): Bundle?
```

Read and return a new Bundle object from the parcel at the current dataPosition(). Returns null if the previously written Bundle object was null.

### readBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBundle(loader: ClassLoader?): Bundle?
```

Read and return a new Bundle object from the parcel at the current dataPosition(), using the given class loader to initialize the class loader of the Bundle for later retrieval of Parcelable objects. Returns null if the previously written Bundle object was null.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readByte(): Byte
```

Read a byte value from the parcel at the current dataPosition().

### readByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readByteArray(val: ByteArray): Unit
```

Read a byte\[\] object from the parcel and copy it into the given byte array.

| Parameters ||
|---|---|
| `val` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |

### readCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readCharArray(val: CharArray): Unit
```

| Parameters ||
|---|---|
| `val` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): This value cannot be `null`. |

### readDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readDouble(): Double
```

Read a double precision floating point value from the parcel at the current dataPosition().

### readDoubleArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readDoubleArray(val: DoubleArray): Unit
```

| Parameters ||
|---|---|
| `val` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): This value cannot be `null`. |

### readException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readException(): Unit
```

Special function for reading an exception result from the header of a parcel, to be used after receiving the result of a transaction. This will throw the exception for you if it had been written to the Parcel, otherwise return and let you read the normal result data from the Parcel.
**See Also**

- writeException
- writeNoException

### readException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readException(
    code: Int, 
    msg: String!
): Unit
```

Throw an exception with the given message. Not intended for use outside the Parcel class.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Used to determine which exception class to throw. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The exception message. |

### readFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFileDescriptor(): ParcelFileDescriptor!
```

Read a FileDescriptor from the parcel at the current dataPosition().

### readFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readFixedArray(val: T): Unit
```

Read a new multi-dimensional array from a parcel. If you want to read Parcelable or IInterface values, use readFixedArray or readFixedArray.

| Parameters ||
|---|---|
| `val` | T: the destination array to hold the read values. This value cannot be `null`. |

**See Also**

- writeTypedArray
- readBooleanArray
- readByteArray
- readCharArray
- readIntArray
- readLongArray
- readFloatArray
- readDoubleArray
- readBinderArray
- readInterfaceArray
- readTypedArray

### readFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!, S : Parcelable!> readFixedArray(
    val: T, 
    c: Parcelable.Creator<S>
): Unit
```

Read a new multi-dimensional array of typed parcelables from a parcel. If you want to read IInterface values, use readFixedArray. For values of other types, use readFixedArray.

| Parameters ||
|---|---|
| `val` | T: the destination array to hold the read values. This value cannot be `null`. |
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<S\>: This value cannot be `null`. |

### readFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!, S : IInterface!> readFixedArray(
    val: T, 
    asInterface: Function<IBinder!, S>
): Unit
```

Read a new multi-dimensional array of typed interfaces from a parcel. If you want to read Parcelable values, use readFixedArray. For values of other types, use readFixedArray.

| Parameters ||
|---|---|
| `val` | T: the destination array to hold the read values. This value cannot be `null`. |
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, S\>: This value cannot be `null`. |

### readFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFloat(): Float
```

Read a floating point value from the parcel at the current dataPosition().

### readFloatArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFloatArray(val: FloatArray): Unit
```

| Parameters ||
|---|---|
| `val` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |

### readHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readHashMap(loader: ClassLoader?): HashMap<Any!, Any!>?
```

**Deprecated:** *Consider using readBundle as stated above, in case this method is still preferred use the type-safer version readHashMap starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Please use readBundle instead (whose data must have been written with writeBundle. Read and return a new HashMap object from the parcel at the current dataPosition(), using the given class loader to load any enclosed Parcelables. Returns null if the previously written map object was null.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readHashMap

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <K : Any!, V : Any!> readHashMap(
    loader: ClassLoader?, 
    clazzKey: Class<out K>, 
    clazzValue: Class<out V>
): HashMap<K, V>?
```

Same as readHashMap but accepts `clazzKey` and `clazzValue` parameter as the types required for each key and value pair.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazzKey` | [Class](../java.lang/Class.md)\<out K\>: This value cannot be `null`. |
| `clazzValue` | [Class](../java.lang/Class.md)\<out V\>: This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/HashMap.html#<K, V>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | if the item to be deserialized is not an instance of that class or any of its children class |

### readInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readInt(): Int
```

Read an integer value from the parcel at the current dataPosition().

### readIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readIntArray(val: IntArray): Unit
```

| Parameters ||
|---|---|
| `val` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |

### readInterfaceArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> readInterfaceArray(
    val: Array<T>, 
    asInterface: Function<IBinder!, T>
): Unit
```

Read an array of T (IInterface) from a parcel.

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: This value cannot be `null`. |
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, T\>: a function to convert IBinder object into T (IInterface). This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the length of \`val\` mismatches the number of items in the parcel. |

### readInterfaceList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> readInterfaceList(
    list: MutableList<T>, 
    asInterface: Function<IBinder!, T>
): Unit
```

Read into the given List items IInterface objects that were written with writeInterfaceList at the current dataPosition().

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>: This value cannot be `null`. |
| `asInterface` | [Function](../java.util.function/Function.md)\< [IBinder](IBinder.md)!, T\>: This value cannot be `null`. |

**See Also**

- writeInterfaceList

### readList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readList(
    outVal: MutableList<Any?>, 
    loader: ClassLoader?
): Unit
```

**Deprecated:** *Use the type-safer version readList starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use readTypedList if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read into an existing List object from the parcel at the current dataPosition(), using the given class loader to load any enclosed Parcelables. If it is null, the default class loader is used.

| Parameters ||
|---|---|
| `outVal` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>: This value cannot be `null`. |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readList(
    outVal: MutableList<in T>, 
    loader: ClassLoader?, 
    clazz: Class<T>
): Unit
```

Same as readList but accepts `clazz` parameter as the type required for each item.

**Warning:** if the list contains items implementing the Parcelable interface, the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readList instead.

| Parameters ||
|---|---|
| `outVal` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<in T\>: This value cannot be `null`. |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readLong(): Long
```

Read a long integer value from the parcel at the current dataPosition().

### readLongArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readLongArray(val: LongArray): Unit
```

| Parameters ||
|---|---|
| `val` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): This value cannot be `null`. |

### readMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readMap(
    outVal: MutableMap<Any?, Any?>, 
    loader: ClassLoader?
): Unit
```

**Deprecated:** *Consider using readBundle as stated above, in case this method is still preferred use the type-safer version readMap starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Please use readBundle instead (whose data must have been written with writeBundle. Read into an existing Map object from the parcel at the current dataPosition().

| Parameters ||
|---|---|
| `outVal` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>: This value cannot be `null`. |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readMap

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <K : Any!, V : Any!> readMap(
    outVal: MutableMap<in K, in V>, 
    loader: ClassLoader?, 
    clazzKey: Class<K>, 
    clazzValue: Class<V>
): Unit
```

Same as readMap but accepts `clazzKey` and `clazzValue` parameter as the types required for each key and value pair.

| Parameters ||
|---|---|
| `outVal` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<in K, in V\>: This value cannot be `null`. |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazzKey` | [Class](../java.lang/Class.md)\<K\>: This value cannot be `null`. |
| --- | --- |
| `clazzValue` | [Class](../java.lang/Class.md)\<V\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | If the item to be deserialized is not an instance of that class or any of its children class |

### readParcelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> readParcelable(loader: ClassLoader?): T?
```

**Deprecated:** *Use the type-safer version readParcelable starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use createFromParcel if possible since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read and return a new Parcelable from the parcel. The given class loader will be used to load any enclosed Parcelables. If it is null, the default class loader will be used.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: A ClassLoader from which to instantiate the Parcelable object, or null for the default class loader. |

| Return ||
|---|---|
| `T?` | Returns the newly created Parcelable, or null if a null object has been written. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if there was an error trying to instantiate the Parcelable. |

### readParcelable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readParcelable(
    loader: ClassLoader?, 
    clazz: Class<T>
): T?
```

Same as readParcelable but accepts `clazz` parameter as the type required for each item.

**Warning:** the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readParcelable instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `T?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readParcelableArray(loader: ClassLoader?): Array<Parcelable!>?
```

**Deprecated:** *Use the type-safer version readParcelableArray starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use createTypedArray if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read and return a new Parcelable array from the parcel. The given class loader will be used to load any enclosed Parcelables.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Parcelable!>?` | the Parcelable array, or null if the array is null |

### readParcelableArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readParcelableArray(
    loader: ClassLoader?, 
    clazz: Class<T>
): Array<T>?
```

Same as readParcelableArray but accepts `clazz` parameter as the type required for each item.

**Warning:** the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readParcelableArray instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readParcelableCreator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readParcelableCreator(loader: ClassLoader?): Parcelable.Creator<*>?
```

**Deprecated:** *Use the type-safer version readParcelableCreator starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Read and return a Parcelable.Creator from the parcel. The given class loader will be used to load the `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator`. If it is null, the default class loader will be used.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: A ClassLoader from which to instantiate the `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` object, or null for the default class loader. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator<*>?` | the previously written `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator`, or null if a null Creator was written. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if there was an error trying to read the `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator`. |

**See Also**

- writeParcelableCreator

### readParcelableCreator

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readParcelableCreator(
    loader: ClassLoader?, 
    clazz: Class<T>
): Parcelable.Creator<T>?
```

Same as readParcelableCreator but accepts `clazz` parameter as the required type.

**Warning:** the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readParcelableCreator instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator<T>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there there was an error trying to read the `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator`. |

### readParcelableList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> readParcelableList(
    list: MutableList<T>, 
    cl: ClassLoader?
): MutableList<T>
```

**Deprecated:** *Use the type-safer version readParcelableList starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use readTypedList if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read the list of `Parcelable` objects at the current data position into the given `list`. The contents of the `list` are replaced. If the serialized list was `null`, `list` is cleared.

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>: This value cannot be `null`. |
| `cl` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

**See Also**

- writeParcelableList

### readParcelableList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readParcelableList(
    list: MutableList<T>, 
    cl: ClassLoader?, 
    clazz: Class<out T>
): MutableList<T>
```

Same as readParcelableList but accepts `clazz` parameter as the type required for each item.

**Warning:** if the list contains items implementing the Parcelable interface, the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readParcelableList instead.

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>: This value cannot be `null`. |
| `cl` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<out T\>: This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readPersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readPersistableBundle(): PersistableBundle?
```

Read and return a new Bundle object from the parcel at the current dataPosition(). Returns null if the previously written Bundle object was null.

### readPersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readPersistableBundle(loader: ClassLoader?): PersistableBundle?
```

Read and return a new Bundle object from the parcel at the current dataPosition(), using the given class loader to initialize the class loader of the Bundle for later retrieval of Parcelable objects. Returns null if the previously written Bundle object was null.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readSerializable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readSerializable(): Serializable?
```

**Deprecated:** *Use the type-safer version readSerializable starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Read and return a new Serializable object from the parcel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Serializable.html#?` | the Serializable object, or null if the Serializable name wasn't found in the parcel. Unlike readSerializable, it uses the nearest valid class loader up the execution stack to instantiate the Serializable object. |

### readSerializable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readSerializable(
    loader: ClassLoader?, 
    clazz: Class<T>
): T?
```

Same as readSerializable but accepts `loader` and `clazz` parameters.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: A ClassLoader from which to instantiate the Serializable object, or null for the default class loader. |
| `clazz` | [Class](../java.lang/Class.md)\<T\>: The type of the object expected. This value cannot be `null`. |

| Return ||
|---|---|
| `T?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children class or there there was an error deserializing the object. |

### readSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readSize(): Size
```

Read a Size from the parcel at the current dataPosition().

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Size.html#` | This value cannot be `null`. |

### readSizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readSizeF(): SizeF
```

Read a SizeF from the parcel at the current dataPosition().

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SizeF.html#` | This value cannot be `null`. |

### readSparseArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readSparseArray(loader: ClassLoader?): SparseArray<T>?
```

**Deprecated:** *Use the type-safer version readSparseArray starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`. Also consider changing the format to use createTypedSparseArray if possible (eg. if the items' class is final) since this is also more performant. Note that changing to the latter also requires changing the writes.*

Read and return a new SparseArray object from the parcel at the current dataPosition(). Returns null if the previously written list object was null. The given class loader will be used to load any enclosed Parcelables.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### readSparseArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readSparseArray(
    loader: ClassLoader?, 
    clazz: Class<out T>
): SparseArray<T>?
```

Same as readSparseArray but accepts `clazz` parameter as the type required for each item.

**Warning:** if the list contains items implementing the Parcelable interface, the class that implements Parcelable has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, getEnclosingClass has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated readSparseArray instead.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |
| `clazz` | [Class](../java.lang/Class.md)\<out T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<T>?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | Throws BadParcelableException if the item to be deserialized is not an instance of that class or any of its children classes or there was an error trying to instantiate an element. |

### readSparseBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readSparseBooleanArray(): SparseBooleanArray?
```

Read and return a new SparseBooleanArray object from the parcel at the current dataPosition(). Returns null if the previously written list object was null.

### readString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readString(): String?
```

Read a string value from the parcel at the current dataPosition().

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### readStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readStringArray(val: Array<String!>): Unit
```

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

### readStringList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readStringList(list: MutableList<String!>): Unit
```

Read into the given List items String objects that were written with writeStringList at the current dataPosition().

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

**See Also**

- writeStringList

### readStrongBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readStrongBinder(): IBinder!
```

Read an object from the parcel at the current dataPosition().

### readTypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readTypedArray(
    val: Array<T>, 
    c: Parcelable.Creator<T>
): Unit
```

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: This value cannot be `null`. |
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: This value cannot be `null`. |

### readTypedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readTypedList(
    list: MutableList<T>, 
    c: Parcelable.Creator<T>
): Unit
```

Read into the given List items containing a particular object type that were written with #writeTypedList at the current dataPosition(). The list *must* have previously been written via #writeTypedList with the same object type.

| Parameters ||
|---|---|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>: This value cannot be `null`. |
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: This value cannot be `null`. |

**See Also**

### readTypedObject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> readTypedObject(c: Parcelable.Creator<T>): T?
```

Read and return a typed Parcelable object from a parcel. Returns null if the previous written object was null. The object *must* have previous been written via writeTypedObject with the same object type.

| Parameters ||
|---|---|
| `c` | [Parcelable.Creator](../android/os/Parcelable.Creator.md)\<T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `T?` | A newly created object of the type that was previously written. |

**See Also**

- writeTypedObject

### readValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readValue(loader: ClassLoader?): Any?
```

Read a typed object from a parcel. The given class loader will be used to load any enclosed Parcelables. If it is null, the default class loader will be used.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)?: This value may be `null`. |

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun recycle(): Unit
```

Put a Parcel object back into the pool. You must not touch the object after this call.

### setDataCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDataCapacity(size: Int): Unit
```

Change the capacity (current available space) of the parcel.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new capacity of the parcel, in bytes. Can not be less than dataSize -- that is, you can not drop existing data with this method. |

### setDataPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDataPosition(pos: Int): Unit
```

Move the current read/write position in the parcel.

| Parameters ||
|---|---|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): New offset in the parcel; must be between 0 and dataSize. |

### setDataSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDataSize(size: Int): Unit
```

Change the amount of data in the parcel. Can be either smaller or larger than the current size. If larger than the current capacity, more memory will be allocated.

| Parameters ||
|---|---|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new number of bytes in the Parcel. |

### setPropagateAllowBlocking

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPropagateAllowBlocking(): Unit
```

This method is used by the AIDL compiler for system components. Not intended to be used by non-system apps.

### unmarshall

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unmarshall(
    data: ByteArray, 
    offset: Int, 
    length: Int
): Unit
```

Fills the raw bytes of this Parcel with the supplied data.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |

### unmarshall

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unmarshall(buffer: ByteBuffer): Unit
```

Fills the raw bytes of this Parcel with data from the supplied buffer.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md): will read buffer.remaining() bytes from the buffer. This value cannot be `null`. |

### writeArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeArray(val: Array<Any!>?): Unit
```

Flatten an Object array into the parcel at the current dataPosition(), growing dataCapacity() if needed. The array values are written using writeValue and must follow the specification there.

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: This value may be `null`. |

### writeBinderArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBinderArray(val: Array<IBinder!>?): Unit
```

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IBinder](IBinder.md)!\>?: This value may be `null`. |

### writeBinderList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBinderList(val: MutableList<IBinder!>?): Unit
```

Flatten a List containing IBinder objects into the parcel, at the current dataPosition() and growing dataCapacity() if needed. They can later be retrieved with createBinderArrayList or readBinderList.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IBinder](IBinder.md)!\>?: The list of strings to be written. This value may be `null`. |

**See Also**

- createBinderArrayList
- readBinderList

### writeBlob

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBlob(b: ByteArray?): Unit
```

Write a blob of data into the parcel at the current dataPosition, growing dataCapacity if needed.

If the blob is small, then it is stored in-place, otherwise it is transferred by way of an anonymous shared memory region. If you prefer send in-place, please use writeByteArray.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: Bytes to place into the parcel. This value may be `null`. |

**See Also**

- readBlob

### writeBlob

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBlob(
    b: ByteArray?, 
    offset: Int, 
    len: Int
): Unit
```

Write a blob of data into the parcel at the current dataPosition, growing dataCapacity if needed.

If the blob is small, then it is stored in-place, otherwise it is transferred by way of an anonymous shared memory region. If you prefer send in-place, please use writeByteArray.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: Bytes to place into the parcel. This value may be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of first byte to be written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of bytes to write. |
| --- | --- |

**See Also**

- readBlob

### writeBoolean

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBoolean(val: Boolean): Unit
```

Write a boolean value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

Note: This method currently delegates to writeInt with a value of 1 or 0 for true or false, respectively, but may change in the future.

### writeBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBooleanArray(val: BooleanArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: This value may be `null`. |

### writeBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBundle(val: Bundle?): Unit
```

Flatten a Bundle into the parcel at the current dataPosition(), growing dataCapacity() if needed.

| Parameters ||
|---|---|
| `val` | [Bundle](Bundle.md)?: This value may be `null`. |

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeByte(val: Byte): Unit
```

Write a byte value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

Note: This method currently delegates to writeInt but may change in the future.

### writeByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeByteArray(b: ByteArray?): Unit
```

Write a byte array into the parcel at the current dataPosition, growing dataCapacity if needed.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: Bytes to place into the parcel. This value may be `null`. |

### writeByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeByteArray(
    b: ByteArray?, 
    offset: Int, 
    len: Int
): Unit
```

Write a byte array into the parcel at the current dataPosition, growing dataCapacity if needed.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: Bytes to place into the parcel. This value may be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of first byte to be written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of bytes to write. |
| --- | --- |

### writeCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeCharArray(val: CharArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: This value may be `null`. |

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDouble(val: Double): Unit
```

Write a double precision floating point value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeDoubleArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDoubleArray(val: DoubleArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: This value may be `null`. |

### writeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeException(e: Exception): Unit
```

Special function for writing an exception result at the header of a parcel, to be used when returning an exception from a transaction. Note that this currently only supports a few exception types; any other exception will be re-thrown by this function as a RuntimeException (to be caught by the system's last-resort exception handling when dispatching a transaction).

The supported exception types are:

- BadParcelableException
- `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`
- `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`
- `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`
- `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`
- NetworkOnMainThreadException

| Parameters ||
|---|---|
| `e` | [Exception](../java.lang/Exception.md): The Exception to be written. This value cannot be `null`. |

**See Also**

- writeNoException

### writeFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeFileDescriptor(val: FileDescriptor): Unit
```

Write a FileDescriptor into the parcel at the current dataPosition(), growing dataCapacity() if needed.

The file descriptor will not be closed, which may result in file descriptor leaks when objects are returned from Binder calls. Use writeToParcel instead, which accepts contextual flags and will close the original file descriptor if `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` is set.

| Parameters ||
|---|---|
| `val` | [FileDescriptor](../java.io/FileDescriptor.md): This value cannot be `null`. |

### writeFixedArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> writeFixedArray(
    val: T?, 
    parcelableFlags: Int, 
    vararg dimensions: Int
): Unit
```

Flatten a homogeneous multi-dimensional array with fixed-size. This delegates to other APIs to write a one-dimensional array. Use readFixedArray or createFixedArray with the same dimensions to unmarshal.

| Parameters ||
|---|---|
| `val` | T?: The array to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. Used only if val is an array of Parcelable objects. |
| `dimensions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an array of int representing length of each dimension. The array should be sized with the exact size of dimensions. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.os.BadParcelableException` | If the array's component type is not supported or if its size doesn't match with the given dimensions. |

**See Also**

- writeBooleanArray
- writeCharArray
- writeIntArray
- writeLongArray
- writeFloatArray
- writeDoubleArray
- writeBinderArray
- writeInterfaceArray
- writeTypedArray

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeFloat(val: Float): Unit
```

Write a floating point value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeFloatArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeFloatArray(val: FloatArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: This value may be `null`. |

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeInt(val: Int): Unit
```

Write an integer value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeIntArray(val: IntArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: This value may be `null`. |

### writeInterfaceArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> writeInterfaceArray(val: Array<T>?): Unit
```

Flatten a homogeneous array containing an IInterface type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the array must be one that implements IInterface.

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: The array of objects to be written. This value may be `null`. |

**See Also**

- createInterfaceArray
- readInterfaceArray
- IInterface

### writeInterfaceList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : IInterface!> writeInterfaceList(val: MutableList<T>?): Unit
```

Flatten a `List` containing T (IInterface) objects into this parcel at the current position. They can later be retrieved with createInterfaceArrayList or readInterfaceList.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>?: This value may be `null`. |

**See Also**

- createInterfaceArrayList
- readInterfaceList

### writeInterfaceToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeInterfaceToken(interfaceName: String): Unit
```

Store or read an IBinder interface token in the parcel at the current dataPosition. This is used to validate that the marshalled transaction is intended for the target interface. This is typically written at the beginning of transactions as a header.

| Parameters ||
|---|---|
| `interfaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### writeList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeList(val: MutableList<Any?>?): Unit
```

Flatten a List into the parcel at the current dataPosition(), growing dataCapacity() if needed. The List values are written using writeValue and must follow the specification there.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>?: This value may be `null`. |

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeLong(val: Long): Unit
```

Write a long integer value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeLongArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeLongArray(val: LongArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: This value may be `null`. |

### writeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeMap(val: MutableMap<Any?, Any?>?): Unit
```

Please use writeBundle instead. Flattens a Map into the parcel at the current dataPosition(), growing dataCapacity() if needed. The Map keys must be String objects. The Map values are written using writeValue and must follow the specification there.

It is strongly recommended to use writeBundle instead of this method, since the Bundle class provides a type-safe API that allows you to avoid mysterious type errors at the point of marshalling.

| Parameters ||
|---|---|
| `val` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>?: This value may be `null`. |

### writeNoException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeNoException(): Unit
```

Special function for writing information at the front of the Parcel indicating that no exception occurred.
**See Also**

- writeException

### writeParcelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeParcelable(
    p: Parcelable?, 
    parcelableFlags: Int
): Unit
```

Flatten the name of the class of the Parcelable and its contents into the parcel.

| Parameters ||
|---|---|
| `p` | [Parcelable](Parcelable.md)?: The Parcelable object to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. |

### writeParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeParcelableArray(
    value: Array<T>?, 
    parcelableFlags: Int
): Unit
```

Write a heterogeneous array of Parcelable objects into the Parcel. Each object in the array is written along with its class name, so that the correct class can later be instantiated. As a result, this has significantly more overhead than writeTypedArray, but will correctly handle an array containing more than one type of object.

| Parameters ||
|---|---|
| `value` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: The array of objects to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. |

**See Also**

- writeTypedArray

### writeParcelableCreator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeParcelableCreator(p: Parcelable): Unit
```

Flatten the name of the class of the Parcelable into this Parcel.

| Parameters ||
|---|---|
| `p` | [Parcelable](Parcelable.md): The Parcelable object to be written. This value cannot be `null`. |

**See Also**

### writeParcelableList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeParcelableList(
    val: MutableList<T>?, 
    flags: Int
): Unit
```

Flatten a `List` containing arbitrary `Parcelable` objects into this parcel at the current position. They can later be retrieved using readParcelableList if required.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>?: This value may be `null`. |

**See Also**

- readParcelableList

### writePersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writePersistableBundle(val: PersistableBundle?): Unit
```

Flatten a PersistableBundle into the parcel at the current dataPosition(), growing dataCapacity() if needed.

| Parameters ||
|---|---|
| `val` | [PersistableBundle](PersistableBundle.md)?: This value may be `null`. |

### writeSerializable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeSerializable(s: Serializable?): Unit
```

Write a generic serializable object in to a Parcel. It is strongly recommended that this method be avoided, since the serialization overhead is extremely large, and this approach will be much slower than using the other approaches to writing data in to a Parcel.

| Parameters ||
|---|---|
| `s` | [Serializable](../java.io/Serializable.md)?: This value may be `null`. |

### writeSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeSize(val: Size): Unit
```

Flatten a Size into the parcel at the current dataPosition(), growing dataCapacity() if needed.

| Parameters ||
|---|---|
| `val` | [Size](../android.util/Size.md): This value cannot be `null`. |

### writeSizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeSizeF(val: SizeF): Unit
```

Flatten a SizeF into the parcel at the current dataPosition(), growing dataCapacity() if needed.

| Parameters ||
|---|---|
| `val` | [SizeF](../android.util/SizeF.md): This value cannot be `null`. |

### writeSparseArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> writeSparseArray(val: SparseArray<T>?): Unit
```

Flatten a generic SparseArray into the parcel at the current dataPosition(), growing dataCapacity() if needed. The SparseArray values are written using writeValue and must follow the specification there.

| Parameters ||
|---|---|
| `val` | [SparseArray](../android.util/SparseArray.md)\<T\>?: This value may be `null`. |

### writeSparseBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeSparseBooleanArray(val: SparseBooleanArray?): Unit
```

| Parameters ||
|---|---|
| `val` | [SparseBooleanArray](../android.util/SparseBooleanArray.md)?: This value may be `null`. |

### writeString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeString(val: String?): Unit
```

Write a string value into the parcel at the current dataPosition(), growing dataCapacity() if needed.

| Parameters ||
|---|---|
| `val` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### writeStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeStringArray(val: Array<String!>?): Unit
```

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |

### writeStringList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeStringList(val: MutableList<String!>?): Unit
```

Flatten a List containing String objects into the parcel, at the current dataPosition() and growing dataCapacity() if needed. They can later be retrieved with createStringArrayList or readStringList.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The list of strings to be written. This value may be `null`. |

**See Also**

- createStringArrayList
- readStringList

### writeStrongBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeStrongBinder(val: IBinder!): Unit
```

Write an object into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeStrongInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeStrongInterface(val: IInterface!): Unit
```

Write an object into the parcel at the current dataPosition(), growing dataCapacity() if needed.

### writeTypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedArray(
    val: Array<T>?, 
    parcelableFlags: Int
): Unit
```

Flatten a homogeneous array containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the array must be one that implements Parcelable. Unlike the writeParcelableArray method, however, only the raw data of the objects is written and not their type, so you must use readTypedArray with the correct corresponding `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` implementation to unmarshall them.

| Parameters ||
|---|---|
| `val` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: The array of objects to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. |

**See Also**

- readTypedArray
- writeParcelableArray
- `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator`

### writeTypedArrayMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedArrayMap(
    val: ArrayMap<String!, T>?, 
    parcelableFlags: Int
): Unit
```

Flatten an `https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#` with string keys containing a particular object type into the parcel at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the array must be one that implements Parcelable. Only the raw data of the objects is written and not their type, so you must use the corresponding createTypedArrayMap

| Parameters ||
|---|---|
| `val` | [ArrayMap](../android.util/ArrayMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, T\>?: The map of objects to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The parcelable flags to use. |

**See Also**

- createTypedArrayMap
- Parcelable

### writeTypedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedList(val: MutableList<T>?): Unit
```

Flatten a List containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the list must be one that implements Parcelable. Unlike the generic writeList() method, however, only the raw data of the objects is written and not their type, so you must use the corresponding readTypedList() to unmarshall them.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>?: The list of objects to be written. This value may be `null`. |

**See Also**

- createTypedArrayList
- readTypedList
- Parcelable

### writeTypedList

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedList(
    val: MutableList<T>?, 
    parcelableFlags: Int
): Unit
```

Flatten a List containing a particular object type into the parcel, at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the list must be one that implements Parcelable. Unlike the generic writeList() method, however, only the raw data of the objects is written and not their type, so you must use the corresponding readTypedList() to unmarshall them.

| Parameters ||
|---|---|
| `val` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>?: The list of objects to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. |

**See Also**

- createTypedArrayList
- readTypedList
- Parcelable

### writeTypedObject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedObject(
    val: T?, 
    parcelableFlags: Int
): Unit
```

Flatten the Parcelable object into the parcel.

| Parameters ||
|---|---|
| `val` | T?: The Parcelable object to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Contextual flags as per writeToParcel. |

**See Also**

- readTypedObject

### writeTypedSparseArray

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> writeTypedSparseArray(
    val: SparseArray<T>?, 
    parcelableFlags: Int
): Unit
```

Flatten a `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` containing a particular object type into the parcel at the current dataPosition() and growing dataCapacity() if needed. The type of the objects in the array must be one that implements Parcelable. Unlike the generic writeSparseArray method, however, only the raw data of the objects is written and not their type, so you must use the corresponding createTypedSparseArray.

| Parameters ||
|---|---|
| `val` | [SparseArray](../android.util/SparseArray.md)\<T\>?: The list of objects to be written. This value may be `null`. |
| `parcelableFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The parcelable flags to use. |

**See Also**

- createTypedSparseArray
- Parcelable

### writeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeValue(v: Any?): Unit
```

Flatten a generic object in to a parcel. The given Object value may currently be one of the following types:

- null
- String
- Byte
- Short
- Integer
- Long
- Float
- Double
- Boolean
- String\[\]
- boolean\[\]
- byte\[\]
- int\[\]
- long\[\]
- Object\[\] (supporting objects of the same type defined here).
- Bundle
- Map (as supported by writeMap).
- Any object that implements the Parcelable protocol.
- Parcelable\[\]
- CharSequence (as supported by writeToParcel).
- List (as supported by writeList).
- `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#` (as supported by writeSparseArray).
- IBinder
- Any object that implements Serializable (but see writeSerializable for caveats). Note that all of the previous types have relatively efficient implementations for writing to a Parcel; having to rely on the generic serialization approach is much less efficient and should be avoided whenever possible.

<br />

Parcelable objects are written with writeToParcel using contextual flags of 0. When serializing objects containing ParcelFileDescriptors, this may result in file descriptor leaks when they are returned from Binder calls (where `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` should be used).

| Parameters ||
|---|---|
| `v` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

## Properties

### STRING_CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_CREATOR: Parcelable.Creator<String!>!
```
