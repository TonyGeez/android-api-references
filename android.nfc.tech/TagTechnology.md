# TagTechnology

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TagTechnology

Kotlin| [Java](https://developer.android.com/reference/android/nfc/tech/TagTechnology "View this page in Java") 
| --- | --- |

```
interface TagTechnology : Closeable
```

| [android.nfc.tech.TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) |

| Known Direct Subclasses [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep), [MifareClassic](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic), [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight), [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef), [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable), [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA), [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB), [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode), [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF), [NfcV](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcV) |------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep) | Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [MifareClassic](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic) | Provides access to MIFARE Classic properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight) | Provides access to MIFARE Ultralight properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef) | Provides access to NDEF content and operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable) | Provide access to NDEF format operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA) | Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB) | Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode) | Provides access to tags containing just a barcode. | | [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF) | Provides access to NFC-F (JIS 6319-4) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | | [NfcV](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcV) | Provides access to NFC-V (ISO 15693) properties and I/O operations on a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

is an interface to a technology in a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)

Obtain a [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) implementation by calling the static method`get()`on the implementation class.

NFC tags are based on a number of independently developed technologies and offer a wide range of capabilities. The [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) implementations provide access to these different technologies and capabilities. Some sub-classes map to technology specification (for example [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA), [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep), others map to pseudo-technologies or capabilities (for example [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef), [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable)).

It is mandatory for all Android NFC devices to provide the following [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) implementations.

- [NfcA](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA)(also known as ISO 14443-3A)
- [NfcB](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcB)(also known as ISO 14443-3B)
- [NfcF](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF)(also known as JIS 6319-4)
- [NfcV](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcV)(also known as ISO 15693)
- [IsoDep](https://developer.android.com/reference/kotlin/android/nfc/tech/IsoDep)
- [Ndef](https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef) on NFC Forum Type 1, Type 2, Type 3 or Type 4 compliant tags

It is optional for Android NFC devices to provide the following [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) implementations. If it is not provided, the Android device will never enumerate that class via [Tag.getTechList](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()).

- [MifareClassic](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic)
- [MifareUltralight](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareUltralight)
- [NfcBarcode](https://developer.android.com/reference/kotlin/android/nfc/tech/NfcBarcode)
- [NdefFormatable](https://developer.android.com/reference/kotlin/android/nfc/tech/NdefFormatable) must only be enumerated on tags for which this Android device is capable of formatting. Proprietary knowledge is often required to format a tag to make it NDEF compatible.

[TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) implementations provide methods that fall into two classes:*cached getters* and*I/O operations*.

#### Cached getters

These methods (usually prefixed by`get`or`is`) return properties of the tag, as determined at discovery time. These methods will never block or cause RF activity, and do not require [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())to have been called. They also never update, for example if a property is changed by an I/O operation with a tag then the cached getter will still return the result from tag discovery time.

#### I/O operations

I/O operations may require RF activity, and may block. They have the following semantics.

- [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())must be called before using any other I/O operation.
- close must be called after completing I/O operations with a [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#), and it will cancel all other blocked I/O operations on other threads (including [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#).
- Only one [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) can be connected at a time. Other calls to [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())will return [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#).
- I/O operations may block, and should never be called on the main application thread.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#close())`()` Disable I/O operations to the tag from this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object, and release resources. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())`()` Enable I/O operations to the tag from this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object. |
| abstract [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | [getTag](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#getTag())`()` Get the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) object backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#isConnected())`()` Helper to indicate if I/O operations should be possible. |

## Public methods

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Disable I/O operations to the tag from this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object, and release resources.

Also causes all blocked I/O operations on other thread to be canceled and return with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#).

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

**See Also**

- <https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect()> 

### connect

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(): Unit
```

Enable I/O operations to the tag from this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object.

May cause RF activity and may block. Must not be called from the main application thread. A blocked call will be canceled with [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) by calling #close from another thread.

Only one [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object can be connected to a [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) at a time.

Applications must call #close when I/O operations are complete.

Requires the [android.Manifest.permission#NFC](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String) permission.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------|
| `TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or connect is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

**See Also**

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTag(): Tag!
```

Get the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) object backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) backing this [TagTechnology](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Helper to indicate if I/O operations should be possible.

Returns true if [connect](https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect())has completed, and #close has not been called, and the [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#) is not known to be out of range.

Does not cause RF activity, and does not block.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
