# NinePatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NinePatch

Kotlin| [Java](https://developer.android.com/reference/android/graphics/NinePatch "View this page in Java") 
| --- | --- |

```
open class NinePatch
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#) |

The NinePatch class permits drawing a bitmap in nine or more sections. Essentially, it allows the creation of custom graphics that will scale the way that you define, when content added within the image exceeds the normal bounds of the graphic. For a thorough explanation of a NinePatch image, read the discussion in the [2D Graphics](https://developer.android.com/guide/topics/graphics/2d-graphics.html#nine-patch) document.

The [Draw 9-Patch](https://developer.android.com/guide/developing/tools/draw9patch.html) tool offers an extremely handy way to create your NinePatch images, using a WYSIWYG graphics editor.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#NinePatch(android.graphics.Bitmap,%20kotlin.ByteArray))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create a drawable projection from a bitmap to nine patches. |
| [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#NinePatch(android.graphics.Bitmap,%20kotlin.ByteArray,%20kotlin.String))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable projection from a bitmap to nine patches. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.Rect))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!`, `location:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!`)` Draws the NinePatch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.Rect,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!`, `location:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)!`)` Draws the NinePatch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.RectF))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!`, `location:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`)` Draws the NinePatch. |
| --- | --- |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)! | [getBitmap](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getBitmap())`()` Returns the bitmap used to draw this NinePatch. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDensity](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getDensity())`()` Return the underlying bitmap's density, as per [Bitmap.getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getHeight())`()` Returns the intrinsic height, in pixels, of this NinePatch. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getName())`()` Returns the name of this NinePatch object if one was specified when calling the constructor. |
| open [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)! | [getPaint](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint())`()` Returns the paint used to draw this NinePatch. |
| [Region](https://developer.android.com/reference/kotlin/android/graphics/Region)! | [getTransparentRegion](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getTransparentRegion(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!`)` Returns a [Region](https://developer.android.com/reference/kotlin/android/graphics/Region) representing the parts of the NinePatch that are completely transparent. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getWidth())`()` Returns the intrinsic width, in pixels, of this NinePatch. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#hasAlpha())`()` Indicates whether this NinePatch contains transparent or translucent pixels. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNinePatchChunk](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#isNinePatchChunk(kotlin.ByteArray))`(`chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Verifies that the specified byte array is a valid 9-patch data chunk. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPaint](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#setPaint(android.graphics.Paint))`(`p:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)!`)` Sets the paint to use when drawing the NinePatch. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#finalize())`()` <br /> |

## Public constructors

### NinePatch

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatch(
    bitmap: Bitmap!, 
    chunk: ByteArray!)
```

Create a drawable projection from a bitmap to nine patches.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)!:The bitmap describing the patches. |
| `chunk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The 9-patch data chunk describing how the underlying bitmap is split apart and drawn. |

### NinePatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NinePatch(
    bitmap: Bitmap!, 
    chunk: ByteArray!, 
    srcName: String!)
```

Create a drawable projection from a bitmap to nine patches.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)!:The bitmap describing the patches. |
| `chunk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The 9-patch data chunk describing how the underlying bitmap is split apart and drawn. |
| `srcName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the source for the bitmap. Might be null. |
| --- | --- |

## Public methods

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    location: Rect!
): Unit
```

Draws the NinePatch. This method will use the paint returned by [getPaint()](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint()).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!:Where to draw the NinePatch. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    location: Rect!, 
    paint: Paint!
): Unit
```

Draws the NinePatch. This method will ignore the paint returned by [getPaint()](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint())and use the specified paint instead.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!:Where to draw the NinePatch. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)!:The Paint to draw through. |
| --- | --- |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    location: RectF!
): Unit
```

Draws the NinePatch. This method will use the paint returned by [getPaint()](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint()).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:Where to draw the NinePatch. |

### getBitmap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBitmap(): Bitmap!
```

Returns the bitmap used to draw this NinePatch. 

### getDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDensity(): Int
```

Return the underlying bitmap's density, as per [Bitmap.getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()). 

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Returns the intrinsic height, in pixels, of this NinePatch. This is equivalent to querying the height of the underlying bitmap returned by [getBitmap()](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getBitmap()). 

### getName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the name of this NinePatch object if one was specified when calling the constructor. 

### getPaint

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPaint(): Paint!
```

Returns the paint used to draw this NinePatch. The paint can be null. 
**See Also**

- [#setPaint(Paint)](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#setPaint(android.graphics.Paint))
- [#draw(Canvas, Rect)](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.Rect))
- [#draw(Canvas, RectF)](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.RectF)) 

### getTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransparentRegion(bounds: Rect!): Region!
```

Returns a [Region](https://developer.android.com/reference/kotlin/android/graphics/Region) representing the parts of the NinePatch that are completely transparent.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!:The location and size of the NinePatch. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Region](https://developer.android.com/reference/kotlin/android/graphics/Region)! | null if the NinePatch has no transparent region to report, else a [Region](https://developer.android.com/reference/kotlin/android/graphics/Region) holding the parts of the specified bounds that are transparent. |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Returns the intrinsic width, in pixels, of this NinePatch. This is equivalent to querying the width of the underlying bitmap returned by [getBitmap()](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getBitmap()). 

### hasAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAlpha(): Boolean
```

Indicates whether this NinePatch contains transparent or translucent pixels. This is equivalent to calling`getBitmap().hasAlpha()`on this NinePatch. 

### isNinePatchChunk

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isNinePatchChunk(chunk: ByteArray!): Boolean
```

Verifies that the specified byte array is a valid 9-patch data chunk.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `chunk` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array representing a 9-patch data chunk. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the specified byte array represents a 9-patch data chunk, false otherwise. |

### setPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPaint(p: Paint!): Unit
```

Sets the paint to use when drawing the NinePatch.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------|
| `p` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)!:The paint that will be used to draw this NinePatch. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint()>
- [#draw(Canvas, Rect)](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.Rect))
- [#draw(Canvas, RectF)](https://developer.android.com/reference/kotlin/android/graphics/NinePatch#draw(android.graphics.Canvas,%20android.graphics.RectF))

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
