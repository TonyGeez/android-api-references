# DisplayHashResultCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayHashResultCallback

Kotlin| [Java](DisplayHashResultCallback.md) 
| --- | --- |

```
interface DisplayHashResultCallback
```

| [android.view.displayhash.DisplayHashResultCallback](DisplayHashResultCallback.md) |

Use when calling [View.generateDisplayHash(String, Rect, Executor,](../android.view/View.md)). The callback will only invoke either [onDisplayHashResult](DisplayHashResultCallback.md))when the system successfully generated the [DisplayHash](DisplayHash.md) or [onDisplayHashError(int)](DisplayHashResultCallback.md))when it failed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_INVALID_BOUNDS](DisplayHashResultCallback.md) The bounds used when requesting the hash hash were invalid or empty. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_INVALID_HASH_ALGORITHM](DisplayHashResultCallback.md) The hash algorithm sent to generate the hash was invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_MISSING_WINDOW](DisplayHashResultCallback.md) The window for the view that requested the hash is no longer around. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_NOT_VISIBLE_ON_SCREEN](DisplayHashResultCallback.md) The view that requested the hash is not visible on screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_TOO_MANY_REQUESTS](DisplayHashResultCallback.md) The caller requested to generate the hash too frequently. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_HASH_ERROR_UNKNOWN](DisplayHashResultCallback.md) An unknown error occurred. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayHashError](DisplayHashResultCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when [android.view.View#generateDisplayHash(String, Rect, Executor, * DisplayHashResultCallback)](../android.view/View.md))results in an error and cannot generate a display hash. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayHashResult](DisplayHashResultCallback.md))`(`displayHash:` ` [DisplayHash](DisplayHash.md)`)` Callback invoked when calling [android.view.View#generateDisplayHash(String, Rect, Executor, * DisplayHashResultCallback)](../android.view/View.md)) |

## Constants

### DISPLAY_HASH_ERROR_INVALID_BOUNDS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_INVALID_BOUNDS: Int
```

The bounds used when requesting the hash hash were invalid or empty. 

 Value: -2

### DISPLAY_HASH_ERROR_INVALID_HASH_ALGORITHM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_INVALID_HASH_ALGORITHM: Int
```

The hash algorithm sent to generate the hash was invalid. This means the value is not one of the supported values in [DisplayHashManager.getSupportedHashAlgorithms()](DisplayHashManager.md)) 

 Value: -5

### DISPLAY_HASH_ERROR_MISSING_WINDOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_MISSING_WINDOW: Int
```

The window for the view that requested the hash is no longer around. This can happen if the window is getting torn down. 

 Value: -3

### DISPLAY_HASH_ERROR_NOT_VISIBLE_ON_SCREEN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_NOT_VISIBLE_ON_SCREEN: Int
```

The view that requested the hash is not visible on screen. This could either mean that the view bounds are offscreen, window bounds are offscreen, view is not visible, or window is not visible. 

 Value: -4

### DISPLAY_HASH_ERROR_TOO_MANY_REQUESTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_TOO_MANY_REQUESTS: Int
```

The caller requested to generate the hash too frequently. The caller should try again at a after some time has passed to ensure the system isn't overloaded. 

 Value: -6

### DISPLAY_HASH_ERROR_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_HASH_ERROR_UNKNOWN: Int
```

An unknown error occurred. 

 Value: -1

## Public methods

### onDisplayHashError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayHashError(errorCode: Int): Unit
```

Callback invoked when [android.view.View#generateDisplayHash(String, Rect, Executor, * DisplayHashResultCallback)](../android.view/View.md))results in an error and cannot generate a display hash.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the error code Value is [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_UNKNOWN](DisplayHashResultCallback.md), [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_INVALID_BOUNDS](DisplayHashResultCallback.md), [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_MISSING_WINDOW](DisplayHashResultCallback.md), [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_NOT_VISIBLE_ON_SCREEN](DisplayHashResultCallback.md), [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_INVALID_HASH_ALGORITHM](DisplayHashResultCallback.md), or [android.view.displayhash.DisplayHashResultCallback#DISPLAY_HASH_ERROR_TOO_MANY_REQUESTS](DisplayHashResultCallback.md) |

### onDisplayHashResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayHashResult(displayHash: DisplayHash): Unit
```

Callback invoked when calling [android.view.View#generateDisplayHash(String, Rect, Executor, * DisplayHashResultCallback)](../android.view/View.md))

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `displayHash` | [DisplayHash](DisplayHash.md):The DisplayHash generated. If the hash cannot be generated, [onDisplayHashError(int)](DisplayHashResultCallback.md))will be called instead This value cannot be`null`. |
