# Picture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Picture

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Picture "View this page in Java") 
| --- | --- |

```
open class Picture
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture#) |

A Picture records drawing calls (via the canvas returned by beginRecording) and can then play them back into Canvas (via [Picture.draw(Canvas)](https://developer.android.com/reference/kotlin/android/graphics/Picture#draw(android.graphics.Canvas))or [Canvas.drawPicture(Picture)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture))).For most content (e.g. text, lines, rectangles), drawing a sequence from a picture can be faster than the equivalent API calls, since the picture performs its playback without incurring any method-call overhead.

**Note:**Prior to API level 23 a picture cannot be replayed on a hardware accelerated canvas.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture#Picture())`()` Creates an empty picture that is ready to record. |
| [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture#Picture(android.graphics.Picture))`(`src:` ` [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture#)!`)` Create a picture by making a copy of what has already been recorded in src. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) | [beginRecording](https://developer.android.com/reference/kotlin/android/graphics/Picture#beginRecording(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` To record a picture, call beginRecording() and then draw into the Canvas that is returned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/Picture#draw(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)`)` Draw this picture on the canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endRecording](https://developer.android.com/reference/kotlin/android/graphics/Picture#endRecording())`()` Call endRecording when the picture is built. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/Picture#getHeight())`()` Get the height of the picture as passed to beginRecording. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/Picture#getWidth())`()` Get the width of the picture as passed to beginRecording. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresHardwareAcceleration](https://developer.android.com/reference/kotlin/android/graphics/Picture#requiresHardwareAcceleration())`()` Indicates whether or not this Picture contains recorded commands that only work when drawn to a hardware-accelerated canvas. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/Picture#finalize())`()` <br /> |

## Public constructors

### Picture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Picture()
```

Creates an empty picture that is ready to record. 

### Picture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Picture(src: Picture!)
```

Create a picture by making a copy of what has already been recorded in src. The contents of src are unchanged, and if src changes later, those changes will not be reflected in this picture.

## Public methods

### beginRecording

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun beginRecording(
    width: Int, 
    height: Int
): Canvas
```

To record a picture, call beginRecording() and then draw into the Canvas that is returned. Nothing we appear on screen, but all of the draw commands (e.g. [Canvas.drawRect(Rect, Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRect(android.graphics.Rect,%20android.graphics.Paint))) will be recorded. To stop recording, call endRecording(). After endRecording() the Canvas that was returned must no longer be used, and nothing should be drawn into it.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) | This value cannot be`null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas): Unit
```

Draw this picture on the canvas.

Prior to [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int), this call could have the side effect of changing the matrix and clip of the canvas if this picture had imbalanced saves/restores.

**Note:** This forces the picture to internally call [Picture.endRecording()](https://developer.android.com/reference/kotlin/android/graphics/Picture#endRecording())in order to prepare for playback.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas):The picture is drawn to this canvas This value cannot be`null`. |

### endRecording

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endRecording(): Unit
```

Call endRecording when the picture is built. After this call, the picture may be drawn, but the canvas that was returned by beginRecording must not be used anymore. This is automatically called if [Picture.draw](https://developer.android.com/reference/kotlin/android/graphics/Picture#draw(android.graphics.Canvas))or [Canvas.drawPicture(Picture)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture))is called. 

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Get the height of the picture as passed to beginRecording. This does not reflect (per se) the content of the picture. 

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Get the width of the picture as passed to beginRecording. This does not reflect (per se) the content of the picture. 

### requiresHardwareAcceleration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requiresHardwareAcceleration(): Boolean
```

Indicates whether or not this Picture contains recorded commands that only work when drawn to a hardware-accelerated canvas. If this returns true then this Picture can only be drawn to another Picture or to a Canvas where canvas.isHardwareAccelerated() is true. Note this value is only updated after recording has finished by a call to [endRecording()](https://developer.android.com/reference/kotlin/android/graphics/Picture#endRecording()). Prior to that it will be the default value of false.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the Picture can only be drawn to a hardware-accelerated canvas, false otherwise. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
