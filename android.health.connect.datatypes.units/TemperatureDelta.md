# TemperatureDelta

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# TemperatureDelta

Kotlin| [Java](TemperatureDelta.md) 
| --- | --- |

```
class TemperatureDelta : Comparable<TemperatureDelta!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.units.TemperatureDelta](TemperatureDelta.md) |

Represents a unit of temperature difference. Supported units: Celsius

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](TemperatureDelta.md))`(`other:` ` [TemperatureDelta](TemperatureDelta.md)`)` Compares this object with the specified object for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](TemperatureDelta.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [TemperatureDelta](TemperatureDelta.md) | [fromCelsius](TemperatureDelta.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Creates a TemperatureDelta object with the specified value in Celsius degrees. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getInCelsius](TemperatureDelta.md))`()` Returns temperature delta in celsius |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](TemperatureDelta.md))`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](TemperatureDelta.md))`()` <br /> |
| --- | --- |

## Public methods

### compareTo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun compareTo(other: TemperatureDelta): Int
```

Compares this object with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [TemperatureDelta](TemperatureDelta.md):the object to be compared. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|----------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the object argument;`false`otherwise. |

### fromCelsius

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static fun fromCelsius(value: Double): TemperatureDelta
```

Creates a TemperatureDelta object with the specified value in Celsius degrees.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value to be set as celsius. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TemperatureDelta](TemperatureDelta.md) | This value cannot be`null`. |

### getInCelsius

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getInCelsius(): Double
```

Returns temperature delta in celsius 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
