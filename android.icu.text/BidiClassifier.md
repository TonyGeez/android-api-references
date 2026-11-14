# BidiClassifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BidiClassifier

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/BidiClassifier "View this page in Java") 

```
open class BidiClassifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier#) |

Overrides default Bidi class values with custom ones.

The override mechanism requires to define a subclass of`BidiClassifier`which overrides the`classifier`method to assign customized Bidi classes.

This may be useful for assigning Bidi classes to PUA characters, or for special application needs. For instance, an application may want to handle all spaces like L or R characters (according to the base direction) when creating the visual ordering of logical lines which are part of a report organized in columns: there should not be interaction between adjacent cells.

To start using this customized classifier with a Bidi object, it must be specified by calling the`Bidi.setCustomClassifier`method; after that, the method`classify`of the custom`BidiClassifier`will be called by the UBA implementation any time the class of a character is to be determined.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier#BidiClassifier(kotlin.Any))`(`context:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [classify](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier#classify(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets customized Bidi class for the code point`c`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContext](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier#getContext())`()` Returns the current classifier context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier#setContext(kotlin.Any))`(`context:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets classifier context, which can be used either by a caller or callee for various purposes. |

## Public constructors

### BidiClassifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BidiClassifier(context: Any!)
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Context for this classifier instance. May be null. |

## Public methods

### classify

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun classify(c: Int): Int
```

Gets customized Bidi class for the code point`c`.

Default implementation, to be overridden.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Code point to be classified. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer representing directional property / Bidi class for the given code point`c`, or UCharacter.getIntPropertyMaxValue(UProperty.BIDI_CLASS)+1 to signify that there is no need to override the standard Bidi class for the given code point. |

### getContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Any!
```

Returns the current classifier context. 

### setContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: Any!): Unit
```

Sets classifier context, which can be used either by a caller or callee for various purposes.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Context for this classifier instance. May be null. |
