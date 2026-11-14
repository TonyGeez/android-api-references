# FileAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileAttribute

```
interface FileAttribute<T : Any!>
```

| [java.nio.file.attribute.FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#) |

An object that encapsulates the value of a file attribute that can be set atomically when creating a new file or directory by invoking the [createFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createFile(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))or [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))methods.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#name())`()` Returns the attribute name. |
| abstractT | [value](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#value())`()` Returns the attribute value. |

## Public methods

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the attribute name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The attribute name |

### value

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun value(): T
```

Returns the attribute value.

| Return ||
|---|---------------------|
| T | The attribute value |
