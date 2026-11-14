# Energy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Energy

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/units/Energy "View this page in Java") 
| --- | --- |

```
class Energy : Comparable<Energy!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.units.Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#) |

Represents a unit of energy. Supported units: calories

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#compareTo(android.health.connect.datatypes.units.Energy))`(`other:` ` [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#)`)` Compares this object with the specified object for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#) | [fromCalories](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#fromCalories(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Creates an Energy object with the specified value in calories. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getInCalories](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#getInCalories())`()` Returns energy in calories |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#toString())`()` <br /> |
| --- | --- |

## Public methods

### compareTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Energy): Int
```

Compares this object with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#):the object to be compared. This value cannot be`null`. |

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

### fromCalories

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromCalories(value: Double): Energy
```

Creates an Energy object with the specified value in calories.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value to be set as calories. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy#) | This value cannot be`null`. |

### getInCalories

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInCalories(): Double
```

Returns energy in calories 

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
