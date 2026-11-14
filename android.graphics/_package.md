# android.graphics

# android.graphics

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnHeaderDecodedListener](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md) | Interface for changing the default settings of a decode. |
| --- | --- |
| [OnPartialImageListener](../android/graphics/ImageDecoder.OnPartialImageListener.md) | Interface for inspecting a [DecodeException](../android/graphics/ImageDecoder.DecodeException.md) and potentially preventing it from being thrown. |
| [PostProcessor](PostProcessor.md) | Helper interface for adding custom processing to an image. |
| [OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md) | Callback interface for being notified that a new stream frame is available. |
| --- | --- |

## Classes

| [Bitmap](Bitmap.md) | <br /> |
| --- | --- |
| [BitmapFactory](BitmapFactory.md) | Creates Bitmap objects from various sources, including files, streams, and byte-arrays. |
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | BitmapRegionDecoder can be used to decode a rectangle region from an image. |
| [BitmapShader](BitmapShader.md) | Shader used to draw a bitmap as a texture. |
| --- | --- |
| [BlendModeColorFilter](BlendModeColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](BlendMode.md). |
| [BlurMaskFilter](BlurMaskFilter.md) | This takes a mask, and blurs its edge by the specified radius. |
| [Camera](Camera.md) | A camera instance can be used to compute 3D transformations and generate a matrix that can be applied, for instance, on a [Canvas](Canvas.md). |
| --- | --- |
| [Canvas](Canvas.md) | The Canvas class holds the "draw" calls. |
| [Color](Color.md) | The`Color`class provides methods for creating, converting and manipulating colors. |
| [ColorFilter](ColorFilter.md) | A color filter can be used with a [Paint](Paint.md) to modify the color of each pixel drawn with that paint. |
| --- | --- |
| [ColorMatrix](ColorMatrix.md) | 4x5 matrix for transforming the color and alpha components of a Bitmap. |
| [ColorMatrixColorFilter](ColorMatrixColorFilter.md) | A color filter that transforms colors through a 4x5 color matrix. |
| [ColorSpace](ColorSpace.md) | A [ColorSpace](ColorSpace.md) is used to identify a specific organization of colors. |
| --- | --- |
| [ComposePathEffect](ComposePathEffect.md) | <br /> |
| [ComposeShader](ComposeShader.md) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](Xfermode.md) subclass. |
| [CornerPathEffect](CornerPathEffect.md) | <br /> |
| --- | --- |
| [DashPathEffect](DashPathEffect.md) | <br /> |
| [DiscretePathEffect](DiscretePathEffect.md) | <br /> |
| [DrawFilter](DrawFilter.md) | A DrawFilter subclass can be installed in a Canvas. |
| --- | --- |
| [EmbossMaskFilter](EmbossMaskFilter.md) | <br /> |
| [Gainmap](Gainmap.md) | Gainmap represents a mechanism for augmenting an SDR image to produce an HDR one with variable display adjustment capability. |
| [HardwareBufferRenderer](HardwareBufferRenderer.md) | Creates an instance of a hardware-accelerated renderer. |
| --- | --- |
| [HardwareRenderer](HardwareRenderer.md) | Creates an instance of a hardware-accelerated renderer. |
| [ImageDecoder](ImageDecoder.md) | A class for converting encoded images (like`PNG`,`JPEG`,`WEBP`,`GIF`, or`HEIF`) into [Drawable](../android.graphics.drawable/Drawable.md) or [Bitmap](Bitmap.md) objects. |
| [ImageFormat](ImageFormat.md) | <br /> |
| --- | --- |
| [Insets](Insets.md) | An Insets instance holds four integer offsets which describe changes to the four edges of a Rectangle. |
| [Interpolator](Interpolator.md) | <br /> |
| [LightingColorFilter](LightingColorFilter.md) | A color filter that can be used to simulate simple lighting effects. |
| --- | --- |
| [LinearGradient](LinearGradient.md) | <br /> |
| [MaskFilter](MaskFilter.md) | MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. |
| [Matrix](Matrix.md) | The Matrix class holds a 3x3 matrix for transforming coordinates. |
| --- | --- |
| [Matrix44](Matrix44.md) | The Matrix44 class holds a 4x4 matrix for transforming coordinates. |
| [Mesh](Mesh.md) | Class representing a mesh object. |
| [MeshSpecification](MeshSpecification.md) | Class responsible for holding specifications for [Mesh](Mesh.md) creations. |
| --- | --- |
| [Movie](Movie.md) | <br /> |
| [NinePatch](NinePatch.md) | The NinePatch class permits drawing a bitmap in nine or more sections. |
| [Outline](Outline.md) | Defines a simple shape, used for bounding graphical regions. |
| --- | --- |
| [Paint](Paint.md) | The Paint class holds the style and color information about how to draw geometries, text and bitmaps. |
| [PaintFlagsDrawFilter](PaintFlagsDrawFilter.md) | <br /> |
| [ParcelableColorSpace](ParcelableColorSpace.md) | A [Parcelable](../android.os/Parcelable.md) wrapper for a [ColorSpace](ColorSpace.md). |
| --- | --- |
| [Path](Path.md) | The Path class encapsulates compound (multiple contour) geometric paths consisting of straight line segments, quadratic curves, and cubic curves. |
| [PathDashPathEffect](PathDashPathEffect.md) | <br /> |
| [PathEffect](PathEffect.md) | PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn. |
| --- | --- |
| [PathIterator](PathIterator.md) | `PathIterator`can be used to query a given [Path](Path.md) object, to discover its operations and point values. |
| [PathMeasure](PathMeasure.md) | <br /> |
| [Picture](Picture.md) | A Picture records drawing calls (via the canvas returned by beginRecording) and can then play them back into Canvas (via [Picture.draw(Canvas)](Picture.md))or [Canvas.drawPicture(Picture)](Canvas.md))). |
| --- | --- |
| [PixelFormat](PixelFormat.md) | <br /> |
| [Point](Point.md) | Point holds two integer coordinates |
| [PointF](PointF.md) | PointF holds two float coordinates |
| --- | --- |
| [PorterDuff](PorterDuff.md) | This class contains the list of alpha compositing and blending modes that can be passed to [PorterDuffXfermode](PorterDuffXfermode.md), a specialized implementation of [Paint](Paint.md)'s [transfer mode](Paint.md)). |
| [PorterDuffColorFilter](PorterDuffColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](PorterDuff.md). |
| [PorterDuffXfermode](PorterDuffXfermode.md) | Specialized implementation of [Paint](Paint.md)'s [transfer mode](Paint.md)). |
| --- | --- |
| [RadialGradient](RadialGradient.md) | <br /> |
| [RecordingCanvas](RecordingCanvas.md) | A Canvas implementation that records view system drawing operations for deferred rendering. |
| [Rect](Rect.md) | Rect holds four integer coordinates for a rectangle. |
| --- | --- |
| [RectF](RectF.md) | RectF holds four float coordinates for a rectangle. |
| [Region](Region.md) | <br /> |
| [RegionIterator](RegionIterator.md) | <br /> |
| --- | --- |
| [RenderEffect](RenderEffect.md) | Intermediate rendering step used to render drawing commands with a corresponding visual effect. |
| [RenderNode](RenderNode.md) | RenderNode is used to build hardware accelerated rendering hierarchies. |
| [RuntimeColorFilter](RuntimeColorFilter.md) | A [RuntimeColorFilter](RuntimeColorFilter.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| --- | --- |
| [RuntimeShader](RuntimeShader.md) | A [RuntimeShader](RuntimeShader.md) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. |
| [RuntimeXfermode](RuntimeXfermode.md) | A [RuntimeXfermode](RuntimeXfermode.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| [Shader](Shader.md) | Shader is the base class for objects that return horizontal spans of colors during drawing. |
| --- | --- |
| [SumPathEffect](SumPathEffect.md) | <br /> |
| [SurfaceTexture](SurfaceTexture.md) | Captures frames from an image stream as an OpenGL ES texture. |
| [SweepGradient](SweepGradient.md) | <br /> |
| --- | --- |
| [Typeface](Typeface.md) | The Typeface class specifies the typeface and intrinsic style of a font. |
| [Xfermode](Xfermode.md) | Xfermode is the base class for objects that are called to implement custom "transfer-modes" in the drawing pipeline. |
| [YuvImage](YuvImage.md) | YuvImage contains YUV data and provides a method that compresses a region of the YUV data to a Jpeg. |
| --- | --- |

## Enums

| [BlendMode](BlendMode.md) | <br /> |
| --- | --- |
