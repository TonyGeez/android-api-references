# TagTechnology

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TagTechnology

Kotlin| [Java](../android/nfc/tech/TagTechnology.md) 
| --- | --- |

```
interface TagTechnology : Closeable
```

| [android.nfc.tech.TagTechnology](../android/nfc/tech/TagTechnology.md) |

| Known Direct Subclasses [IsoDep](../android/nfc/tech/IsoDep.md), [MifareClassic](../android/nfc/tech/MifareClassic.md), [MifareUltralight](../android/nfc/tech/MifareUltralight.md), [Ndef](../android/nfc/tech/Ndef.md), [NdefFormatable](../android/nfc/tech/NdefFormatable.md), [NfcA](../android/nfc/tech/NfcA.md), [NfcB](../android/nfc/tech/NfcB.md), [NfcBarcode](../android/nfc/tech/NfcBarcode.md), [NfcF](../android/nfc/tech/NfcF.md), [NfcV](../android/nfc/tech/NfcV.md) |------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [IsoDep](../android/nfc/tech/IsoDep.md) | Provides access to ISO-DEP (ISO 14443-4) properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [MifareClassic](../android/nfc/tech/MifareClassic.md) | Provides access to MIFARE Classic properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [MifareUltralight](../android/nfc/tech/MifareUltralight.md) | Provides access to MIFARE Ultralight properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [Ndef](../android/nfc/tech/Ndef.md) | Provides access to NDEF content and operations on a [Tag](../android/nfc/Tag.md). | | [NdefFormatable](../android/nfc/tech/NdefFormatable.md) | Provide access to NDEF format operations on a [Tag](../android/nfc/Tag.md). | | [NfcA](../android/nfc/tech/NfcA.md) | Provides access to NFC-A (ISO 14443-3A) properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [NfcB](../android/nfc/tech/NfcB.md) | Provides access to NFC-B (ISO 14443-3B) properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [NfcBarcode](../android/nfc/tech/NfcBarcode.md) | Provides access to tags containing just a barcode. | | [NfcF](../android/nfc/tech/NfcF.md) | Provides access to NFC-F (JIS 6319-4) properties and I/O operations on a [Tag](../android/nfc/Tag.md). | | [NfcV](../android/nfc/tech/NfcV.md) | Provides access to NFC-V (ISO 15693) properties and I/O operations on a [Tag](../android/nfc/Tag.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

is an interface to a technology in a [Tag](../android/nfc/Tag.md)

Obtain a [TagTechnology](../android/nfc/tech/TagTechnology.md) implementation by calling the static method`get()`on the implementation class.

NFC tags are based on a number of independently developed technologies and offer a wide range of capabilities. The [TagTechnology](../android/nfc/tech/TagTechnology.md) implementations provide access to these different technologies and capabilities. Some sub-classes map to technology specification (for example [NfcA](../android/nfc/tech/NfcA.md), [IsoDep](../android/nfc/tech/IsoDep.md), others map to pseudo-technologies or capabilities (for example [Ndef](../android/nfc/tech/Ndef.md), [NdefFormatable](../android/nfc/tech/NdefFormatable.md)).

It is mandatory for all Android NFC devices to provide the following [TagTechnology](../android/nfc/tech/TagTechnology.md) implementations.

- [NfcA](../android/nfc/tech/NfcA.md)(also known as ISO 14443-3A)
- [NfcB](../android/nfc/tech/NfcB.md)(also known as ISO 14443-3B)
- [NfcF](../android/nfc/tech/NfcF.md)(also known as JIS 6319-4)
- [NfcV](../android/nfc/tech/NfcV.md)(also known as ISO 15693)
- [IsoDep](../android/nfc/tech/IsoDep.md)
- [Ndef](../android/nfc/tech/Ndef.md) on NFC Forum Type 1, Type 2, Type 3 or Type 4 compliant tags

It is optional for Android NFC devices to provide the following [TagTechnology](../android/nfc/tech/TagTechnology.md) implementations. If it is not provided, the Android device will never enumerate that class via [Tag.getTechList](../android/nfc/Tag.md)).

- [MifareClassic](../android/nfc/tech/MifareClassic.md)
- [MifareUltralight](../android/nfc/tech/MifareUltralight.md)
- [NfcBarcode](../android/nfc/tech/NfcBarcode.md)
- [NdefFormatable](../android/nfc/tech/NdefFormatable.md) must only be enumerated on tags for which this Android device is capable of formatting. Proprietary knowledge is often required to format a tag to make it NDEF compatible.

[TagTechnology](../android/nfc/tech/TagTechnology.md) implementations provide methods that fall into two classes:*cached getters* and*I/O operations*.

#### Cached getters

These methods (usually prefixed by`get`or`is`) return properties of the tag, as determined at discovery time. These methods will never block or cause RF activity, and do not require [connect](../android/nfc/tech/TagTechnology.md))to have been called. They also never update, for example if a property is changed by an I/O operation with a tag then the cached getter will still return the result from tag discovery time.

#### I/O operations

I/O operations may require RF activity, and may block. They have the following semantics.

- [connect](../android/nfc/tech/TagTechnology.md))must be called before using any other I/O operation.
- close must be called after completing I/O operations with a [TagTechnology](../android/nfc/tech/TagTechnology.md), and it will cancel all other blocked I/O operations on other threads (including [connect](../android/nfc/tech/TagTechnology.md))with [IOException](../java/io/IOException.md).
- Only one [TagTechnology](../android/nfc/tech/TagTechnology.md) can be connected at a time. Other calls to [connect](../android/nfc/tech/TagTechnology.md))will return [IOException](../java/io/IOException.md).
- I/O operations may block, and should never be called on the main application thread.

**Note:** Methods that perform I/O operations require the [android.Manifest.permission#NFC](../android/Manifest.permission.md) permission.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/nfc/tech/TagTechnology.md))`()` Disable I/O operations to the tag from this [TagTechnology](../android/nfc/tech/TagTechnology.md) object, and release resources. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/nfc/tech/TagTechnology.md))`()` Enable I/O operations to the tag from this [TagTechnology](../android/nfc/tech/TagTechnology.md) object. |
| abstract [Tag](../android/nfc/Tag.md)! | [getTag](../android/nfc/tech/TagTechnology.md))`()` Get the [Tag](../android/nfc/Tag.md) object backing this [TagTechnology](../android/nfc/tech/TagTechnology.md) object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/nfc/tech/TagTechnology.md))`()` Helper to indicate if I/O operations should be possible. |

## Public methods

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Disable I/O operations to the tag from this [TagTechnology](../android/nfc/tech/TagTechnology.md) object, and release resources.

Also causes all blocked I/O operations on other thread to be canceled and return with [IOException](../java/io/IOException.md).

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

Enable I/O operations to the tag from this [TagTechnology](../android/nfc/tech/TagTechnology.md) object.

May cause RF activity and may block. Must not be called from the main application thread. A blocked call will be canceled with [IOException](../java/io/IOException.md) by calling #close from another thread.

Only one [TagTechnology](../android/nfc/tech/TagTechnology.md) object can be connected to a [Tag](../android/nfc/Tag.md) at a time.

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

Get the [Tag](../android/nfc/Tag.md) object backing this [TagTechnology](../android/nfc/tech/TagTechnology.md) object.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag](../android/nfc/Tag.md)! | the [Tag](../android/nfc/Tag.md) backing this [TagTechnology](../android/nfc/tech/TagTechnology.md) object. |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Helper to indicate if I/O operations should be possible.

Returns true if [connect](../android/nfc/tech/TagTechnology.md))has completed, and #close has not been called, and the [Tag](../android/nfc/Tag.md) is not known to be out of range.

Does not cause RF activity, and does not block.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if I/O operations should be possible |
