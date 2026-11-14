# NfcEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcEvent

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NfcEvent "View this page in Java") 

```
class NfcEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.nfc.NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#) |

Wraps information associated with any NFC event.

Immutable object, with direct access to the (final) fields.

An [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#) object is usually included in callbacks from [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter). Check the documentation of the callback to see which fields may be set.

This wrapper object is used (instead of parameters in the callback) because it allows new fields to be added without breaking API compatibility.

## Summary

| Properties ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter)! | [nfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#nfcAdapter:android.nfc.NfcAdapter) The [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter) associated with the NFC event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [peerLlcpMajorVersion](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#peerLlcpMajorVersion:kotlin.Int) The major LLCP version number of the peer associated with the NFC event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [peerLlcpMinorVersion](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent#peerLlcpMinorVersion:kotlin.Int) The minor LLCP version number of the peer associated with the NFC event. |

## Properties

### nfcAdapter

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val nfcAdapter: NfcAdapter!
```

The [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter) associated with the NFC event. 

### peerLlcpMajorVersion

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val peerLlcpMajorVersion: Int
```

The major LLCP version number of the peer associated with the NFC event. 

### peerLlcpMinorVersion

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val peerLlcpMinorVersion: Int
```

The minor LLCP version number of the peer associated with the NFC event.
