# android.graphics

# android.graphics

Kotlin| [Java](../android/graphics/_package.md)
| --- | --- |

## Interfaces

| [OnHeaderDecodedListener](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md) | Interface for changing the default settings of a decode. |
| --- | --- |
| [OnPartialImageListener](../android/graphics/ImageDecoder.OnPartialImageListener.md) | Interface for inspecting a [DecodeException](../android/graphics/ImageDecoder.DecodeException.md) and potentially preventing it from being thrown. |
| [PostProcessor](../android/graphics/PostProcessor.md) | Helper interface for adding custom processing to an image. |
| [OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md) | Callback interface for being notified that a new stream frame is available. |
| --- | --- |

## Classes

| [Bitmap](../android/graphics/Bitmap.md) | <br /> |
| --- | --- |
| [BitmapFactory](../android/graphics/BitmapFactory.md) | Creates Bitmap objects from various sources, including files, streams, and byte-arrays. |
| [BitmapRegionDecoder](../android/graphics/BitmapRegionDecoder.md) | BitmapRegionDecoder can be used to decode a rectangle region from an image. |
| [BitmapShader](../android/graphics/BitmapShader.md) | Shader used to draw a bitmap as a texture. |
| --- | --- |
| [BlendModeColorFilter](../android/graphics/BlendModeColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](../android/graphics/BlendMode.md). |
| [BlurMaskFilter](../android/graphics/BlurMaskFilter.md) | This takes a mask, and blurs its edge by the specified radius. |
| [Camera](../android/graphics/Camera.md) | A camera instance can be used to compute 3D transformations and generate a matrix that can be applied, for instance, on a [Canvas](../android/graphics/Canvas.md). |
| --- | --- |
| [Canvas](../android/graphics/Canvas.md) | The Canvas class holds the "draw" calls. |
| [Color](../android/graphics/Color.md) | The`Color`class provides methods for creating, converting and manipulating colors. |
| [ColorFilter](../android/graphics/ColorFilter.md) | A color filter can be used with a [Paint](../android/graphics/Paint.md) to modify the color of each pixel drawn with that paint. |
| --- | --- |
| [ColorMatrix](../android/graphics/ColorMatrix.md) | 4x5 matrix for transforming the color and alpha components of a Bitmap. |
| [ColorMatrixColorFilter](../android/graphics/ColorMatrixColorFilter.md) | A color filter that transforms colors through a 4x5 color matrix. |
| [ColorSpace](../android/graphics/ColorSpace.md) | A [ColorSpace](../android/graphics/ColorSpace.md) is used to identify a specific organization of colors. |
| --- | --- |
| [ComposePathEffect](../android/graphics/ComposePathEffect.md) | <br /> |
| [ComposeShader](../android/graphics/ComposeShader.md) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](../android/graphics/Xfermode.md) subclass. |
| [CornerPathEffect](../android/graphics/CornerPathEffect.md) | <br /> |
| --- | --- |
| [DashPathEffect](../android/graphics/DashPathEffect.md) | <br /> |
| [DiscretePathEffect](../android/graphics/DiscretePathEffect.md) | <br /> |
| [DrawFilter](../android/graphics/DrawFilter.md) | A DrawFilter subclass can be installed in a Canvas. |
| --- | --- |
| [EmbossMaskFilter](../android/graphics/EmbossMaskFilter.md) | <br /> |
| [Gainmap](../android/graphics/Gainmap.md) | Gainmap represents a mechanism for augmenting an SDR image to produce an HDR one with variable display adjustment capability. |
| [HardwareBufferRenderer](../android/graphics/HardwareBufferRenderer.md) | Creates an instance of a hardware-accelerated renderer. |
| --- | --- |
| [HardwareRenderer](../android/graphics/HardwareRenderer.md) | Creates an instance of a hardware-accelerated renderer. |
| [ImageDecoder](../android/graphics/ImageDecoder.md) | A class for converting encoded images (like`PNG`,`JPEG`,`WEBP`,`GIF`, or`HEIF`) into [Drawable](../android/graphics/drawable/Drawable.md) or [Bitmap](../android/graphics/Bitmap.md) objects. |
| [ImageFormat](../android/graphics/ImageFormat.md) | <br /> |
| --- | --- |
| [Insets](../android/graphics/Insets.md) | An Insets instance holds four integer offsets which describe changes to the four edges of a Rectangle. |
| [Interpolator](../android/graphics/Interpolator.md) | <br /> |
| [LightingColorFilter](../android/graphics/LightingColorFilter.md) | A color filter that can be used to simulate simple lighting effects. |
| --- | --- |
| [LinearGradient](../android/graphics/LinearGradient.md) | <br /> |
| [MaskFilter](../android/graphics/MaskFilter.md) | MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. |
| [Matrix](../android/graphics/Matrix.md) | The Matrix class holds a 3x3 matrix for transforming coordinates. |
| --- | --- |
| [Matrix44](../android/graphics/Matrix44.md) | The Matrix44 class holds a 4x4 matrix for transforming coordinates. |
| [Mesh](../android/graphics/Mesh.md) | Class representing a mesh object. |
| [MeshSpecification](../android/graphics/MeshSpecification.md) | Class responsible for holding specifications for [Mesh](../android/graphics/Mesh.md) creations. |
| --- | --- |
| [Movie](../android/graphics/Movie.md) | <br /> |
| [NinePatch](../android/graphics/NinePatch.md) | The NinePatch class permits drawing a bitmap in nine or more sections. |
| [Outline](../android/graphics/Outline.md) | Defines a simple shape, used for bounding graphical regions. |
| --- | --- |
| [Paint](../android/graphics/Paint.md) | The Paint class holds the style and color information about how to draw geometries, text and bitmaps. |
| [PaintFlagsDrawFilter](../android/graphics/PaintFlagsDrawFilter.md) | <br /> |
| [ParcelableColorSpace](../android/graphics/ParcelableColorSpace.md) | A [Parcelable](../android/os/Parcelable.md) wrapper for a [ColorSpace](../android/graphics/ColorSpace.md). |
| --- | --- |
| [Path](../android/graphics/Path.md) | The Path class encapsulates compound (multiple contour) geometric paths consisting of straight line segments, quadratic curves, and cubic curves. |
| [PathDashPathEffect](../android/graphics/PathDashPathEffect.md) | <br /> |
| [PathEffect](../android/graphics/PathEffect.md) | PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn. |
| --- | --- |
| [PathIterator](../android/graphics/PathIterator.md) | `PathIterator`can be used to query a given [Path](../android/graphics/Path.md) object, to discover its operations and point values. |
| [PathMeasure](../android/graphics/PathMeasure.md) | <br /> |
| [Picture](../android/graphics/Picture.md) | A Picture records drawing calls (via the canvas returned by beginRecording) and can then play them back into Canvas (via [Picture.draw(Canvas)](../android/graphics/Picture.md))or [Canvas.drawPicture(Picture)](../android/graphics/Canvas.md))). |
| --- | --- |
| [PixelFormat](../android/graphics/PixelFormat.md) | <br /> |
| [Point](../android/graphics/Point.md) | Point holds two integer coordinates |
| [PointF](../android/graphics/PointF.md) | PointF holds two float coordinates |
| --- | --- |
| [PorterDuff](../android/graphics/PorterDuff.md) | This class contains the list of alpha compositing and blending modes that can be passed to [PorterDuffXfermode](../android/graphics/PorterDuffXfermode.md), a specialized implementation of [Paint](../android/graphics/Paint.md)'s [transfer mode](../android/graphics/Paint.md)). |
| [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](../android/graphics/PorterDuff.md). |
| [PorterDuffXfermode](../android/graphics/PorterDuffXfermode.md) | Specialized implementation of [Paint](../android/graphics/Paint.md)'s [transfer mode](../android/graphics/Paint.md)). |
| --- | --- |
| [RadialGradient](../android/graphics/RadialGradient.md) | <br /> |
| [RecordingCanvas](../android/graphics/RecordingCanvas.md) | A Canvas implementation that records view system drawing operations for deferred rendering. |
| [Rect](../android/graphics/Rect.md) | Rect holds four integer coordinates for a rectangle. |
| --- | --- |
| [RectF](../android/graphics/RectF.md) | RectF holds four float coordinates for a rectangle. |
| [Region](../android/graphics/Region.md) | <br /> |
| [RegionIterator](../android/graphics/RegionIterator.md) | <br /> |
| --- | --- |
| [RenderEffect](../android/graphics/RenderEffect.md) | Intermediate rendering step used to render drawing commands with a corresponding visual effect. |
| [RenderNode](../android/graphics/RenderNode.md) | RenderNode is used to build hardware accelerated rendering hierarchies. |
| [RuntimeColorFilter](../android/graphics/RuntimeColorFilter.md) | A [RuntimeColorFilter](../android/graphics/RuntimeColorFilter.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| --- | --- |
| [RuntimeShader](../android/graphics/RuntimeShader.md) | A [RuntimeShader](../android/graphics/RuntimeShader.md) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. |
| [RuntimeXfermode](../android/graphics/RuntimeXfermode.md) | A [RuntimeXfermode](../android/graphics/RuntimeXfermode.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| [Shader](../android/graphics/Shader.md) | Shader is the base class for objects that return horizontal spans of colors during drawing. |
| --- | --- |
| [SumPathEffect](../android/graphics/SumPathEffect.md) | <br /> |
| [SurfaceTexture](../android/graphics/SurfaceTexture.md) | Captures frames from an image stream as an OpenGL ES texture. |
| [SweepGradient](../android/graphics/SweepGradient.md) | <br /> |
| --- | --- |
| [Typeface](../android/graphics/Typeface.md) | The Typeface class specifies the typeface and intrinsic style of a font. |
| [Xfermode](../android/graphics/Xfermode.md) | Xfermode is the base class for objects that are called to implement custom "transfer-modes" in the drawing pipeline. |
| [YuvImage](../android/graphics/YuvImage.md) | YuvImage contains YUV data and provides a method that compresses a region of the YUV data to a Jpeg. |
| --- | --- |

## Enums

| [BlendMode](../android/graphics/BlendMode.md) | <br /> |
| --- | --- |
