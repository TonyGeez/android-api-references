# Scale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Scale

Kotlin| [Java](Scale.md) 
| --- | --- |

```
open class Scale
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.Scale](Scale.md) |

A class that defines a quantity by which a number should be multiplied when formatting.

To create a Multiplier, use one of the factory methods.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Scale](Scale.md)! | [byBigDecimal](Scale.md))`(`multiplicand:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` Multiply numbers by an arbitrary value before formatting. |
| openstatic [Scale](Scale.md)! | [byDouble](Scale.md))`(`multiplicand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Multiply numbers by an arbitrary value before formatting. |
| openstatic [Scale](Scale.md)! | [byDoubleAndPowerOfTen](Scale.md))`(`multiplicand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `power:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiply a number by both a power of ten and by an arbitrary double value before formatting. |
| --- | --- |
| openstatic [Scale](Scale.md)! | [none](Scale.md))`()` Do not change the value of numbers when formatting or parsing. |
| openstatic [Scale](Scale.md)! | [powerOfTen](Scale.md))`(`power:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiply numbers by 100 before formatting. |

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
| [Scale](Scale.md)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md) 

### byDouble

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byDouble(multiplicand: Double): Scale!
```

Multiply numbers by an arbitrary value before formatting. Useful for unit conversions.

This method takes a double; also see the version that takes a BigDecimal.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Scale](Scale.md)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md) 

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
| [Scale](Scale.md)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md) 

### none

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun none(): Scale!
```

Do not change the value of numbers when formatting or parsing.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Scale](Scale.md)! | A Multiplier to prevent any multiplication. |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md) 

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
| [Scale](Scale.md)! | A Multiplier for passing to the setter in NumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md)
