# ZipPathValidator.Callback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

```
interface Callback
```

| [dalvik.system.ZipPathValidator.Callback](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback#) |

Interface that defines the core validation mechanism when accessing zip file entry paths.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onZipEntryAccess](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.Callback#onZipEntryAccess(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called to check the validity of the path of a zip entry. |

## Public methods

### onZipEntryAccess

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onZipEntryAccess(path: String): Unit
```

Called to check the validity of the path of a zip entry. The default implementation accepts all paths without raising any exceptions.

This method will be called by [java.util.zip.ZipInputStream#getNextEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipInputStream.html#getNextEntry())or [java.util.zip.ZipFile#ZipFile(String)](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ZipFile(kotlin.String)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the zip entry. This value cannot be`null`. |

| Exceptions ||
|------------------------------|--------------------------------------------------------------|
| `java.util.zip.ZipException` | If the zip entry is invalid depending on the implementation. |
