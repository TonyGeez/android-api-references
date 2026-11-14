# TracingConfig

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TracingConfig

Kotlin| [Java](https://developer.android.com/reference/android/webkit/TracingConfig "View this page in Java") 
| --- | --- |

```
open class TracingConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.TracingConfig](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#) |

Holds tracing configuration information and predefined settings.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig.Builder) Builder used to create [TracingConfig](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_ALL](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_ALL:kotlin.Int) Predefined set of categories, includes all categories enabled by default in chromium. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_ANDROID_WEBVIEW](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_ANDROID_WEBVIEW:kotlin.Int) Predefined set of categories typically useful for analyzing WebViews. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_FRAME_VIEWER](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_FRAME_VIEWER:kotlin.Int) Predefined set of categories for studying difficult rendering performance problems. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_INPUT_LATENCY](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_INPUT_LATENCY:kotlin.Int) Predefined set of categories for analyzing input latency issues. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_JAVASCRIPT_AND_RENDERING](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_JAVASCRIPT_AND_RENDERING:kotlin.Int) Predefined set of categories for analyzing javascript and rendering issues. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_NONE](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_NONE:kotlin.Int) Indicates that there are no predefined categories. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_RENDERING](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_RENDERING:kotlin.Int) Predefined set of categories for analyzing rendering issues. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORIES_WEB_DEVELOPER](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_WEB_DEVELOPER:kotlin.Int) Predefined set of categories typically useful for web developers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORD_CONTINUOUSLY](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_CONTINUOUSLY:kotlin.Int) Record trace events continuously using an internal ring buffer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORD_UNTIL_FULL](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_UNTIL_FULL:kotlin.Int) Record trace events until the internal tracing buffer is full. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCustomIncludedCategories](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#getCustomIncludedCategories())`()` Returns the list of included custom category patterns for this configuration. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPredefinedCategories](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#getPredefinedCategories())`()` Returns a bitmask of the predefined category sets of this configuration. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTracingMode](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#getTracingMode())`()` Returns the tracing mode of this configuration. |
| --- | --- |

## Constants

### CATEGORIES_ALL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_ALL: Int
```

Predefined set of categories, includes all categories enabled by default in chromium. Use with caution: this setting may produce large trace output. 

 Value: 1

### CATEGORIES_ANDROID_WEBVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_ANDROID_WEBVIEW: Int
```

Predefined set of categories typically useful for analyzing WebViews. Typically includes "android_webview" and "Java" categories. 

 Value: 2

### CATEGORIES_FRAME_VIEWER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_FRAME_VIEWER: Int
```

Predefined set of categories for studying difficult rendering performance problems. Typically includes "blink", "compositor", "gpu", "renderer.scheduler", "v8" and some other compositor categories which are disabled by default. 

 Value: 64

### CATEGORIES_INPUT_LATENCY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_INPUT_LATENCY: Int
```

Predefined set of categories for analyzing input latency issues. Typically includes "input", "renderer.scheduler" categories. 

 Value: 8

### CATEGORIES_JAVASCRIPT_AND_RENDERING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_JAVASCRIPT_AND_RENDERING: Int
```

Predefined set of categories for analyzing javascript and rendering issues. Typically includes "blink", "compositor", "gpu", "renderer.scheduler" and "v8" categories. 

 Value: 32

### CATEGORIES_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_NONE: Int
```

Indicates that there are no predefined categories. 

 Value: 0

### CATEGORIES_RENDERING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_RENDERING: Int
```

Predefined set of categories for analyzing rendering issues. Typically includes "blink", "compositor" and "gpu" categories. 

 Value: 16

### CATEGORIES_WEB_DEVELOPER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORIES_WEB_DEVELOPER: Int
```

Predefined set of categories typically useful for web developers. Typically includes "blink", "compositor", "renderer.scheduler" and "v8" categories. 

 Value: 4

### RECORD_CONTINUOUSLY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORD_CONTINUOUSLY: Int
```

Record trace events continuously using an internal ring buffer. Default tracing mode. Overwrites old events if they exceed buffer capacity. Uses less memory than the [RECORD_UNTIL_FULL](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_UNTIL_FULL:kotlin.Int) mode. Depending on the implementation typically allows up to 64k events to be stored. 

 Value: 1

### RECORD_UNTIL_FULL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORD_UNTIL_FULL: Int
```

Record trace events until the internal tracing buffer is full. Typically the buffer memory usage is larger than [RECORD_CONTINUOUSLY](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_CONTINUOUSLY:kotlin.Int). Depending on the implementation typically allows up to 256k events to be stored. 

 Value: 0

## Public methods

### getCustomIncludedCategories

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCustomIncludedCategories(): MutableList<String!>
```

Returns the list of included custom category patterns for this configuration.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | Empty list if no custom category patterns are specified. This value cannot be`null`. |

### getPredefinedCategories

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPredefinedCategories(): Int
```

Returns a bitmask of the predefined category sets of this configuration.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Bitmask of predefined category sets. Value is either`0`or a combination of [android.webkit.TracingConfig#CATEGORIES_NONE](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_NONE:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_ALL](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_ALL:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_ANDROID_WEBVIEW](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_ANDROID_WEBVIEW:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_WEB_DEVELOPER](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_WEB_DEVELOPER:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_INPUT_LATENCY](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_INPUT_LATENCY:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_RENDERING](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_RENDERING:kotlin.Int), [android.webkit.TracingConfig#CATEGORIES_JAVASCRIPT_AND_RENDERING](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_JAVASCRIPT_AND_RENDERING:kotlin.Int), and [android.webkit.TracingConfig#CATEGORIES_FRAME_VIEWER](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#CATEGORIES_FRAME_VIEWER:kotlin.Int) |

### getTracingMode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTracingMode(): Int
```

Returns the tracing mode of this configuration.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The tracing mode of this configuration. Value is [android.webkit.TracingConfig#RECORD_UNTIL_FULL](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_UNTIL_FULL:kotlin.Int), or [android.webkit.TracingConfig#RECORD_CONTINUOUSLY](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig#RECORD_CONTINUOUSLY:kotlin.Int) |
