# android.graphics

# android.graphics

Kotlin| [Java](https://developer.android.com/reference/android/graphics/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener) | Interface for changing the default settings of a decode. |
| --- | --- |
| [OnPartialImageListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener) | Interface for inspecting a [DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException) and potentially preventing it from being thrown. |
| [PostProcessor](https://developer.android.com/reference/kotlin/android/graphics/PostProcessor) | Helper interface for adding custom processing to an image. |
| [OnFrameAvailableListener](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.OnFrameAvailableListener) | Callback interface for being notified that a new stream frame is available. |
| --- | --- |

## Classes

| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) | <br /> |
| --- | --- |
| [BitmapFactory](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory) | Creates Bitmap objects from various sources, including files, streams, and byte-arrays. |
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder) | BitmapRegionDecoder can be used to decode a rectangle region from an image. |
| [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader) | Shader used to draw a bitmap as a texture. |
| --- | --- |
| [BlendModeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode). |
| [BlurMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter) | This takes a mask, and blurs its edge by the specified radius. |
| [Camera](https://developer.android.com/reference/kotlin/android/graphics/Camera) | A camera instance can be used to compute 3D transformations and generate a matrix that can be applied, for instance, on a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas). |
| --- | --- |
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) | The Canvas class holds the "draw" calls. |
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color) | The`Color`class provides methods for creating, converting and manipulating colors. |
| [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter) | A color filter can be used with a [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) to modify the color of each pixel drawn with that paint. |
| --- | --- |
| [ColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrix) | 4x5 matrix for transforming the color and alpha components of a Bitmap. |
| [ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter) | A color filter that transforms colors through a 4x5 color matrix. |
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | A [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) is used to identify a specific organization of colors. |
| --- | --- |
| [ComposePathEffect](https://developer.android.com/reference/kotlin/android/graphics/ComposePathEffect) | <br /> |
| [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode) subclass. |
| [CornerPathEffect](https://developer.android.com/reference/kotlin/android/graphics/CornerPathEffect) | <br /> |
| --- | --- |
| [DashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/DashPathEffect) | <br /> |
| [DiscretePathEffect](https://developer.android.com/reference/kotlin/android/graphics/DiscretePathEffect) | <br /> |
| [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter) | A DrawFilter subclass can be installed in a Canvas. |
| --- | --- |
| [EmbossMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/EmbossMaskFilter) | <br /> |
| [Gainmap](https://developer.android.com/reference/kotlin/android/graphics/Gainmap) | Gainmap represents a mechanism for augmenting an SDR image to produce an HDR one with variable display adjustment capability. |
| [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer) | Creates an instance of a hardware-accelerated renderer. |
| --- | --- |
| [HardwareRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareRenderer) | Creates an instance of a hardware-accelerated renderer. |
| [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder) | A class for converting encoded images (like`PNG`,`JPEG`,`WEBP`,`GIF`, or`HEIF`) into [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) or [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) objects. |
| [ImageFormat](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat) | <br /> |
| --- | --- |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets) | An Insets instance holds four integer offsets which describe changes to the four edges of a Rectangle. |
| [Interpolator](https://developer.android.com/reference/kotlin/android/graphics/Interpolator) | <br /> |
| [LightingColorFilter](https://developer.android.com/reference/kotlin/android/graphics/LightingColorFilter) | A color filter that can be used to simulate simple lighting effects. |
| --- | --- |
| [LinearGradient](https://developer.android.com/reference/kotlin/android/graphics/LinearGradient) | <br /> |
| [MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter) | MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. |
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix) | The Matrix class holds a 3x3 matrix for transforming coordinates. |
| --- | --- |
| [Matrix44](https://developer.android.com/reference/kotlin/android/graphics/Matrix44) | The Matrix44 class holds a 4x4 matrix for transforming coordinates. |
| [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) | Class representing a mesh object. |
| [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification) | Class responsible for holding specifications for [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) creations. |
| --- | --- |
| [Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie) | <br /> |
| [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch) | The NinePatch class permits drawing a bitmap in nine or more sections. |
| [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline) | Defines a simple shape, used for bounding graphical regions. |
| --- | --- |
| [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) | The Paint class holds the style and color information about how to draw geometries, text and bitmaps. |
| [PaintFlagsDrawFilter](https://developer.android.com/reference/kotlin/android/graphics/PaintFlagsDrawFilter) | <br /> |
| [ParcelableColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ParcelableColorSpace) | A [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) wrapper for a [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace). |
| --- | --- |
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path) | The Path class encapsulates compound (multiple contour) geometric paths consisting of straight line segments, quadratic curves, and cubic curves. |
| [PathDashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect) | <br /> |
| [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) | PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn. |
| --- | --- |
| [PathIterator](https://developer.android.com/reference/kotlin/android/graphics/PathIterator) | `PathIterator`can be used to query a given [Path](https://developer.android.com/reference/kotlin/android/graphics/Path) object, to discover its operations and point values. |
| [PathMeasure](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure) | <br /> |
| [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture) | A Picture records drawing calls (via the canvas returned by beginRecording) and can then play them back into Canvas (via [Picture.draw(Canvas)](https://developer.android.com/reference/kotlin/android/graphics/Picture#draw(android.graphics.Canvas))or [Canvas.drawPicture(Picture)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture))). |
| --- | --- |
| [PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat) | <br /> |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point) | Point holds two integer coordinates |
| [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF) | PointF holds two float coordinates |
| --- | --- |
| [PorterDuff](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff) | This class contains the list of alpha compositing and blending modes that can be passed to [PorterDuffXfermode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode), a specialized implementation of [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)'s [transfer mode](https://developer.android.com/reference/kotlin/android/graphics/Paint#setXfermode(android.graphics.Xfermode)). |
| [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff). |
| [PorterDuffXfermode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode) | Specialized implementation of [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)'s [transfer mode](https://developer.android.com/reference/kotlin/android/graphics/Paint#setXfermode(android.graphics.Xfermode)). |
| --- | --- |
| [RadialGradient](https://developer.android.com/reference/kotlin/android/graphics/RadialGradient) | <br /> |
| [RecordingCanvas](https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas) | A Canvas implementation that records view system drawing operations for deferred rendering. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect) | Rect holds four integer coordinates for a rectangle. |
| --- | --- |
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF) | RectF holds four float coordinates for a rectangle. |
| [Region](https://developer.android.com/reference/kotlin/android/graphics/Region) | <br /> |
| [RegionIterator](https://developer.android.com/reference/kotlin/android/graphics/RegionIterator) | <br /> |
| --- | --- |
| [RenderEffect](https://developer.android.com/reference/kotlin/android/graphics/RenderEffect) | Intermediate rendering step used to render drawing commands with a corresponding visual effect. |
| [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) | RenderNode is used to build hardware accelerated rendering hierarchies. |
| [RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter) | A [RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| --- | --- |
| [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader) | A [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. |
| [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode) | A [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. |
| [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) | Shader is the base class for objects that return horizontal spans of colors during drawing. |
| --- | --- |
| [SumPathEffect](https://developer.android.com/reference/kotlin/android/graphics/SumPathEffect) | <br /> |
| [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture) | Captures frames from an image stream as an OpenGL ES texture. |
| [SweepGradient](https://developer.android.com/reference/kotlin/android/graphics/SweepGradient) | <br /> |
| --- | --- |
| [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface) | The Typeface class specifies the typeface and intrinsic style of a font. |
| [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode) | Xfermode is the base class for objects that are called to implement custom "transfer-modes" in the drawing pipeline. |
| [YuvImage](https://developer.android.com/reference/kotlin/android/graphics/YuvImage) | YuvImage contains YUV data and provides a method that compresses a region of the YUV data to a Jpeg. |
| --- | --- |

## Enums

| [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode) | <br /> |
| --- | --- |
