# ZipPathValidator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipPathValidator

```
class ZipPathValidator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [dalvik.system.ZipPathValidator](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator#) |

Enables validation of zip file entry paths to prevent exploitation of the path traversal vulnerability, e.g. zip path entries containing ".." or "/". For more details, read [this](https://developer.android.com/topic/security/risks/zip-path-traversal).

The default implementation accepts all zip file entry paths without raising any exceptions.

For custom validation rules, the core functionality should be implemented in a [Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback) interface and that instance should be set in [setCallback(dalvik.system.ZipPathValidator.Callback)](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator#setCallback(dalvik.system.ZipPathValidator.Callback)).

Existing validation could be set to a default one by calling [clearCallback()](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator#clearCallback()).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback) Interface that defines the core validation mechanism when accessing zip file entry paths. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearCallback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator#clearCallback())`()` Clears the current validation mechanism by setting the current callback instance to a default validation. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCallback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator#setCallback(dalvik.system.ZipPathValidator.Callback))`(`callback:` ` [ZipPathValidator.Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback)`)` Sets the current callback implementation for zip paths. |

## Public methods

### clearCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun clearCallback(): Unit
```

Clears the current validation mechanism by setting the current callback instance to a default validation. 

### setCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setCallback(callback: ZipPathValidator.Callback): Unit
```

Sets the current callback implementation for zip paths.

The provided callback should not perform IO or any blocking operations, but only perform path validation. A typical implementation will validate String entries in a single pass and throw a [ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException.html#) if the path contains potentially hazardous components such as "..".

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ZipPathValidator.Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback):An instance of [Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback)'s implementation. This value cannot be`null`. |
