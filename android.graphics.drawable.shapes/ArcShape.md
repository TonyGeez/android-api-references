Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArcShape

Kotlin | [Java](ArcShape.md)
| --- | --- |

```
open class ArcShape : RectShape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](Shape.md) |||
| | ↳ | [android.graphics.drawable.shapes.RectShape](RectShape.md) ||
| | | ↳ | [android.graphics.drawable.shapes.ArcShape](ArcShape.md) |
| --- | --- | --- | --- |

Creates an arc shape. The arc shape starts at a specified angle and sweeps clockwise, drawing slices of pie.

The arc can be drawn to a `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` with its own #draw(android.graphics.Canvas,android.graphics.Paint) method, but more graphical control is available if you instead pass the ArcShape to a `https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable.html#`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#ArcShape(kotlin.Float,%20kotlin.Float)(startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` ArcShape constructor. |

| Public methods ||
|---|---|
| open [ArcShape](ArcShape.md) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#clone()()` Creates and returns a copy of this object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#draw(android.graphics.Canvas,%20android.graphics.Paint)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#!, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#!)` Draws this shape into the provided Canvas, with the provided Paint. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Computes the Outline of the shape and return it in the supplied Outline parameter. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#getStartAngle()()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#getSweepAngle()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getHeight()()` Returns the height of the Shape. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getWidth()()` Returns the width of the Shape. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hasAlpha()()` Checks whether the Shape is opaque. Default impl returns `true`. Override if your subclass can be opaque. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Resizes the dimensions of this shape. Must be called before `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint)`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#onResize(kotlin.Float,%20kotlin.Float)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Callback method called when `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)` is executed. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#rect()()` Returns the RectF that defines this rectangle's bounds. <br /> | ||

## Public constructors

### ArcShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArcShape(
    startAngle: Float, 
    sweepAngle: Float)
```

ArcShape constructor.

| Parameters ||
|---|---|
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the sweep angle (in degrees). Anything equal to or greater than 360 results in a complete circle/oval. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): ArcShape
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape#` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(
    canvas: Canvas!, 
    paint: Paint!
): Unit
```

Draws this shape into the provided Canvas, with the provided Paint.

Before calling this, you must call `https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)`.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md)!: the Canvas within which this shape should be drawn |
| `paint` | [Paint](../android.graphics/Paint.md)!: the Paint object that defines this shape's characteristics |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutline(outline: Outline): Unit
```

Computes the Outline of the shape and return it in the supplied Outline parameter. The default implementation does nothing and `outline` is not changed.

| Parameters ||
|---|---|
| `outline` | [Outline](../android.graphics/Outline.md): the Outline to be populated with the result. Must be non-`null`. |

### getStartAngle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartAngle(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the angle (in degrees) where the arc begins |

### getSweepAngle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSweepAngle(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the sweep angle (in degrees) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
