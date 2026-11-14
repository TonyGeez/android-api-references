# Transformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformation

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/Transformation "View this page in Java") 

```
open class Transformation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.animation.Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#) |

Defines the transformation to be applied at one point in time of an Animation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALPHA](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_ALPHA:kotlin.Int) Indicates a transformation that applies an alpha only (uses an identity matrix.) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BOTH](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_BOTH:kotlin.Int) Indicates a transformation that applies an alpha and a matrix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IDENTITY](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_IDENTITY:kotlin.Int) Indicates a transformation that has no effect (alpha = 1 and identity matrix.) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MATRIX](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_MATRIX:kotlin.Int) Indicates a transformation that applies a matrix only (alpha = 1.) |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#Transformation())`()` Creates a new transformation with alpha = 1 and the identity matrix. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#clear())`()` Reset the transformation to a state that leaves the object being animated in an unmodified state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [compose](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#compose(android.view.animation.Transformation))`(`t:` ` [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#)!`)` Apply this Transformation to an existing Transformation, e. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAlpha](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#getAlpha())`()` <br /> |
| open [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)! | [getMatrix](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#getMatrix())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransformationType](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#getTransformationType())`()` Indicates the nature of this transformation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#set(android.view.animation.Transformation))`(`t:` ` [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#)!`)` Clones the specified transformation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#setAlpha(kotlin.Float))`(`alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the degree of transparency |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransformationType](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#setTransformationType(kotlin.Int))`(`transformationType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the transformation type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toShortString](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#toShortString())`()` Return a string representation of the transformation in a compact form. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#toString())`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [mAlpha](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#mAlpha:kotlin.Float) <br /> |
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)! | [mMatrix](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#mMatrix:android.graphics.Matrix) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mTransformationType](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#mTransformationType:kotlin.Int) <br /> |

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

Reset the transformation to a state that leaves the object being animated in an unmodified state. The transformation type is [TYPE_BOTH](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_BOTH:kotlin.Int) by default. 

### compose

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compose(t: Transformation!): Unit
```

Apply this Transformation to an existing Transformation, e.g. apply a scale effect to something that has already been rotated.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `t` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#)!: |

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
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)! | The 3x3 Matrix representing the transformation to apply to the coordinates of the object being animated |

### getTransformationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformationType(): Int
```

Indicates the nature of this transformation.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALPHA](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_ALPHA:kotlin.Int), [TYPE_MATRIX](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_MATRIX:kotlin.Int), [TYPE_BOTH](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_BOTH:kotlin.Int) or [TYPE_IDENTITY](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_IDENTITY:kotlin.Int). |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(t: Transformation!): Unit
```

Clones the specified transformation.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#)!:The transformation to clone. |

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
| `transformationType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [TYPE_ALPHA](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_ALPHA:kotlin.Int), [TYPE_MATRIX](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_MATRIX:kotlin.Int), [TYPE_BOTH](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_BOTH:kotlin.Int) or [TYPE_IDENTITY](https://developer.android.com/reference/kotlin/android/view/animation/Transformation#TYPE_IDENTITY:kotlin.Int). |

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
