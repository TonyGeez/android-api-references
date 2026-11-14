# Movie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Movie

Kotlin| [Java](Movie.md) 
| --- | --- |

```
open class Movie
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Movie](Movie.md) |

| **This class was deprecated in API level 28.**
|
| Prefer [android.graphics.drawable.AnimatedImageDrawable](../android.graphics.drawable/AnimatedImageDrawable.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Movie](Movie.md)! | [decodeByteArray](Movie.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Movie](Movie.md)! | [decodeFile](Movie.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Movie](Movie.md)! | [decodeStream](Movie.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](Movie.md))`(`canvas:` ` [Canvas](Canvas.md)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](Movie.md))`(`canvas:` ` [Canvas](Canvas.md)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](Paint.md)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [duration](Movie.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [height](Movie.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](Movie.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setTime](Movie.md))`(`relativeMilliseconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [width](Movie.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](Movie.md))`()` <br /> |

## Public methods

### decodeByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decodeByteArray(
    data: ByteArray!, 
    offset: Int, 
    length: Int
): Movie!
```

**Deprecated:** *Deprecated in Java.* 

### decodeFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decodeFile(pathName: String!): Movie!
```

**Deprecated:** *Deprecated in Java.* 

### decodeStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decodeStream(is: InputStream!): Movie!
```

**Deprecated:** *Deprecated in Java.* 

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    x: Float, 
    y: Float, 
    paint: Paint!
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### duration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun duration(): Int
```

**Deprecated:** *Deprecated in Java.* 

### height

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun height(): Int
```

**Deprecated:** *Deprecated in Java.* 

### isOpaque

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpaque(): Boolean
```

**Deprecated:** *Deprecated in Java.* 

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(relativeMilliseconds: Int): Boolean
```

**Deprecated:** *Deprecated in Java.* 

### width

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun width(): Int
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
