# FileAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileAttribute

```
interface FileAttribute<T : Any!>
```

| [java.nio.file.attribute.FileAttribute](../java/nio/file/attribute/FileAttribute.md) |

An object that encapsulates the value of a file attribute that can be set atomically when creating a new file or directory by invoking the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/nio/file/attribute/FileAttribute.md))`()` Returns the attribute name. |
| abstractT | [value](../java/nio/file/attribute/FileAttribute.md))`()` Returns the attribute value. |

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
