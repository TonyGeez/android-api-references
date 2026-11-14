# CardEmulation.NfcEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcEventCallback

Kotlin| [Java](https://developer.android.com/reference/android/nfc/cardemulation/CardEmulation.NfcEventCallback "View this page in Java") 
| --- | --- |

```
interface NfcEventCallback
```

| [android.nfc.cardemulation.CardEmulation.NfcEventCallback](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#) |

Callback interface for NFC-related events. These callbacks will be called when registered with [registerNfcEventCallback(java.util.concurrent.Executor,android.nfc.cardemulation.CardEmulation.NfcEventCallback)](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerNfcEventCallback(java.util.concurrent.Executor,%20android.nfc.cardemulation.CardEmulation.NfcEventCallback))and while the registered caller is still alive. When you are done listening to the callbacks, you should unregister it with [unregisterNfcEventCallback(android.nfc.cardemulation.CardEmulation.NfcEventCallback)](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#unregisterNfcEventCallback(android.nfc.cardemulation.CardEmulation.NfcEventCallback)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAidConflictOccurred](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onAidConflictOccurred(kotlin.String))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an AID conflict is detected during an NFC transaction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAidNotRouted](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onAidNotRouted(kotlin.String))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an AID is not routed to any service during an NFC transaction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInternalErrorReported](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onInternalErrorReported(kotlin.Int))`(`errorType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when an internal error is reported by the NFC stack. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNfcStateChanged](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onNfcStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the NFC adapter state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onObserveModeStateChanged](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onObserveModeStateChanged(kotlin.Boolean))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when observe mode has been enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOffHostAidSelected](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onOffHostAidSelected(kotlin.String,%20kotlin.String))`(`aid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `offHostSecureElement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method is called when an off-host AID is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreferredServiceChanged](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onPreferredServiceChanged(kotlin.Boolean))`(`isPreferred:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when this package gains or loses preferred NFC service status. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRemoteFieldChanged](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback#onRemoteFieldChanged(kotlin.Boolean))`(`isDetected:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when the NFC controller is in card emulation mode and an NFC reader's field is either detected or lost. |

## Public methods

### onAidConflictOccurred

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAidConflictOccurred(aid: String): Unit
```

This method is called when an AID conflict is detected during an NFC transaction. This can happen when multiple services are registered for the same AID. If your service is registered for this AID you may want to instruct users to bring your app to the foreground and ensure you call [setPreferredService(android.app.Activity,android.content.ComponentName)](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setPreferredService(android.app.Activity,%20android.content.ComponentName))to ensure the transaction is routed to your service.

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
| `errorType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of the internal error Value is [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_UNKNOWN:kotlin.Int), [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_NFC_CRASH_RESTART](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_NFC_CRASH_RESTART:kotlin.Int), [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR:kotlin.Int), or [android.nfc.cardemulation.CardEmulation#NFC_INTERNAL_ERROR_COMMAND_TIMEOUT](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_COMMAND_TIMEOUT:kotlin.Int) |

### onNfcStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNfcStateChanged(state: Int): Unit
```

This method is called when the NFC adapter state changes.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new NFC adapter state Value is [android.nfc.NfcAdapter#STATE_OFF](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#STATE_OFF:kotlin.Int), [android.nfc.NfcAdapter#STATE_TURNING_ON](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#STATE_TURNING_ON:kotlin.Int), [android.nfc.NfcAdapter#STATE_ON](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#STATE_ON:kotlin.Int), or [android.nfc.NfcAdapter#STATE_TURNING_OFF](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#STATE_TURNING_OFF:kotlin.Int) |

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
| `offHostSecureElement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Secure Element on which the AID was routed to. Will be string with prefix SIM or prefix eSE ([Reader.getName()](https://developer.android.com/reference/kotlin/android/se/omapi/Reader.html#getName())). Ref: GSMA TS.26 - NFC Handset Requirements TS26_NFC_REQ_069: For UICC, Secure Element Name SHALL be SIM\[smartcard slot\] (e.g. SIM/SIM1, SIM2... SIMn). TS26_NFC_REQ_070: For embedded SE, Secure Element Name SHALL be eSE\[number\] (e.g. eSE/eSE1, eSE2, etc.). This value cannot be`null`. |

### onPreferredServiceChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPreferredServiceChanged(isPreferred: Boolean): Unit
```

This method is called when this package gains or loses preferred NFC service status. This can happen by way of either it becoming the default wallet role holder (see [android.app.role.RoleManager#ROLE_WALLET](https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String)) or the preferred service of the foreground activity, set with [setPreferredService(android.app.Activity,android.content.ComponentName)](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setPreferredService(android.app.Activity,%20android.content.ComponentName)).

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
