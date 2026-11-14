# Power

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Power

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/units/Power "View this page in Java") 
| --- | --- |

```
class Power : Comparable<Power!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.units.Power](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#) |

Represents a unit of power. Supported units: watts

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#compareTo(android.health.connect.datatypes.units.Power))`(`other:` ` [Power](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#)`)` Compares this object with the specified object for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Power](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#) | [fromWatts](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#fromWatts(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Creates a Power object with the specified value in Watts. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getInWatts](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#getInWatts())`()` Returns power in watts |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#toString())`()` <br /> |
| --- | --- |

## Public methods

### compareTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Power): Int
```

Compares this object with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [Power](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#):the object to be compared. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### fromWatts

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromWatts(value: Double): Power
```

Creates a Power object with the specified value in Watts.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value to be set as watts. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------|
| [Power](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Power#) | This value cannot be`null`. |

### getInWatts

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInWatts(): Double
```

Returns power in watts 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
