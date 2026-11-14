# NdefFormatable

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NdefFormatable

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/NdefFormatable "View this page in Java") 
| --- | --- |

```
class NdefFormatable : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#) |

Provide access to NDEF format operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#).

Acquire a [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#) object using [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#get(android.nfc.Tag)).

Android devices with NFC must only enumerate and implement this class for tags for which it can format to NDEF.

Unfortunately the procedures to convert unformated tags to NDEF formatted tags are not specified by NFC Forum, and are not generally well-known. So there is no mandatory set of tags for which all Android devices with NFC must support [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#connect())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [format](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#format(android.nfc.NdefMessage))`(`firstMessage:` ` [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!`)` Format a tag as NDEF, and write a [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatReadOnly](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#formatReadOnly(android.nfc.NdefMessage))`(`firstMessage:` ` [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!`)` Formats a tag as NDEF, write a [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#), and make read-only. |
| static [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#)! | [get](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#get(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!`)` Get an instance of [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#) for the given tag. |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#getTag())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#isConnected())`()` <br /> |

## Public methods

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### connect

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(): Unit
```

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or connect is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### format

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(firstMessage: NdefMessage!): Unit
```

Format a tag as NDEF, and write a [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#).

This is a multi-step process, an IOException is thrown if any one step fails.

The card is left in a read-write state after this operation.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `firstMessage` | [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!:the NDEF message to write after formatting, can be null |

| Exceptions ||
|--------------------------------|----------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `android.nfc.FormatException` | if the NDEF Message to write is malformed |
| --- | --- |

### formatReadOnly

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatReadOnly(firstMessage: NdefMessage!): Unit
```

Formats a tag as NDEF, write a [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#), and make read-only.

This is a multi-step process, an IOException is thrown if any one step fails.

The card is left in a read-only state if this method returns successfully.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `firstMessage` | [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage.html#)!:the NDEF message to write after formatting |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |
| `android.nfc.FormatException` | if the NDEF Message to write is malformed |
| --- | --- |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### get

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(tag: Tag!): NdefFormatable!
```

Get an instance of [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#) for the given tag.

Does not cause any RF activity and does not block.

Returns null if [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#) was not enumerated in [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()). This indicates the tag is not NDEF formatable by this Android device.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!:an NDEF formatable tag |

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------|
| [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable#)! | NDEF formatable object |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
