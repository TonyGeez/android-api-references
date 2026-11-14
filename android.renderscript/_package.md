# android.renderscript

# android.renderscript

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnBufferAvailableListener](https://developer.android.com/reference/kotlin/android/renderscript/Allocation.OnBufferAvailableListener) | Interface to handle notification when new buffers are available via [USAGE_IO_INPUT](https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int). |
| --- | --- |

## Classes

| [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) | This class provides the primary method through which data is passed to and from RenderScript kernels. |
| --- | --- |
| [AllocationAdapter](https://developer.android.com/reference/kotlin/android/renderscript/AllocationAdapter) | Only intended for use by generated reflected code. |
| [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) | BaseObj is the base class for all RenderScript objects owned by a RS context. |
| [Byte2](https://developer.android.com/reference/kotlin/android/renderscript/Byte2) | Class for exposing the native RenderScript byte2 type back to the Android system. |
| --- | --- |
| [Byte3](https://developer.android.com/reference/kotlin/android/renderscript/Byte3) | Class for exposing the native RenderScript byte3 type back to the Android system. |
| [Byte4](https://developer.android.com/reference/kotlin/android/renderscript/Byte4) | Class for exposing the native RenderScript byte4 type back to the Android system. |
| [Double2](https://developer.android.com/reference/kotlin/android/renderscript/Double2) | Vector version of the basic double type. |
| --- | --- |
| [Double3](https://developer.android.com/reference/kotlin/android/renderscript/Double3) | Vector version of the basic double type. |
| [Double4](https://developer.android.com/reference/kotlin/android/renderscript/Double4) | Vector version of the basic double type. |
| [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) | An Element represents one item within an . |
| --- | --- |
| [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker) | Utility class for packing arguments and structures from Android system objects to RenderScript objects. |
| [Float2](https://developer.android.com/reference/kotlin/android/renderscript/Float2) | Vector version of the basic float type. |
| [Float3](https://developer.android.com/reference/kotlin/android/renderscript/Float3) | Vector version of the basic float type. |
| --- | --- |
| [Float4](https://developer.android.com/reference/kotlin/android/renderscript/Float4) | Vector version of the basic float type. |
| [Int2](https://developer.android.com/reference/kotlin/android/renderscript/Int2) | Vector version of the basic int type. |
| [Int3](https://developer.android.com/reference/kotlin/android/renderscript/Int3) | Vector version of the basic int type. |
| --- | --- |
| [Int4](https://developer.android.com/reference/kotlin/android/renderscript/Int4) | Vector version of the basic int type. |
| [Long2](https://developer.android.com/reference/kotlin/android/renderscript/Long2) | Vector version of the basic long type. |
| [Long3](https://developer.android.com/reference/kotlin/android/renderscript/Long3) | Vector version of the basic long type. |
| --- | --- |
| [Long4](https://developer.android.com/reference/kotlin/android/renderscript/Long4) | Vector version of the basic long type. |
| [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f) | Class for exposing the native RenderScript rs_matrix2x2 type back to the Android system. |
| [Matrix3f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix3f) | Class for exposing the native RenderScript rs_matrix3x3 type back to the Android system. |
| --- | --- |
| [Matrix4f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix4f) | Class for exposing the native RenderScript rs_matrix4x4 type back to the Android system. |
| [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript) | This class provides access to a RenderScript context, which controls RenderScript initialization, resource management, and teardown. |
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler) | Sampler object that defines how Allocations can be read as textures within a kernel. |
| --- | --- |
| [Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) | The parent class for all executable scripts. |
| [ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC) | The superclass for all user-defined scripts. |
| [ScriptGroup](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup) | A group of kernels that are executed together with one execution call as if they were a single kernel |
| --- | --- |
| [ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) | Base class for all Intrinsic scripts. |
| [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. |
| [ScriptIntrinsicBLAS](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. |
| --- | --- |
| [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend) | Intrinsic kernels for blending two [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) objects. |
| [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur) | Intrinsic Gausian blur filter. |
| [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix) | Intrinsic for applying a color matrix to allocations. |
| --- | --- |
| [ScriptIntrinsicConvolve3x3](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve3x3) | Intrinsic for applying a 3x3 convolve to an allocation. |
| [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5) | Intrinsic for applying a 5x5 convolve to an allocation. |
| [ScriptIntrinsicHistogram](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicHistogram) | Intrinsic Histogram filter. |
| --- | --- |
| [ScriptIntrinsicLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicLUT) | Intrinsic for applying a per-channel lookup table. |
| [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize) | Intrinsic for performing a resize of a 2D allocation. |
| [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB) | Intrinsic for converting an Android YUV buffer to RGB. |
| --- | --- |
| [Short2](https://developer.android.com/reference/kotlin/android/renderscript/Short2) | Class for exposing the native RenderScript Short2 type back to the Android system. |
| [Short3](https://developer.android.com/reference/kotlin/android/renderscript/Short3) | Vector version of the basic short type. |
| [Short4](https://developer.android.com/reference/kotlin/android/renderscript/Short4) | Vector version of the basic short type. |
| --- | --- |
| [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type) | A Type describes the [android.renderscript.Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) and dimensions used for an or a parallel operation. |

## Exceptions

| [RSDriverException](https://developer.android.com/reference/kotlin/android/renderscript/RSDriverException) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
| [RSIllegalArgumentException](https://developer.android.com/reference/kotlin/android/renderscript/RSIllegalArgumentException) | Base class for all exceptions thrown by the Android RenderScript |
| [RSInvalidStateException](https://developer.android.com/reference/kotlin/android/renderscript/RSInvalidStateException) | Base class for all exceptions thrown by the Android RenderScript |
| [RSRuntimeException](https://developer.android.com/reference/kotlin/android/renderscript/RSRuntimeException) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
