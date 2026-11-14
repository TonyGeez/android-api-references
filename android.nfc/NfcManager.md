# NfcManager

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcManager

Kotlin| [Java](NfcManager.md) 
| --- | --- |

```
class NfcManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NfcManager](NfcManager.md) |

High level manager used to obtain an instance of an [NfcAdapter](NfcAdapter.md).

Use [android.content.Context#getSystemService(java.lang.String)](../android.content/Context.md))with [Context.NFC_SERVICE](../android.content/Context.md) to create an [NfcManager](NfcManager.md), then call [getDefaultAdapter](NfcManager.md))to obtain the [NfcAdapter](NfcAdapter.md).

Alternately, you can just call the static helper [NfcAdapter.getDefaultAdapter(android.content.Context)](NfcAdapter.md)).
|
| ### Developer Guides
|
| For more information about using NFC, read the [Near Field Communication](https://developer.android.com/guide/topics/nfc/index.html) developer guide.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NfcAdapter](NfcAdapter.md)! | [getDefaultAdapter](NfcManager.md))`()` Get the default NFC Adapter for this device. |

## Public methods

### getDefaultAdapter

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultAdapter(): NfcAdapter!
```

Get the default NFC Adapter for this device.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------|
| [NfcAdapter](NfcAdapter.md)! | the default NFC Adapter |
