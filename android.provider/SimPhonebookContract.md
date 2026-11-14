# SimPhonebookContract

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimPhonebookContract

Kotlin| [Java](https://developer.android.com/reference/android/provider/SimPhonebookContract "View this page in Java") 

```
class SimPhonebookContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.SimPhonebookContract](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract#) |

The contract between the provider of contact records on the device's SIM cards and applications. Contains definitions of the supported URIs and columns.

### Permissions

<br />

Querying this provider requires [android.Manifest.permission#READ_CONTACTS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String) and writing to this provider requires [android.Manifest.permission#WRITE_CONTACTS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_CONTACTS:kotlin.String)

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ElementaryFiles](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract.ElementaryFiles) Constants for metadata about the elementary files of the SIM cards in the phone. |
| | [SimRecords](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract.SimRecords) Constants for the contact records on a SIM card. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract#AUTHORITY:kotlin.String) The authority for the SIM phonebook provider. |

| Properties ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [AUTHORITY_URI](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract#AUTHORITY_URI:android.net.Uri) The content:// style uri to the authority for the SIM phonebook provider. |

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
