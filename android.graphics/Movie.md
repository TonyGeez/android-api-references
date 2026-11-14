# Movie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Movie

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Movie "View this page in Java") 

```
open class Movie
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie#) |

| **This class was deprecated in API level 28.**
|
| Prefer [android.graphics.drawable.AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie#)! | [decodeByteArray](https://developer.android.com/reference/kotlin/android/graphics/Movie#decodeByteArray(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie#)! | [decodeFile](https://developer.android.com/reference/kotlin/android/graphics/Movie#decodeFile(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie#)! | [decodeStream](https://developer.android.com/reference/kotlin/android/graphics/Movie#decodeStream(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/Movie#draw(android.graphics.Canvas,%20kotlin.Float,%20kotlin.Float))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/Movie#draw(android.graphics.Canvas,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [duration](https://developer.android.com/reference/kotlin/android/graphics/Movie#duration())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [height](https://developer.android.com/reference/kotlin/android/graphics/Movie#height())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](https://developer.android.com/reference/kotlin/android/graphics/Movie#isOpaque())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setTime](https://developer.android.com/reference/kotlin/android/graphics/Movie#setTime(kotlin.Int))`(`relativeMilliseconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [width](https://developer.android.com/reference/kotlin/android/graphics/Movie#width())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/Movie#finalize())`()` <br /> |

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
