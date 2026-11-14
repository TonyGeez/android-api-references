# java.nio

# java.nio

## Classes

| [Buffer](../java/nio/Buffer.md) | A container for data of a specific primitive type. |
| --- | --- |
| [ByteBuffer](../java/nio/ByteBuffer.md) | A byte buffer. |
| [ByteOrder](../java/nio/ByteOrder.md) | A typesafe enumeration for byte orders. |
| [CharBuffer](../java/nio/CharBuffer.md) | A char buffer. |
| --- | --- |
| [DoubleBuffer](../java/nio/DoubleBuffer.md) | A double buffer. |
| [FloatBuffer](../java/nio/FloatBuffer.md) | A float buffer. |
| [IntBuffer](../java/nio/IntBuffer.md) | An int buffer. |
| --- | --- |
| [LongBuffer](../java/nio/LongBuffer.md) | A long buffer. |
| [MappedByteBuffer](../java/nio/MappedByteBuffer.md) | A direct byte buffer whose content is a memory-mapped region of a file. |
| [ShortBuffer](../java/nio/ShortBuffer.md) | A short buffer. |
| --- | --- |

## Exceptions

| [BufferOverflowException](../java/nio/BufferOverflowException.md) | Unchecked exception thrown when a relative*put*operation reaches the target buffer's limit. |
| --- | --- |
| [BufferUnderflowException](../java/nio/BufferUnderflowException.md) | Unchecked exception thrown when a relative*get*operation reaches the source buffer's limit. |
| [InvalidMarkException](../java/nio/InvalidMarkException.md) | Unchecked exception thrown when an attempt is made to reset a buffer when its mark is not defined. |
| [ReadOnlyBufferException](../java/nio/ReadOnlyBufferException.md) | Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer. |
| --- | --- |
