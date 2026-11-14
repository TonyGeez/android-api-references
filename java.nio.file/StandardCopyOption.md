# StandardCopyOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardCopyOption

```
class StandardCopyOption : CopyOption
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#)\> ||
| | ↳ | [java.nio.file.StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#) |

| Known Direct Subclasses [StandardCopyOption.ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:ATOMIC_MOVE), [StandardCopyOption.COPY_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:COPY_ATTRIBUTES), [StandardCopyOption.REPLACE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:REPLACE_EXISTING) |----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------| | [StandardCopyOption.ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:ATOMIC_MOVE) | Move the file as an atomic file system operation. | | [StandardCopyOption.COPY_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:COPY_ATTRIBUTES) | Copy attributes to the new file. | | [StandardCopyOption.REPLACE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:REPLACE_EXISTING) | Replace an existing file if it exists. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the standard copy options.

## Summary

| Enum values ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:ATOMIC_MOVE) Move the file as an atomic file system operation. |
| [COPY_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:COPY_ATTRIBUTES) Copy attributes to the new file. |
| [REPLACE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:REPLACE_EXISTING) Replace an existing file if it exists. |

## Enum values

### ATOMIC_MOVE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ATOMIC_MOVE : StandardCopyOption
```

Move the file as an atomic file system operation. 

### COPY_ATTRIBUTES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val COPY_ATTRIBUTES : StandardCopyOption
```

Copy attributes to the new file. 

### REPLACE_EXISTING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REPLACE_EXISTING : StandardCopyOption
```

Replace an existing file if it exists.
