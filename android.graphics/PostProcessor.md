# PostProcessor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PostProcessor

Kotlin | [Java](https://developer.android.com/reference/android/graphics/PostProcessor "View this page in Java") 

```
interface PostProcessor
```

| [android.graphics.PostProcessor](https://developer.android.com/reference/kotlin/android/graphics/PostProcessor#) |

Helper interface for adding custom processing to an image.

The image being processed may be a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable), a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap), or a frame of an [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable) produced by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder). This is called before the requested object is returned.

This custom processing can even be applied to images that will be returned as immutable objects, such as a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) with `Config` [Bitmap.Config.HARDWARE](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config) returned by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder).

On an [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable), the callback will only be called once, but the drawing commands will be applied to each frame, as if the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) had been returned by [Picture.beginRecording](https://developer.android.com/reference/kotlin/android/graphics/Picture#beginRecording(kotlin.Int,%20kotlin.Int)).

Supplied to ImageDecoder via [setPostProcessor](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setPostProcessor(android.graphics.PostProcessor)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onPostProcess](https://developer.android.com/reference/kotlin/android/graphics/PostProcessor#onPostProcess(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas)`)` Do any processing after (for example) decoding. |

## Public methods

### onPostProcess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPostProcess(canvas: Canvas): Int
```

Do any processing after (for example) decoding.

Drawing to the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) will behave as if the initial processing (e.g. decoding) already exists in the Canvas. An implementation can draw effects on top of this, or it can even draw behind it using [PorterDuff.Mode.DST_OVER](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode). A common effect is to add transparency to the corners to achieve rounded corners. That can be done with the following code: 

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas): The [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) to draw to. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Opacity of the result after drawing. [PixelFormat.UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#UNKNOWN:kotlin.Int) means that the implementation did not change whether the image has alpha. Return this unless you added transparency (e.g. with the code above, in which case you should return [PixelFormat.TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSLUCENT:kotlin.Int)) or you forced the image to be opaque (e.g. by drawing everywhere with an opaque color and [PorterDuff.Mode.DST_OVER](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode), in which case you should return [PixelFormat.OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#OPAQUE:kotlin.Int)). [PixelFormat.TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSLUCENT:kotlin.Int) means that the implementation added transparency. This is safe to return even if the image already had transparency. This is also safe to return if the result is opaque, though it may draw more slowly. [PixelFormat.OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#OPAQUE:kotlin.Int) means that the implementation forced the image to be opaque. This is safe to return even if the image was already opaque. [PixelFormat.TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSPARENT:kotlin.Int) (or any other integer) is not allowed, and will result in throwing an [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#). Value is [android.graphics.PixelFormat#UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#UNKNOWN:kotlin.Int), [android.graphics.PixelFormat#TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSLUCENT:kotlin.Int), [android.graphics.PixelFormat#TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSPARENT:kotlin.Int), or [android.graphics.PixelFormat#OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#OPAQUE:kotlin.Int) |
