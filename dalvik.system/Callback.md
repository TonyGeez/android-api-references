# ZipPathValidator.Callback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

```
interface Callback
```

| [dalvik.system.ZipPathValidator.Callback](../dalvik/system/ZipPathValidator.Callback.md) |

Interface that defines the core validation mechanism when accessing zip file entry paths.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onZipEntryAccess](../dalvik/system/ZipPathValidator.Callback.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called to check the validity of the path of a zip entry. |

## Public methods

### onZipEntryAccess

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onZipEntryAccess(path: String): Unit
```

Called to check the validity of the path of a zip entry. The default implementation accepts all paths without raising any exceptions.

This method will be called by [java.util.zip.ZipInputStream#getNextEntry](../java/util/zip/ZipInputStream.md))or [java.util.zip.ZipFile#ZipFile(String)](../java/util/zip/ZipFile.md)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the zip entry. This value cannot be`null`. |

| Exceptions ||
|------------------------------|--------------------------------------------------------------|
| `java.util.zip.ZipException` | If the zip entry is invalid depending on the implementation. |
