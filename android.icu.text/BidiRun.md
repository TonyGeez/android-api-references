# BidiRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BidiRun

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/BidiRun "View this page in Java") 
| --- | --- |

```
open class BidiRun
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#) |

A BidiRun represents a sequence of characters at the same embedding level. The Bidi algorithm decomposes a piece of text into sequences of characters at the same embedding level, each such sequence is called a "run".

A BidiRun represents such a run by storing its essential properties, but does not duplicate the characters which form the run.

The "limit" of the run is the position just after the last character, i.e., one more than that position.

This class has no public constructor, and its members cannot be modified by users.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getDirection](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getDirection())`()` Get direction of run |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getEmbeddingLevel](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getEmbeddingLevel())`()` Get level of run |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getLength())`()` Get length of run |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLimit](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getLimit())`()` Get position of one character after the end of the run in the source text |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStart](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getStart())`()` Get the first logical position of the run in the source text |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEvenRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#isEvenRun())`()` Check if run level is even |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOddRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#isOddRun())`()` Check if run level is odd |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#toString())`()` String to display run |

## Public methods

### getDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirection(): Byte
```

Get direction of run 

### getEmbeddingLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmbeddingLevel(): Byte
```

Get level of run 

### getLength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Int
```

Get length of run 

### getLimit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLimit(): Int
```

Get position of one character after the end of the run in the source text 

### getStart

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStart(): Int
```

Get the first logical position of the run in the source text 

### isEvenRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEvenRun(): Boolean
```

Check if run level is even

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the embedding level of this run is even, i.e. it is a left-to-right run. |

### isOddRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOddRun(): Boolean
```

Check if run level is odd

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the embedding level of this run is odd, i.e. it is a right-to-left run. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

String to display run

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
