# ObbScanner

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObbScanner

Kotlin| [Java](ObbScanner.md) 
| --- | --- |

```
open class ObbScanner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.ObbScanner](ObbScanner.md) |

Class to scan Opaque Binary Blob (OBB) files. Use this to get information about an OBB file for use in a program via [ObbInfo](ObbInfo.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ObbInfo](ObbInfo.md)! | [getObbInfo](ObbScanner.md))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Scan a file for OBB information. |

## Public methods

### getObbInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getObbInfo(filePath: String!): ObbInfo!
```

Scan a file for OBB information.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to the OBB file to be scanned. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ObbInfo](ObbInfo.md)! | ObbInfo object information corresponding to the file path |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the OBB file couldn't be found |
| `java.io.IOException` | if the OBB file couldn't be read |
