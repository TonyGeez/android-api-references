# TagTechnology

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TagTechnology

Kotlin| [Java](TagTechnology.md) 
| --- | --- |

```
interface TagTechnology : Closeable
```

| [android.nfc.tech.TagTechnology](TagTechnology.md) |

| Known Direct Subclasses [IsoDep](IsoDep.md), [MifareClassic](MifareClassic.md), [MifareUltralight](MifareUltralight.md), [Ndef](Ndef.md), [NdefFormatable](NdefFormatable.md), [NfcA](NfcA.md), [NfcB](NfcB.md), [NfcBarcode](NfcBarcode.md), [NfcF](NfcF.md), [NfcV](NfcV.md) |------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [IsoDep](IsoDep.md) | Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [MifareClassic](MifareClassic.md) | Provides access to MIFARE Classic properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [MifareUltralight](MifareUltralight.md) | Provides access to MIFARE Ultralight properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [Ndef](Ndef.md) | Provides access to NDEF content and operations on a [Tag](../android.nfc/Tag.md). | | [NdefFormatable](NdefFormatable.md) | Provide access to NDEF format operations on a [Tag](../android.nfc/Tag.md). | | [NfcA](NfcA.md) | Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [NfcB](NfcB.md) | Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [NfcBarcode](NfcBarcode.md) | Provides access to tags containing just a barcode. | | [NfcF](NfcF.md) | Provides access to NFC-F (JIS 6319-4) properties and I/O operations on a [Tag](../android.nfc/Tag.md). | | [NfcV](NfcV.md) | Provides access to NFC-V (ISO 15693) properties and I/O operations on a [Tag](../android.nfc/Tag.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

is an interface to a technology in a [Tag](../android.nfc/Tag.md)

Obtain a [TagTechnology](TagTechnology.md) implementation by calling the static method`get()`on the implementation class.

NFC tags are based on a number of independently developed technologies and offer a wide range of capabilities. The [TagTechnology](TagTechnology.md) implementations provide access to these different technologies and capabilities. Some sub-classes map to technology specification (for example [NfcA](NfcA.md), [IsoDep](IsoDep.md), others map to pseudo-technologies or capabilities (for example [Ndef](Ndef.md), [NdefFormatable](NdefFormatable.md)).

It is mandatory for all Android NFC devices to provide the following [TagTechnology](TagTechnology.md) implementations.

- [NfcA](NfcA.md)(also known as ISO 14443-3A)
- [NfcB](NfcB.md)(also known as ISO 14443-3B)
- [NfcF](NfcF.md)(also known as JIS 6319-4)
- [NfcV](NfcV.md)(also known as ISO 15693)
- [IsoDep](IsoDep.md)
- [Ndef](Ndef.md) on NFC Forum Type 1, Type 2, Type 3 or Type 4 compliant tags

It is optional for Android NFC devices to provide the following [TagTechnology](TagTechnology.md) implementations. If it is not provided, the Android device will never enumerate that class via [Tag.getTechList](../android.nfc/Tag.md)).

- [MifareClassic](MifareClassic.md)
- [MifareUltralight](MifareUltralight.md)
- [NfcBarcode](NfcBarcode.md)
- [NdefFormatable](NdefFormatable.md) must only be enumerated on tags for which this Android device is capable of formatting. Proprietary knowledge is often required to format a tag to make it NDEF compatible.

[TagTechnology](TagTechnology.md) implementations provide methods that fall into two classes:*cached getters* and*I/O operations*.

#### Cached getters

These methods (usually prefixed by`get`or`is`) return properties of the tag, as determined at discovery time. These methods will never block or cause RF activity, and do not require [connect](TagTechnology.md))to have been called. They also never update, for example if a property is changed by an I/O operation with a tag then the cached getter will still return the result from tag discovery time.

#### I/O operations

I/O operations may require RF activity, and may block. They have the following semantics.

- [connect](TagTechnology.md))must be called before using any other I/O operation.
- close must be called after completing I/O operations with a [TagTechnology](TagTechnology.md), and it will cancel all other blocked I/O operations on other threads (including [connect](TagTechnology.md))with [IOException](../java.io/IOException.md).
- Only one [TagTechnology](TagTechnology.md) can be connected at a time. Other calls to [connect](TagTechnology.md))will return [IOException](../java.io/IOException.md).
- I/O operations may block, and should never be called on the main application thread.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](TagTechnology.md))`()` Disable I/O operations to the tag from this [TagTechnology](TagTechnology.md) object, and release resources. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](TagTechnology.md))`()` Enable I/O operations to the tag from this [TagTechnology](TagTechnology.md) object. |
| abstract [Tag](../android.nfc/Tag.md)! | [getTag](TagTechnology.md))`()` Get the [Tag](../android.nfc/Tag.md) object backing this [TagTechnology](TagTechnology.md) object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](TagTechnology.md))`()` Helper to indicate if I/O operations should be possible. |

## Public methods

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Disable I/O operations to the tag from this [TagTechnology](TagTechnology.md) object, and release resources.

Also causes all blocked I/O operations on other thread to be canceled and return with [IOException](../java.io/IOException.md).

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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

Enable I/O operations to the tag from this [TagTechnology](TagTechnology.md) object.

May cause RF activity and may block. Must not be called from the main application thread. A blocked call will be canceled with [IOException](../java.io/IOException.md) by calling #close from another thread.

Only one [TagTechnology](TagTechnology.md) object can be connected to a [Tag](../android.nfc/Tag.md) at a time.

Applications must call #close when I/O operations are complete.

Requires the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

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

Get the [Tag](../android.nfc/Tag.md) object backing this [TagTechnology](TagTechnology.md) object.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android.nfc/Tag.md)! | the [Tag](../android.nfc/Tag.md) backing this [TagTechnology](TagTechnology.md) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Helper to indicate if I/O operations should be possible.

Returns true if [connect](TagTechnology.md))has completed, and #close has not been called, and the [Tag](../android.nfc/Tag.md) is not known to be out of range.

Does not cause RF activity, and does not block.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
