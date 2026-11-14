# NfcAdapter.CreateBeamUrisCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateBeamUrisCallback

Kotlin| [Java](https://developer.android.com/reference/android/nfc/NfcAdapter.CreateBeamUrisCallback "View this page in Java") 
| --- | --- |

```
interface CreateBeamUrisCallback
```

| [android.nfc.NfcAdapter.CreateBeamUrisCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateBeamUrisCallback#) |

| **This interface was deprecated in API level 29.**
|
| this feature is removed. File sharing can work using other technology like Bluetooth.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>! | [createBeamUris](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateBeamUrisCallback#createBeamUris(android.nfc.NfcEvent))`(`event:` ` [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent)!`)` <br /> |

## Public methods

### createBeamUris

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createBeamUris(event: NfcEvent!): Array<Uri!>!
```

**Deprecated:** *Deprecated in Java.*
