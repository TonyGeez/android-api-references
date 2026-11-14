# Number

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Number

```
abstract class Number : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Number](../java/lang/Number.md) |

The abstract class`Number`is the superclass of platform classes representing numeric values that are convertible to the primitive types`byte`,`double`,`float`,`int`,`long`, and`short`. The specific semantics of the conversion from the numeric value of a particular`Number`implementation to a given primitive type is defined by the`Number`implementation in question. For platform classes, the conversion is often analogous to a narrowing primitive conversion or a widening primitive conversion as defined in The Java Language Specification for converting between primitive types. Therefore, conversions may lose information about the overall magnitude of a numeric value, may lose precision, and may even return a result of a different sign than the input. See the documentation of a given`Number`implementation for conversion details.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [Number](../java/lang/Number.md))`()` Constructor for subclasses to call. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [byteValue](../java/lang/Number.md))`()` Returns the value of the specified number as a`byte`. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [doubleValue](../java/lang/Number.md))`()` Returns the value of the specified number as a`double`. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [floatValue](../java/lang/Number.md))`()` Returns the value of the specified number as a`float`. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [intValue](../java/lang/Number.md))`()` Returns the value of the specified number as an`int`. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [longValue](../java/lang/Number.md))`()` Returns the value of the specified number as a`long`. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [shortValue](../java/lang/Number.md))`()` Returns the value of the specified number as a`short`. |
| --- | --- |

## Public constructors

### Number

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Number()
```

Constructor for subclasses to call.

## Public methods

### byteValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun byteValue(): Byte
```

Returns the value of the specified number as a`byte`.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the numeric value represented by this object after conversion to type`byte`. |

### doubleValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doubleValue(): Double
```

Returns the value of the specified number as a`double`.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### floatValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun floatValue(): Float
```

Returns the value of the specified number as a`float`.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### intValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun intValue(): Int
```

Returns the value of the specified number as an`int`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### longValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun longValue(): Long
```

Returns the value of the specified number as a`long`.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### shortValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shortValue(): Short
```

Returns the value of the specified number as a`short`.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the numeric value represented by this object after conversion to type`short`. |
