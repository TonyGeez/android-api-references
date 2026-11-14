# FileTypeDetector

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileTypeDetector

```
abstract class FileTypeDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.spi.FileTypeDetector](../java/nio/file/spi/FileTypeDetector.md) |

A file type detector for probing a file to guess its file type.

A file type detector is a concrete implementation of this class, has a zero-argument constructor, and implements the abstract methods specified below.

The means by which a file type detector determines the file type is highly implementation specific. A simple implementation might examine the*file extension* (a convention used in some platforms) and map it to a file type. In other cases, the file type may be stored as a file [attribute](../java/nio/file/attribute/_package.md) or the bytes in a file may be examined to guess its file type.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileTypeDetector](../java/nio/file/spi/FileTypeDetector.md))`()` Initializes a new instance of this class. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [probeContentType](../java/nio/file/spi/FileTypeDetector.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Probes the given file to guess its content type. |

## Protected constructors

### FileTypeDetector

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileTypeDetector()
```

Initializes a new instance of this class.

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("fileTypeDetector")` |

## Public methods

### probeContentType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun probeContentType(path: Path!): String!
```

Probes the given file to guess its content type.

The means by which this method determines the file type is highly implementation specific. It may simply examine the file name, it may use a file [attribute](../java/nio/file/attribute/_package.md), or it may examines bytes in the file.

The probe result is the string form of the value of a Multipurpose Internet Mail Extension (MIME) content type as defined by [*RFC 2045: Multipurpose Internet Mail Extensions (MIME) Part One: Format of Internet Message Bodies*](http://www.ietf.org/rfc/rfc2045.txt). The string must be parsable according to the grammar in the RFC 2045.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to probe |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The content type or`null`if the file type is not recognized |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | An I/O error occurs |
| `java.lang.SecurityException` | If the implementation requires to access the file, and a security manager is installed, and it denies an unspecified permission required by a file system provider implementation. If the file reference is associated with the default file system provider then the [SecurityManager.checkRead(String)](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

**See Also**

- [java.nio.file.Files#probeContentType](../java/nio/file/Files.md))
