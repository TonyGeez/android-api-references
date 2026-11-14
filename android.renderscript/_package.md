# android.renderscript

# android.renderscript

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnBufferAvailableListener](../android/renderscript/Allocation.OnBufferAvailableListener.md) | Interface to handle notification when new buffers are available via [USAGE_IO_INPUT](Allocation.md). |
| --- | --- |

## Classes

| [Allocation](Allocation.md) | This class provides the primary method through which data is passed to and from RenderScript kernels. |
| --- | --- |
| [AllocationAdapter](AllocationAdapter.md) | Only intended for use by generated reflected code. |
| [BaseObj](BaseObj.md) | BaseObj is the base class for all RenderScript objects owned by a RS context. |
| [Byte2](Byte2.md) | Class for exposing the native RenderScript byte2 type back to the Android system. |
| --- | --- |
| [Byte3](Byte3.md) | Class for exposing the native RenderScript byte3 type back to the Android system. |
| [Byte4](Byte4.md) | Class for exposing the native RenderScript byte4 type back to the Android system. |
| [Double2](Double2.md) | Vector version of the basic double type. |
| --- | --- |
| [Double3](Double3.md) | Vector version of the basic double type. |
| [Double4](Double4.md) | Vector version of the basic double type. |
| [Element](Element.md) | An Element represents one item within an . |
| --- | --- |
| [FieldPacker](FieldPacker.md) | Utility class for packing arguments and structures from Android system objects to RenderScript objects. |
| [Float2](Float2.md) | Vector version of the basic float type. |
| [Float3](Float3.md) | Vector version of the basic float type. |
| --- | --- |
| [Float4](Float4.md) | Vector version of the basic float type. |
| [Int2](Int2.md) | Vector version of the basic int type. |
| [Int3](Int3.md) | Vector version of the basic int type. |
| --- | --- |
| [Int4](Int4.md) | Vector version of the basic int type. |
| [Long2](Long2.md) | Vector version of the basic long type. |
| [Long3](Long3.md) | Vector version of the basic long type. |
| --- | --- |
| [Long4](Long4.md) | Vector version of the basic long type. |
| [Matrix2f](Matrix2f.md) | Class for exposing the native RenderScript rs_matrix2x2 type back to the Android system. |
| [Matrix3f](Matrix3f.md) | Class for exposing the native RenderScript rs_matrix3x3 type back to the Android system. |
| --- | --- |
| [Matrix4f](Matrix4f.md) | Class for exposing the native RenderScript rs_matrix4x4 type back to the Android system. |
| [RenderScript](RenderScript.md) | This class provides access to a RenderScript context, which controls RenderScript initialization, resource management, and teardown. |
| [Sampler](Sampler.md) | Sampler object that defines how Allocations can be read as textures within a kernel. |
| --- | --- |
| [Script](Script.md) | The parent class for all executable scripts. |
| [ScriptC](ScriptC.md) | The superclass for all user-defined scripts. |
| [ScriptGroup](ScriptGroup.md) | A group of kernels that are executed together with one execution call as if they were a single kernel |
| --- | --- |
| [ScriptIntrinsic](ScriptIntrinsic.md) | Base class for all Intrinsic scripts. |
| [ScriptIntrinsic3DLUT](ScriptIntrinsic3DLUT.md) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. |
| [ScriptIntrinsicBLAS](ScriptIntrinsicBLAS.md) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. |
| --- | --- |
| [ScriptIntrinsicBlend](ScriptIntrinsicBlend.md) | Intrinsic kernels for blending two [android.renderscript.Allocation](Allocation.md) objects. |
| [ScriptIntrinsicBlur](ScriptIntrinsicBlur.md) | Intrinsic Gausian blur filter. |
| [ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md) | Intrinsic for applying a color matrix to allocations. |
| --- | --- |
| [ScriptIntrinsicConvolve3x3](ScriptIntrinsicConvolve3x3.md) | Intrinsic for applying a 3x3 convolve to an allocation. |
| [ScriptIntrinsicConvolve5x5](ScriptIntrinsicConvolve5x5.md) | Intrinsic for applying a 5x5 convolve to an allocation. |
| [ScriptIntrinsicHistogram](ScriptIntrinsicHistogram.md) | Intrinsic Histogram filter. |
| --- | --- |
| [ScriptIntrinsicLUT](ScriptIntrinsicLUT.md) | Intrinsic for applying a per-channel lookup table. |
| [ScriptIntrinsicResize](ScriptIntrinsicResize.md) | Intrinsic for performing a resize of a 2D allocation. |
| [ScriptIntrinsicYuvToRGB](ScriptIntrinsicYuvToRGB.md) | Intrinsic for converting an Android YUV buffer to RGB. |
| --- | --- |
| [Short2](Short2.md) | Class for exposing the native RenderScript Short2 type back to the Android system. |
| [Short3](Short3.md) | Vector version of the basic short type. |
| [Short4](Short4.md) | Vector version of the basic short type. |
| --- | --- |
| [Type](Type.md) | A Type describes the [android.renderscript.Element](Element.md) and dimensions used for an or a parallel operation. |

## Exceptions

| [RSDriverException](RSDriverException.md) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
| [RSIllegalArgumentException](RSIllegalArgumentException.md) | Base class for all exceptions thrown by the Android RenderScript |
| [RSInvalidStateException](RSInvalidStateException.md) | Base class for all exceptions thrown by the Android RenderScript |
| [RSRuntimeException](RSRuntimeException.md) | Base class for all exceptions thrown by the Android RenderScript |
| --- | --- |
