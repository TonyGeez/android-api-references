# CardEmulation.NfcEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcEventCallback

Kotlin| [Java](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md) 
| --- | --- |

```
interface NfcEventCallback
```

| [android.nfc.cardemulation.CardEmulation.NfcEventCallback](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md) |

Callback interface for NFC-related events. These callbacks will be called when registered with [registerNfcEventCallback(java.util.concurrent.Executor,android.nfc.cardemulation.CardEmulation.NfcEventCallback)](CardEmulation.md))and while the registered caller is still alive. When you are done listening to the callbacks, you should unregister it with [unregisterNfcEventCallback(android.nfc.cardemulation.CardEmulation.NfcEventCallback)](CardEmulation.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAidConflictOccurred](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an AID conflict is detected during an NFC transaction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAidNotRouted](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an AID is not routed to any service during an NFC transaction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInternalErrorReported](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`errorType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when an internal error is reported by the NFC stack. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNfcStateChanged](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the NFC adapter state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onObserveModeStateChanged](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when observe mode has been enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOffHostAidSelected](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `offHostSecureElement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an off-host AID is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreferredServiceChanged](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`isPreferred:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when this package gains or loses preferred NFC service status. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRemoteFieldChanged](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md))`(`isDetected:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when the NFC controller is in card emulation mode and an NFC reader's field is either detected or lost. |

## Public methods

### onAidConflictOccurred

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAidConflictOccurred(aid: String): Unit
```

This method is called when an AID conflict is detected during an NFC transaction. This can happen when multiple services are registered for the same AID. If your service is registered for this AID you may want to instruct users to bring your app to the foreground and ensure you call [setPreferredService(android.app.Activity,android.content.ComponentName)](CardEmulation.md))to ensure the transaction is routed to your service.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The AID that is in conflict This value cannot be`null`. |

### onAidNotRouted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAidNotRouted(aid: String): Unit
```

This method is called when an AID is not routed to any service during an NFC transaction. This can happen when no service is registered for the given AID.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the AID that was not routed This value cannot be`null`. |

### onInternalErrorReported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInternalErrorReported(errorType: Int): Unit
```

This method is called when an internal error is reported by the NFC stack. No action is required in response to these events as the NFC stack will automatically attempt to recover. These errors are reported for informational purposes only. Note that these errors can be reported when performing various internal NFC operations (such as during device shutdown) and cannot always be explicitly correlated with NFC transaction failures.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of the internal error Value is [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_UNKNOWN](CardEmulation.md), [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_NFC_CRASH_RESTART](CardEmulation.md), [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR](CardEmulation.md), or [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_COMMAND_TIMEOUT](CardEmulation.md) |

### onNfcStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNfcStateChanged(state: Int): Unit
```

This method is called when the NFC adapter state changes.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new NFC adapter state Value is [android.nfc.NfcAdapter#STATE_OFF](../android.nfc/NfcAdapter.md), [android.nfc.NfcAdapter#STATE_TURNING_ON](../android.nfc/NfcAdapter.md), [android.nfc.NfcAdapter#STATE_ON](../android.nfc/NfcAdapter.md), or [android.nfc.NfcAdapter#STATE_TURNING_OFF](../android.nfc/NfcAdapter.md) |

### onObserveModeStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onObserveModeStateChanged(isEnabled: Boolean): Unit
```

This method is called when observe mode has been enabled or disabled.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if observe mode has been enabled, false if it has been disabled |

### onOffHostAidSelected

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOffHostAidSelected(
    aid: String, 
    offHostSecureElement: String
): Unit
```

This method is called when an off-host AID is selected. This indicates that an offhost (Secure Element or UICC) transaction has started.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The AID that was selected This value cannot be`null`. |
| `offHostSecureElement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Secure Element on which the AID was routed to. Will be string with prefix SIM or prefix eSE ([Reader.getName()](../android.se.omapi/Reader.md))). Ref: GSMA TS.26 - NFC Handset Requirements TS26_NFC_REQ_069: For UICC, Secure Element Name SHALL be SIM\[smartcard slot\] (e.g. SIM/SIM1, SIM2... SIMn). TS26_NFC_REQ_070: For embedded SE, Secure Element Name SHALL be eSE\[number\] (e.g. eSE/eSE1, eSE2, etc.). This value cannot be`null`. |

### onPreferredServiceChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPreferredServiceChanged(isPreferred: Boolean): Unit
```

This method is called when this package gains or loses preferred NFC service status. This can happen by way of either it becoming the default wallet role holder (see [android.app.role.RoleManager#ROLE_WALLET](../android.app.role/RoleManager.md)) or the preferred service of the foreground activity, set with [setPreferredService(android.app.Activity,android.content.ComponentName)](CardEmulation.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPreferred` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true is this service has become the preferred NFC service, false if it is no longer the preferred service |

### onRemoteFieldChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRemoteFieldChanged(isDetected: Boolean): Unit
```

This method is called when the NFC controller is in card emulation mode and an NFC reader's field is either detected or lost.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `isDetected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if an NFC reader is detected, false if it is lost |
