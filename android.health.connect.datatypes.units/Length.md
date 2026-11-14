# Length

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Length

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/units/Length "View this page in Java") 
| --- | --- |

```
class Length : Comparable<Length!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.units.Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#) |

Represents a unit of length. Supported units: meters

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#compareTo(android.health.connect.datatypes.units.Length))`(`other:` ` [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#)`)` Compares this object with the specified object for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#) | [fromMeters](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#fromMeters(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Creates a Length object with the specified value in meters. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getInMeters](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#getInMeters())`()` Returns length in meters |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#toString())`()` <br /> |
| --- | --- |

## Public methods

### compareTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Length): Int
```

Compares this object with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#):the object to be compared. This value cannot be`null`. |

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

### fromMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromMeters(value: Double): Length
```

Creates a Length object with the specified value in meters.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value to be set as meters. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length#) | This value cannot be`null`. |

### getInMeters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInMeters(): Double
```

Returns length in meters 

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
