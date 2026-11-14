Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageDecoder

```
class ImageDecoder : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#) |

A class for converting encoded images (like `PNG`, `JPEG`, `WEBP`, `GIF`, or `HEIF`) into `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` objects.

To use it, first create a `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` using one of the `createSource` overloads. For example, to decode from a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, call `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(android.content.ContentResolver,%20android.net.Uri)` and pass the result to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source)` or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source)`:

```kotlin
File file = new File(...);
   ImageDecoder.Source source = ImageDecoder.createSource(file);
   Drawable drawable = ImageDecoder.decodeDrawable(source);
   
```

To change the default settings, pass the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` and an `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)` or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)`. For example, to create a sampled image with half the width and height of the original image, call `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSampleSize(kotlin.Int)` inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`:

```kotlin
OnHeaderDecodedListener listener = new OnHeaderDecodedListener() {
       public void onHeaderDecoded(ImageDecoder decoder, ImageInfo info, Source source) {
           decoder.setTargetSampleSize(2);
       }
   };
   Drawable drawable = ImageDecoder.decodeDrawable(source, listener);
   
```

The `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` contains information about the encoded image, like its width and height, and the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` can be used to match to a particular `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` if a single `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` is used with multiple `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` objects.

The `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` can also be implemented as a lambda:

```kotlin
Drawable drawable = ImageDecoder.decodeDrawable(source, (decoder, info, src) -> {
       decoder.setTargetSampleSize(2);
   });
   
```

If the encoded image is an animated `GIF` or `WEBP`, #decodeDrawable will return an `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable`. To start its animation, call `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable#start()`:

```kotlin
Drawable drawable = ImageDecoder.decodeDrawable(source);
   if (drawable instanceof AnimatedImageDrawable) {
       ((AnimatedImageDrawable) drawable).start();
   }
   
```

By default, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` created by `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#` (including one that is inside a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable`) will be immutable (i.e. `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isMutable()` returns `false`), and it will typically have `Config` `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`. Although these properties can be changed with `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setMutableRequired(kotlin.Boolean)` (which is only compatible with `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source)` and `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)`) and `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setAllocator(kotlin.Int)`, it is also possible to apply custom effects regardless of the mutability of the final returned object by passing a `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor` to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setPostProcessor(android.graphics.PostProcessor)`. A `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor` can also be a lambda:

```kotlin
Drawable drawable = ImageDecoder.decodeDrawable(source, (decoder, info, src) -> {
       decoder.setPostProcessor((canvas) -> {
               // This will create rounded corners.
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
       });
   });
   
```

If the encoded image is incomplete or contains an error, or if an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` occurs during decoding, a `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException` will be thrown. In some cases, the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#` may have decoded part of the image. In order to display the partial image, an `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` must be passed to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setOnPartialImageListener(android.graphics.ImageDecoder.OnPartialImageListener)`. For example:

```kotlin
Drawable drawable = ImageDecoder.decodeDrawable(source, (decoder, info, src) -> {
       decoder.setOnPartialImageListener((DecodeException e) -> {
               // Returning true indicates to create a Drawable or Bitmap even
               // if the whole image could not be decoded. Any remaining lines
               // will be blank.
               return true;
       });
   });
   
```

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException` Information about an interrupted decode. |
| | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` Information about an encoded image. |
| abstract | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` Interface for changing the default settings of a decode. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` Interface for inspecting a `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException` and potentially preventing it from being thrown. |
| abstract | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` Source of encoded image data. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_DEFAULT:kotlin.Int` Use the default allocation for the pixel memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_HARDWARE:kotlin.Int` Require a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SHARED_MEMORY:kotlin.Int` Use shared memory for the pixel memory. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SOFTWARE:kotlin.Int` Use a software allocation for the pixel memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_DEFAULT:kotlin.Int` Use the most natural `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` for the internal `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_LOW_RAM:kotlin.Int` Save memory if possible by using a denser `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` at the cost of some image quality. |
| --- | --- |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#close()()` Closes this resource, relinquishing any underlying resources. |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(android.content.ContentResolver,%20android.net.Uri)(cr: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(android.content.res.AssetManager,%20kotlin.String)(assets: https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#, fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a file in the "assets" directory. |
| --- | --- |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(android.content.res.Resources,%20kotlin.Int)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a resource. |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(kotlin.ByteArray)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a byte array. |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a byte array. |
| --- | --- |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(java.io.File)(file: https://developer.android.com/reference/kotlin/java/io/File.html#)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/io/File.html#`. |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(java.nio.ByteBuffer)(buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` |
| static [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(java.util.concurrent.Callable)(callable: https://developer.android.com/reference/kotlin/java/util/concurrent/Callable.html#<https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#!>)` Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/util/concurrent/Callable.html#` that returns a new `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` for each request. |
| --- | --- |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source)(src: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source)` Create a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` from a `Source` |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)(src: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source, listener: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)` Create a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` from a `Source`. |
| static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source)(src: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source)` Create a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` from a `Source` |
| --- | --- |
| static [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)(src: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source, listener: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)` Create a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` from a `Source`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getAllocationLimit()()` Get the maximum memory limit in bytes for image decoding. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getAllocator()()` Return the allocator for the pixel memory. |
| --- | --- |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)? | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getCrop()()` Return the cropping rectangle, if set. |
| static [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)? | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getDefaultProcessListener()()` Return the process-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. |
| static [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)? | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getDefaultThreadListener()()` Return the thread-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getMemorySizePolicy()()` Retrieve the memory policy for the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| [ImageDecoder.OnPartialImageListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener)? | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getOnPartialImageListener()()` Return the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` currently set. |
| [PostProcessor](https://developer.android.com/reference/kotlin/android/graphics/PostProcessor)? | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#getPostProcessor()()` Return the `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor` currently set. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#isDecodeAsAlphaMaskEnabled()()` Return whether to treat single channel input as alpha. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#isMimeTypeSupported(kotlin.String)(mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return if the given MIME type is a supported file format that can be decoded by this class. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#isMutableRequired()()` Return whether the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` will be mutable. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#isUnpremultipliedRequired()()` Return whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` will have unpremultiplied pixels. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setAllocationLimit(kotlin.Long)(limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set a maximum memory limit (bytes) for an image decode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setAllocator(kotlin.Int)(allocator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Choose the backing for the pixel memory. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setCrop(android.graphics.Rect)(subset: https://developer.android.com/reference/kotlin/android/graphics/Rect?)` Crop the output to `subset` of the (possibly) scaled image. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDecodeAsAlphaMaskEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specify whether to potentially treat the output as an alpha mask. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDefaultProcessListener(android.graphics.ImageDecoder.OnHeaderDecodedListener)(listener: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener?)` Set the process-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDefaultThreadListener(android.graphics.ImageDecoder.OnHeaderDecodedListener)(listener: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener?)` Set the thread-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setMemorySizePolicy(kotlin.Int)(policy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify the memory policy for the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setMutableRequired(kotlin.Boolean)(mutable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specify whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` should be mutable. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setOnPartialImageListener(android.graphics.ImageDecoder.OnPartialImageListener)(listener: https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener?)` Set (replace) the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` on this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setPostProcessor(android.graphics.PostProcessor)(postProcessor: https://developer.android.com/reference/kotlin/android/graphics/PostProcessor?)` Modify the image after decoding and scaling. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetColorSpace(android.graphics.ColorSpace)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace!)` Specify the desired `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace` for the output. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSampleSize(kotlin.Int)(sampleSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the target size with a sampleSize. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSize(kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify the size of the output `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setUnpremultipliedRequired(kotlin.Boolean)(unpremultipliedRequired: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specify whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` should have unpremultiplied pixels. |
| --- | --- |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### ALLOCATOR_DEFAULT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOCATOR_DEFAULT: Int
```

Use the default allocation for the pixel memory. Will typically result in a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` allocation, but may be software for small images. In addition, this will switch to software when HARDWARE is incompatible, e.g. `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setMutableRequired(kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDecodeAsAlphaMaskEnabled(kotlin.Boolean)`.

 Value: 0

### ALLOCATOR_HARDWARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOCATOR_HARDWARE: Int
```

Require a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`.

When this is combined with incompatible options, like `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setMutableRequired(kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDecodeAsAlphaMaskEnabled(kotlin.Boolean)`, #decodeDrawable or #decodeBitmap will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

 Value: 3

### ALLOCATOR_SHARED_MEMORY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOCATOR_SHARED_MEMORY: Int
```

Use shared memory for the pixel memory.

Useful for sharing across processes.

 Value: 2

### ALLOCATOR_SOFTWARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOCATOR_SOFTWARE: Int
```

Use a software allocation for the pixel memory.

Useful for drawing to a software `https://developer.android.com/reference/kotlin/android/graphics/Canvas` or for accessing the pixels on the final output.

 Value: 1

### MEMORY_POLICY_DEFAULT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMORY_POLICY_DEFAULT: Int
```

Use the most natural `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` for the internal `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`.

This is the recommended default for most applications and usages. This will use the closest `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` for the encoded source. If the encoded source does not exactly match any `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, the next highest quality `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` will be used avoiding any loss in image quality.

 Value: 1

### MEMORY_POLICY_LOW_RAM

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMORY_POLICY_LOW_RAM: Int
```

Save memory if possible by using a denser `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` at the cost of some image quality.

For example an opaque 8-bit image may be compressed into an `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` configuration, sacrificing image quality to save memory.

 Value: 0

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the try-with-resources statement.

This is an implementation detail of `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#`, and should never be called manually.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### createSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(
    cr: ContentResolver, 
    uri: Uri
): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`.

##### Accepts the following URI schemes:

- content (`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String`)
- android.resource (`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_ANDROID_RESOURCE:kotlin.String`)
- file (`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_FILE:kotlin.String`)

. 
This method is safe to call from any thread.

<br />

| Parameters ||
|---|---|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): to retrieve from. This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): of the image file. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

### createSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(
    assets: AssetManager, 
    fileName: String
): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a file in the "assets" directory. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `assets` | [AssetManager](https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#): This value cannot be `null`. |
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | This value cannot be `null`. |

### createSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(
    res: Resources, 
    resId: Int
): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a resource. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `res` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#): the `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` object containing the image data. This value cannot be `null`. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource ID of the image data. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

### createSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(data: ByteArray): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a byte array.

Note: If this `Source` is passed to #decodeDrawable, and the encoded image is animated, the returned `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable` will continue reading from `data`, so its contents must not be modified, even after the `AnimatedImageDrawable` is returned. `data`'s contents should never be modified during decode.
. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): byte array of compressed image data. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if data is null. |

### createSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(
    data: ByteArray, 
    offset: Int, 
    length: Int
): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a byte array.

Note: If this `Source` is passed to #decodeDrawable, and the encoded image is animated, the returned `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable` will continue reading from `data`, so its contents must not be modified, even after the `AnimatedImageDrawable` is returned. `data`'s contents should never be modified during decode.
. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): byte array of compressed image data. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): offset into data for where the decoder should begin parsing. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of bytes, beginning at offset, to parse. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if offset and length are not within data. |
| `java.lang.NullPointerException` | if data is null. |

### createSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(file: File): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/io/File.html#`.

This method should only be used for files that you have direct access to; if you'd like to work with files hosted outside your app, use an API like `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(java.util.concurrent.Callable)` or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#createSource(android.content.ContentResolver,%20android.net.Uri)`. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

### createSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(buffer: ByteBuffer): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#`

Decoding will start from `https://developer.android.com/reference/kotlin/java/nio/Buffer.html#position()`. The position of `buffer` will not be affected.

Note: If this `Source` is passed to #decodeDrawable, and the encoded image is animated, the returned `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable` will continue reading from the `buffer`, so its contents must not be modified, even after the `AnimatedImageDrawable` is returned. `buffer`'s contents should never be modified during decode.
. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

### createSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSource(callable: Callable<AssetFileDescriptor!>): ImageDecoder.Source
```

Create a new `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` from a `https://developer.android.com/reference/kotlin/java/util/concurrent/Callable.html#` that returns a new `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` for each request. This provides control over how the `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` is created, such as passing options into android.content.ContentResolver#openTypedAssetFileDescriptor, or enabling use of a `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`.

It's important for the given `https://developer.android.com/reference/kotlin/java/util/concurrent/Callable.html#` to return a new, unique `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#` for each invocation, to support reuse of the returned `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source`. 
This method is safe to call from any thread.

| Parameters ||
|---|---|
| `callable` | [Callable](https://developer.android.com/reference/kotlin/java/util/concurrent/Callable.html#)\< [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source` | a new Source object, which can be passed to #decodeDrawable or #decodeBitmap. This value cannot be `null`. |

### decodeBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decodeBitmap(src: ImageDecoder.Source): Bitmap
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` from a `Source`

Since there is no `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`, the default settings will be used. In order to change any settings, call `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)` instead.
. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `src` | [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source): representing the encoded image. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` | Bitmap containing the image. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `src` is not found, is an unsupported format, or cannot be decoded for any reason. |

### decodeBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decodeBitmap(
    src: ImageDecoder.Source, 
    listener: ImageDecoder.OnHeaderDecodedListener
): Bitmap
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` from a `Source`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `src` | [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source): representing the encoded image. This value cannot be `null`. |
| `listener` | [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener): for learning the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` and changing any default settings on the `ImageDecoder`. This will be called on the same thread as `decodeBitmap` before that method returns. This is required in order to change any of the default settings. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` | Bitmap containing the image. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `src` is not found, is an unsupported format, or cannot be decoded for any reason. |

### decodeDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decodeDrawable(src: ImageDecoder.Source): Drawable
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` from a `Source`

Since there is no `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`, the default settings will be used. In order to change any settings, call `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)` instead.
. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `src` | [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source): representing the encoded image. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | Drawable for displaying the image. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `src` is not found, is an unsupported format, or cannot be decoded for any reason. |

### decodeDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun decodeDrawable(
    src: ImageDecoder.Source, 
    listener: ImageDecoder.OnHeaderDecodedListener
): Drawable
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` from a `Source`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `src` | [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source): representing the encoded image. This value cannot be `null`. |
| `listener` | [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener): for learning the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` and changing any default settings on the `ImageDecoder`. This will be called on the same thread as `decodeDrawable` before that method returns. This is required in order to change any of the default settings. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | Drawable for displaying the image. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if `src` is not found, is an unsupported format, or cannot be decoded for any reason. |

### getAllocationLimit

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllocationLimit(): Long
```

Get the maximum memory limit in bytes for image decoding.

### getAllocator

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllocator(): Int
```

Return the allocator for the pixel memory.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SOFTWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SHARED_MEMORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_HARDWARE:kotlin.Int` |

### getCrop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCrop(): Rect?
```

Return the cropping rectangle, if set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect?` | This value may be `null`. |

### getDefaultProcessListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultProcessListener(): ImageDecoder.OnHeaderDecodedListener?
```

Return the process-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener?` | This value may be `null`. |

### getDefaultThreadListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultThreadListener(): ImageDecoder.OnHeaderDecodedListener?
```

Return the thread-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener?` | This value may be `null`. |

### getMemorySizePolicy

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMemorySizePolicy(): Int
```

Retrieve the memory policy for the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_LOW_RAM:kotlin.Int` |

### getOnPartialImageListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOnPartialImageListener(): ImageDecoder.OnPartialImageListener?
```

Return the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` currently set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener?` | This value may be `null`. |

### getPostProcessor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPostProcessor(): PostProcessor?
```

Return the `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor` currently set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor?` | This value may be `null`. |

### isDecodeAsAlphaMaskEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDecodeAsAlphaMaskEnabled(): Boolean
```

Return whether to treat single channel input as alpha.

This returns whether `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDecodeAsAlphaMaskEnabled(kotlin.Boolean)` was set to `true`. It may still return `true` even if the image has more than one channel and therefore will not be treated as an alpha mask.

### isMimeTypeSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isMimeTypeSupported(mimeType: String): Boolean
```

Return if the given MIME type is a supported file format that can be decoded by this class. This can be useful to determine if a file can be decoded directly, or if it needs to be converted into a more general format using an API like `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`.

| Parameters ||
|---|---|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### isMutableRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMutableRequired(): Boolean
```

Return whether the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` will be mutable.

### isUnpremultipliedRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUnpremultipliedRequired(): Boolean
```

Return whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` will have unpremultiplied pixels.

### setAllocationLimit

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAllocationLimit(limit: Long): Unit
```

Set a maximum memory limit (bytes) for an image decode.

Memory usage is tracked during the decoding process, for instance when calling decodeBitmap or decodeDrawable. If an allocation is expected to raise the decode memory usage over the allocation limit, the decode is aborted and an `https://developer.android.com/reference/kotlin/java/io/IOException.html#` is thrown by decode function.

The limit is applied per each image decode. The default limit is 0.5GiB. 0 indicates no limit.

### setAllocator

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAllocator(allocator: Int): Unit
```

Choose the backing for the pixel memory.

This is ignored for animated drawables.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `allocator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Type of allocator to use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SOFTWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_SHARED_MEMORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_HARDWARE:kotlin.Int` |

### setCrop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCrop(subset: Rect?): Unit
```

Crop the output to `subset` of the (possibly) scaled image.

`subset` must be contained within the size set by `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSize(kotlin.Int,%20kotlin.Int)` or the bounds of the image if setTargetSize was not called. Otherwise an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown by #decodeDrawable/#decodeBitmap.

NOT intended as a replacement for `https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#decodeRegion(android.graphics.Rect,%20android.graphics.BitmapFactory.Options)`. This supports all formats, but merely crops the output.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `subset` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?: This value may be `null`. |

### setDecodeAsAlphaMaskEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDecodeAsAlphaMaskEnabled(enabled: Boolean): Unit
```

Specify whether to potentially treat the output as an alpha mask.

If this is set to `true` and the image is encoded in a format with only one channel, treat that channel as alpha. Otherwise this call has no effect.

This is incompatible with `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_HARDWARE:kotlin.Int`. Trying to combine them will result in #decodeDrawable/ #decodeBitmap throwing an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

### setDefaultProcessListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setDefaultProcessListener(listener: ImageDecoder.OnHeaderDecodedListener?): Unit
```

Set the process-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. A subsequent call will overwrite any previous calls.

If there is no thread-level default set on the current thread, this is the first `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` to run during image decoding. At the time of decoding, a listener can also be provided to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)` which is run after the process-level default.

Note: setting a thread-level default via `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDefaultThreadListener(android.graphics.ImageDecoder.OnHeaderDecodedListener)` will cause the process-level default to be skipped on that thread. The listener passed to #decodeDrawable will always run.

| Parameters ||
|---|---|
| `listener` | [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)?: This value may be `null`. |

### setDefaultThreadListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setDefaultThreadListener(listener: ImageDecoder.OnHeaderDecodedListener?): Unit
```

Set the thread-level default `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener`. A subsequent call will overwrite any previous calls.

If set, this is the first `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener` to run during image decoding. At the time of decoding, a listener can also be provided to `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)` which is run after the thread-level default.

Note: setting a thread-level default will cause the process-level default set by `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setDefaultProcessListener(android.graphics.ImageDecoder.OnHeaderDecodedListener)` to be skipped on that thread. The listener passed to #decodeDrawable will always run.

| Parameters ||
|---|---|
| `listener` | [ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener)?: This value may be `null`. |

### setMemorySizePolicy

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMemorySizePolicy(policy: Int): Unit
```

Specify the memory policy for the decoded `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `policy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#MEMORY_POLICY_LOW_RAM:kotlin.Int` |

### setMutableRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMutableRequired(mutable: Boolean): Unit
```

Specify whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` should be mutable.

By default, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` created by #decodeBitmap will be immutable i.e. `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isMutable()` returns `false`. This can be changed with `setMutableRequired(true)`.

Mutable Bitmaps are incompatible with `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#ALLOCATOR_HARDWARE:kotlin.Int`, because `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` Bitmaps cannot be mutable. Attempting to combine them will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

Mutable Bitmaps are also incompatible with #decodeDrawable, which would require retrieving the Bitmap from the returned Drawable in order to modify. Attempting to decode a mutable `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

### setOnPartialImageListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnPartialImageListener(listener: ImageDecoder.OnPartialImageListener?): Unit
```

Set (replace) the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener` on this object.

Will be called if there is an error in the input. Without one, an error will result in an `Exception` being thrown.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `listener` | [ImageDecoder.OnPartialImageListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener)?: This value may be `null`. |

### setPostProcessor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPostProcessor(postProcessor: PostProcessor?): Unit
```

Modify the image after decoding and scaling.

This allows adding effects prior to returning a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. For a `Drawable` or an immutable `Bitmap`, this is the only way to process the image after decoding.

If combined with `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSize(kotlin.Int,%20kotlin.Int)` and/or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setCrop(android.graphics.Rect)`, `https://developer.android.com/reference/kotlin/android/graphics/PostProcessor#onPostProcess(android.graphics.Canvas)` occurs last.

If set on a nine-patch image, the nine-patch data is ignored.

For an animated image, the drawing commands drawn on the `https://developer.android.com/reference/kotlin/android/graphics/Canvas` will be recorded immediately and then applied to each frame.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `postProcessor` | [PostProcessor](https://developer.android.com/reference/kotlin/android/graphics/PostProcessor)?: This value may be `null`. |

### setTargetColorSpace

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTargetColorSpace(colorSpace: ColorSpace!): Unit
```

Specify the desired `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace` for the output.

If non-null, the decoder will try to decode into `colorSpace`. If it is null, which is the default, or the request cannot be met, the decoder will pick either the color space embedded in the image or the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace` best suited for the requested image configuration (for instance `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` for the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` configuration and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` for `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`).

Only `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color spaces are currently supported. An `IllegalArgumentException` will be thrown by #decodeDrawable/ #decodeBitmap when setting a non-RGB color space such as `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the specified color space's transfer function must be an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters`. An `IllegalArgumentException` will be thrown by the decode methods if calling `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb#getTransferParameters()` on the specified color space returns null. Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the color spaces with non ICC parametric curve transfer function are allowed. E.g., `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

### setTargetSampleSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTargetSampleSize(sampleSize: Int): Unit
```

Set the target size with a sampleSize.

By default, the output size will match the size of the encoded image, which can be retrieved from the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` in `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

Requests the decoder to subsample the original image, returning a smaller image to save memory. The `sampleSize` is the number of pixels in either dimension that correspond to a single pixel in the output. For example, `sampleSize == 4` returns an image that is 1/4 the width/height of the original, and 1/16 the number of pixels.

Must be greater than or equal to 1.

This has the same effect as calling `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSize(kotlin.Int,%20kotlin.Int)` with dimensions based on the `sampleSize`. Unlike dividing the original width and height by the `sampleSize` manually, calling this method allows `ImageDecoder` to round in the direction that it can do most efficiently.

Only the last call to this or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSize(kotlin.Int,%20kotlin.Int)` is respected.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `sampleSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): sampling rate of the encoded image. Value is 1 or greater |

### setTargetSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTargetSize(
    width: Int, 
    height: Int
): Unit
```

Specify the size of the output `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`.

By default, the output size will match the size of the encoded image, which can be retrieved from the `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo` in `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

This will sample or scale the output to an arbitrary size that may be smaller or larger than the encoded size.

Only the last call to this or `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setTargetSampleSize(kotlin.Int)` is respected.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): width in pixels of the output, must be greater than 0. The units of this value are pixels. Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): height in pixels of the output, must be greater than 0. The units of this value are pixels. Value is 1 or greater |

### setUnpremultipliedRequired

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setUnpremultipliedRequired(unpremultipliedRequired: Boolean): Unit
```

Specify whether the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` should have unpremultiplied pixels.

By default, ImageDecoder will create a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` with premultiplied pixels, which is required for drawing with the `https://developer.android.com/reference/kotlin/android/view/View.html#` system (i.e. to a `https://developer.android.com/reference/kotlin/android/graphics/Canvas`). Calling this method with a value of `true` will result in #decodeBitmap returning a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` with unpremultiplied pixels. See `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isPremultiplied()`. This is incompatible with #decodeDrawable; attempting to decode an unpremultiplied `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

Like all setters on ImageDecoder, this must be called inside `https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source)`.

## Protected methods

### finalize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
