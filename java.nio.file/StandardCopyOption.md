# StandardCopyOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardCopyOption

```
class StandardCopyOption : CopyOption
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.StandardCopyOption](../java/nio/file/StandardCopyOption.md)\> ||
| | ↳ | [java.nio.file.StandardCopyOption](../java/nio/file/StandardCopyOption.md) |

| Known Direct Subclasses [StandardCopyOption.ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md), [StandardCopyOption.COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md), [StandardCopyOption.REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) |----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------| | [StandardCopyOption.ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md) | Move the file as an atomic file system operation. | | [StandardCopyOption.COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md) | Copy attributes to the new file. | | [StandardCopyOption.REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) | Replace an existing file if it exists. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the standard copy options.

## Summary

| Enum values ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md) Move the file as an atomic file system operation. |
| [COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md) Copy attributes to the new file. |
| [REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) Replace an existing file if it exists. |

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
