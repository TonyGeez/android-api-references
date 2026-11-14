# Transformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformation

Kotlin| [Java](Transformation.md) 
| --- | --- |

```
open class Transformation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.animation.Transformation](Transformation.md) |

Defines the transformation to be applied at one point in time of an Animation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALPHA](Transformation.md) Indicates a transformation that applies an alpha only (uses an identity matrix.) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOTH](Transformation.md) Indicates a transformation that applies an alpha and a matrix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IDENTITY](Transformation.md) Indicates a transformation that has no effect (alpha = 1 and identity matrix.) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MATRIX](Transformation.md) Indicates a transformation that applies a matrix only (alpha = 1.) |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Transformation](Transformation.md))`()` Creates a new transformation with alpha = 1 and the identity matrix. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](Transformation.md))`()` Reset the transformation to a state that leaves the object being animated in an unmodified state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [compose](Transformation.md))`(`t:` ` [Transformation](Transformation.md)!`)` Apply this Transformation to an existing Transformation, e. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAlpha](Transformation.md))`()` <br /> |
| --- | --- |
| open [Matrix](../android.graphics/Matrix.md)! | [getMatrix](Transformation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransformationType](Transformation.md))`()` Indicates the nature of this transformation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](Transformation.md))`(`t:` ` [Transformation](Transformation.md)!`)` Clones the specified transformation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](Transformation.md))`(`alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the degree of transparency |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransformationType](Transformation.md))`(`transformationType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the transformation type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toShortString](Transformation.md))`()` Return a string representation of the transformation in a compact form. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Transformation.md))`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [mAlpha](Transformation.md) <br /> |
| [Matrix](../android.graphics/Matrix.md)! | [mMatrix](Transformation.md) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mTransformationType](Transformation.md) <br /> |
| --- | --- |

## Constants

### TYPE_ALPHA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALPHA: Int
```

Indicates a transformation that applies an alpha only (uses an identity matrix.) 

 Value: 1

### TYPE_BOTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BOTH: Int
```

Indicates a transformation that applies an alpha and a matrix. 

 Value: 3

### TYPE_IDENTITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IDENTITY: Int
```

Indicates a transformation that has no effect (alpha = 1 and identity matrix.) 

 Value: 0

### TYPE_MATRIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MATRIX: Int
```

Indicates a transformation that applies a matrix only (alpha = 1.) 

 Value: 2

## Public constructors

### Transformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Transformation()
```

Creates a new transformation with alpha = 1 and the identity matrix.

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Reset the transformation to a state that leaves the object being animated in an unmodified state. The transformation type is [TYPE_BOTH](Transformation.md) by default. 

### compose

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compose(t: Transformation!): Unit
```

Apply this Transformation to an existing Transformation, e.g. apply a scale effect to something that has already been rotated.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `t` | [Transformation](Transformation.md)!: |

### getAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlpha(): Float
```

| Return ||
|--------------------------------------------------------------------------------|----------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The degree of transparency |

### getMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMatrix(): Matrix!
```

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Matrix](../android.graphics/Matrix.md)! | The 3x3 Matrix representing the transformation to apply to the coordinates of the object being animated |

### getTransformationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformationType(): Int
```

Indicates the nature of this transformation.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALPHA](Transformation.md), [TYPE_MATRIX](Transformation.md), [TYPE_BOTH](Transformation.md) or [TYPE_IDENTITY](Transformation.md). |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(t: Transformation!): Unit
```

Clones the specified transformation.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Transformation](Transformation.md)!:The transformation to clone. |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlpha(alpha: Float): Unit
```

Sets the degree of transparency

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):1.0 means fully opaque and 0.0 means fully transparent Value is between 0.0f and 1.0f inclusive |

### setTransformationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTransformationType(transformationType: Int): Unit
```

Sets the transformation type.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transformationType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [TYPE_ALPHA](Transformation.md), [TYPE_MATRIX](Transformation.md), [TYPE_BOTH](Transformation.md) or [TYPE_IDENTITY](Transformation.md). |

### toShortString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toShortString(): String!
```

Return a string representation of the transformation in a compact form. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### mAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mAlpha: Float
```  

### mMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mMatrix: Matrix!
```  

### mTransformationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mTransformationType: Int
```
