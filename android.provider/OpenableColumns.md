# OpenableColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OpenableColumns

Kotlin| [Java](OpenableColumns.md) 
| --- | --- |

```
interface OpenableColumns
```

| [android.provider.OpenableColumns](OpenableColumns.md) |

| Known Direct Subclasses [VoicemailContract.Voicemails](../android/provider/VoicemailContract.Voicemails.md) |------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------| | [VoicemailContract.Voicemails](../android/provider/VoicemailContract.Voicemails.md) | Defines fields exposed through the /voicemail path of this content provider. | |
| --- | --- | --- | --- | --- | --- | --- |

These are standard columns for openable URIs. Providers that serve openable URIs*must*support at least these columns when queried.

To find the content type of a URI, use [ContentResolver.getType(android.net.Uri)](../android.content/ContentResolver.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME](OpenableColumns.md) The human-friendly name of file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SIZE](OpenableColumns.md) The number of bytes in the file identified by the openable URI. |

## Constants

### DISPLAY_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME: String
```

The human-friendly name of file. If this is not provided then the name should default to the the last segment of the file's URI. 

 Value: "_display_name"

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: String
```

The number of bytes in the file identified by the openable URI. Null if unknown. 

 Value: "_size"
