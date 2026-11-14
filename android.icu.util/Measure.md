# Measure

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Measure

Kotlin| [Java](../android/icu/util/Measure.md) 
| --- | --- |

```
open class Measure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.Measure](../android/icu/util/Measure.md) |

| Known Direct Subclasses [CurrencyAmount](../android/icu/util/CurrencyAmount.md) |--------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [CurrencyAmount](../android/icu/util/CurrencyAmount.md) | An amount of currency, consisting of a Number and a Currency. | |
| --- | --- | --- | --- | --- | --- | --- |

An amount of a specified unit, consisting of a Number and a Unit. For example, a length measure consists of a Number and a length unit, such as feet or meters.

Measure objects are parsed and formatted by subclasses of MeasureFormat.

Measure objects are immutable. All subclasses must guarantee that. (However, subclassing is discouraged.)

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Measure](../android/icu/util/Measure.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `unit:` ` [MeasureUnit](../android/icu/util/MeasureUnit.md)!`)` Constructs a new object given a number and a unit. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/util/Measure.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the given object is equal to this object. |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getNumber](../android/icu/util/Measure.md))`()` Returns the numeric value of this object. |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [getUnit](../android/icu/util/Measure.md))`()` Returns the unit of this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/util/Measure.md))`()` Returns a hashcode for this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/util/Measure.md))`()` Returns a string representation of this object. |

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
| `unit` | [MeasureUnit](../android/icu/util/MeasureUnit.md)!:the unit |

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
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | this object's Unit |

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
