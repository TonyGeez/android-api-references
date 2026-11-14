# LayoutDirection

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayoutDirection

Kotlin| [Java](https://developer.android.com/reference/android/util/LayoutDirection "View this page in Java") 
| --- | --- |

```
class LayoutDirection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection#) |

A class for defining layout directions. A layout direction can be left-to-right (LTR) or right-to-left (RTL). It can also be inherited (from a parent) or deduced from the default language script of a locale.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INHERIT](https://developer.android.com/reference/kotlin/android/util/LayoutDirection#INHERIT:kotlin.Int) Horizontal layout direction is inherited. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCALE](https://developer.android.com/reference/kotlin/android/util/LayoutDirection#LOCALE:kotlin.Int) Horizontal layout direction is deduced from the default language script for the locale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LTR](https://developer.android.com/reference/kotlin/android/util/LayoutDirection#LTR:kotlin.Int) Horizontal layout direction is from Left to Right. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RTL](https://developer.android.com/reference/kotlin/android/util/LayoutDirection#RTL:kotlin.Int) Horizontal layout direction is from Right to Left. |

## Constants

### INHERIT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INHERIT: Int
```

Horizontal layout direction is inherited. 

 Value: 2

### LOCALE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCALE: Int
```

Horizontal layout direction is deduced from the default language script for the locale. 

 Value: 3

### LTR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTR: Int
```

Horizontal layout direction is from Left to Right. 

 Value: 0

### RTL

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTL: Int
```

Horizontal layout direction is from Right to Left. 

 Value: 1
