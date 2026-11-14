# NfcManager

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcManager

Kotlin| [Java](../android/nfc/NfcManager.md) 
| --- | --- |

```
class NfcManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NfcManager](../android/nfc/NfcManager.md) |

High level manager used to obtain an instance of an [NfcAdapter](../android/nfc/NfcAdapter.md).

Use [android.content.Context#getSystemService(java.lang.String)](../android/content/Context.md))with [Context.NFC_SERVICE](../android/content/Context.md) to create an [NfcManager](../android/nfc/NfcManager.md), then call [getDefaultAdapter](../android/nfc/NfcManager.md))to obtain the [NfcAdapter](../android/nfc/NfcAdapter.md).

Alternately, you can just call the static helper [NfcAdapter.getDefaultAdapter(android.content.Context)](../android/nfc/NfcAdapter.md)).
|
| ### Developer Guides
|
| For more information about using NFC, read the [Near Field Communication](https://developer.android.com/guide/topics/nfc/index.html) developer guide.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NfcAdapter](../android/nfc/NfcAdapter.md)! | [getDefaultAdapter](../android/nfc/NfcManager.md))`()` Get the default NFC Adapter for this device. |

## Public methods

### getDefaultAdapter

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultAdapter(): NfcAdapter!
```

Get the default NFC Adapter for this device.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------|
| [NfcAdapter](../android/nfc/NfcAdapter.md)! | the default NFC Adapter |
