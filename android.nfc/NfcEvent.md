# NfcEvent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcEvent

Kotlin| [Java](NfcEvent.md) 
| --- | --- |

```
class NfcEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.NfcEvent](NfcEvent.md) |

Wraps information associated with any NFC event.

Immutable object, with direct access to the (final) fields.

An [NfcEvent](NfcEvent.md) object is usually included in callbacks from [NfcAdapter](NfcAdapter.md). Check the documentation of the callback to see which fields may be set.

This wrapper object is used (instead of parameters in the callback) because it allows new fields to be added without breaking API compatibility.

## Summary

| Properties ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NfcAdapter](NfcAdapter.md)! | [nfcAdapter](NfcEvent.md) The [NfcAdapter](NfcAdapter.md) associated with the NFC event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [peerLlcpMajorVersion](NfcEvent.md) The major LLCP version number of the peer associated with the NFC event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [peerLlcpMinorVersion](NfcEvent.md) The minor LLCP version number of the peer associated with the NFC event. |
| --- | --- |

## Properties

### nfcAdapter

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val nfcAdapter: NfcAdapter!
```

The [NfcAdapter](NfcAdapter.md) associated with the NFC event. 

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
