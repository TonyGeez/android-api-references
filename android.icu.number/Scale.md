# Scale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Scale

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/Scale "View this page in Java") 

```
open class Scale
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.number.Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#) |

A class that defines a quantity by which a number should be multiplied when formatting.

To create a Multiplier, use one of the factory methods.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | [byBigDecimal](https://developer.android.com/reference/kotlin/android/icu/number/Scale#byBigDecimal(java.math.BigDecimal))`(`multiplicand:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Multiply numbers by an arbitrary value before formatting. |
| openstatic [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | [byDouble](https://developer.android.com/reference/kotlin/android/icu/number/Scale#byDouble(kotlin.Double))`(`multiplicand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Multiply numbers by an arbitrary value before formatting. |
| openstatic [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | [byDoubleAndPowerOfTen](https://developer.android.com/reference/kotlin/android/icu/number/Scale#byDoubleAndPowerOfTen(kotlin.Double,%20kotlin.Int))`(`multiplicand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `power:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiply a number by both a power of ten and by an arbitrary double value before formatting. |
| openstatic [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | [none](https://developer.android.com/reference/kotlin/android/icu/number/Scale#none())`()` Do not change the value of numbers when formatting or parsing. |
| openstatic [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | [powerOfTen](https://developer.android.com/reference/kotlin/android/icu/number/Scale#powerOfTen(kotlin.Int))`(`power:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiply numbers by 100 before formatting. |

## Public methods

### byBigDecimal

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byBigDecimal(multiplicand: BigDecimal!): Scale!
```

Multiply numbers by an arbitrary value before formatting. Useful for unit conversions.

This method takes a BigDecimal; also see the version that takes a double.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### byDouble

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byDouble(multiplicand: Double): Scale!
```

Multiply numbers by an arbitrary value before formatting. Useful for unit conversions.

This method takes a double; also see the version that takes a BigDecimal.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### byDoubleAndPowerOfTen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byDoubleAndPowerOfTen(
    multiplicand: Double, 
    power: Int
): Scale!
```

Multiply a number by both a power of ten and by an arbitrary double value before formatting.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### none

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun none(): Scale!
```

Do not change the value of numbers when formatting or parsing.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | A Multiplier to prevent any multiplication. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### powerOfTen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun powerOfTen(power: Int): Scale!
```

Multiply numbers by 100 before formatting. Useful for combining with a percent unit: 

```kotlin
NumberFormatter.with().unit(NoUnit.PERCENT).multiplier(Multiplier.powerOfTen(2))
  
```

<br />

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale#)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
