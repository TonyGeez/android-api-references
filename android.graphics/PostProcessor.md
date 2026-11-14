# PostProcessor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PostProcessor

Kotlin | [Java](PostProcessor.md) 
| --- | --- |

```
interface PostProcessor
```

| [android.graphics.PostProcessor](PostProcessor.md) |

Helper interface for adding custom processing to an image.

The image being processed may be a [Drawable](../android.graphics.drawable/Drawable.md), a [Bitmap](Bitmap.md), or a frame of an [AnimatedImageDrawable](../android.graphics.drawable/AnimatedImageDrawable.md) produced by [ImageDecoder](ImageDecoder.md). This is called before the requested object is returned.

This custom processing can even be applied to images that will be returned as immutable objects, such as a [Bitmap](Bitmap.md) with `Config` [Bitmap.Config.HARDWARE](../android/graphics/Bitmap.Config.md) returned by [ImageDecoder](ImageDecoder.md).

On an [AnimatedImageDrawable](../android.graphics.drawable/AnimatedImageDrawable.md), the callback will only be called once, but the drawing commands will be applied to each frame, as if the [Canvas](Canvas.md) had been returned by [Picture.beginRecording](Picture.md)).

Supplied to ImageDecoder via [setPostProcessor](ImageDecoder.md)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onPostProcess](PostProcessor.md))`(`canvas:` ` [Canvas](Canvas.md)`)` Do any processing after (for example) decoding. |

## Public methods

### onPostProcess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPostProcess(canvas: Canvas): Int
```

Do any processing after (for example) decoding.

Drawing to the [Canvas](Canvas.md) will behave as if the initial processing (e.g. decoding) already exists in the Canvas. An implementation can draw effects on top of this, or it can even draw behind it using [PorterDuff.Mode.DST_OVER](../android/graphics/PorterDuff.Mode.md). A common effect is to add transparency to the corners to achieve rounded corners. That can be done with the following code: 

```kotlin
Path path = new Path();
   path.setFillType(Path.FillType.INVERSE_EVEN_ODD);
   int width = canvas.getWidth();
   int height = canvas.getHeight();
   path.addRoundRect(0, 0, width, height, 20, 20, Path.Direction.CW);
   Paint paint = new Paint();
   paint.setAntiAlias(true);
   paint.setColor(Color.TRANSPARENT);
   paint.setXfermode(new PorterDuffXfermode(PorterDuff.Mode.SRC));
   canvas.drawPath(path, paint);
   return PixelFormat.TRANSLUCENT;
   
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](Canvas.md): The [Canvas](Canvas.md) to draw to. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Opacity of the result after drawing. [PixelFormat.UNKNOWN](PixelFormat.md) means that the implementation did not change whether the image has alpha. Return this unless you added transparency (e.g. with the code above, in which case you should return [PixelFormat.TRANSLUCENT](PixelFormat.md)) or you forced the image to be opaque (e.g. by drawing everywhere with an opaque color and [PorterDuff.Mode.DST_OVER](../android/graphics/PorterDuff.Mode.md), in which case you should return [PixelFormat.OPAQUE](PixelFormat.md)). [PixelFormat.TRANSLUCENT](PixelFormat.md) means that the implementation added transparency. This is safe to return even if the image already had transparency. This is also safe to return if the result is opaque, though it may draw more slowly. [PixelFormat.OPAQUE](PixelFormat.md) means that the implementation forced the image to be opaque. This is safe to return even if the image was already opaque. [PixelFormat.TRANSPARENT](PixelFormat.md) (or any other integer) is not allowed, and will result in throwing an [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md). Value is [android.graphics.PixelFormat#UNKNOWN](PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](PixelFormat.md) |
