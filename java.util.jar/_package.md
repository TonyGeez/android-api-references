# java.util.jar

# java.util.jar

## Interfaces

| [Packer](../java/util/jar/Pack200.Packer.md) | The packer engine applies various transformations to the input JAR file, making the pack stream highly compressible by a compressor such as gzip or zip. |
| --- | --- |
| [Unpacker](../java/util/jar/Pack200.Unpacker.md) | The unpacker engine converts the packed stream to a JAR file. |

## Classes

| [Attributes](../java/util/jar/Attributes.md) | The Attributes class maps Manifest attribute names to associated string values. |
| --- | --- |
| [JarEntry](../java/util/jar/JarEntry.md) | This class is used to represent a JAR file entry. |
| [JarFile](../java/util/jar/JarFile.md) | The`JarFile`class is used to read the contents of a jar file from any file that can be opened with`java.io.RandomAccessFile`. |
| [JarInputStream](../java/util/jar/JarInputStream.md) | The`JarInputStream`class is used to read the contents of a JAR file from any input stream. |
| --- | --- |
| [JarOutputStream](../java/util/jar/JarOutputStream.md) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. |
| [Manifest](../java/util/jar/Manifest.md) | The Manifest class is used to maintain Manifest entry names and their associated Attributes. |
| [Pack200](../java/util/jar/Pack200.md) | Transforms a JAR file to or from a packed stream in Pack200 format. |
| --- | --- |

## Exceptions

| [JarException](../java/util/jar/JarException.md) | Signals that an error of some sort has occurred while reading from or writing to a JAR file. |
| --- | --- |
