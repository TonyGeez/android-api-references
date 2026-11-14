# SimPhonebookContract

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimPhonebookContract

Kotlin| [Java](SimPhonebookContract.md) 
| --- | --- |

```
class SimPhonebookContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.SimPhonebookContract](SimPhonebookContract.md) |

The contract between the provider of contact records on the device's SIM cards and applications. Contains definitions of the supported URIs and columns.

### Permissions

<br />

Querying this provider requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md) and writing to this provider requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ElementaryFiles](../android/provider/SimPhonebookContract.ElementaryFiles.md) Constants for metadata about the elementary files of the SIM cards in the phone. |
| | [SimRecords](../android/provider/SimPhonebookContract.SimRecords.md) Constants for the contact records on a SIM card. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](SimPhonebookContract.md) The authority for the SIM phonebook provider. |

| Properties ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android.net/Uri.md) | [AUTHORITY_URI](SimPhonebookContract.md) The content:// style uri to the authority for the SIM phonebook provider. |

## Constants

### AUTHORITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

The authority for the SIM phonebook provider. 

 Value: "com.android.simphonebook"

## Properties

### AUTHORITY_URI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY_URI: Uri
```

The content:// style uri to the authority for the SIM phonebook provider.
