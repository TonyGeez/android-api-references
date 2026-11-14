# NdefFormatable

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NdefFormatable

Kotlin| [Java](NdefFormatable.md) 
| --- | --- |

```
class NdefFormatable : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.NdefFormatable](NdefFormatable.md) |

Provide access to NDEF format operations on a [Tag](../android.nfc/Tag.md).

Acquire a [NdefFormatable](NdefFormatable.md) object using [get](NdefFormatable.md)).

Android devices with NFC must only enumerate and implement this class for tags for which it can format to NDEF.

Unfortunately the procedures to convert unformated tags to NDEF formatted tags are not specified by NFC Forum, and are not generally well-known. So there is no mandatory set of tags for which all Android devices with NFC must support [NdefFormatable](NdefFormatable.md).

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](NdefFormatable.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](NdefFormatable.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [format](NdefFormatable.md))`(`firstMessage:` ` [NdefMessage](../android.nfc/NdefMessage.md)!`)` Format a tag as NDEF, and write a [NdefMessage](../android.nfc/NdefMessage.md). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatReadOnly](NdefFormatable.md))`(`firstMessage:` ` [NdefMessage](../android.nfc/NdefMessage.md)!`)` Formats a tag as NDEF, write a [NdefMessage](../android.nfc/NdefMessage.md), and make read-only. |
| static [NdefFormatable](NdefFormatable.md)! | [get](NdefFormatable.md))`(`tag:` ` [Tag](../android.nfc/Tag.md)!`)` Get an instance of [NdefFormatable](NdefFormatable.md) for the given tag. |
| [Tag](../android.nfc/Tag.md)! | [getTag](NdefFormatable.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](NdefFormatable.md))`()` <br /> |

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

Format a tag as NDEF, and write a [NdefMessage](../android.nfc/NdefMessage.md).

This is a multi-step process, an IOException is thrown if any one step fails.

The card is left in a read-write state after this operation.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `firstMessage` | [NdefMessage](../android.nfc/NdefMessage.md)!:the NDEF message to write after formatting, can be null |

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

Formats a tag as NDEF, write a [NdefMessage](../android.nfc/NdefMessage.md), and make read-only.

This is a multi-step process, an IOException is thrown if any one step fails.

The card is left in a read-only state if this method returns successfully.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) if #close is called from another thread.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `firstMessage` | [NdefMessage](../android.nfc/NdefMessage.md)!:the NDEF message to write after formatting |

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

Get an instance of [NdefFormatable](NdefFormatable.md) for the given tag.

Does not cause any RF activity and does not block.

Returns null if [NdefFormatable](NdefFormatable.md) was not enumerated in [Tag.getTechList](../android.nfc/Tag.md)). This indicates the tag is not NDEF formatable by this Android device.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `tag` | [Tag](../android.nfc/Tag.md)!:an NDEF formatable tag |

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------|
| [NdefFormatable](NdefFormatable.md)! | NDEF formatable object |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): Tag!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android.nfc/Tag.md)! | the [Tag](../android.nfc/Tag.md) backing this [TagTechnology](TagTechnology.md) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
