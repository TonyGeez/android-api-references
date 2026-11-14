Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserDefinedFileAttributeView

```
interface UserDefinedFileAttributeView : FileAttributeView
```

| [java.nio.file.attribute.UserDefinedFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#) |

A file attribute view that provides a view of a file's user-defined attributes, sometimes known as *extended attributes*. User-defined file attributes are used to store metadata with a file that is not meaningful to the file system. It is primarily intended for file system implementations that support such a capability directly but may be emulated. The details of such emulation are highly implementation specific and therefore not specified.

This `FileAttributeView` provides a view of a file's user-defined attributes as a set of name/value pairs, where the attribute name is represented by a `String`. An implementation may require to encode and decode from the platform or file system representation when accessing the attribute. The value has opaque content. This attribute view defines the `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#read(kotlin.String,%20java.nio.ByteBuffer)` and `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#write(kotlin.String,%20java.nio.ByteBuffer)` methods to read the value into or write from a `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#`. This `FileAttributeView` is not intended for use where the size of an attribute value is larger than `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int`.

User-defined attributes may be used in some implementations to store security related attributes so consequently, in the case of the default provider at least, all methods that access user-defined attributes require the `RuntimePermission("accessUserDefinedAttributes")` permission when a security manager is installed.

The java.nio.file.FileStore#supportsFileAttributeView method may be used to test if a specific `https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#` supports the storage of user-defined attributes.

Where dynamic access to file attributes is required, the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getAttribute(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption)` method may be used to read the attribute value. The attribute value is returned as a byte array (byte\[\]). The `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption)` method may be used to write the value of a user-defined attribute from a buffer (as if by invoking the `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#write(kotlin.String,%20java.nio.ByteBuffer)` method), or byte array (byte\[\]).

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#delete(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Deletes a user-defined attribute. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#list()()` Returns a list containing the names of the user-defined attributes. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#name()()` Returns the name of this attribute view. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#read(kotlin.String,%20java.nio.ByteBuffer)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dst: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` Read the value of a user-defined attribute into a buffer. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#size(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the size of the value of a user-defined attribute. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#write(kotlin.String,%20java.nio.ByteBuffer)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, src: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!)` Writes the value of a user-defined attribute from a buffer. |
| --- | --- |

## Public methods

### delete

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun delete(name: String!): Unit
```

Deletes a user-defined attribute.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The attribute name |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs or the attribute does not exist |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("accessUserDefinedAttributes")` or its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)` method denies write access to the file. |

### list

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun list(): MutableList<String!>!
```

Returns a list containing the names of the user-defined attributes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | An unmodifiable list containing the names of the file's user-defined |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("accessUserDefinedAttributes")` or its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)` method denies read access to the file. |

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun name(): String!
```

Returns the name of this attribute view. Attribute views of this type have the name `"user"`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the attribute view |

### read

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun read(
    name: String!, 
    dst: ByteBuffer!
): Int
```

Read the value of a user-defined attribute into a buffer.

This method reads the value of the attribute into the given buffer as a sequence of bytes, failing if the number of bytes remaining in the buffer is insufficient to read the complete attribute value. The number of bytes transferred into the buffer is `n`, where `n` is the size of the attribute value. The first byte in the sequence is at index `p` and the last byte is at index `p + n - 1`, where `p` is the buffer's position. Upon return the buffer's position will be equal to `p + n`; its limit will not have changed.

**Usage Example:** Suppose we want to read a file's MIME type that is stored as a user-defined attribute with the name "`user.mimetype`".

```kotlin
UserDefinedFileAttributeView view =
         Files.getFileAttributeView(path, UserDefinedFileAttributeView.class);
     String name = "user.mimetype";
     ByteBuffer buf = ByteBuffer.allocate(view.size(name));
     view.read(name, buf);
     buf.flip();
     String value = Charset.defaultCharset().decode(buf).toString();
  
```

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The attribute name |
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The destination buffer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes read, possibly zero |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs or there is insufficient space in the destination buffer for the attribute value |
| `java.lang.IllegalArgumentException` | If the destination buffer is read-only |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("accessUserDefinedAttributes")` or its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)` method denies read access to the file. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView#size(kotlin.String)`

### size

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun size(name: String!): Int
```

Returns the size of the value of a user-defined attribute.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The attribute name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size of the attribute value, in bytes. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.ArithmeticException` | If the size of the attribute is larger than `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int` |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("accessUserDefinedAttributes")` or its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)` method denies read access to the file. |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun write(
    name: String!, 
    src: ByteBuffer!
): Int
```

Writes the value of a user-defined attribute from a buffer.

This method writes the value of the attribute from a given buffer as a sequence of bytes. The size of the value to transfer is `r`, where `r` is the number of bytes remaining in the buffer, that is `src.remaining()`. The sequence of bytes is transferred from the buffer starting at index `p`, where `p` is the buffer's position. Upon return, the buffer's position will be equal to `p + n`, where `n` is the number of bytes transferred; its limit will not have changed.

If an attribute of the given name already exists then its value is replaced. If the attribute does not exist then it is created. If it implementation specific if a test to check for the existence of the attribute and the creation of attribute are atomic with respect to other file system activities.

Where there is insufficient space to store the attribute, or the attribute name or value exceed an implementation specific maximum size then an `IOException` is thrown.

**Usage Example:** Suppose we want to write a file's MIME type as a user-defined attribute:

```kotlin
UserDefinedFileAttributeView view =
         FIles.getFileAttributeView(path, UserDefinedFileAttributeView.class);
     view.write("user.mimetype", Charset.defaultCharset().encode("text/html"));
  
```

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The attribute name |
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!: The buffer containing the attribute value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes written, possibly zero |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#``("accessUserDefinedAttributes")` or its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String)` method denies write access to the file. |
