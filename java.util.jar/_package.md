# java.util.jar

# java.util.jar

## Interfaces

| [Packer](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Packer) | The packer engine applies various transformations to the input JAR file, making the pack stream highly compressible by a compressor such as gzip or zip. |
| --- | --- |
| [Unpacker](https://developer.android.com/reference/kotlin/java/util/jar/Pack200.Unpacker) | The unpacker engine converts the packed stream to a JAR file. |

## Classes

| [Attributes](https://developer.android.com/reference/kotlin/java/util/jar/Attributes) | The Attributes class maps Manifest attribute names to associated string values. |
| --- | --- |
| [JarEntry](https://developer.android.com/reference/kotlin/java/util/jar/JarEntry) | This class is used to represent a JAR file entry. |
| [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile) | The`JarFile`class is used to read the contents of a jar file from any file that can be opened with`java.io.RandomAccessFile`. |
| [JarInputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarInputStream) | The`JarInputStream`class is used to read the contents of a JAR file from any input stream. |
| --- | --- |
| [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. |
| [Manifest](https://developer.android.com/reference/kotlin/java/util/jar/Manifest) | The Manifest class is used to maintain Manifest entry names and their associated Attributes. |
| [Pack200](https://developer.android.com/reference/kotlin/java/util/jar/Pack200) | Transforms a JAR file to or from a packed stream in Pack200 format. |
| --- | --- |

## Exceptions

| [JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException) | Signals that an error of some sort has occurred while reading from or writing to a JAR file. |
| --- | --- |
