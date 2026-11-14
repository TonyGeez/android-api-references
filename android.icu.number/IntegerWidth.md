# IntegerWidth

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntegerWidth

Kotlin | [Java](../android/icu/number/IntegerWidth.md) 
| --- | --- |

```
open class IntegerWidth
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.IntegerWidth](../android/icu/number/IntegerWidth.md) |

A class that defines the strategy for padding and truncating integers before the decimal separator.

To create an IntegerWidth, use one of the factory methods.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntegerWidth](../android/icu/number/IntegerWidth.md)! | [truncateAt](../android/icu/number/IntegerWidth.md))`(`maxInt:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Truncate numbers exceeding a certain number of numerals before the decimal separator. |
| open static [IntegerWidth](../android/icu/number/IntegerWidth.md)! | [zeroFillTo](../android/icu/number/IntegerWidth.md))`(`minInt:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pad numbers at the beginning with zeros to guarantee a certain number of numerals before the decimal separator. |

## Public methods

### truncateAt

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun truncateAt(maxInt: Int): IntegerWidth!
```

Truncate numbers exceeding a certain number of numerals before the decimal separator. For example, with maxInt=3, the number 1234 will get printed as "234".

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxInt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of places before the decimal separator. maxInt == -1 means no truncation. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [IntegerWidth](../android/icu/number/IntegerWidth.md)! | An IntegerWidth for passing to the NumberFormatter integerWidth() setter. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than -1. |

**See Also**

- [android.icu.number.NumberFormatter](../android/icu/number/NumberFormatter.md) 

### zeroFillTo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun zeroFillTo(minInt: Int): IntegerWidth!
```

Pad numbers at the beginning with zeros to guarantee a certain number of numerals before the decimal separator.

For example, with minInt=3, the number 55 will get printed as "055".

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `minInt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of places before the decimal separator. |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [IntegerWidth](../android/icu/number/IntegerWidth.md)! | An IntegerWidth for chaining or passing to the NumberFormatter integerWidth() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 0. |

**See Also**

- [android.icu.number.NumberFormatter](../android/icu/number/NumberFormatter.md)
