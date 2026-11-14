# NfcAdapter.ReaderCallback

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReaderCallback

Kotlin| [Java](../android/nfc/NfcAdapter.ReaderCallback.md) 
| --- | --- |

```
interface ReaderCallback
```

| [android.nfc.NfcAdapter.ReaderCallback](../android/nfc/NfcAdapter.ReaderCallback.md) |

A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode.

Register your`ReaderCallback`implementation with [android.nfc.NfcAdapter#enableReaderMode](NfcAdapter.md))and disable it with [android.nfc.NfcAdapter#disableReaderMode](NfcAdapter.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTagDiscovered](../android/nfc/NfcAdapter.ReaderCallback.md))`(`tag:` ` [Tag](Tag.md)!`)` <br /> |

## Public methods

### onTagDiscovered

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTagDiscovered(tag: Tag!): Unit
```
