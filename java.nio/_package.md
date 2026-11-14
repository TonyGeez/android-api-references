# java.nio

# java.nio

## Classes

| [Buffer](Buffer.md) | A container for data of a specific primitive type. |
| --- | --- |
| [ByteBuffer](ByteBuffer.md) | A byte buffer. |
| [ByteOrder](ByteOrder.md) | A typesafe enumeration for byte orders. |
| [CharBuffer](CharBuffer.md) | A char buffer. |
| --- | --- |
| [DoubleBuffer](DoubleBuffer.md) | A double buffer. |
| [FloatBuffer](FloatBuffer.md) | A float buffer. |
| [IntBuffer](IntBuffer.md) | An int buffer. |
| --- | --- |
| [LongBuffer](LongBuffer.md) | A long buffer. |
| [MappedByteBuffer](MappedByteBuffer.md) | A direct byte buffer whose content is a memory-mapped region of a file. |
| [ShortBuffer](ShortBuffer.md) | A short buffer. |
| --- | --- |

## Exceptions

| [BufferOverflowException](BufferOverflowException.md) | Unchecked exception thrown when a relative*put*operation reaches the target buffer's limit. |
| --- | --- |
| [BufferUnderflowException](BufferUnderflowException.md) | Unchecked exception thrown when a relative*get*operation reaches the source buffer's limit. |
| [InvalidMarkException](InvalidMarkException.md) | Unchecked exception thrown when an attempt is made to reset a buffer when its mark is not defined. |
| [ReadOnlyBufferException](ReadOnlyBufferException.md) | Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer. |
| --- | --- |
