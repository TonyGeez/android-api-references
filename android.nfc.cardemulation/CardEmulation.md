Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CardEmulation

```
class CardEmulation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.cardemulation.CardEmulation](CardEmulation.md) |

This class can be used to query the state of NFC card emulation services. For a general introduction into NFC card emulation, please read the [NFC card emulation developer guide](https://developer.android.com/guide/topics/connectivity/nfc/hce.html).

<br />

Use of this class requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_HOST_CARD_EMULATION:kotlin.String` to be present on the device.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback` Callback interface for NFC-related events. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String` Activity action: ask the user to change the default card emulation service for a certain category. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_OTHER:kotlin.String` Category that can be used for all other card emulation services. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` Category used for NFC payment services. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#EXTRA_CATEGORY:kotlin.String` The category extra for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#EXTRA_SERVICE_COMPONENT:kotlin.String` The service `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` object passed in as an extra for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_COMMAND_TIMEOUT:kotlin.Int` This error is reported when the NFC stack times out while waiting for a response to a command sent to the NFC hardware. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_NFC_CRASH_RESTART:kotlin.Int` This error is reported when the NFC command watchdog restarts the NFC stack. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR:kotlin.Int` This error is reported when the NFC controller does not respond or there's an NCI transport error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#NFC_INTERNAL_ERROR_UNKNOWN:kotlin.Int` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROPERTY_ALLOW_SHARED_ROLE_PRIORITY:kotlin.String` Property name used to indicate that an application wants to allow associated services to share the same AID routing priority when this application is the role holder. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_DEFAULT:kotlin.Int` Route to the default value in config file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_DH:kotlin.Int` Route to Device Host (DH). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_ESE:kotlin.Int` Route to eSE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_NDEF_NFCEE:kotlin.Int` Route to T4T NDEF-NCEE emulation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_UICC:kotlin.Int` Route to UICC. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#PROTOCOL_AND_TECHNOLOGY_ROUTE_UNSET:kotlin.Int` Route unset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ALWAYS_ASK:kotlin.Int` Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ASK_IF_CONFLICT:kotlin.Int` Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_PREFER_DEFAULT:kotlin.Int` Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#categoryAllowsForegroundPreference(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns whether the user has allowed AIDs registered in the specified category to be handled by a service that is preferred by the foreground application, instead of by a pre-configured default. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getAidsForPreferredPaymentService()()` Retrieves the registered AIDs for the preferred payment service. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getAidsForService(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Retrieves the currently registered AIDs for the specified category for a service. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getDefaultNfcSubscriptionId()()` Returns the system's default NFC subscription id. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getDescriptionForPreferredPaymentService()()` Returns a user-visible description of the preferred payment service. |
| static [CardEmulation](CardEmulation.md)! | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getInstance(android.nfc.NfcAdapter)(adapter: https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.html#!)` Helper to get an instance of this class. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getPollingLoopFiltersForService(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve all the polling loop filters registered for a `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getPollingLoopPatternFiltersForService(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve all the polling loop pattern filters registered for a `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getRouteDestinationForPreferredPaymentService()()` Retrieves the route destination for the preferred payment service. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the service selection mode for the passed in category. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isDefaultServiceForAid(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, aid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allows an application to query whether a service is currently the default handler for a specified ISO7816-4 Application ID. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isDefaultServiceForCategory(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allows an application to query whether a service is currently the default service to handle a card emulation category. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isDeviceScreenOnRequiredForService(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Checks whether the device must have its screen on for the service to be activated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isDeviceUnlockRequiredForService(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Checks whether the device must be unlocked for the service to be activated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isEuiccSupported()()` Is EUICC supported as a Secure Element EE which supports off host card emulation. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerAidsForService(android.content.ComponentName,%20kotlin.String,%20kotlin.collections.MutableList)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, aids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Registers a list of AIDs for a specific category for the specified service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerNfcEventCallback(java.util.concurrent.Executor,%20android.nfc.cardemulation.CardEmulation.NfcEventCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback)` Register a callback for NFC events. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, pollingLoopFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, autoTransact: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Register a polling loop filter (PLF) for a HostApduService and indicate whether it should auto-transact or not. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopPatternFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, pollingLoopPatternFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, autoTransact: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Register a polling loop pattern filter (PLPF) for a HostApduService and indicate whether it should auto-transact or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#removeAidsForService(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes a previously registered list of AIDs for the specified category for the service provided. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#removePollingLoopFilterForService(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, pollingLoopFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Unregister a polling loop filter (PLF) for a HostApduService. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#removePollingLoopPatternFilterForService(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, pollingLoopPatternFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Unregister a polling loop pattern filter (PLPF) for a HostApduService. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setOffHostForService(android.content.ComponentName,%20kotlin.String)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, offHostSecureElement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Sets the off-host Secure Element for the given service. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setPreferredService(android.app.Activity,%20android.content.ComponentName)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Allows a foreground application to specify which card emulation service should be preferred while a specific Activity is in the foreground. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setRequireDeviceScreenOnForService(android.content.ComponentName,%20kotlin.Boolean)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the device must have its screen on for the service to be activated. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setRequireDeviceUnlockForService(android.content.ComponentName,%20kotlin.Boolean)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the device must be unlocked for the service to be activated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setShouldDefaultToObserveModeForService(android.content.ComponentName,%20kotlin.Boolean)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether when this service becomes the preferred service, if the NFC stack should enable observe mode or disable observe mode. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#supportsAidPrefixRegistration()()` Some devices may allow an application to register all AIDs that starts with a certain prefix, e. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#unregisterNfcEventCallback(android.nfc.cardemulation.CardEmulation.NfcEventCallback)(callback: https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation.NfcEventCallback)` Unregister an NFC event callback that was previously registered with `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerNfcEventCallback(java.util.concurrent.Executor,%20android.nfc.cardemulation.CardEmulation.NfcEventCallback)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#unsetOffHostForService(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Unsets the off-host Secure Element for the given service. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#unsetPreferredService(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!)` Unsets the preferred service for the specified Activity. |

## Constants

### ACTION_CHANGE_DEFAULT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANGE_DEFAULT: String
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#createRequestRoleIntent(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String` parameter and `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` instead.*

Activity action: ask the user to change the default card emulation service for a certain category. This will show a dialog that asks the user whether they want to replace the current default service with the service identified with the ComponentName specified in `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#EXTRA_SERVICE_COMPONENT:kotlin.String`, for the category specified in `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#EXTRA_CATEGORY:kotlin.String`. There is an optional extra field using `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` to specify the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the user that owns the app.

 Value: "android.nfc.cardemulation.action.ACTION_CHANGE_DEFAULT"

### CATEGORY_OTHER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_OTHER: String
```

Category that can be used for all other card emulation services.

 Value: "other"

### CATEGORY_PAYMENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_PAYMENT: String
```

Category used for NFC payment services.

 Value: "payment"

### EXTRA_CATEGORY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CATEGORY: String
```

The category extra for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`.

 Value: "category"

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`

### EXTRA_SERVICE_COMPONENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SERVICE_COMPONENT: String
```

The service `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` object passed in as an extra for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`.

 Value: "component"

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#ACTION_CHANGE_DEFAULT:kotlin.String`

### NFC_INTERNAL_ERROR_COMMAND_TIMEOUT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NFC_INTERNAL_ERROR_COMMAND_TIMEOUT: Int
```

This error is reported when the NFC stack times out while waiting for a response to a command sent to the NFC hardware.

 Value: 3

### NFC_INTERNAL_ERROR_NFC_CRASH_RESTART

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NFC_INTERNAL_ERROR_NFC_CRASH_RESTART: Int
```

This error is reported when the NFC command watchdog restarts the NFC stack.

 Value: 1

### NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NFC_INTERNAL_ERROR_NFC_HARDWARE_ERROR: Int
```

This error is reported when the NFC controller does not respond or there's an NCI transport error.

 Value: 2

### NFC_INTERNAL_ERROR_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NFC_INTERNAL_ERROR_UNKNOWN: Int
```

 Value: 0

### PROPERTY_ALLOW_SHARED_ROLE_PRIORITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ALLOW_SHARED_ROLE_PRIORITY: String
```

Property name used to indicate that an application wants to allow associated services to share the same AID routing priority when this application is the role holder. Wallet role holder can either:
- Set "android:value" to "true". This will allow any package signed by the same certificate to request for role holder priority.
- Set "android:value" to some other package name. This will only allow this package to request for role holder priority (can be signed by different certificates).
- Example:

```kotlin
<code>&lt;application&gt;
        ...
        &lt;property android:name="android.nfc.cardemulation.PROPERTY_ALLOW_SHARED_ROLE_PRIORITY"
          android:value="true"/&gt;
      &lt;/application&gt;
      </code>
```

```kotlin
<code>&lt;service&gt;
        ...
        &lt;property android:name="android.nfc.cardemulation.PROPERTY_ALLOW_SHARED_ROLE_PRIORITY"
          android:value="com.org.example"/&gt;
      &lt;/service&gt;
      </code>
```

 Value: "android.nfc.cardemulation.PROPERTY_ALLOW_SHARED_ROLE_PRIORITY"

### PROTOCOL_AND_TECHNOLOGY_ROUTE_DEFAULT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_DEFAULT: Int
```

Route to the default value in config file.

 Value: 3

### PROTOCOL_AND_TECHNOLOGY_ROUTE_DH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_DH: Int
```

Route to Device Host (DH).

 Value: 0

### PROTOCOL_AND_TECHNOLOGY_ROUTE_ESE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_ESE: Int
```

Route to eSE.

 Value: 1

### PROTOCOL_AND_TECHNOLOGY_ROUTE_NDEF_NFCEE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_NDEF_NFCEE: Int
```

Route to T4T NDEF-NCEE emulation.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#`

### PROTOCOL_AND_TECHNOLOGY_ROUTE_UICC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_UICC: Int
```

Route to UICC.

 Value: 2

### PROTOCOL_AND_TECHNOLOGY_ROUTE_UNSET

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROTOCOL_AND_TECHNOLOGY_ROUTE_UNSET: Int
```

Route unset.

 Value: -1

### SELECTION_MODE_ALWAYS_ASK

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SELECTION_MODE_ALWAYS_ASK: Int
```

Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`.

In this mode, when using ISO-DEP card emulation with `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService` or `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/OffHostApduService`, whenever an Application ID (AID) of this category is selected, the user is asked which service they want to use to handle the transaction, even if there is only one matching service.

 Value: 1

### SELECTION_MODE_ASK_IF_CONFLICT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SELECTION_MODE_ASK_IF_CONFLICT: Int
```

Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`.

In this mode, when using ISO-DEP card emulation with `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService` or `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/OffHostApduService`, the user will only be asked to select a service if the Application ID (AID) selected by the reader has been registered by multiple services. If there is only one service that has registered for the AID, that service will be invoked directly.

 Value: 2

### SELECTION_MODE_PREFER_DEFAULT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SELECTION_MODE_PREFER_DEFAULT: Int
```

Return value for `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)`.

In this mode, the user has set a default service for this category.

When using ISO-DEP card emulation with `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService` or `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/OffHostApduService`, if a remote NFC device selects any of the Application IDs (AIDs) that the default service has registered in this category, that service will automatically be bound to to handle the transaction.

 Value: 0

## Public methods

### categoryAllowsForegroundPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun categoryAllowsForegroundPreference(category: String!): Boolean
```

Returns whether the user has allowed AIDs registered in the specified category to be handled by a service that is preferred by the foreground application, instead of by a pre-configured default. Foreground applications can set such preferences using the `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setPreferredService(android.app.Activity,%20android.content.ComponentName)` method.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this method will always return true.

| Parameters ||
|---|---|
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category, e.g. `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether AIDs in the category can be handled by a service specified by the foreground app. |

### getAidsForPreferredPaymentService

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAidsForPreferredPaymentService(): MutableList<String!>?
```

Retrieves the registered AIDs for the preferred payment service. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_PREFERRED_PAYMENT_INFO:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | The list of AIDs registered for this category, or null if it couldn't be found. |

### getAidsForService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAidsForService(
    service: ComponentName!, 
    category: String!
): MutableList<String!>!
```

Retrieves the currently registered AIDs for the specified category for a service.

Note that this will only return AIDs that were dynamically registered using `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerAidsForService(android.content.ComponentName,%20kotlin.String,%20kotlin.collections.MutableList)` method. It will \*not\* return AIDs that were statically registered in the manifest.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md)!: The component name of the service |
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category for which the AIDs were registered, e.g. `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | The list of AIDs registered for this category, or null if it couldn't be found. |

### getDefaultNfcSubscriptionId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefaultNfcSubscriptionId(): Int
```

Returns the system's default NFC subscription id.

For devices with multiple UICC/EUICC that is configured to be NFCEE, this returns the default UICC NFCEE that will handle NFC offhost CE transactions

If the device has no UICC that can serve as NFCEE, this will return `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#INVALID_SUBSCRIPTION_ID:kotlin.Int`.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the default NFC subscription Id if set, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#INVALID_SUBSCRIPTION_ID:kotlin.Int` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getDescriptionForPreferredPaymentService

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescriptionForPreferredPaymentService(): CharSequence?
```

Returns a user-visible description of the preferred payment service.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, the preferred payment service no longer exists and is replaced by `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String`. This will return the description for one of the services registered by the role holder (if any). If there are multiple services registered, it is unspecified which of those will be used to obtain the service description here. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_PREFERRED_PAYMENT_INFO:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the preferred payment service description. This value may be `null`. |

### getInstance

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(adapter: NfcAdapter!): CardEmulation!
```

Helper to get an instance of this class.

| Parameters ||
|---|---|
| `adapter` | [NfcAdapter](../android.nfc/NfcAdapter.md)!: A reference to an NfcAdapter object. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#!` | |

### getPollingLoopFiltersForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPollingLoopFiltersForService(service: ComponentName): MutableList<String!>
```

Retrieve all the polling loop filters registered for a `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService`.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to retrieve the filter for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | List of polling loop filters, will be empty if there are none registered. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the service is not valid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`

### getPollingLoopPatternFiltersForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPollingLoopPatternFiltersForService(service: ComponentName): MutableList<String!>
```

Retrieve all the polling loop pattern filters registered for a `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService`.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to retrieve the filter for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | List of polling loop pattern filters, will be empty if there are none registered. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the service is not valid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopPatternFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)`

### getRouteDestinationForPreferredPaymentService

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRouteDestinationForPreferredPaymentService(): String?
```

Retrieves the route destination for the preferred payment service.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, the preferred payment service no longer exists and is replaced by `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String`. This will return the route for one of the services registered by the role holder (if any). If there are multiple services registered, it is unspecified which of those will be used to determine the route. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_PREFERRED_PAYMENT_INFO:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The route destination secure element name of the preferred payment service. HCE payment: "Host" OffHost payment: 1. String with prefix SIM or prefix eSE string. Ref: GSMA TS.26 - NFC Handset Requirements TS26_NFC_REQ_069: For UICC, Secure Element Name SHALL be SIM\[smartcard slot\] (e.g. SIM/SIM1, SIM2... SIMn). TS26_NFC_REQ_070: For embedded SE, Secure Element Name SHALL be eSE\[number\] (e.g. eSE/eSE1, eSE2, etc.). 2. "OffHost" if the payment service does not specify secure element name. This value may be `null`. |

### getSelectionModeForCategory

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectionModeForCategory(category: String!): Int
```

Returns the service selection mode for the passed in category. Valid return values are:

`https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_PREFER_DEFAULT:kotlin.Int` the user has requested a default service for this category, which will be preferred.

`https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ALWAYS_ASK:kotlin.Int` the user has requested to be asked every time what service they would like to use in this category.

`https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ASK_IF_CONFLICT:kotlin.Int` the user will only be asked to pick a service if there is a conflict.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, the default service defined by the holder of `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String` and is category agnostic.

| Parameters ||
|---|---|
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category, for example `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the selection mode for the passed in category |

### isDefaultServiceForAid

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDefaultServiceForAid(
    service: ComponentName!, 
    aid: String!
): Boolean
```

Allows an application to query whether a service is currently the default handler for a specified ISO7816-4 Application ID.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md)!: The ComponentName of the service |
| `aid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The ISO7816-4 Application ID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the service is the default handler for the specified AID Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission. |

### isDefaultServiceForCategory

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDefaultServiceForCategory(
    service: ComponentName!, 
    category: String!
): Boolean
```

Allows an application to query whether a service is currently the default service to handle a card emulation category.

Note that if `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#getSelectionModeForCategory(kotlin.String)` returns `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ALWAYS_ASK:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ASK_IF_CONFLICT:kotlin.Int`, this method will always return false. That is because in these selection modes a default can't be set at the category level. For categories where the selection mode is `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ALWAYS_ASK:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#SELECTION_MODE_ASK_IF_CONFLICT:kotlin.Int`, use `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#isDefaultServiceForAid(android.content.ComponentName,%20kotlin.String)` to determine whether a service is the default for a specific AID.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md)!: The ComponentName of the service |
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether service is currently the default service for the category. Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission. |

### isDeviceScreenOnRequiredForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDeviceScreenOnRequiredForService(service: ComponentName): Boolean
```

Checks whether the device must have its screen on for the service to be activated.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device must have its screen on for the service to be activated, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided service has not been registered |

### isDeviceUnlockRequiredForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDeviceUnlockRequiredForService(service: ComponentName): Boolean
```

Checks whether the device must be unlocked for the service to be activated.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device must be unlocked for the service to be activated, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided service has not been registered |

### isEuiccSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEuiccSupported(): Boolean
```

Is EUICC supported as a Secure Element EE which supports off host card emulation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the device supports EUICC for off host card emulation, false otherwise. |

### registerAidsForService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAidsForService(
    service: ComponentName!, 
    category: String!, 
    aids: MutableList<String!>!
): Boolean
```

Registers a list of AIDs for a specific category for the specified service.

If a list of AIDs for that category was previously registered for this service (either statically through the manifest, or dynamically by using this API), that list of AIDs will be replaced with this one.

Note that you can only register AIDs for a service that is running under the same UID as the caller of this API. Typically this means you need to call this from the same package as the service itself, though UIDs can also be shared between packages using shared UIDs.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md)!: The component name of the service |
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category of AIDs to be registered |
| `aids` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: A list containing the AIDs to be registered |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the registration was successful. |

### registerNfcEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerNfcEventCallback(
    executor: Executor, 
    callback: CardEmulation.NfcEventCallback
): Unit
```

Register a callback for NFC events.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The Executor to run the call back with. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [CardEmulation.NfcEventCallback](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md): The callback to register. This value cannot be `null`. |

### registerPollingLoopFilterForService

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerPollingLoopFilterForService(
    service: ComponentName, 
    pollingLoopFilter: String, 
    autoTransact: Boolean
): Boolean
```

Register a polling loop filter (PLF) for a HostApduService and indicate whether it should auto-transact or not. The PLF can be sequence of an even number of at least 2 hexadecimal numbers (0-9, A-F or a-f), representing a series of bytes. When non-standard polling loop frame matches this sequence exactly, it may be delivered to `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService#processPollingFrames(kotlin.collections.MutableList)`. If auto-transact is set to true and this service is currently preferred or there are no other services registered for this filter then observe mode will also be disabled.

When auto-transact is set to true, if the filter matches the following requirements, it will be considered to be included in the firmware filtering list (if the device supports exit frames). Filters not matching these requirements will be handled via the NFC stack software auto-transact functionality.

- The filter must not exceed 16 bytes (32 hexadecimal characters).

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to register the filter for. This value cannot be `null`. |
| `pollingLoopFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The filter to register. This value cannot be `null`. |
| `autoTransact` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to have the NFC stack automatically disable observe mode and allow transactions to proceed when this filter matches, false otherwise |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the filter was registered, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the passed in string doesn't parse to at least one byte |

### registerPollingLoopPatternFilterForService

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerPollingLoopPatternFilterForService(
    service: ComponentName, 
    pollingLoopPatternFilter: String, 
    autoTransact: Boolean
): Boolean
```

Register a polling loop pattern filter (PLPF) for a HostApduService and indicate whether it should auto-transact or not. The pattern may include the characters 0-9 and A-F as well as the regular expression operators \`.\`, \`?\` and \`\*\` after the first byte. When the beginning of a non-standard polling loop frame matches this sequence exactly, it may be delivered to `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService#processPollingFrames(kotlin.collections.MutableList)`. If auto-transact is set to true and this service is currently preferred or there are no other services registered for this filter then observe mode will also be disabled.

When auto-transact is set to true, if the pattern matches the following requirements, it will be considered to be included in the firmware filtering list (if the device supports exit frames). Patterns not matching these requirements will be handled via the NFC stack software auto-transact functionality.

- The pattern must not include the \`?\` operator.
- The \`\*\` operator is only supported if it is the only character or if it is preceded by a \`.\` and is at the end of the pattern (e.g. \`.\*\`).
- The pattern must have an even number of characters unless it ends with the \`.\*\` suffix.
- The pattern must not exceed 32 characters (excluding the \`.\*\` suffix).

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to register the filter for. This value cannot be `null`. |
| `pollingLoopPatternFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The pattern filter to register, must to be compatible with `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#compile(kotlin.String)` and only contain hexadecimal numbers and \`.\`, \`?\` and \`\*\` operators. This value cannot be `null`. |
| `autoTransact` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to have the NFC stack automatically disable observe mode and allow transactions to proceed when this filter matches, false otherwise |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the filter was registered, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the filter contains elements other than hexadecimal numbers and \`.\`, \`?\` and \`\*\` operators |
| `java.util.regex.PatternSyntaxException` | if the regex syntax is invalid |

### removeAidsForService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAidsForService(
    service: ComponentName!, 
    category: String!
): Boolean
```

Removes a previously registered list of AIDs for the specified category for the service provided.

Note that this will only remove AIDs that were dynamically registered using the `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerAidsForService(android.content.ComponentName,%20kotlin.String,%20kotlin.collections.MutableList)` method. It will \*not\* remove AIDs that were statically registered in the manifest. If dynamically registered AIDs are removed using this method, and a statically registered AID group for the same category exists in the manifest, the static AID group will become active again.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md)!: The component name of the service |
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category of the AIDs to be removed, e.g. `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the group was successfully removed. |

### removePollingLoopFilterForService

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removePollingLoopFilterForService(
    service: ComponentName, 
    pollingLoopFilter: String
): Boolean
```

Unregister a polling loop filter (PLF) for a HostApduService. If the PLF had previously been registered via `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)` for this service it will be removed.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to unregister the filter for. This value cannot be `null`. |
| `pollingLoopFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The filter to unregister. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the filter was removed, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the passed in string doesn't parse to at least one byte |

### removePollingLoopPatternFilterForService

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removePollingLoopPatternFilterForService(
    service: ComponentName, 
    pollingLoopPatternFilter: String
): Boolean
```

Unregister a polling loop pattern filter (PLPF) for a HostApduService. If the PLF had previously been registered via `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerPollingLoopFilterForService(android.content.ComponentName,%20kotlin.String,%20kotlin.Boolean)` for this service it will be removed.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The HostApduService to unregister the filter for. This value cannot be `null`. |
| `pollingLoopPatternFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The filter to unregister, must to be compatible with `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#compile(kotlin.String)` and only contain hexadecimal numbers and\`.\`, \`?\` and \`\*\` operators. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the filter was removed, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the filter containst elements other than hexadecimal numbers and \`.\`, \`?\` and \`\*\` operators |
| `java.util.regex.PatternSyntaxException` | if the regex syntax is invalid |

### setOffHostForService

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOffHostForService(
    service: ComponentName, 
    offHostSecureElement: String
): Boolean
```

Sets the off-host Secure Element for the given service.

If off-host SE was initially set (either statically through the manifest, or dynamically by using this API), it will be replaced with this one. All AIDs registered by this service will be re-routed to this Secure Element if successful. AIDs that was statically assigned using manifest will re-route to off-host SE that stated in manifest after NFC toggle.

Note that you can only set off-host SE for a service that is running under the same UID as the caller of this API. Typically this means you need to call this from the same package as the service itself, though UIDs can also be shared between packages using shared UIDs.

Registeration will be successful only if the Secure Element exists on the device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String`

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |
| `offHostSecureElement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Secure Element to register the AID to. Only accept strings with prefix SIM or prefix eSE. Ref: GSMA TS.26 - NFC Handset Requirements TS26_NFC_REQ_069: For UICC, Secure Element Name SHALL be SIM\[smartcard slot\] (e.g. SIM/SIM1, SIM2... SIMn). TS26_NFC_REQ_070: For embedded SE, Secure Element Name SHALL be eSE\[number\] (e.g. eSE/eSE1, eSE2, etc.). This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the registration was successful. This value cannot be `null`. |

### setPreferredService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPreferredService(
    activity: Activity!, 
    service: ComponentName!
): Boolean
```

Allows a foreground application to specify which card emulation service should be preferred while a specific Activity is in the foreground.

The specified Activity must currently be in resumed state. A good paradigm is to call this method in your `https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume()`, and to call `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#unsetPreferredService(android.app.Activity)` in your `https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause()`.

This method call will fail in two specific scenarios:

- If the service registers one or more AIDs in the `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_PAYMENT:kotlin.String` category, but the user has indicated that foreground apps are not allowed to override the default payment service.
- If the service registers one or more AIDs in the `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#CATEGORY_OTHER:kotlin.String` category that are also handled by the default payment service, and the user has indicated that foreground apps are not allowed to override the default payment service.

Use `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#categoryAllowsForegroundPreference(kotlin.String)` to determine whether foreground apps can override the default payment service.

Note that this preference is not persisted by the OS, and hence must be called every time the Activity is resumed.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, this method will prefer all services matching the package name of the activity.

| Parameters ||
|---|---|
| `activity` | [Activity](../android.app/Activity.md)!: The activity which prefers this service to be invoked |
| `service` | [ComponentName](../android.content/ComponentName.md)!: The service to be preferred while this activity is in the foreground |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the registration was successful |

### setRequireDeviceScreenOnForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRequireDeviceScreenOnForService(
    service: ComponentName, 
    enable: Boolean
): Unit
```

Sets whether the device must have its screen on for the service to be activated. This API overrides the `android:requireDeviceScreenOn` attribute declared in the service's manifest.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the service should only be activated when the device's screen is on |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided service has not been registered |

### setRequireDeviceUnlockForService

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRequireDeviceUnlockForService(
    service: ComponentName, 
    enable: Boolean
): Unit
```

Sets whether the device must be unlocked for the service to be activated. This API overrides the `android:requireDeviceUnlock` attribute declared in the service's manifest.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the service should only be activated when the device is unlocked |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided service has not been registered |

### setShouldDefaultToObserveModeForService

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setShouldDefaultToObserveModeForService(
    service: ComponentName, 
    enable: Boolean
): Boolean
```

Sets whether when this service becomes the preferred service, if the NFC stack should enable observe mode or disable observe mode. The default is to not enable observe mode when a service either the foreground default service or the default payment service so not calling this method will preserve that behavior.

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the service should default to observe mode or not |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the change was successful. |

### supportsAidPrefixRegistration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun supportsAidPrefixRegistration(): Boolean
```

Some devices may allow an application to register all AIDs that starts with a certain prefix, e.g. "A000000004\*" to register all MasterCard AIDs. Use this method to determine whether this device supports registering AID prefixes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether AID prefix registering is supported on this device. |

### unregisterNfcEventCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterNfcEventCallback(callback: CardEmulation.NfcEventCallback): Unit
```

Unregister an NFC event callback that was previously registered with `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#registerNfcEventCallback(java.util.concurrent.Executor,%20android.nfc.cardemulation.CardEmulation.NfcEventCallback)`.

| Parameters ||
|---|---|
| `callback` | [CardEmulation.NfcEventCallback](../android/nfc/cardemulation/CardEmulation.NfcEventCallback.md): The previously registered callback to unregister. This value cannot be `null`. |

### unsetOffHostForService

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unsetOffHostForService(service: ComponentName): Boolean
```

Unsets the off-host Secure Element for the given service.

Note that this will only remove Secure Element that was dynamically set using the `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setOffHostForService(android.content.ComponentName,%20kotlin.String)` and resets it to a value that was statically assigned using manifest.

Note that you can only unset off-host SE for a service that is running under the same UID as the caller of this API. Typically this means you need to call this from the same package as the service itself, though UIDs can also be shared between packages using shared UIDs. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String`

| Parameters ||
|---|---|
| `service` | [ComponentName](../android.content/ComponentName.md): The component name of the service. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the registration was successful. This value cannot be `null`. |

### unsetPreferredService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unsetPreferredService(activity: Activity!): Boolean
```

Unsets the preferred service for the specified Activity.

Note that the specified Activity must still be in resumed state at the time of this call. A good place to call this method is in your `https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause()` implementation.

| Parameters ||
|---|---|
| `activity` | [Activity](../android.app/Activity.md)!: The activity which the service was registered for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true when successful |
