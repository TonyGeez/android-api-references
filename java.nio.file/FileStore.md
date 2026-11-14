# FileStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileStore

```
abstract class FileStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.FileStore](FileStore.md) |

Storage for files. A`FileStore`represents a storage pool, device, partition, volume, concrete file system or other implementation specific means of file storage. The`FileStore`for where a file is stored is obtained by invoking the [getFileStore](Files.md))method, or all file stores can be enumerated by invoking the [getFileStores](FileSystem.md))method.

In addition to the methods defined by this class, a file store may support one or more [FileStoreAttributeView](../java.nio.file.attribute/FileStoreAttributeView.md) classes that provide a read-only or updatable view of a set of file store attributes.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileStore](FileStore.md))`()` Initializes a new instance of this class. |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](FileStore.md))`(`attribute:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Reads the value of a file store attribute. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBlockSize](FileStore.md))`()` Returns the number of bytes per block in this file store. |
| abstractV | [getFileStoreAttributeView](FileStore.md))`(`type:` ` [Class](../java.lang/Class.md)<V>!`)` Returns a`FileStoreAttributeView`of the given type. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalSpace](FileStore.md))`()` Returns the size, in bytes, of the file store. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUnallocatedSpace](FileStore.md))`()` Returns the number of unallocated bytes in the file store. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUsableSpace](FileStore.md))`()` Returns the number of bytes available to this Java virtual machine on the file store. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](FileStore.md))`()` Tells whether this file store is read-only. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](FileStore.md))`()` Returns the name of this file store. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsFileAttributeView](FileStore.md))`(`type:` ` [Class](../java.lang/Class.md)<out` ` [FileAttributeView](../java.nio.file.attribute/FileAttributeView.md)!>!`)` Tells whether or not this file store supports the file attributes identified by the given file attribute view. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsFileAttributeView](FileStore.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tells whether or not this file store supports the file attributes identified by the given file attribute view. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [type](FileStore.md))`()` Returns the*type*of this file store. |

## Protected constructors

### FileStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileStore()
```

Initializes a new instance of this class.

## Public methods

### getAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttribute(attribute: String!): Any!
```

Reads the value of a file store attribute.

The`attribute`parameter identifies the attribute to be read and takes the form:
*view-name* **:** *attribute-name* where the character`':'`stands for itself.

*view-name* is the [name](../java.nio.file.attribute/AttributeView.md))of a [AttributeView](FileStore.md) that identifies a set of file attributes.*attribute-name*is the name of the attribute.

**Usage Example:**Suppose we want to know if ZFS compression is enabled (assuming the "zfs" view is supported): 

```kotlin
boolean compression = (Boolean)fs.getAttribute("zfs:compression");
  
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------|
| `attribute` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute to read |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the attribute value;`null`may be valid for some attributes |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available or it does not support reading the attribute |
| `java.io.IOException` | if an I/O error occurs |

### getBlockSize

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockSize(): Long
```

Returns the number of bytes per block in this file store.

File storage is typically organized into discrete sequences of bytes called*blocks*. A block is the smallest storage unit of a file store. Every read and write operation is performed on a multiple of blocks.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a positive value representing the block size of this file store, in bytes |

| Exceptions ||
|-------------------------------------------|-----------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.UnsupportedOperationException` | if the operation is not supported |

### getFileStoreAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : FileStoreAttributeView!> getFileStoreAttributeView(type: Class<V>!): V
```

Returns a`FileStoreAttributeView`of the given type.

This method is intended to be used where the file store attribute view defines type-safe methods to read or update the file store attributes. The`type`parameter is the type of the attribute view required and the method returns an instance of that type if supported.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileStoreAttributeView`type |
| `type` | [Class](../java.lang/Class.md)\<V\>!:the`Class`object corresponding to the attribute view |

| Return ||
|---|--------------------------------------------------------------------------------------------------|
| V | a file store attribute view of the specified type or`null`if the attribute view is not available |

### getTotalSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTotalSpace(): Long
```

Returns the size, in bytes, of the file store.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the size of the file store, in bytes |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### getUnallocatedSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUnallocatedSpace(): Long
```

Returns the number of unallocated bytes in the file store.

The returned number of unallocated bytes is a hint, but not a guarantee, that it is possible to use most or any of these bytes. The number of unallocated bytes is most likely to be accurate immediately after the space attributes are obtained. It is likely to be made inaccurate by any external I/O operations including those made on the system outside of this virtual machine.

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of unallocated bytes |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### getUsableSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUsableSpace(): Long
```

Returns the number of bytes available to this Java virtual machine on the file store.

The returned number of available bytes is a hint, but not a guarantee, that it is possible to use most or any of these bytes. The number of usable bytes is most likely to be accurate immediately after the space attributes are obtained. It is likely to be made inaccurate by any external I/O operations including those made on the system outside of this Java virtual machine.

| Return ||
|------------------------------------------------------------------------------|-------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of bytes available |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### isReadOnly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Tells whether this file store is read-only. A file store is read-only if it does not support write operations or other changes to files. Any attempt to create a file, open an existing file for writing etc. causes an`IOException`to be thrown.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this file store is read-only |

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of this file store. The format of the name is highly implementation specific. It will typically be the name of the storage pool or volume.

The string returned by this method may differ from the string returned by the [toString](../java.lang/Object.md))method.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this file store |

### supportsFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsFileAttributeView(type: Class<out FileAttributeView!>!): Boolean
```

Tells whether or not this file store supports the file attributes identified by the given file attribute view.

Invoking this method to test if the file store supports [BasicFileAttributeView](../java.nio.file.attribute/BasicFileAttributeView.md) will always return`true`. In the case of the default provider, this method cannot guarantee to give the correct result when the file store is not a local storage device. The reasons for this are implementation specific and therefore unspecified.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Class](../java.lang/Class.md)\<out [FileAttributeView](../java.nio.file.attribute/FileAttributeView.md)!\>!:the file attribute view type |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the file attribute view is supported |

### supportsFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsFileAttributeView(name: String!): Boolean
```

Tells whether or not this file store supports the file attributes identified by the given file attribute view.

Invoking this method to test if the file store supports [BasicFileAttributeView](../java.nio.file.attribute/BasicFileAttributeView.md), identified by the name "`basic`" will always return`true`. In the case of the default provider, this method cannot guarantee to give the correct result when the file store is not a local storage device. The reasons for this are implementation specific and therefore unspecified.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the [name](../java.nio.file.attribute/AttributeView.md))of file attribute view |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the file attribute view is supported |

### type

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun type(): String!
```

Returns the*type*of this file store. The format of the string returned by this method is highly implementation specific. It may indicate, for example, the format used or if the file store is local or remote.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representing the type of this file store |
