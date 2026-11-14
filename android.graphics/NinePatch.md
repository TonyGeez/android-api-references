# NinePatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NinePatch

Kotlin| [Java](../android/graphics/NinePatch.md) 
| --- | --- |

```
open class NinePatch
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.NinePatch](../android/graphics/NinePatch.md) |

The NinePatch class permits drawing a bitmap in nine or more sections. Essentially, it allows the creation of custom graphics that will scale the way that you define, when content added within the image exceeds the normal bounds of the graphic. For a thorough explanation of a NinePatch image, read the discussion in the [2D Graphics](https://developer.android.com/guide/topics/graphics/2d-graphics.html#nine-patch) document.

The [Draw 9-Patch](https://developer.android.com/guide/developing/tools/draw9patch.html) tool offers an extremely handy way to create your NinePatch images, using a WYSIWYG graphics editor.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NinePatch](../android/graphics/NinePatch.md))`(`bitmap:` ` [Bitmap](../android/graphics/Bitmap.md)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create a drawable projection from a bitmap to nine patches. |
| [NinePatch](../android/graphics/NinePatch.md))`(`bitmap:` ` [Bitmap](../android/graphics/Bitmap.md)!`, `chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a drawable projection from a bitmap to nine patches. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/NinePatch.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `location:` ` [Rect](../android/graphics/Rect.md)!`)` Draws the NinePatch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/NinePatch.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `location:` ` [Rect](../android/graphics/Rect.md)!`, `paint:` ` [Paint](../android/graphics/Paint.md)!`)` Draws the NinePatch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/NinePatch.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `location:` ` [RectF](../android/graphics/RectF.md)!`)` Draws the NinePatch. |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)! | [getBitmap](../android/graphics/NinePatch.md))`()` Returns the bitmap used to draw this NinePatch. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDensity](../android/graphics/NinePatch.md))`()` Return the underlying bitmap's density, as per [Bitmap.getDensity()](../android/graphics/Bitmap.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](../android/graphics/NinePatch.md))`()` Returns the intrinsic height, in pixels, of this NinePatch. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/graphics/NinePatch.md))`()` Returns the name of this NinePatch object if one was specified when calling the constructor. |
| open [Paint](../android/graphics/Paint.md)! | [getPaint](../android/graphics/NinePatch.md))`()` Returns the paint used to draw this NinePatch. |
| [Region](../android/graphics/Region.md)! | [getTransparentRegion](../android/graphics/NinePatch.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)!`)` Returns a [Region](../android/graphics/Region.md) representing the parts of the NinePatch that are completely transparent. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](../android/graphics/NinePatch.md))`()` Returns the intrinsic width, in pixels, of this NinePatch. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](../android/graphics/NinePatch.md))`()` Indicates whether this NinePatch contains transparent or translucent pixels. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNinePatchChunk](../android/graphics/NinePatch.md))`(`chunk:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Verifies that the specified byte array is a valid 9-patch data chunk. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPaint](../android/graphics/NinePatch.md))`(`p:` ` [Paint](../android/graphics/Paint.md)!`)` Sets the paint to use when drawing the NinePatch. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/NinePatch.md))`()` <br /> |

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
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md)!:The bitmap describing the patches. |
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
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md)!:The bitmap describing the patches. |
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

Draws the NinePatch. This method will use the paint returned by [getPaint()](../android/graphics/NinePatch.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [Rect](../android/graphics/Rect.md)!:Where to draw the NinePatch. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    location: Rect!, 
    paint: Paint!
): Unit
```

Draws the NinePatch. This method will ignore the paint returned by [getPaint()](../android/graphics/NinePatch.md))and use the specified paint instead.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [Rect](../android/graphics/Rect.md)!:Where to draw the NinePatch. |
| `paint` | [Paint](../android/graphics/Paint.md)!:The Paint to draw through. |
| --- | --- |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    location: RectF!
): Unit
```

Draws the NinePatch. This method will use the paint returned by [getPaint()](../android/graphics/NinePatch.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:A container for the current matrix and clip used to draw the NinePatch. |
| `location` | [RectF](../android/graphics/RectF.md)!:Where to draw the NinePatch. |

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

Return the underlying bitmap's density, as per [Bitmap.getDensity()](../android/graphics/Bitmap.md)). 

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Returns the intrinsic height, in pixels, of this NinePatch. This is equivalent to querying the height of the underlying bitmap returned by [getBitmap()](../android/graphics/NinePatch.md)). 

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

- [#setPaint(Paint)](../android/graphics/NinePatch.md))
- [#draw(Canvas, Rect)](../android/graphics/NinePatch.md))
- [#draw(Canvas, RectF)](../android/graphics/NinePatch.md)) 

### getTransparentRegion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransparentRegion(bounds: Rect!): Region!
```

Returns a [Region](../android/graphics/Region.md) representing the parts of the NinePatch that are completely transparent.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android/graphics/Rect.md)!:The location and size of the NinePatch. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Region](../android/graphics/Region.md)! | null if the NinePatch has no transparent region to report, else a [Region](../android/graphics/Region.md) holding the parts of the specified bounds that are transparent. |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Returns the intrinsic width, in pixels, of this NinePatch. This is equivalent to querying the width of the underlying bitmap returned by [getBitmap()](../android/graphics/NinePatch.md)). 

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
| `p` | [Paint](../android/graphics/Paint.md)!:The paint that will be used to draw this NinePatch. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/NinePatch#getPaint()>
- [#draw(Canvas, Rect)](../android/graphics/NinePatch.md))
- [#draw(Canvas, RectF)](../android/graphics/NinePatch.md))

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
