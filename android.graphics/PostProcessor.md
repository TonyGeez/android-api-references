# PostProcessor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PostProcessor

Kotlin | [Java](../android/graphics/PostProcessor.md) 
| --- | --- |

```
interface PostProcessor
```

| [android.graphics.PostProcessor](../android/graphics/PostProcessor.md) |

Helper interface for adding custom processing to an image.

The image being processed may be a [Drawable](../android/graphics/drawable/Drawable.md), a [Bitmap](../android/graphics/Bitmap.md), or a frame of an [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md) produced by [ImageDecoder](../android/graphics/ImageDecoder.md). This is called before the requested object is returned.

This custom processing can even be applied to images that will be returned as immutable objects, such as a [Bitmap](../android/graphics/Bitmap.md) with `Config` [Bitmap.Config.HARDWARE](../android/graphics/Bitmap.Config.md) returned by [ImageDecoder](../android/graphics/ImageDecoder.md).

On an [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md), the callback will only be called once, but the drawing commands will be applied to each frame, as if the [Canvas](../android/graphics/Canvas.md) had been returned by [Picture.beginRecording](../android/graphics/Picture.md)).

Supplied to ImageDecoder via [setPostProcessor](../android/graphics/ImageDecoder.md)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onPostProcess](../android/graphics/PostProcessor.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`)` Do any processing after (for example) decoding. |

## Public methods

### onPostProcess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPostProcess(canvas: Canvas): Int
```

Do any processing after (for example) decoding.

Drawing to the [Canvas](../android/graphics/Canvas.md) will behave as if the initial processing (e.g. decoding) already exists in the Canvas. An implementation can draw effects on top of this, or it can even draw behind it using [PorterDuff.Mode.DST_OVER](../android/graphics/PorterDuff.Mode.md). A common effect is to add transparency to the corners to achieve rounded corners. That can be done with the following code: 

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
| `canvas` | [Canvas](../android/graphics/Canvas.md): The [Canvas](../android/graphics/Canvas.md) to draw to. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Opacity of the result after drawing. [PixelFormat.UNKNOWN](../android/graphics/PixelFormat.md) means that the implementation did not change whether the image has alpha. Return this unless you added transparency (e.g. with the code above, in which case you should return [PixelFormat.TRANSLUCENT](../android/graphics/PixelFormat.md)) or you forced the image to be opaque (e.g. by drawing everywhere with an opaque color and [PorterDuff.Mode.DST_OVER](../android/graphics/PorterDuff.Mode.md), in which case you should return [PixelFormat.OPAQUE](../android/graphics/PixelFormat.md)). [PixelFormat.TRANSLUCENT](../android/graphics/PixelFormat.md) means that the implementation added transparency. This is safe to return even if the image already had transparency. This is also safe to return if the result is opaque, though it may draw more slowly. [PixelFormat.OPAQUE](../android/graphics/PixelFormat.md) means that the implementation forced the image to be opaque. This is safe to return even if the image was already opaque. [PixelFormat.TRANSPARENT](../android/graphics/PixelFormat.md) (or any other integer) is not allowed, and will result in throwing an [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md). Value is [android.graphics.PixelFormat#UNKNOWN](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSLUCENT](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#TRANSPARENT](../android/graphics/PixelFormat.md), or [android.graphics.PixelFormat#OPAQUE](../android/graphics/PixelFormat.md) |
