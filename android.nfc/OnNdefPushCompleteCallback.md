# NfcAdapter.OnNdefPushCompleteCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnNdefPushCompleteCallback

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NfcAdapter.OnNdefPushCompleteCallback "View this page in Java") 

```
interface OnNdefPushCompleteCallback
```

| [android.nfc.NfcAdapter.OnNdefPushCompleteCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnNdefPushCompleteCallback#) |

| **This interface was deprecated in API level 29.**
|
| this feature is removed. File sharing can work using other technology like Bluetooth.

A callback to be invoked when the system successfully delivers your [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage) to another device.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNdefPushComplete](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnNdefPushCompleteCallback#onNdefPushComplete(android.nfc.NfcEvent))`(`event:` ` [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent)!`)` Called on successful NDEF push. |

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
| `event` | [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent)!: [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent) with the [NfcEvent.nfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#nfcAdapter:android.nfc.NfcAdapter) field set |
