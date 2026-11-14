# NfcManager

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcManager

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NfcManager "View this page in Java") 

```
class NfcManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.nfc.NfcManager](https://developer.android.com/reference/kotlin/android/nfc/NfcManager#) |

High level manager used to obtain an instance of an [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter).

Use [android.content.Context#getSystemService(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String))with [Context.NFC_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#NFC_SERVICE:kotlin.String) to create an [NfcManager](https://developer.android.com/reference/kotlin/android/nfc/NfcManager#), then call [getDefaultAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcManager#getDefaultAdapter())to obtain the [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter).

Alternately, you can just call the static helper [NfcAdapter.getDefaultAdapter(android.content.Context)](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#getDefaultAdapter(android.content.Context)).
|
| ### Developer Guides
|
| For more information about using NFC, read the [Near Field Communication](https://developer.android.com/guide/topics/nfc/index.html) developer guide.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter)! | [getDefaultAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcManager#getDefaultAdapter())`()` Get the default NFC Adapter for this device. |

## Public methods

### getDefaultAdapter

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultAdapter(): NfcAdapter!
```

Get the default NFC Adapter for this device.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------|
| [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter)! | the default NFC Adapter |
