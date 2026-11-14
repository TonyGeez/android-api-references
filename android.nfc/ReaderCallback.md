# NfcAdapter.ReaderCallback

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReaderCallback

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NfcAdapter.ReaderCallback "View this page in Java") 
| --- | --- |

```
interface ReaderCallback
```

| [android.nfc.NfcAdapter.ReaderCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback#) |

A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode.

Register your`ReaderCallback`implementation with [android.nfc.NfcAdapter#enableReaderMode](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle))and disable it with [android.nfc.NfcAdapter#disableReaderMode](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disableReaderMode(android.app.Activity)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTagDiscovered](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback#onTagDiscovered(android.nfc.Tag))`(`tag:` ` [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag)!`)` <br /> |

## Public methods

### onTagDiscovered

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTagDiscovered(tag: Tag!): Unit
```
