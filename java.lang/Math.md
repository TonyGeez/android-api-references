Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Math

```
class Math
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Math](../java/lang/Math.md) |

The class `Math` contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions.

Unlike some of the numeric methods of class `https://developer.android.com/reference/kotlin/java/lang/StrictMath`, all implementations of the equivalent functions of class `Math` are not defined to return the bit-for-bit same results. This relaxation permits better-performing implementations where strict reproducibility is not required.

By default many of the `Math` methods simply call the equivalent method in `StrictMath` for their implementation. Code generators are encouraged to use platform-specific native libraries or microprocessor instructions, where available, to provide higher-performance implementations of `Math` methods. Such higher-performance implementations still must conform to the specification for `Math`.

The quality of implementation specifications concern two properties, accuracy of the returned result and monotonicity of the method. Accuracy of the floating-point `Math` methods is measured in terms of ulps,"units in the last place". For a given floating-point format, an [ulp](../java/lang/Math.md)) of a specific real number value is the distance between the two floating-point values bracketing that numerical value. When discussing the accuracy of a method as a whole rather than at a specific argument, the number of ulps cited is for the worst-case error at any argument. If a method always has an error less than 0.5 ulps, the method always returns the floating-point number nearest the exact result; such a method is correctly rounded. A "correctly rounded" method is generally the best a floating-point approximation can be; however, it is impractical for many floating-point methods to be correctly rounded. Instead, for the `Math` class, a larger error bound of 1 or 2 ulps is allowed for certain methods. Informally, with a 1 ulp error bound, when the exact result is a representable number, the exact result should be returned as the computed result; otherwise, either of the two floating-point values which bracket the exact result may be returned. For exact results large in magnitude, one of the endpoints of the bracket may be infinite. Besides accuracy at individual arguments, maintaining proper relations between the method at different arguments is also important. Therefore, most methods with more than 0.5 ulp errors are required to be "semi-monotonic": whenever the mathematical function is non-decreasing, so is the floating-point approximation, likewise, whenever the mathematical function is non-increasing, so is the floating-point approximation. Not all approximations that have 1 ulp accuracy will automatically meet the monotonicity requirements.

The platform uses signed two's complement integer arithmetic with `int` and `long` primitive types. The developer should choose the primitive type to ensure that arithmetic operations consistently produce correct results, which in some cases means the operations will not overflow the range of values of the computation. The best practice is to choose the primitive type and algorithm to avoid overflow. In cases where the size is `int` or `long` and overflow errors need to be detected, the methods whose names end with `Exact` throw an `ArithmeticException` when the results overflow.

## IEEE 754 Recommended Operations

The 2019 revision of the IEEE 754 floating-point standard includes a section of recommended operations and the semantics of those operations if they are included in a programming environment. The recommended operations present in this class include `https://developer.android.com/reference/kotlin/java/lang/Math#sin(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#cos(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#tan(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#asin(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#acos(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#atan(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#exp(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#expm1(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#log(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#log10(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#log1p(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#sinh(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#cosh(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#tanh(kotlin.Double)`, `https://developer.android.com/reference/kotlin/java/lang/Math#hypot(kotlin.Double,%20kotlin.Double)`, and `https://developer.android.com/reference/kotlin/java/lang/Math#pow(kotlin.Double,%20kotlin.Double)`. (The `https://developer.android.com/reference/kotlin/java/lang/Math#sqrt(kotlin.Double)` operation is a required part of IEEE 754 from a different section of the standard.) The special case behavior of the recommended operations generally follows the guidance of the IEEE 754 standard. However, the `pow` method defines different behavior for some arguments, as noted in its [specification](../java/lang/Math.md)). The IEEE 754 standard defines its operations to be correctly rounded, which is a more stringent quality of implementation condition than required for most of the methods in question that are also included in this class.

## Summary

| Constants ||
|---|---|
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#E:kotlin.Double` The `double` value that is closer than any other to *e*, the base of the natural logarithms. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#PI:kotlin.Double` The `double` value that is closer than any other to *pi* (π), the ratio of the circumference of a circle to its diameter. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#TAU:kotlin.Double` The `double` value that is closer than any other to *tau* (τ), the ratio of the circumference of a circle to its radius. |
| --- | --- |

| Public methods ||
|---|---|
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#IEEEremainder(kotlin.Double,%20kotlin.Double)(f1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, f2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Computes the remainder operation on two arguments as prescribed by the IEEE 754 standard. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the absolute value of a `double` value. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the absolute value of a `float` value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the absolute value of an `int` value. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the absolute value of a `long` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the mathematical absolute value of an `int` value if it is exactly representable as an `int`, throwing `ArithmeticException` if the result overflows the positive `int` range. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the mathematical absolute value of an `long` value if it is exactly representable as an `long`, throwing `ArithmeticException` if the result overflows the positive `long` range. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#acos(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the arc cosine of a value; the returned angle is in the range 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#addExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the sum of its arguments, throwing an exception if the result overflows an `int`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#addExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the sum of its arguments, throwing an exception if the result overflows a `long`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#asin(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the arc sine of a value; the returned angle is in the range −*pi* /2 through *pi*/2. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#atan(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the arc tangent of a value; the returned angle is in the range −*pi* /2 through *pi*/2. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#atan2(kotlin.Double,%20kotlin.Double)(y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the angle *theta* from the conversion of rectangular coordinates (`x`, `y`) to polar coordinates (r, *theta*). |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#cbrt(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the cube root of a `double` value. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceil(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the smallest (closest to negative infinity) `double` value that is greater than or equal to the argument and is equal to a mathematical integer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDivExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDivExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the ceiling modulus of the `int` arguments. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the ceiling modulus of the `long` and `int` arguments. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the ceiling modulus of the `long` arguments. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#clamp(kotlin.Double,%20kotlin.Double,%20kotlin.Double)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Clamps the value to fit between min and max. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#clamp(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Clamps the value to fit between min and max. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#clamp(kotlin.Long,%20kotlin.Int,%20kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Clamps the value to fit between min and max. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#clamp(kotlin.Long,%20kotlin.Long,%20kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Clamps the value to fit between min and max. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#copySign(kotlin.Double,%20kotlin.Double)(magnitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, sign: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the first floating-point argument with the sign of the second floating-point argument. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#copySign(kotlin.Float,%20kotlin.Float)(magnitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sign: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the first floating-point argument with the sign of the second floating-point argument. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#cos(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the trigonometric cosine of an angle. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#cosh(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the hyperbolic cosine of a `double` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#decrementExact(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the argument decremented by one, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#decrementExact(kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the argument decremented by one, throwing an exception if the result overflows a `long`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#divideExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the quotient of the arguments, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#divideExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the quotient of the arguments, throwing an exception if the result overflows a `long`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#exp(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns Euler's number *e* raised to the power of a `double` value. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#expm1(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns *e*x −1. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floor(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the largest (closest to positive infinity) `double` value that is less than or equal to the argument and is equal to a mathematical integer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorDivExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorDivExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the floor modulus of the `int` arguments. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the floor modulus of the `long` and `int` arguments. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the floor modulus of the `long` arguments. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#fma(kotlin.Double,%20kotlin.Double,%20kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the fused multiply add of the three arguments; that is, returns the exact product of the first two arguments summed with the third argument and then rounded once to the nearest `double`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#fma(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the fused multiply add of the three arguments; that is, returns the exact product of the first two arguments summed with the third argument and then rounded once to the nearest `float`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#getExponent(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the unbiased exponent used in the representation of a `double`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#getExponent(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the unbiased exponent used in the representation of a `float`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#hypot(kotlin.Double,%20kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns sqrt(*x* 2 +*y*2) without intermediate overflow or underflow. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#incrementExact(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the argument incremented by one, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#incrementExact(kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the argument incremented by one, throwing an exception if the result overflows a `long`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#log(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the natural logarithm (base *e* ) of a `double` value. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#log10(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the base 10 logarithm of a `double` value. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#log1p(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the natural logarithm of the sum of the argument and 1. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Double,%20kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the greater of two `double` values. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the greater of two `float` values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the greater of two `int` values. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#max(kotlin.Long,%20kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the greater of two `long` values. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Double,%20kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the smaller of two `double` values. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the smaller of two `float` values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the smaller of two `int` values. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#min(kotlin.Long,%20kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the smaller of two `long` values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the product of the arguments, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyExact(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the product of the arguments, throwing an exception if the result overflows a `long`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the product of the arguments, throwing an exception if the result overflows a `long`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyFull(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the exact mathematical product of the arguments. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyHigh(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns as a `long` the most significant 64 bits of the 128-bit product of two 64-bit factors. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#negateExact(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the negation of the argument, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#negateExact(kotlin.Long)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the negation of the argument, throwing an exception if the result overflows a `long`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextAfter(kotlin.Double,%20kotlin.Double)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the floating-point number adjacent to the first argument in the direction of the second argument. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextAfter(kotlin.Float,%20kotlin.Double)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the floating-point number adjacent to the first argument in the direction of the second argument. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextDown(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the floating-point value adjacent to `d` in the direction of negative infinity. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextDown(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the floating-point value adjacent to `f` in the direction of negative infinity. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextUp(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the floating-point value adjacent to `d` in the direction of positive infinity. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#nextUp(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the floating-point value adjacent to `f` in the direction of positive infinity. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#pow(kotlin.Double,%20kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the value of the first argument raised to the power of the second argument. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#powExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `x` raised to the power of `n`, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#powExact(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `x` raised to the power of `n`, throwing an exception if the result overflows a `long`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#random()()` Returns a `double` value with a positive sign, greater than or equal to `0.0` and less than `1.0`. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#rint(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the `double` value that is closest in value to the argument and is equal to a mathematical integer. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#round(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the closest `long` to the argument, with ties rounding to positive infinity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#round(kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the closest `int` to the argument, with ties rounding to positive infinity. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#scalb(kotlin.Double,%20kotlin.Int)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, scaleFactor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `d` × 2`scaleFactor` rounded as if performed by a single correctly rounded floating-point multiply. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#scalb(kotlin.Float,%20kotlin.Int)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, scaleFactor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `f` × 2`scaleFactor` rounded as if performed by a single correctly rounded floating-point multiply. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#signum(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the signum function of the argument; zero if the argument is zero, 1. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#signum(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the signum function of the argument; zero if the argument is zero, 1. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#sin(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the trigonometric sine of an angle. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#sinh(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the hyperbolic sine of a `double` value. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#sqrt(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the correctly rounded positive square root of a `double` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#subtractExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the difference of the arguments, throwing an exception if the result overflows an `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#subtractExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the difference of the arguments, throwing an exception if the result overflows a `long`. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#tan(kotlin.Double)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the trigonometric tangent of an angle. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#tanh(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the hyperbolic tangent of a `double` value. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#toDegrees(kotlin.Double)(angrad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Converts an angle measured in radians to an approximately equivalent angle measured in degrees. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#toIntExact(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the value of the `long` argument, throwing an exception if the value overflows an `int`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#toRadians(kotlin.Double)(angdeg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Converts an angle measured in degrees to an approximately equivalent angle measured in radians. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ulp(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the size of an ulp of the argument. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#ulp(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the size of an ulp of the argument. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedMultiplyExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedMultiplyExact(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `long`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedMultiplyExact(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `long`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedMultiplyHigh(kotlin.Long,%20kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns as a `long` the most significant 64 bits of the unsigned 128-bit product of two unsigned 64-bit factors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedPowExact(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns unsigned `x` raised to the power of `n`, throwing an exception if the result overflows an unsigned `int`. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedPowExact(kotlin.Long,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns unsigned `x` raised to the power of `n`, throwing an exception if the result overflows an unsigned `long`. |

## Constants

### E

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val E: Double
```

The `double` value that is closer than any other to *e*, the base of the natural logarithms.

 Value: 2.718281828459045

### PI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PI: Double
```

The `double` value that is closer than any other to *pi* (π), the ratio of the circumference of a circle to its diameter.

 Value: 3.141592653589793

### TAU

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAU: Double
```

The `double` value that is closer than any other to *tau* (τ), the ratio of the circumference of a circle to its radius.

 Value: 6.283185307179586

## Public methods

### IEEEremainder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun IEEEremainder(
    f1: Double, 
    f2: Double
): Double
```

Computes the remainder operation on two arguments as prescribed by the IEEE 754 standard. The remainder value is mathematically equal to `f1 - f2` × *n* , where *n* is the mathematical integer closest to the exact mathematical value of the quotient `f1/f2`, and if two mathematical integers are equally close to `f1/f2`, then *n* is the integer that is even. If the remainder is zero, its sign is the same as the sign of the first argument. Special cases:

- If either argument is NaN, or the first argument is infinite, or the second argument is positive zero or negative zero, then the result is NaN.
- If the first argument is finite and the second argument is infinite, then the result is the same as the first argument.

<br />

| Parameters ||
|---|---|
| `f1` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the dividend. |
| `f2` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the divisor. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the remainder when `f1` is divided by `f2`. |

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun abs(a: Double): Double
```

Returns the absolute value of a `double` value. If the argument is not negative, the argument is returned. If the argument is negative, the negation of the argument is returned. Special cases:

- If the argument is positive zero or negative zero, the result is positive zero.
- If the argument is infinite, the result is positive infinity.
- If the argument is NaN, the result is NaN.

<br />

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the absolute value of the argument. |

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun abs(a: Float): Float
```

Returns the absolute value of a `float` value. If the argument is not negative, the argument is returned. If the argument is negative, the negation of the argument is returned. Special cases:

- If the argument is positive zero or negative zero, the result is positive zero.
- If the argument is infinite, the result is positive infinity.
- If the argument is NaN, the result is NaN.

<br />

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the absolute value of the argument. |

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun abs(a: Int): Int
```

Returns the absolute value of an `int` value. If the argument is not negative, the argument is returned. If the argument is negative, the negation of the argument is returned.

Note that if the argument is equal to the value of `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int`, the most negative representable `int` value, the result is that same value, which is negative. In contrast, the `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Int)` method throws an `ArithmeticException` for this value.

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the absolute value of the argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Int)`

### abs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun abs(a: Long): Long
```

Returns the absolute value of a `long` value. If the argument is not negative, the argument is returned. If the argument is negative, the negation of the argument is returned.

Note that if the argument is equal to the value of `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long`, the most negative representable `long` value, the result is that same value, which is negative. In contrast, the `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Long)` method throws an `ArithmeticException` for this value.

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the absolute value of the argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#absExact(kotlin.Long)`

### absExact

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun absExact(a: Int): Int
```

Returns the mathematical absolute value of an `int` value if it is exactly representable as an `int`, throwing `ArithmeticException` if the result overflows the positive `int` range.

Since the range of two's complement integers is asymmetric with one additional negative value (JLS {@jls 4.2.1}), the mathematical absolute value of `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int` overflows the positive `int` range, so an exception is thrown for that argument.

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the absolute value of the argument, unless overflow occurs |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the argument is `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Int)`

### absExact

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun absExact(a: Long): Long
```

Returns the mathematical absolute value of an `long` value if it is exactly representable as an `long`, throwing `ArithmeticException` if the result overflows the positive `long` range.

Since the range of two's complement integers is asymmetric with one additional negative value (JLS {@jls 4.2.1}), the mathematical absolute value of `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long` overflows the positive `long` range, so an exception is thrown for that argument.

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the argument whose absolute value is to be determined |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the absolute value of the argument, unless overflow occurs |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the argument is `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#abs(kotlin.Long)`

### acos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun acos(a: Double): Double
```

Returns the arc cosine of a value; the returned angle is in the range 0.0 through *pi*. Special case:

- If the argument is NaN or its absolute value is greater than 1, then the result is NaN.
- If the argument is `1.0`, the result is positive zero.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value whose arc cosine is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the arc cosine of the argument. |

### addExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun addExact(
    x: Int, 
    y: Int
): Int
```

Returns the sum of its arguments, throwing an exception if the result overflows an `int`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### addExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun addExact(
    x: Long, 
    y: Long
): Long
```

Returns the sum of its arguments, throwing an exception if the result overflows a `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### asin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun asin(a: Double): Double
```

Returns the arc sine of a value; the returned angle is in the range −*pi* /2 through *pi*/2. Special cases:

- If the argument is NaN or its absolute value is greater than 1, then the result is NaN.
- If the argument is zero, then the result is a zero with the same sign as the argument.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value whose arc sine is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the arc sine of the argument. |

### atan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun atan(a: Double): Double
```

Returns the arc tangent of a value; the returned angle is in the range −*pi* /2 through *pi*/2. Special cases:

- If the argument is NaN, then the result is NaN.
- If the argument is zero, then the result is a zero with the same sign as the argument.
- If the argument is java.lang.Double#isInfinite, then the result is the closest value to *pi*/2 with the same sign as the input.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value whose arc tangent is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the arc tangent of the argument. |

### atan2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun atan2(
    y: Double, 
    x: Double
): Double
```

Returns the angle *theta* from the conversion of rectangular coordinates (`x`, `y`) to polar coordinates (r, *theta* ). This method computes the phase *theta* by computing an arc tangent of `y/x` in the range of −*pi* to *pi*. Special cases:

- If either argument is NaN, then the result is NaN.
- If the first argument is positive zero and the second argument is positive, or the first argument is positive and finite and the second argument is positive infinity, then the result is positive zero.
- If the first argument is negative zero and the second argument is positive, or the first argument is negative and finite and the second argument is positive infinity, then the result is negative zero.
- If the first argument is positive zero and the second argument is negative, or the first argument is positive and finite and the second argument is negative infinity, then the result is the `double` value closest to *pi*.
- If the first argument is negative zero and the second argument is negative, or the first argument is negative and finite and the second argument is negative infinity, then the result is the `double` value closest to -*pi*.
- If the first argument is positive and the second argument is positive zero or negative zero, or the first argument is positive infinity and the second argument is finite, then the result is the `double` value closest to *pi*/2.
- If the first argument is negative and the second argument is positive zero or negative zero, or the first argument is negative infinity and the second argument is finite, then the result is the `double` value closest to -*pi*/2.
- If both arguments are positive infinity, then the result is the `double` value closest to *pi*/4.
- If the first argument is positive infinity and the second argument is negative infinity, then the result is the `double` value closest to 3\**pi*/4.
- If the first argument is negative infinity and the second argument is positive infinity, then the result is the `double` value closest to -*pi*/4.
- If both arguments are negative infinity, then the result is the `double` value closest to -3\**pi*/4.

<br />

The computed result must be within 2 ulps of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `y` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the ordinate coordinate |
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the abscissa coordinate |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the *theta* component of the point (*r* , *theta* ) in polar coordinates that corresponds to the point (*x* , *y*) in Cartesian coordinates. |

### cbrt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun cbrt(a: Double): Double
```

Returns the cube root of a `double` value. For positive finite `x`, `cbrt(-x) == -cbrt(x)`; that is, the cube root of a negative value is the negative of the cube root of that value's magnitude. Special cases:

- If the argument is NaN, then the result is NaN.
- If the argument is infinite, then the result is an infinity with the same sign as the argument.
- If the argument is zero, then the result is a zero with the same sign as the argument.

<br />

The computed result must be within 1 ulp of the exact result.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the cube root of `a`. |

### ceil

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceil(a: Double): Double
```

Returns the smallest (closest to negative infinity) `double` value that is greater than or equal to the argument and is equal to a mathematical integer. Special cases:

- If the argument value is already equal to a mathematical integer, then the result is the same as the argument.
- If the argument is NaN or an infinity or positive zero or negative zero, then the result is the same as the argument.
- If the argument value is less than zero but greater than -1.0, then the result is negative zero.

Note that the value of `Math.ceil(x)` is exactly the value of `-Math.floor(-x)`.

<br />

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the smallest (closest to negative infinity) floating-point value that is greater than or equal to the argument and is equal to a mathematical integer. |

### ceilDiv

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilDiv(
    x: Int, 
    y: Int
): Int
```

Returns the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. There is one special case: if the dividend is [Integer.MIN_VALUE](../java/lang/Integer.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Integer.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward positive infinity (ceiling) rounding mode. The ceiling rounding mode gives different results from truncation when the exact quotient is not an integer and is positive.

- If the signs of the arguments are different, the results of `ceilDiv` and the `/` operator are the same. 
 For example, `ceilDiv(-4, 3) == -1` and `(-4 / 3) == -1`.
- If the signs of the arguments are the same, `ceilDiv` returns the smallest integer greater than or equal to the quotient while the `/` operator returns the largest integer less than or equal to the quotient. They differ if and only if the quotient is not an integer. 
 For example, `ceilDiv(4, 3) == 2`, whereas `(4 / 3) == 1`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#ceil(kotlin.Double)`

### ceilDiv

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilDiv(
    x: Long, 
    y: Int
): Long
```

Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. There is one special case: if the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Long.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward positive infinity (ceiling) rounding mode. The ceiling rounding mode gives different results from truncation when the exact result is not an integer and is positive.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#ceil(kotlin.Double)`

### ceilDiv

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilDiv(
    x: Long, 
    y: Long
): Long
```

Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. There is one special case: if the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Long.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward positive infinity (ceiling) rounding mode. The ceiling rounding mode gives different results from truncation when the exact result is not an integer and is positive.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#ceil(kotlin.Double)`

### ceilDivExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilDivExact(
    x: Int, 
    y: Int
): Int
```

Returns the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. This method is identical to `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)` except that it throws an `ArithmeticException` when the dividend is [Integer.MIN_VALUE](../java/lang/Integer.md) and the divisor is `-1` instead of ignoring the integer overflow and returning `Integer.MIN_VALUE`.

The ceil modulus method `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)` is a suitable counterpart both for this method and for the `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)` method.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the smallest (closest to negative infinity) `int` value that is greater than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero, or the dividend `x` is `Integer.MIN_VALUE` and the divisor `y` is `-1`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`

### ceilDivExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilDivExact(
    x: Long, 
    y: Long
): Long
```

Returns the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. This method is identical to `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Long)` except that it throws an `ArithmeticException` when the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1` instead of ignoring the integer overflow and returning `Long.MIN_VALUE`.

The ceil modulus method `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Long,%20kotlin.Long)` is a suitable counterpart both for this method and for the `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Long)` method.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the smallest (closest to negative infinity) `long` value that is greater than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero, or the dividend `x` is `Long.MIN_VALUE` and the divisor `y` is `-1`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Long)`

### ceilMod

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilMod(
    x: Int, 
    y: Int
): Int
```

Returns the ceiling modulus of the `int` arguments.

The ceiling modulus is `r = x - (ceilDiv(x, y) * y)`, has the opposite sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `ceilDiv` and `ceilMod` is such that:

- `ceilDiv(x, y) * y + ceilMod(x, y) == x`

The difference in values between `ceilMod` and the `%` operator is due to the difference between `ceilDiv` and the `/` operator, as detailed in [ceilDiv(int,int)](../java/lang/Math.md)).

Examples:

- Regardless of the signs of the arguments, `ceilMod`(x, y) is zero exactly when `x % y` is zero as well.
- If neither `ceilMod`(x, y) nor `x % y` is zero, they differ exactly when the signs of the arguments are the same. 
 - `ceilMod(+4, +3) == -2`; and `(+4 % +3) == +1`
 - `ceilMod(-4, -3) == +2`; and `(-4 % -3) == -1`
 - `ceilMod(+4, -3) == +1`; and `(+4 % -3) == +1`
 - `ceilMod(-4, +3) == -1`; and `(-4 % +3) == -1`

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ceiling modulus `x - (ceilDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Int,%20kotlin.Int)`

### ceilMod

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilMod(
    x: Long, 
    y: Int
): Int
```

Returns the ceiling modulus of the `long` and `int` arguments.

The ceiling modulus is `r = x - (ceilDiv(x, y) * y)`, has the opposite sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `ceilDiv` and `ceilMod` is such that:

- `ceilDiv(x, y) * y + ceilMod(x, y) == x`

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ceiling modulus `x - (ceilDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Int)`

### ceilMod

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ceilMod(
    x: Long, 
    y: Long
): Long
```

Returns the ceiling modulus of the `long` arguments.

The ceiling modulus is `r = x - (ceilDiv(x, y) * y)`, has the opposite sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `ceilDiv` and `ceilMod` is such that:

- `ceilDiv(x, y) * y + ceilMod(x, y) == x`

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#ceilMod(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the ceiling modulus `x - (ceilDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#ceilDiv(kotlin.Long,%20kotlin.Long)`

### clamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clamp(
    value: Double, 
    min: Double, 
    max: Double
): Double
```

Clamps the value to fit between min and max. If the value is less than `min`, then `min` is returned. If the value is greater than `max`, then `max` is returned. Otherwise, the original value is returned. If value is NaN, the result is also NaN.

Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. E.g., `clamp(-0.0, 0.0, 1.0)` returns 0.0.

| Parameters ||
|---|---|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): value to clamp |
| `min` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): minimal allowed value |
| `max` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): maximal allowed value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | a clamped value that fits into `min..max` interval |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if either of `min` and `max` arguments is NaN, or `min > max`, or `min` is +0.0, and `max` is -0.0. |

### clamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clamp(
    value: Float, 
    min: Float, 
    max: Float
): Float
```

Clamps the value to fit between min and max. If the value is less than `min`, then `min` is returned. If the value is greater than `max`, then `max` is returned. Otherwise, the original value is returned. If value is NaN, the result is also NaN.

Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. E.g., `clamp(-0.0f, 0.0f, 1.0f)` returns 0.0f.

| Parameters ||
|---|---|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): value to clamp |
| `min` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): minimal allowed value |
| `max` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): maximal allowed value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a clamped value that fits into `min..max` interval |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if either of `min` and `max` arguments is NaN, or `min > max`, or `min` is +0.0f, and `max` is -0.0f. |

### clamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clamp(
    value: Long, 
    min: Int, 
    max: Int
): Int
```

Clamps the value to fit between min and max. If the value is less than `min`, then `min` is returned. If the value is greater than `max`, then `max` is returned. Otherwise, the original value is returned.

While the original value of type long may not fit into the int type, the bounds have the int type, so the result always fits the int type. This allows to use method to safely cast long value to int with saturation.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): value to clamp |
| `min` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): minimal allowed value |
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): maximal allowed value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a clamped value that fits into `min..max` interval |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `min > max` |

### clamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clamp(
    value: Long, 
    min: Long, 
    max: Long
): Long
```

Clamps the value to fit between min and max. If the value is less than `min`, then `min` is returned. If the value is greater than `max`, then `max` is returned. Otherwise, the original value is returned.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): value to clamp |
| `min` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): minimal allowed value |
| `max` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): maximal allowed value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a clamped value that fits into `min..max` interval |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `min > max` |

### copySign

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copySign(
    magnitude: Double, 
    sign: Double
): Double
```

Returns the first floating-point argument with the sign of the second floating-point argument. Note that unlike the `https://developer.android.com/reference/kotlin/java/lang/StrictMath#copySign(kotlin.Double,%20kotlin.Double)` method, this method does not require NaN `sign` arguments to be treated as positive values; implementations are permitted to treat some NaN arguments as positive and other NaN arguments as negative to allow greater performance.

| Parameters ||
|---|---|
| `magnitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the parameter providing the magnitude of the result |
| `sign` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the parameter providing the sign of the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | a value with the magnitude of `magnitude` and the sign of `sign`. |

### copySign

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copySign(
    magnitude: Float, 
    sign: Float
): Float
```

Returns the first floating-point argument with the sign of the second floating-point argument. Note that unlike the `https://developer.android.com/reference/kotlin/java/lang/StrictMath#copySign(kotlin.Float,%20kotlin.Float)` method, this method does not require NaN `sign` arguments to be treated as positive values; implementations are permitted to treat some NaN arguments as positive and other NaN arguments as negative to allow greater performance.

| Parameters ||
|---|---|
| `magnitude` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the parameter providing the magnitude of the result |
| `sign` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the parameter providing the sign of the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a value with the magnitude of `magnitude` and the sign of `sign`. |

### cos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun cos(a: Double): Double
```

Returns the trigonometric cosine of an angle. Special cases:

- If the argument is NaN or an infinity, then the result is NaN.
- If the argument is zero, then the result is `1.0`.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an angle, in radians. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the cosine of the argument. |

### cosh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun cosh(x: Double): Double
```

Returns the hyperbolic cosine of a `double` value. The hyperbolic cosine of *x* is defined to be (*ex + e−x* )/2 where *e* is [Euler's number](../java/lang/Math.md).

Special cases:

- If the argument is NaN, then the result is NaN.
- If the argument is infinite, then the result is positive infinity.
- If the argument is zero, then the result is `1.0`.

The computed result must be within 2.5 ulps of the exact result.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The number whose hyperbolic cosine is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The hyperbolic cosine of `x`. |

### decrementExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decrementExact(a: Int): Int
```

Returns the argument decremented by one, throwing an exception if the result overflows an `int`. The overflow only occurs for [the minimum value](../java/lang/Integer.md).

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to decrement |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### decrementExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decrementExact(a: Long): Long
```

Returns the argument decremented by one, throwing an exception if the result overflows a `long`. The overflow only occurs for [the minimum value](../java/lang/Long.md).

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to decrement |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### divideExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun divideExact(
    x: Int, 
    y: Int
): Int
```

Returns the quotient of the arguments, throwing an exception if the result overflows an `int`. Such overflow occurs in this method if `x` is `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int` and `y` is `-1`. In contrast, if `Integer.MIN_VALUE / -1` were evaluated directly, the result would be `Integer.MIN_VALUE` and no exception would be thrown.

If `y` is zero, an `ArithmeticException` is thrown (JLS {@jls 15.17.2}).

The built-in remainder operator "`%`" is a suitable counterpart both for this method and for the built-in division operator "`/`".

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the quotient `x / y` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `y` is zero or the quotient overflows an int |

### divideExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun divideExact(
    x: Long, 
    y: Long
): Long
```

Returns the quotient of the arguments, throwing an exception if the result overflows a `long`. Such overflow occurs in this method if `x` is `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long` and `y` is `-1`. In contrast, if `Long.MIN_VALUE / -1` were evaluated directly, the result would be `Long.MIN_VALUE` and no exception would be thrown.

If `y` is zero, an `ArithmeticException` is thrown (JLS {@jls 15.17.2}).

The built-in remainder operator "`%`" is a suitable counterpart both for this method and for the built-in division operator "`/`".

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the quotient `x / y` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if `y` is zero or the quotient overflows a long |

### exp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun exp(a: Double): Double
```

Returns Euler's number *e* raised to the power of a `double` value. Special cases:

- If the argument is NaN, the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is negative infinity, then the result is positive zero.
- If the argument is zero, then the result is `1.0`.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the exponent to raise *e* to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value *e* `a`, where *e* is the base of the natural logarithms. |

### expm1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun expm1(x: Double): Double
```

Returns *e* x −1. Note that for values of *x* near 0, the exact sum of `expm1(x)` + 1 is much closer to the true result of *e* x than `exp(x)`.

Special cases:

- If the argument is NaN, the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is negative infinity, then the result is -1.0.
- If the argument is zero, then the result is a zero with the same sign as the argument.

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic. The result of `expm1` for any finite input must be greater than or equal to `-1.0`. Note that once the exact result of *e* `x` - 1 is within 1/2 ulp of the limit value -1, `-1.0` should be returned.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the exponent to raise *e* to in the computation of *e* `x` −1. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value *e* `x` - 1. |

### floor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floor(a: Double): Double
```

Returns the largest (closest to positive infinity) `double` value that is less than or equal to the argument and is equal to a mathematical integer. Special cases:

- If the argument value is already equal to a mathematical integer, then the result is the same as the argument.
- If the argument is NaN or an infinity or positive zero or negative zero, then the result is the same as the argument.

<br />

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the largest (closest to positive infinity) floating-point value that less than or equal to the argument and is equal to a mathematical integer. |

### floorDiv

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorDiv(
    x: Int, 
    y: Int
): Int
```

Returns the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. There is one special case: if the dividend is [Integer.MIN_VALUE](../java/lang/Integer.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Integer.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward negative infinity (floor) rounding mode. The floor rounding mode gives different results from truncation when the exact quotient is not an integer and is negative.

- If the signs of the arguments are the same, the results of `floorDiv` and the `/` operator are the same. 
 For example, `floorDiv(4, 3) == 1` and `(4 / 3) == 1`.
- If the signs of the arguments are different, `floorDiv` returns the largest integer less than or equal to the quotient while the `/` operator returns the smallest integer greater than or equal to the quotient. They differ if and only if the quotient is not an integer. 
 For example, `floorDiv(-4, 3) == -2`, whereas `(-4 / 3) == -1`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#floor(kotlin.Double)`

### floorDiv

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorDiv(
    x: Long, 
    y: Int
): Long
```

Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. There is one special case: if the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Long.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward negative infinity (floor) rounding mode. The floor rounding mode gives different results from truncation when the exact result is not an integer and is negative.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Long,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#floor(kotlin.Double)`

### floorDiv

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorDiv(
    x: Long, 
    y: Long
): Long
```

Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. There is one special case: if the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1`, then integer overflow occurs and the result is equal to `Long.MIN_VALUE`.

Normal integer division operates under the round to zero rounding mode (truncation). This operation instead acts under the round toward negative infinity (floor) rounding mode. The floor rounding mode gives different results from truncation when the exact result is not an integer and is negative.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Long,%20kotlin.Long)`
- `https://developer.android.com/reference/kotlin/java/lang/Math#floor(kotlin.Double)`

### floorDivExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorDivExact(
    x: Int, 
    y: Int
): Int
```

Returns the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. This method is identical to `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)` except that it throws an `ArithmeticException` when the dividend is [Integer.MIN_VALUE](../java/lang/Integer.md) and the divisor is `-1` instead of ignoring the integer overflow and returning `Integer.MIN_VALUE`.

The floor modulus method `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Int,%20kotlin.Int)` is a suitable counterpart both for this method and for the `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)` method.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the largest (closest to positive infinity) `int` value that is less than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero, or the dividend `x` is `Integer.MIN_VALUE` and the divisor `y` is `-1`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`

### floorDivExact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorDivExact(
    x: Long, 
    y: Long
): Long
```

Returns the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. This method is identical to `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Long)` except that it throws an `ArithmeticException` when the dividend is [Long.MIN_VALUE](../java/lang/Long.md) and the divisor is `-1` instead of ignoring the integer overflow and returning `Long.MIN_VALUE`.

The floor modulus method `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Long,%20kotlin.Long)` is a suitable counterpart both for this method and for the `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Long)` method.

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the largest (closest to positive infinity) `long` value that is less than or equal to the algebraic quotient. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero, or the dividend `x` is `Long.MIN_VALUE` and the divisor `y` is `-1`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Long)`

### floorMod

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorMod(
    x: Int, 
    y: Int
): Int
```

Returns the floor modulus of the `int` arguments.

The floor modulus is `r = x - (floorDiv(x, y) * y)`, has the same sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `floorDiv` and `floorMod` is such that:

- `floorDiv(x, y) * y + floorMod(x, y) == x`

The difference in values between `floorMod` and the `%` operator is due to the difference between `floorDiv` and the `/` operator, as detailed in [floorDiv(int,int)](../java/lang/Math.md)).

Examples:

- Regardless of the signs of the arguments, `floorMod`(x, y) is zero exactly when `x % y` is zero as well.
- If neither `floorMod`(x, y) nor `x % y` is zero, they differ exactly when the signs of the arguments differ. 
 - `floorMod(+4, +3) == +1`; and `(+4 % +3) == +1`
 - `floorMod(-4, -3) == -1`; and `(-4 % -3) == -1`
 - `floorMod(+4, -3) == -2`; and `(+4 % -3) == +1`
 - `floorMod(-4, +3) == +2`; and `(-4 % +3) == -1`

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the floor modulus `x - (floorDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Int,%20kotlin.Int)`

### floorMod

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorMod(
    x: Long, 
    y: Int
): Int
```

Returns the floor modulus of the `long` and `int` arguments.

The floor modulus is `r = x - (floorDiv(x, y) * y)`, has the same sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `floorDiv` and `floorMod` is such that:

- `floorDiv(x, y) * y + floorMod(x, y) == x`

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the floor modulus `x - (floorDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Int)`

### floorMod

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun floorMod(
    x: Long, 
    y: Long
): Long
```

Returns the floor modulus of the `long` arguments.

The floor modulus is `r = x - (floorDiv(x, y) * y)`, has the same sign as the divisor `y` or is zero, and is in the range of `-abs(y) < r < +abs(y)`.

The relationship between `floorDiv` and `floorMod` is such that:

- `floorDiv(x, y) * y + floorMod(x, y) == x`

For examples, see `https://developer.android.com/reference/kotlin/java/lang/Math#floorMod(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the dividend |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the divisor |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the floor modulus `x - (floorDiv(x, y) * y)` |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the divisor `y` is zero |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#floorDiv(kotlin.Long,%20kotlin.Long)`

### fma

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fma(
    a: Double, 
    b: Double, 
    c: Double
): Double
```

Returns the fused multiply add of the three arguments; that is, returns the exact product of the first two arguments summed with the third argument and then rounded once to the nearest `double`. The rounding is done using the [round to nearest even](../java/math/RoundingMode.md). In contrast, if `a * b + c` is evaluated as a regular floating-point expression, two rounding errors are involved, the first for the multiply operation, the second for the addition operation.

Special cases:

- If any argument is NaN, the result is NaN.
- If one of the first two arguments is infinite and the other is zero, the result is NaN.
- If the exact product of the first two arguments is infinite (in other words, at least one of the arguments is infinite and the other is neither zero nor NaN) and the third argument is an infinity of the opposite sign, the result is NaN.

Note that `fma(a, 1.0, c)` returns the same result as (`a + c`). However, `fma(a, b, +0.0)` does *not* always return the same result as (`a * b`) since `fma(-0.0, +0.0, +0.0)` is `+0.0` while (`-0.0 * +0.0`) is `-0.0`; `fma(a, b, -0.0)` is equivalent to (`a * b`) however.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |
| `c` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | (*a* × *b* + *c* ) computed, as if with unlimited range and precision, and rounded once to the nearest `double` value |

### fma

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fma(
    a: Float, 
    b: Float, 
    c: Float
): Float
```

Returns the fused multiply add of the three arguments; that is, returns the exact product of the first two arguments summed with the third argument and then rounded once to the nearest `float`. The rounding is done using the [round to nearest even](../java/math/RoundingMode.md). In contrast, if `a * b + c` is evaluated as a regular floating-point expression, two rounding errors are involved, the first for the multiply operation, the second for the addition operation.

Special cases:

- If any argument is NaN, the result is NaN.
- If one of the first two arguments is infinite and the other is zero, the result is NaN.
- If the exact product of the first two arguments is infinite (in other words, at least one of the arguments is infinite and the other is neither zero nor NaN) and the third argument is an infinity of the opposite sign, the result is NaN.

Note that `fma(a, 1.0f, c)` returns the same result as (`a + c`). However, `fma(a, b, +0.0f)` does *not* always return the same result as (`a * b`) since `fma(-0.0f, +0.0f, +0.0f)` is `+0.0f` while (`-0.0f * +0.0f`) is `-0.0f`; `fma(a, b, -0.0f)` is equivalent to (`a * b`) however.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a value |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a value |
| `c` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | (*a* × *b* + *c* ) computed, as if with unlimited range and precision, and rounded once to the nearest `float` value |

### getExponent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getExponent(d: Double): Int
```

Returns the unbiased exponent used in the representation of a `double`. Special cases:

- If the argument is NaN or infinite, then the result is `https://developer.android.com/reference/kotlin/java/lang/Double#MAX_EXPONENT:kotlin.Int` + 1.
- If the argument is zero or subnormal, then the result is `https://developer.android.com/reference/kotlin/java/lang/Double#MIN_EXPONENT:kotlin.Int` - 1.

<br />

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a `double` value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the unbiased exponent of the argument |

### getExponent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getExponent(f: Float): Int
```

Returns the unbiased exponent used in the representation of a `float`. Special cases:

- If the argument is NaN or infinite, then the result is `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_EXPONENT:kotlin.Int` + 1.
- If the argument is zero or subnormal, then the result is `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_EXPONENT:kotlin.Int` - 1.

<br />

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a `float` value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the unbiased exponent of the argument |

### hypot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hypot(
    x: Double, 
    y: Double
): Double
```

Returns sqrt(*x* 2 +*y*2) without intermediate overflow or underflow.

Special cases:

- If either argument is infinite, then the result is positive infinity.
- If either argument is NaN and neither argument is infinite, then the result is NaN.
- If both arguments are zero, the result is positive zero.

The computed result must be within 1.5 ulps of the exact result. If one parameter is held constant, the results must be semi-monotonic in the other parameter.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |
| `y` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | sqrt(*x* 2 +*y*2) without intermediate overflow or underflow |

### incrementExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun incrementExact(a: Int): Int
```

Returns the argument incremented by one, throwing an exception if the result overflows an `int`. The overflow only occurs for [the maximum value](../java/lang/Integer.md).

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to increment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### incrementExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun incrementExact(a: Long): Long
```

Returns the argument incremented by one, throwing an exception if the result overflows a `long`. The overflow only occurs for [the maximum value](../java/lang/Long.md).

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to increment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun log(a: Double): Double
```

Returns the natural logarithm (base *e* ) of a `double` value. Special cases:

- If the argument is NaN or less than zero, then the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is positive zero or negative zero, then the result is negative infinity.
- If the argument is `1.0`, then the result is positive zero.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value ln `a`, the natural logarithm of `a`. |

### log10

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun log10(a: Double): Double
```

Returns the base 10 logarithm of a `double` value. Special cases:

- If the argument is NaN or less than zero, then the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is positive zero or negative zero, then the result is negative infinity.
- If the argument is equal to 10*n* for integer *n* , then the result is *n* . In particular, if the argument is `1.0` (100), then the result is positive zero.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the base 10 logarithm of `a`. |

### log1p

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun log1p(x: Double): Double
```

Returns the natural logarithm of the sum of the argument and 1. Note that for small values `x`, the result of `log1p(x)` is much closer to the true result of ln(1 + `x`) than the floating-point evaluation of `log(1.0+x)`.

Special cases:

- If the argument is NaN or less than -1, then the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is negative one, then the result is negative infinity.
- If the argument is zero, then the result is a zero with the same sign as the argument.

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value ln(`x` + 1), the natural log of `x` + 1 |

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    a: Double, 
    b: Double
): Double
```

Returns the greater of two `double` values. That is, the result is the argument closer to positive infinity. If the arguments have the same value, the result is that same value. If either value is NaN, then the result is NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. If one argument is positive zero and the other negative zero, the result is positive zero.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an argument. |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the larger of `a` and `b`. |

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    a: Float, 
    b: Float
): Float
```

Returns the greater of two `float` values. That is, the result is the argument closer to positive infinity. If the arguments have the same value, the result is that same value. If either value is NaN, then the result is NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. If one argument is positive zero and the other negative zero, the result is positive zero.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): an argument. |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the larger of `a` and `b`. |

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    a: Int, 
    b: Int
): Int
```

Returns the greater of two `int` values. That is, the result is the argument closer to the value of `https://developer.android.com/reference/kotlin/java/lang/Integer#MAX_VALUE:kotlin.Int`. If the arguments have the same value, the result is that same value.

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an argument. |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the larger of `a` and `b`. |

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun max(
    a: Long, 
    b: Long
): Long
```

Returns the greater of two `long` values. That is, the result is the argument closer to the value of `https://developer.android.com/reference/kotlin/java/lang/Long#MAX_VALUE:kotlin.Long`. If the arguments have the same value, the result is that same value.

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): an argument. |
| `b` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the larger of `a` and `b`. |

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    a: Double, 
    b: Double
): Double
```

Returns the smaller of two `double` values. That is, the result is the value closer to negative infinity. If the arguments have the same value, the result is that same value. If either value is NaN, then the result is NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. If one argument is positive zero and the other is negative zero, the result is negative zero.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an argument. |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the smaller of `a` and `b`. |

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    a: Float, 
    b: Float
): Float
```

Returns the smaller of two `float` values. That is, the result is the value closer to negative infinity. If the arguments have the same value, the result is that same value. If either value is NaN, then the result is NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. If one argument is positive zero and the other is negative zero, the result is negative zero.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): an argument. |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the smaller of `a` and `b`. |

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    a: Int, 
    b: Int
): Int
```

Returns the smaller of two `int` values. That is, the result the argument closer to the value of `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int`. If the arguments have the same value, the result is that same value.

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an argument. |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the smaller of `a` and `b`. |

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun min(
    a: Long, 
    b: Long
): Long
```

Returns the smaller of two `long` values. That is, the result is the argument closer to the value of `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long`. If the arguments have the same value, the result is that same value.

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): an argument. |
| `b` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): another argument. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the smaller of `a` and `b`. |

### multiplyExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun multiplyExact(
    x: Int, 
    y: Int
): Int
```

Returns the product of the arguments, throwing an exception if the result overflows an `int`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### multiplyExact

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun multiplyExact(
    x: Long, 
    y: Int
): Long
```

Returns the product of the arguments, throwing an exception if the result overflows a `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### multiplyExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun multiplyExact(
    x: Long, 
    y: Long
): Long
```

Returns the product of the arguments, throwing an exception if the result overflows a `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### multiplyFull

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun multiplyFull(
    x: Int, 
    y: Int
): Long
```

Returns the exact mathematical product of the arguments.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

### multiplyHigh

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun multiplyHigh(
    x: Long, 
    y: Long
): Long
```

Returns as a `long` the most significant 64 bits of the 128-bit product of two 64-bit factors.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#unsignedMultiplyHigh(kotlin.Long,%20kotlin.Long)`

### negateExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun negateExact(a: Int): Int
```

Returns the negation of the argument, throwing an exception if the result overflows an `int`. The overflow only occurs for [the minimum value](../java/lang/Integer.md).

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to negate |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### negateExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun negateExact(a: Long): Long
```

Returns the negation of the argument, throwing an exception if the result overflows a `long`. The overflow only occurs for [the minimum value](../java/lang/Long.md).

| Parameters ||
|---|---|
| `a` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to negate |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### nextAfter

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextAfter(
    start: Double, 
    direction: Double
): Double
```

Returns the floating-point number adjacent to the first argument in the direction of the second argument. If both arguments compare as equal the second argument is returned.

Special cases:

- If either argument is a NaN, then NaN is returned.
- If both arguments are signed zeros, `direction` is returned unchanged (as implied by the requirement of returning the second argument if the arguments compare as equal).
- If `start` is ±`https://developer.android.com/reference/kotlin/java/lang/Double#MIN_VALUE:kotlin.Double` and `direction` has a value such that the result should have a smaller magnitude, then a zero with the same sign as `start` is returned.
- If `start` is infinite and `direction` has a value such that the result should have a smaller magnitude, `https://developer.android.com/reference/kotlin/java/lang/Double#MAX_VALUE:kotlin.Double` with the same sign as `start` is returned.
- If `start` is equal to ± `https://developer.android.com/reference/kotlin/java/lang/Double#MAX_VALUE:kotlin.Double` and `direction` has a value such that the result should have a larger magnitude, an infinity with same sign as `start` is returned.

| Parameters ||
|---|---|
| `start` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): starting floating-point value |
| `direction` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): value indicating which of `start`'s neighbors or `start` should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The floating-point number adjacent to `start` in the direction of `direction`. |

### nextAfter

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextAfter(
    start: Float, 
    direction: Double
): Float
```

Returns the floating-point number adjacent to the first argument in the direction of the second argument. If both arguments compare as equal a value equivalent to the second argument is returned.

Special cases:

- If either argument is a NaN, then NaN is returned.
- If both arguments are signed zeros, a value equivalent to `direction` is returned.
- If `start` is ±`https://developer.android.com/reference/kotlin/java/lang/Float#MIN_VALUE:kotlin.Float` and `direction` has a value such that the result should have a smaller magnitude, then a zero with the same sign as `start` is returned.
- If `start` is infinite and `direction` has a value such that the result should have a smaller magnitude, `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_VALUE:kotlin.Float` with the same sign as `start` is returned.
- If `start` is equal to ± `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_VALUE:kotlin.Float` and `direction` has a value such that the result should have a larger magnitude, an infinity with same sign as `start` is returned.

| Parameters ||
|---|---|
| `start` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): starting floating-point value |
| `direction` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): value indicating which of `start`'s neighbors or `start` should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The floating-point number adjacent to `start` in the direction of `direction`. |

### nextDown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextDown(d: Double): Double
```

Returns the floating-point value adjacent to `d` in the direction of negative infinity. This method is semantically equivalent to `nextAfter(d, Double.NEGATIVE_INFINITY)`; however, a `nextDown` implementation may run faster than its equivalent `nextAfter` call.

Special Cases:

- If the argument is NaN, the result is NaN.
- If the argument is negative infinity, the result is negative infinity.
- If the argument is zero, the result is `-Double.MIN_VALUE`

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): starting floating-point value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The adjacent floating-point value closer to negative infinity. |

### nextDown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextDown(f: Float): Float
```

Returns the floating-point value adjacent to `f` in the direction of negative infinity. This method is semantically equivalent to `nextAfter(f, Float.NEGATIVE_INFINITY)`; however, a `nextDown` implementation may run faster than its equivalent `nextAfter` call.

Special Cases:

- If the argument is NaN, the result is NaN.
- If the argument is negative infinity, the result is negative infinity.
- If the argument is zero, the result is `-Float.MIN_VALUE`

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): starting floating-point value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The adjacent floating-point value closer to negative infinity. |

### nextUp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextUp(d: Double): Double
```

Returns the floating-point value adjacent to `d` in the direction of positive infinity. This method is semantically equivalent to `nextAfter(d, Double.POSITIVE_INFINITY)`; however, a `nextUp` implementation may run faster than its equivalent `nextAfter` call.

Special Cases:

- If the argument is NaN, the result is NaN.
- If the argument is positive infinity, the result is positive infinity.
- If the argument is zero, the result is `https://developer.android.com/reference/kotlin/java/lang/Double#MIN_VALUE:kotlin.Double`

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): starting floating-point value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The adjacent floating-point value closer to positive infinity. |

### nextUp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nextUp(f: Float): Float
```

Returns the floating-point value adjacent to `f` in the direction of positive infinity. This method is semantically equivalent to `nextAfter(f, Float.POSITIVE_INFINITY)`; however, a `nextUp` implementation may run faster than its equivalent `nextAfter` call.

Special Cases:

- If the argument is NaN, the result is NaN.
- If the argument is positive infinity, the result is positive infinity.
- If the argument is zero, the result is `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_VALUE:kotlin.Float`

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): starting floating-point value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The adjacent floating-point value closer to positive infinity. |

### pow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pow(
    a: Double, 
    b: Double
): Double
```

Returns the value of the first argument raised to the power of the second argument. Special cases:

- If the second argument is positive or negative zero, then the result is 1.0.
- If the second argument is 1.0, then the result is the same as the first argument.
- If the first argument is 1.0, then the result is 1.0.
- If the second argument is NaN, then the result is NaN except where the first argument is 1.0.
- If the first argument is NaN and the second argument is nonzero, then the result is NaN.
- If
 - the absolute value of the first argument is greater than 1 and the second argument is positive infinity, or
 - the absolute value of the first argument is less than 1 and the second argument is negative infinity,
 then the result is positive infinity.
- If
 - the absolute value of the first argument is greater than 1 and the second argument is negative infinity, or
 - the absolute value of the first argument is less than 1 and the second argument is positive infinity,
 then the result is positive zero.
- If the absolute value of the first argument equals 1 and the second argument is infinite, then the result is 1.0.
- If
 - the first argument is positive zero and the second argument is greater than zero, or
 - the first argument is positive infinity and the second argument is less than zero,
 then the result is positive zero.
- If
 - the first argument is positive zero and the second argument is less than zero, or
 - the first argument is positive infinity and the second argument is greater than zero,
 then the result is positive infinity.
- If
 - the first argument is negative zero and the second argument is greater than zero but not a finite odd integer, or
 - the first argument is negative infinity and the second argument is less than zero but not a finite odd integer,
 then the result is positive zero.
- If
 - the first argument is negative zero and the second argument is a positive finite odd integer, or
 - the first argument is negative infinity and the second argument is a negative finite odd integer,
 then the result is negative zero.
- If
 - the first argument is negative zero and the second argument is less than zero but not a finite odd integer, or
 - the first argument is negative infinity and the second argument is greater than zero but not a finite odd integer,
 then the result is positive infinity.
- If
 - the first argument is negative zero and the second argument is a negative finite odd integer, or
 - the first argument is negative infinity and the second argument is a positive finite odd integer,
 then the result is negative infinity.
- If the first argument is finite and less than zero
 - if the second argument is a finite even integer, the result is equal to the result of raising the absolute value of the first argument to the power of the second argument
 - if the second argument is a finite odd integer, the result is equal to the negative of the result of raising the absolute value of the first argument to the power of the second argument
 - if the second argument is finite and not an integer, then the result is NaN.
- If both arguments are integers, then the result is exactly equal to the mathematical result of raising the first argument to the power of the second argument if that result can in fact be represented exactly as a `double` value.

<br />

(In the foregoing descriptions, a floating-point value is considered to be an integer if and only if it is finite and a fixed point of the method `https://developer.android.com/reference/kotlin/java/lang/Math#ceil(kotlin.Double)` or, equivalently, a fixed point of the method `https://developer.android.com/reference/kotlin/java/lang/Math#floor(kotlin.Double)`. A value is a fixed point of a one-argument method if and only if the result of applying the method to the value is equal to the value.)

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the base. |
| `b` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the exponent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value `a``b`. |

### powExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun powExact(
    x: Int, 
    n: Int
): Int
```

Returns `x` raised to the power of `n`, throwing an exception if the result overflows an `int`. When `n` is 0, the returned value is 1.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the base. |
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the exponent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `x` raised to the power of `n`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when `n` is negative, or when the result overflows an int. |

### powExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun powExact(
    x: Long, 
    n: Int
): Long
```

Returns `x` raised to the power of `n`, throwing an exception if the result overflows a `long`. When `n` is 0, the returned value is 1.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the base. |
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the exponent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `x` raised to the power of `n`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when `n` is negative, or when the result overflows a long. |

### random

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun random(): Double
```

Returns a `double` value with a positive sign, greater than or equal to `0.0` and less than `1.0`. Returned values are chosen pseudorandomly with (approximately) uniform distribution from that range.

When this method is first called, it creates a single new pseudorandom-number generator, exactly as if by the expression
`new java.util.Random()` This new pseudorandom-number generator is used thereafter for all calls to this method and is used nowhere else.

This method is properly synchronized to allow correct use by more than one thread. However, if many threads need to generate pseudorandom numbers at a great rate, it may reduce contention for each thread to have its own pseudorandom-number generator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | a pseudorandom `double` greater than or equal to `0.0` and less than `1.0`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#nextDown(kotlin.Double)`
- `https://developer.android.com/reference/kotlin/java/util/Random.html#nextDouble()`

### rint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun rint(a: Double): Double
```

Returns the `double` value that is closest in value to the argument and is equal to a mathematical integer. If two `double` values that are mathematical integers are equally close, the result is the integer value that is even. Special cases:

- If the argument value is already equal to a mathematical integer, then the result is the same as the argument.
- If the argument is NaN or an infinity or positive zero or negative zero, then the result is the same as the argument.

<br />

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a `double` value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the closest floating-point value to `a` that is equal to a mathematical integer. |

### round

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun round(a: Double): Long
```

Returns the closest `long` to the argument, with ties rounding to positive infinity.

Special cases:

- If the argument is NaN, the result is 0.
- If the argument is negative infinity or any value less than or equal to the value of `Long.MIN_VALUE`, the result is equal to the value of `Long.MIN_VALUE`.
- If the argument is positive infinity or any value greater than or equal to the value of `Long.MAX_VALUE`, the result is equal to the value of `Long.MAX_VALUE`.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a floating-point value to be rounded to a `long`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value of the argument rounded to the nearest `long` value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Long#MAX_VALUE:kotlin.Long`
- `https://developer.android.com/reference/kotlin/java/lang/Long#MIN_VALUE:kotlin.Long`

### round

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun round(a: Float): Int
```

Returns the closest `int` to the argument, with ties rounding to positive infinity.

Special cases:

- If the argument is NaN, the result is 0.
- If the argument is negative infinity or any value less than or equal to the value of `Integer.MIN_VALUE`, the result is equal to the value of `Integer.MIN_VALUE`.
- If the argument is positive infinity or any value greater than or equal to the value of `Integer.MAX_VALUE`, the result is equal to the value of `Integer.MAX_VALUE`.

| Parameters ||
|---|---|
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a floating-point value to be rounded to an integer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of the argument rounded to the nearest `int` value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Integer#MAX_VALUE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#MIN_VALUE:kotlin.Int`

### scalb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun scalb(
    d: Double, 
    scaleFactor: Int
): Double
```

Returns `d` × 2`scaleFactor` rounded as if performed by a single correctly rounded floating-point multiply. If the exponent of the result is between `https://developer.android.com/reference/kotlin/java/lang/Double#MIN_EXPONENT:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/lang/Double#MAX_EXPONENT:kotlin.Int`, the answer is calculated exactly. If the exponent of the result would be larger than `Double.MAX_EXPONENT`, an infinity is returned. Note that if the result is subnormal, precision may be lost; that is, when `scalb(x, n)` is subnormal, `scalb(scalb(x, n), -n)` may not equal *x* . When the result is non-NaN, the result has the same sign as `d`.

Special cases:

- If the first argument is NaN, NaN is returned.
- If the first argument is infinite, then an infinity of the same sign is returned.
- If the first argument is zero, then a zero of the same sign is returned.

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): number to be scaled by a power of two. |
| `scaleFactor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): power of 2 used to scale `d` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `d` × 2`scaleFactor` |

### scalb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun scalb(
    f: Float, 
    scaleFactor: Int
): Float
```

Returns `f` × 2`scaleFactor` rounded as if performed by a single correctly rounded floating-point multiply. If the exponent of the result is between `https://developer.android.com/reference/kotlin/java/lang/Float#MIN_EXPONENT:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/lang/Float#MAX_EXPONENT:kotlin.Int`, the answer is calculated exactly. If the exponent of the result would be larger than `Float.MAX_EXPONENT`, an infinity is returned. Note that if the result is subnormal, precision may be lost; that is, when `scalb(x, n)` is subnormal, `scalb(scalb(x, n), -n)` may not equal *x* . When the result is non-NaN, the result has the same sign as `f`.

Special cases:

- If the first argument is NaN, NaN is returned.
- If the first argument is infinite, then an infinity of the same sign is returned.
- If the first argument is zero, then a zero of the same sign is returned.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): number to be scaled by a power of two. |
| `scaleFactor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): power of 2 used to scale `f` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `f` × 2`scaleFactor` |

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun signum(d: Double): Double
```

Returns the signum function of the argument; zero if the argument is zero, 1.0 if the argument is greater than zero, -1.0 if the argument is less than zero.

Special Cases:

- If the argument is NaN, then the result is NaN.
- If the argument is positive zero or negative zero, then the result is the same as the argument.

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the floating-point value whose signum is to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the signum function of the argument |

### signum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun signum(f: Float): Float
```

Returns the signum function of the argument; zero if the argument is zero, 1.0f if the argument is greater than zero, -1.0f if the argument is less than zero.

Special Cases:

- If the argument is NaN, then the result is NaN.
- If the argument is positive zero or negative zero, then the result is the same as the argument.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the floating-point value whose signum is to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the signum function of the argument |

### sin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sin(a: Double): Double
```

Returns the trigonometric sine of an angle. Special cases:

- If the argument is NaN or an infinity, then the result is NaN.
- If the argument is zero, then the result is a zero with the same sign as the argument.

<br />

The computed result must be within 1 ulp of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an angle, in radians. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the sine of the argument. |

### sinh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sinh(x: Double): Double
```

Returns the hyperbolic sine of a `double` value. The hyperbolic sine of *x* is defined to be (*ex − e−x* )/2 where *e* is [Euler's number](../java/lang/Math.md).

Special cases:

- If the argument is NaN, then the result is NaN.
- If the argument is infinite, then the result is an infinity with the same sign as the argument.
- If the argument is zero, then the result is a zero with the same sign as the argument.

The computed result must be within 2.5 ulps of the exact result.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The number whose hyperbolic sine is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The hyperbolic sine of `x`. |

### sqrt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sqrt(a: Double): Double
```

Returns the correctly rounded positive square root of a `double` value. Special cases:

- If the argument is NaN or less than zero, then the result is NaN.
- If the argument is positive infinity, then the result is positive infinity.
- If the argument is positive zero or negative zero, then the result is the same as the argument.

Otherwise, the result is the `double` value closest to the true mathematical square root of the argument value.

<br />

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the positive square root of `a`. If the argument is NaN or less than zero, the result is NaN. |

### subtractExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun subtractExact(
    x: Int, 
    y: Int
): Int
```

Returns the difference of the arguments, throwing an exception if the result overflows an `int`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second value to subtract from the first |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an int |

### subtractExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun subtractExact(
    x: Long, 
    y: Long
): Long
```

Returns the difference of the arguments, throwing an exception if the result overflows a `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second value to subtract from the first |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows a long |

### tan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun tan(a: Double): Double
```

Returns the trigonometric tangent of an angle. Special cases:

- If the argument is NaN or an infinity, then the result is NaN.
- If the argument is zero, then the result is a zero with the same sign as the argument.

<br />

The computed result must be within 1.25 ulps of the exact result. Results must be semi-monotonic.

| Parameters ||
|---|---|
| `a` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an angle, in radians. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the tangent of the argument. |

### tanh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun tanh(x: Double): Double
```

Returns the hyperbolic tangent of a `double` value. The hyperbolic tangent of *x* is defined to be (*ex − e−x* )/(*ex + e−x* ), in other words, [sinh(*x*)](../java/lang/Math.md))/ [cosh(*x*)](../java/lang/Math.md)). Note that the absolute value of the exact tanh is always less than 1.

Special cases:

- If the argument is NaN, then the result is NaN.
- If the argument is zero, then the result is a zero with the same sign as the argument.
- If the argument is positive infinity, then the result is `+1.0`.
- If the argument is negative infinity, then the result is `-1.0`.

The computed result must be within 2.5 ulps of the exact result. The result of `tanh` for any finite input must have an absolute value less than or equal to 1. Note that once the exact result of tanh is within 1/2 of an ulp of the limit value of ±1, correctly signed ±`1.0` should be returned.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The number whose hyperbolic tangent is to be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The hyperbolic tangent of `x`. |

### toDegrees

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toDegrees(angrad: Double): Double
```

Converts an angle measured in radians to an approximately equivalent angle measured in degrees. The conversion from radians to degrees is generally inexact; users should *not* expect `cos(toRadians(90.0))` to exactly equal `0.0`.

| Parameters ||
|---|---|
| `angrad` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an angle, in radians |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the measurement of the angle `angrad` in degrees. |

### toIntExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toIntExact(value: Long): Int
```

Returns the value of the `long` argument, throwing an exception if the value overflows an `int`.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the long value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the argument as an int |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the `argument` overflows an int |

### toRadians

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toRadians(angdeg: Double): Double
```

Converts an angle measured in degrees to an approximately equivalent angle measured in radians. The conversion from degrees to radians is generally inexact.

| Parameters ||
|---|---|
| `angdeg` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): an angle, in degrees |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the measurement of the angle `angdeg` in radians. |

### ulp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ulp(d: Double): Double
```

Returns the size of an ulp of the argument. An ulp, unit in the last place, of a `double` value is the positive distance between this floating-point value and the `double` value next larger in magnitude. Note that for non-NaN *x* , `ulp(-x) == ulp(x)`.

Special Cases:

- If the argument is NaN, then the result is NaN.
- If the argument is positive or negative infinity, then the result is positive infinity.
- If the argument is positive or negative zero, then the result is `Double.MIN_VALUE`.
- If the argument is ±`Double.MAX_VALUE`, then the result is equal to 2971.

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the floating-point value whose ulp is to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the size of an ulp of the argument |

### ulp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ulp(f: Float): Float
```

Returns the size of an ulp of the argument. An ulp, unit in the last place, of a `float` value is the positive distance between this floating-point value and the `float` value next larger in magnitude. Note that for non-NaN *x* , `ulp(-x) == ulp(x)`.

Special Cases:

- If the argument is NaN, then the result is NaN.
- If the argument is positive or negative infinity, then the result is positive infinity.
- If the argument is positive or negative zero, then the result is `Float.MIN_VALUE`.
- If the argument is ±`Float.MAX_VALUE`, then the result is equal to 2104.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the floating-point value whose ulp is to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the size of an ulp of the argument |

### unsignedMultiplyExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedMultiplyExact(
    x: Int, 
    y: Int
): Int
```

Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `int`.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first unsigned value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second unsigned value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an unsigned int |

### unsignedMultiplyExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedMultiplyExact(
    x: Long, 
    y: Int
): Long
```

Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first unsigned value |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second unsigned value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an unsigned long |

### unsignedMultiplyExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedMultiplyExact(
    x: Long, 
    y: Long
): Long
```

Returns the product of the unsigned arguments, throwing an exception if the result overflows an unsigned `long`.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first unsigned value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second unsigned value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if the result overflows an unsigned long |

### unsignedMultiplyHigh

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedMultiplyHigh(
    x: Long, 
    y: Long
): Long
```

Returns as a `long` the most significant 64 bits of the unsigned 128-bit product of two unsigned 64-bit factors.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the first value |
| `y` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the result |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math#multiplyHigh(kotlin.Long,%20kotlin.Long)`

### unsignedPowExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedPowExact(
    x: Int, 
    n: Int
): Int
```

Returns unsigned `x` raised to the power of `n`, throwing an exception if the result overflows an unsigned `int`. When `n` is 0, the returned value is 1.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the unsigned base. |
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the exponent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `x` raised to the power of `n`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when `n` is negative, or when the result overflows an unsigned int. |

### unsignedPowExact

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun unsignedPowExact(
    x: Long, 
    n: Int
): Long
```

Returns unsigned `x` raised to the power of `n`, throwing an exception if the result overflows an unsigned `long`. When `n` is 0, the returned value is 1.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the unsigned base. |
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the exponent. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `x` raised to the power of `n`. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when `n` is negative, or when the result overflows an unsigned long. |
