# android.renderscript

# android.renderscript

Kotlin| [Java](../android/renderscript/_package.md)
| --- | --- |

## Interfaces

| [OnBufferAvailableListener](../android/renderscript/Allocation.OnBufferAvailableListener.md) | Interface to handle notification when new buffers are available via [USAGE_IO_INPUT](../android/renderscript/Allocation.md). |
| --- | --- |

## Classes

| [Allocation](../android/renderscript/Allocation.md) | This class provides the primary method through which data is passed to and from RenderScript kernels. |
| --- | --- |
| [AllocationAdapter](../android/renderscript/AllocationAdapter.md) | Only intended for use by generated reflected code. |
| [BaseObj](../android/renderscript/BaseObj.md) | BaseObj is the base class for all RenderScript objects owned by a RS context. |
| [Byte2](../android/renderscript/Byte2.md) | Class for exposing the native RenderScript byte2 type back to the Android system. |
| --- | --- |
| [Byte3](../android/renderscript/Byte3.md) | Class for exposing the native RenderScript byte3 type back to the Android system. |
| [Byte4](../android/renderscript/Byte4.md) | Class for exposing the native RenderScript byte4 type back to the Android system. |
| [Double2](../android/renderscript/Double2.md) | Vector version of the basic double type. |
| --- | --- |
| [Double3](../android/renderscript/Double3.md) | Vector version of the basic double type. |
| [Double4](../android/renderscript/Double4.md) | Vector version of the basic double type. |
| [Element](../android/renderscript/Element.md) | An Element represents one item within an . |
| --- | --- |
| [FieldPacker](../android/renderscript/FieldPacker.md) | Utility class for packing arguments and structures from Android system objects to RenderScript objects. |
| [Float2](../android/renderscript/Float2.md) | Vector version of the basic float type. |
| [Float3](../android/renderscript/Float3.md) | Vector version of the basic float type. |
| --- | --- |
| [Float4](../android/renderscript/Float4.md) | Vector version of the basic float type. |
| [Int2](../android/renderscript/Int2.md) | Vector version of the basic int type. |
| [Int3](../android/renderscript/Int3.md) | Vector version of the basic int type. |
| --- | --- |
| [Int4](../android/renderscript/Int4.md) | Vector version of the basic int type. |
| [Long2](../android/renderscript/Long2.md) | Vector version of the basic long type. |
| [Long3](../android/renderscript/Long3.md) | Vector version of the basic long type. |
| --- | --- |
| [Long4](../android/renderscript/Long4.md) | Vector version of the basic long type. |
| [Matrix2f](../android/renderscript/Matrix2f.md) | Class for exposing the native RenderScript rs_matrix2x2 type back to the Android system. |
| [Matrix3f](../android/renderscript/Matrix3f.md) | Class for exposing the native RenderScript rs_matrix3x3 type back to the Android system. |
| --- | --- |
| [Matrix4f](../android/renderscript/Matrix4f.md) | Class for exposing the native RenderScript rs_matrix4x4 type back to the Android system. |
| [RenderScript](../android/renderscript/RenderScript.md) | This class provides access to a RenderScript context, which controls RenderScript initialization, resource management, and teardown. |
| [Sampler](../android/renderscript/Sampler.md) | Sampler object that defines how Allocations can be read as textures within a kernel. |
| --- | --- |
| [Script](../android/renderscript/Script.md) | The parent class for all executable scripts. |
| [ScriptC](../android/renderscript/ScriptC.md) | The superclass for all user-defined scripts. |
| [ScriptGroup](../android/renderscript/ScriptGroup.md) | A group of kernels that are executed together with one execution call as if they were a single kernel |
| --- | --- |
| [ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) | Base class for all Intrinsic scripts. |
| [ScriptIntrinsic3DLUT](../android/renderscript/ScriptIntrinsic3DLUT.md) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. |
| [ScriptIntrinsicBLAS](../android/renderscript/ScriptIntrinsicBLAS.md) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. |
| --- | --- |
| [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md) | Intrinsic kernels for blending two [android.renderscript.Allocation](../android/renderscript/Allocation.md) objects. |
| [ScriptIntrinsicBlur](../android/renderscript/ScriptIntrinsicBlur.md) | Intrinsic Gausian blur filter. |
| [ScriptIntrinsicColorMatrix](../android/renderscript/ScriptIntrinsicColorMatrix.md) | Intrinsic for applying a color matrix to allocations. |
| --- | --- |
| [ScriptIntrinsicConvolve3x3](../android/renderscript/ScriptIntrinsicConvolve3x3.md) | Intrinsic for applying a 3x3 convolve to an allocation. |
| [ScriptIntrinsicConvolve5x5](../android/renderscript/ScriptIntrinsicConvolve5x5.md) | Intrinsic for applying a 5x5 convolve to an allocation. |
| [ScriptIntrinsicHistogram](../android/renderscript/ScriptIntrinsicHistogram.md) | Intrinsic Histogram filter. |
| --- | --- |
| [ScriptIntrinsicLUT](../android/renderscript/ScriptIntrinsicLUT.md) | Intrinsic for applying a per-channel lookup table. |
| [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md) | Intrinsic for performing a resize of a 2D allocation. |
| [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md) | Intrinsic for converting an Android YUV buffer to RGB. |
| --- | --- |
| [Short2](../android/renderscript/Short2.md) | Class for exposing the native RenderScript Short2 type back to the Android system. |
| [Short3](../android/renderscript/Short3.md) | Vector version of the basic short type. |
| [Short4](../android/renderscript/Short4.md) | Vector version of the basic short type. |
| --- | --- |
| [Type](../android/renderscript/Type.md) | A Type describes the [android.renderscript.Element](../android/renderscript/Element.md) and dimensions used for an or a parallel operation. |

## Exceptions

| [RSDriverException](../android/renderscript/RSDriverException.md) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
| [RSIllegalArgumentException](../android/renderscript/RSIllegalArgumentException.md) | Base class for all exceptions thrown by the Android RenderScript |
| [RSInvalidStateException](../android/renderscript/RSInvalidStateException.md) | Base class for all exceptions thrown by the Android RenderScript |
| [RSRuntimeException](../android/renderscript/RSRuntimeException.md) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
