# NfcAdapter.OnNdefPushCompleteCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnNdefPushCompleteCallback

Kotlin| [Java](../android/nfc/NfcAdapter.OnNdefPushCompleteCallback.md) 
| --- | --- |

```
interface OnNdefPushCompleteCallback
```

| [android.nfc.NfcAdapter.OnNdefPushCompleteCallback](../android/nfc/NfcAdapter.OnNdefPushCompleteCallback.md) |

| **This interface was deprecated in API level 29.**
|
| this feature is removed. File sharing can work using other technology like Bluetooth.

A callback to be invoked when the system successfully delivers your [NdefMessage](../android/nfc/NdefMessage.md) to another device.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNdefPushComplete](../android/nfc/NfcAdapter.OnNdefPushCompleteCallback.md))`(`event:` ` [NfcEvent](../android/nfc/NfcEvent.md)!`)` Called on successful NDEF push. |

## Public methods

### onNdefPushComplete

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNdefPushComplete(event: NfcEvent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called on successful NDEF push.

This callback is usually made on a binder thread (not the UI thread).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [NfcEvent](../android/nfc/NfcEvent.md)!: [NfcEvent](../android/nfc/NfcEvent.md) with the [NfcEvent.nfcAdapter](../android/nfc/NfcEvent.md) field set |
