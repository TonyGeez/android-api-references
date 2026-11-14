# NfcAdapter.CreateNdefMessageCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateNdefMessageCallback

Kotlin| [Java](../android/nfc/NfcAdapter.CreateNdefMessageCallback.md) 
| --- | --- |

```
interface CreateNdefMessageCallback
```

| [android.nfc.NfcAdapter.CreateNdefMessageCallback](../android/nfc/NfcAdapter.CreateNdefMessageCallback.md) |

| **This interface was deprecated in API level 29.**
|
| this feature is removed. File sharing can work using other technology like Bluetooth.

A callback to be invoked when another NFC device capable of NDEF push (Android Beam) is within range.

Implement this interface and pass it to`NfcAdapter#setNdefPushMessageCallback setNdefPushMessageCallback()`in order to create an [NdefMessage](NdefMessage.md) at the moment that another device is within range for NFC. Using this callback allows you to create a message with data that might vary based on the content currently visible to the user. Alternatively, you can call`setNdefPushMessage setNdefPushMessage()`if the [NdefMessage](NdefMessage.md) always contains the same data.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NdefMessage](NdefMessage.md)! | [createNdefMessage](../android/nfc/NfcAdapter.CreateNdefMessageCallback.md))`(`event:` ` [NfcEvent](NfcEvent.md)!`)` Called to provide a [NdefMessage](NdefMessage.md) to push. |

## Public methods

### createNdefMessage

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createNdefMessage(event: NfcEvent!): NdefMessage!
```

**Deprecated:** *Deprecated in Java.*

Called to provide a [NdefMessage](NdefMessage.md) to push.

This callback is usually made on a binder thread (not the UI thread).

Called when this device is in range of another device that might support NDEF push. It allows the application to create the NDEF message only when it is required.

NDEF push cannot occur until this method returns, so do not block for too long.

The Android operating system will usually show a system UI on top of your activity during this time, so do not try to request input from the user to complete the callback, or provide custom NDEF push UI. The user probably will not see it.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [NfcEvent](NfcEvent.md)!: [NfcEvent](NfcEvent.md) with the [NfcEvent.nfcAdapter](NfcEvent.md) field set |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [NdefMessage](NdefMessage.md)! | NDEF message to push, or null to not provide a message |
