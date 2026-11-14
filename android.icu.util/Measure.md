# Measure

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Measure

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/Measure "View this page in Java") 
| --- | --- |

```
open class Measure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure#) |

| Known Direct Subclasses [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount) |--------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount) | An amount of currency, consisting of a Number and a Currency. | |
| --- | --- | --- | --- | --- | --- | --- |

An amount of a specified unit, consisting of a Number and a Unit. For example, a length measure consists of a Number and a length unit, such as feet or meters.

Measure objects are parsed and formatted by subclasses of MeasureFormat.

Measure objects are immutable. All subclasses must guarantee that. (However, subclassing is discouraged.)

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure#Measure(kotlin.Number,%20android.icu.util.MeasureUnit))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `unit:` ` [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!`)` Constructs a new object given a number and a unit. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/util/Measure#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the given object is equal to this object. |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getNumber](https://developer.android.com/reference/kotlin/android/icu/util/Measure#getNumber())`()` Returns the numeric value of this object. |
| open [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [getUnit](https://developer.android.com/reference/kotlin/android/icu/util/Measure#getUnit())`()` Returns the unit of this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/util/Measure#hashCode())`()` Returns a hashcode for this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/util/Measure#toString())`()` Returns a string representation of this object. |

## Public constructors

### Measure

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Measure(
    number: Number!, 
    unit: MeasureUnit!)
```

Constructs a new object given a number and a unit.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `number` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:the number |
| `unit` | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!:the unit |

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Returns true if the given object is equal to this object.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this object is equal to the given object |

### getNumber

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumber(): Number!
```

Returns the numeric value of this object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | this object's Number |

### getUnit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnit(): MeasureUnit!
```

Returns the unit of this object.

| Return ||
|---------------------------------------------------------------------------------------------|--------------------|
| [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | this object's Unit |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hashcode for this object.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a 32-bit hash |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation consisting of the ISO currency code together with the numeric amount |
