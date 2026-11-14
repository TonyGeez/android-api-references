# TextDirectionHeuristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextDirectionHeuristic

Kotlin| [Java](TextDirectionHeuristic.md) 
| --- | --- |

```
interface TextDirectionHeuristic
```

| [android.text.TextDirectionHeuristic](TextDirectionHeuristic.md) |

Interface for objects that use a heuristic for guessing at the paragraph direction by examining text.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtl](TextDirectionHeuristic.md))`(`array:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Guess if a chars array is in the RTL direction or not. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtl](TextDirectionHeuristic.md))`(`cs:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Guess if a`CharSequence`is in the RTL direction or not. |

## Public methods

### isRtl

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRtl(
    array: CharArray!, 
    start: Int, 
    count: Int
): Boolean
```

Guess if a chars array is in the RTL direction or not.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the char array. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):start index, inclusive. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length to check, must not be negative and not greater than`array.length - start`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if all chars in the range are to be considered in a RTL direction, false otherwise. |

### isRtl

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRtl(
    cs: CharSequence!, 
    start: Int, 
    count: Int
): Boolean
```

Guess if a`CharSequence`is in the RTL direction or not.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the CharSequence. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):start index, inclusive. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length to check, must not be negative and not greater than`CharSequence.length() - start`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if all chars in the range are to be considered in a RTL direction, false otherwise. |
