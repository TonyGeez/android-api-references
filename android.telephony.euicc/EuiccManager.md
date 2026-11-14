Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EuiccManager

Kotlin | [Java](https://developer.android.com/reference/android/telephony/euicc/EuiccManager "View this page in Java")

```
open class EuiccManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.euicc.EuiccManager](https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#) |

EuiccManager is the application interface to eUICCs, or eSIMs/embedded SIMs.

You do not instantiate this class directly; instead, you retrieve an instance through `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#EUICC_SERVICE:kotlin.String`. This instance will be created using the default eUICC.

On a device with multiple eUICCs, you may want to create multiple EuiccManagers. To do this you can call `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#createForCardId(kotlin.Int)`.

See `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isEnabled()` before attempting to use these APIs. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ACTION_MANAGE_EMBEDDED_SUBSCRIPTIONS:kotlin.String` Intent action to launch the embedded SIM (eUICC) management settings screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ACTION_NOTIFY_CARRIER_SETUP_INCOMPLETE:kotlin.String` Broadcast Action: The action sent to carrier app so it knows the carrier setup is not completed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ACTION_START_EUICC_ACTIVATION:kotlin.String` Intent action sent by a carrier app to launch the eSIM activation flow provided by the LPA UI (LUI). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_ERROR:kotlin.Int` Result code for an operation indicating that an unresolvable error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_OK:kotlin.Int` Result code for an operation indicating that the operation succeeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` Result code for an operation indicating that the user must take some action before the operation can continue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_ADDRESS_MISSING:kotlin.Int` Address is missing e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_CARRIER_LOCKED:kotlin.Int` Operation such as downloading/switching to another profile failed due to device being carrier locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_CERTIFICATE_ERROR:kotlin.Int` Certificate needed for authentication is not valid or missing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_CONNECTION_ERROR:kotlin.Int` Failure to create a connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_DISALLOWED_BY_PPR:kotlin.Int` Failed to load profile onto eUICC due to Profile Policy Rules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_EUICC_INSUFFICIENT_MEMORY:kotlin.Int` There is no more space available on the eUICC for new profiles. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_EUICC_MISSING:kotlin.Int` eUICC is missing or defective on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INCOMPATIBLE_CARRIER:kotlin.Int` The profile's carrier is incompatible with the LPA. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INSTALL_PROFILE:kotlin.Int` Failure to load the profile onto the eUICC card. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INVALID_ACTIVATION_CODE:kotlin.Int` The activation code(SGP.22 v2.2 section\[4.1\]) is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INVALID_CONFIRMATION_CODE:kotlin.Int` The confirmation code(SGP.22 v2.2 section\[4.7\]) is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INVALID_PORT:kotlin.Int` Failure due to target port is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INVALID_RESPONSE:kotlin.Int` Response format is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_NO_PROFILES_AVAILABLE:kotlin.Int` No profiles available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_OPERATION_BUSY:kotlin.Int` The operation is currently busy, try again later. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_SIM_MISSING:kotlin.Int` No SIM card is available in the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_TIME_OUT:kotlin.Int` Timed out while waiting for an operation to complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_UNSUPPORTED_VERSION:kotlin.Int` The eUICC card(hardware) version is incompatible with the software |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EUICC_MEMORY_FIELD_UNAVAILABLE:kotlin.Long` Temporary failure to retrieve available memory because eUICC is not ready. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String` Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a detailed result code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DOWNLOADABLE_SUBSCRIPTION:kotlin.String` Key for an extra set on `getDownloadableSubscriptionMetadata` PendingIntent result callbacks providing the downloadable subscription metadata. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_ERROR_CODE:kotlin.String` Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a ErrorCode of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`, value will be an int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_OPERATION_CODE:kotlin.String` Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a OperationCode of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`, value will be an int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE:kotlin.String` Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a ReasonCode\[5. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE:kotlin.String` Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a SubjectCode\[5. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_USE_QR_SCANNER:kotlin.String` Key for an extra set on actions `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ACTION_START_EUICC_ACTIVATION:kotlin.String` providing a boolean value of whether to start eSIM activation with QR scanner. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#META_DATA_CARRIER_ICON:kotlin.String` Optional meta-data attribute for a carrier app providing an icon to use to represent the carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_APDU:kotlin.Int` The exception of failing to execute an APDU command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_DOWNLOAD:kotlin.Int` Download profile error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_EUICC_CARD:kotlin.Int` eUICC card error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_EUICC_GSMA:kotlin.Int` eUICC returned an error defined in GSMA (SGP.22 v2.2) while running one of the ES10x functions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_HTTP:kotlin.Int` HTTP error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_METADATA:kotlin.Int` Subscription's metadata error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SIM_SLOT:kotlin.Int` SIM slot error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SMDX:kotlin.Int` SMDX(SMDP/SMDS) error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SMDX_SUBJECT_REASON_CODE:kotlin.Int` SubjectCode\[5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SWITCH:kotlin.Int` Generic switching profile error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SYSTEM:kotlin.Int` Internal system error. |

| Public methods ||
|---|---|
| open [EuiccManager](https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#createForCardId(kotlin.Int)(cardId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new EuiccManager object pinned to the given card ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#deleteSubscription(kotlin.Int,%20android.app.PendingIntent)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!)` Deletes the given subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#downloadSubscription(android.telephony.euicc.DownloadableSubscription,%20kotlin.Boolean,%20android.app.PendingIntent)(subscription: https://developer.android.com/reference/kotlin/android/telephony/euicc/DownloadableSubscription!, switchAfterDownload: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!)` Attempt to download the given `https://developer.android.com/reference/kotlin/android/telephony/euicc/DownloadableSubscription`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#getAvailableMemoryInBytes()()` Returns the available memory in bytes of the eUICC. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#getEid()()` Returns the EID identifying the eUICC hardware. |
| open [EuiccInfo](https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccInfo)? | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#getEuiccInfo()()` Returns information about the eUICC chip/device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isEnabled()()` Whether embedded subscriptions are currently enabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isSimPortAvailable(kotlin.Int)(portIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the passing portIndex is available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#startResolutionActivity(android.app.Activity,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!)` Start an activity to resolve a user-resolvable error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20android.app.PendingIntent)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!)` Switch to (enable) the given subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, portIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Switch to (enable) the given subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#updateSubscriptionNickname(kotlin.Int,%20kotlin.String,%20android.app.PendingIntent)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, nickname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Update the nickname for the given subscription. |

## Constants

### ACTION_MANAGE_EMBEDDED_SUBSCRIPTIONS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_EMBEDDED_SUBSCRIPTIONS: String
```

Intent action to launch the embedded SIM (eUICC) management settings screen.

This screen shows a list of embedded profiles and offers the user the ability to switch between them, download new profiles, and delete unused profiles.

The activity will immediately finish with `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isEnabled()` is false. This is ued by non-LPA app to bring up LUI.

 Value: "android.telephony.euicc.action.MANAGE_EMBEDDED_SUBSCRIPTIONS"

### ACTION_NOTIFY_CARRIER_SETUP_INCOMPLETE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFY_CARRIER_SETUP_INCOMPLETE: String
```

Broadcast Action: The action sent to carrier app so it knows the carrier setup is not completed.

 Value: "android.telephony.euicc.action.NOTIFY_CARRIER_SETUP_INCOMPLETE"

### ACTION_START_EUICC_ACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_START_EUICC_ACTIVATION: String
```

Intent action sent by a carrier app to launch the eSIM activation flow provided by the LPA UI (LUI). The carrier app must send this intent with one of the following:

`https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_USE_QR_SCANNER:kotlin.String` not set or set to false: The LPA should try to get an activation code from the carrier app by binding to the carrier app service implementing `android.service.euicc.EuiccService#ACTION_BIND_CARRIER_PROVISIONING_SERVICE`.

`https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_USE_QR_SCANNER:kotlin.String` set to true: The LPA should launch a QR scanner for the user to scan an eSIM profile QR code.

Upon completion, the LPA should return one of the following results to the carrier app:

`Activity.RESULT_OK`: The LPA has succeeded in downloading the new eSIM profile.

`Activity.RESULT_CANCELED`: The carrier app should treat this as if the user pressed the back button.

Anything else: The carrier app should treat this as an error.

LPA needs to check if caller's package name is allowed to perform this action.

 Value: "android.telephony.euicc.action.START_EUICC_ACTIVATION"

### EMBEDDED_SUBSCRIPTION_RESULT_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMBEDDED_SUBSCRIPTION_RESULT_ERROR: Int
```

Result code for an operation indicating that an unresolvable error occurred. `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String` will be populated with a detailed error code for logging/debugging purposes only.

 Value: 2

### EMBEDDED_SUBSCRIPTION_RESULT_OK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMBEDDED_SUBSCRIPTION_RESULT_OK: Int
```

Result code for an operation indicating that the operation succeeded.

 Value: 0

### EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR: Int
```

Result code for an operation indicating that the user must take some action before the operation can continue.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#startResolutionActivity(android.app.Activity,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent)`

### ERROR_ADDRESS_MISSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_ADDRESS_MISSING: Int
```

Address is missing e.g SMDS/SMDP address is missing.

 Value: 10011

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_CARRIER_LOCKED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CARRIER_LOCKED: Int
```

Operation such as downloading/switching to another profile failed due to device being carrier locked.

 Value: 10000

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_CERTIFICATE_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CERTIFICATE_ERROR: Int
```

Certificate needed for authentication is not valid or missing. E.g SMDP/SMDS authentication failed.

 Value: 10012

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_CONNECTION_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CONNECTION_ERROR: Int
```

Failure to create a connection.

 Value: 10014

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_DISALLOWED_BY_PPR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DISALLOWED_BY_PPR: Int
```

Failed to load profile onto eUICC due to Profile Policy Rules.

 Value: 10010

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_EUICC_INSUFFICIENT_MEMORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_EUICC_INSUFFICIENT_MEMORY: Int
```

There is no more space available on the eUICC for new profiles.

 Value: 10004

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_EUICC_MISSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_EUICC_MISSING: Int
```

eUICC is missing or defective on the device.

 Value: 10006

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_INCOMPATIBLE_CARRIER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INCOMPATIBLE_CARRIER: Int
```

The profile's carrier is incompatible with the LPA.

 Value: 10003

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_INSTALL_PROFILE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INSTALL_PROFILE: Int
```

Failure to load the profile onto the eUICC card. e.g 1. iccid of the profile already exists on the eUICC. 2. GSMA(.22 v2.2) Profile Install Result - installFailedDueToDataMismatch 3. operation was interrupted 4. SIMalliance error in PEStatus(SGP.22 v2.2 section 2.5.6.1)

 Value: 10009

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_INVALID_ACTIVATION_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_ACTIVATION_CODE: Int
```

The activation code(SGP.22 v2.2 section\[4.1\]) is invalid.

 Value: 10001

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_INVALID_CONFIRMATION_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_CONFIRMATION_CODE: Int
```

The confirmation code(SGP.22 v2.2 section\[4.7\]) is invalid.

 Value: 10002

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_INVALID_PORT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_PORT: Int
```

Failure due to target port is not supported.

 Value: 10017

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)`

### ERROR_INVALID_RESPONSE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_RESPONSE: Int
```

Response format is invalid. e.g SMDP/SMDS response contains invalid json, header or/and ASN1.

 Value: 10015

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_NO_PROFILES_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NO_PROFILES_AVAILABLE: Int
```

No profiles available.

 Value: 10013

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_OPERATION_BUSY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_OPERATION_BUSY: Int
```

The operation is currently busy, try again later.

 Value: 10016

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_SIM_MISSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SIM_MISSING: Int
```

No SIM card is available in the device.

 Value: 10008

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_TIME_OUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TIME_OUT: Int
```

Timed out while waiting for an operation to complete. i.e restart, disable, switch reset etc.

 Value: 10005

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### ERROR_UNSUPPORTED_VERSION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNSUPPORTED_VERSION: Int
```

The eUICC card(hardware) version is incompatible with the software

 Value: 10007

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### EUICC_MEMORY_FIELD_UNAVAILABLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EUICC_MEMORY_FIELD_UNAVAILABLE: Long
```

Temporary failure to retrieve available memory because eUICC is not ready.

 Value: -1L

### EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE: String
```

Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a detailed result code.

The value of this key is an integer and contains two portions. The first byte is OperationCode and the reaming three bytes is the ErrorCode. OperationCode is the first byte of the result code and is a categorization which defines what type of operation took place when an error occurred. e.g `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_DOWNLOAD:kotlin.Int` means the error is related to download.Since the OperationCode only uses at most one byte, the maximum allowed quantity is 255(0xFF). ErrorCode is the remaining three bytes of the result code, and it denotes what happened. e.g a combination of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_DOWNLOAD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_TIME_OUT:kotlin.Int` will suggest the download operation has timed out. The only exception here is `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SMDX_SUBJECT_REASON_CODE:kotlin.Int`, where instead of ErrorCode, SubjectCode\[5.2.6.1 from GSMA (SGP.22 v2.2) and ReasonCode\[5.2.6.2\] from GSMA (SGP.22 v2.2) are encoded. @see `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE:kotlin.String` In the case where ErrorCode contains a value of 0, it means it's an unknown error. E.g Intent only contains `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_DOWNLOAD:kotlin.Int` and ErrorCode is 0 implies this is an unknown Download error.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_DETAILED_CODE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_OPERATION_CODE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_ERROR_CODE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE:kotlin.String`

### EXTRA_EMBEDDED_SUBSCRIPTION_DOWNLOADABLE_SUBSCRIPTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_DOWNLOADABLE_SUBSCRIPTION: String
```

Key for an extra set on `getDownloadableSubscriptionMetadata` PendingIntent result callbacks providing the downloadable subscription metadata.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_DOWNLOADABLE_SUBSCRIPTION"

### EXTRA_EMBEDDED_SUBSCRIPTION_ERROR_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_ERROR_CODE: String
```

Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a ErrorCode of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`, value will be an int.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_ERROR_CODE"

### EXTRA_EMBEDDED_SUBSCRIPTION_OPERATION_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_OPERATION_CODE: String
```

Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a OperationCode of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`, value will be an int.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_OPERATION_CODE"

### EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE: String
```

Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a ReasonCode\[5.2.6.2\] from GSMA (SGP.22 v2.2) decoded from `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`. The value of this extra will be a String.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_SMDX_REASON_CODE"

### EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE: String
```

Key for an extra set on `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` result callbacks providing a SubjectCode\[5.2.6.1\] from GSMA (SGP.22 v2.2) decoded from `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`. The value of this extra will be a String.

 Value: "android.telephony.euicc.extra.EMBEDDED_SUBSCRIPTION_SMDX_SUBJECT_CODE"

### EXTRA_USE_QR_SCANNER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_USE_QR_SCANNER: String
```

Key for an extra set on actions `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ACTION_START_EUICC_ACTIVATION:kotlin.String` providing a boolean value of whether to start eSIM activation with QR scanner.

Expected type of the extra data: boolean

 Value: "android.telephony.euicc.extra.USE_QR_SCANNER"

### META_DATA_CARRIER_ICON

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_CARRIER_ICON: String
```

Optional meta-data attribute for a carrier app providing an icon to use to represent the carrier. If not provided, the app's launcher icon will be used as a fallback.

 Value: "android.telephony.euicc.carriericon"

### OPERATION_APDU

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_APDU: Int
```

The exception of failing to execute an APDU command. It can be caused by an error happening on opening the basic or logical channel, or the response of the APDU command is not success (0x9000).

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_DOWNLOAD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_DOWNLOAD: Int
```

Download profile error.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_EUICC_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_EUICC_CARD: Int
```

eUICC card error.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_EUICC_GSMA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_EUICC_GSMA: Int
```

eUICC returned an error defined in GSMA (SGP.22 v2.2) while running one of the ES10x functions.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_HTTP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_HTTP: Int
```

HTTP error

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_METADATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_METADATA: Int
```

Subscription's metadata error

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_SIM_SLOT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_SIM_SLOT: Int
```

SIM slot error. Failed to switch slot, failed to access the physical slot etc.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_SMDX

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_SMDX: Int
```

SMDX(SMDP/SMDS) error

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_SMDX_SUBJECT_REASON_CODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_SMDX_SUBJECT_REASON_CODE: Int
```

SubjectCode\[5.2.6.1\] and ReasonCode\[5.2.6.2\] error from GSMA (SGP.22 v2.2) When `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#OPERATION_SMDX_SUBJECT_REASON_CODE:kotlin.Int` is used as the `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`, the remaining three bytes of the integer result from `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String` will be used to stored the SubjectCode and ReasonCode from the GSMA spec and NOT ErrorCode. The encoding will follow the format of: 1. The first byte of the result will be 255(0xFF). 2. Remaining three bytes(24 bits) will be split into six sections, 4 bits in each section. 3. A SubjectCode/ReasonCode will take 12 bits each. 4. The maximum number can be represented per section is 15, as that is the maximum number allowed to be stored into 4 bits 5. Maximum supported nested category from GSMA is three layers. E.g 8.11.1.2 is not supported. E.g given SubjectCode(8.11.1) and ReasonCode(5.1) Base10: 0 10 8 11 1 0 5 1 Base2: 0000 1010 1000 1011 0001 0000 0101 0001 Base16: 0 A 8 B 1 0 5 1 Thus the integer stored in `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String` is 0xA8B1051(176885841)

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_SWITCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_SWITCH: Int
```

Generic switching profile error

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

### OPERATION_SYSTEM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPERATION_SYSTEM: Int
```

Internal system error.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EXTRA_EMBEDDED_SUBSCRIPTION_DETAILED_CODE:kotlin.String`

## Public methods

### createForCardId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createForCardId(cardId: Int): EuiccManager
```

Create a new EuiccManager object pinned to the given card ID.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#` | an EuiccManager that uses the given card ID for all calls. This value cannot be `null`. |

### deleteSubscription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteSubscription(
    subscriptionId: Int, 
    callbackIntent: PendingIntent!
): Unit
```

Deletes the given subscription.

If this subscription is currently active, the device will first switch away from it onto an "empty" subscription.

Requires that the calling app has carrier privileges according to the metadata of the profile to be deleted, or the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission. Starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, if the caller is a device owner, profile owner, or holds the `android.Manifest.permission#MANAGE_DEVICE_POLICY_MANAGED_SUBSCRIPTIONS` permission, then the caller can delete a subscription that was downloaded by that caller. If such a caller tries to delete any other subscription then the operation will fail with `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_ERROR:kotlin.Int`. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MANAGED_SUBSCRIPTIONS:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the subscription to delete. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: a PendingIntent to launch when the operation completes. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### downloadSubscription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun downloadSubscription(
    subscription: DownloadableSubscription!, 
    switchAfterDownload: Boolean, 
    callbackIntent: PendingIntent!
): Unit
```

Attempt to download the given `https://developer.android.com/reference/kotlin/android/telephony/euicc/DownloadableSubscription`.

Requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` or the calling app must be authorized to manage both the currently-active subscription on the current eUICC and the subscription to be downloaded according to the subscription metadata. Without the former, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to accept the download.

Starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, if the caller has the `android.Manifest.permission#MANAGE_DEVICE_POLICY_MANAGED_SUBSCRIPTIONS` permission or is a profile owner or device owner, then the downloaded subscription will be managed by that caller. In case the caller is device owner or profile owner of an organization-owned device, `switchAfterDownload` can be set to true to automatically enable the subscription after download. If the caller is a profile owner on non organization owned device `switchAfterDownload` should be false otherwise the operation will fail with `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_ERROR:kotlin.Int`.

On a multi-active SIM device, requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or a calling app only if the targeted eUICC does not currently have an active subscription or the calling app is authorized to manage the active subscription on the target eUICC, and the calling app is authorized to manage any active subscription on any SIM. Without it, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to accept the download. The caller should also be authorized to manage the subscription to be downloaded.

If device support `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String` and switchAfterDownload is `true`, the subscription will be enabled on an esim port based on the following selection rules:

- In SS(Single SIM) mode, if the embedded slot already has an active port, then download and enable the subscription on this port.
- In SS mode, if the embedded slot is not active, then try to download and enable the subscription on the default port 0 of eUICC.
- In DSDS mode, find first available port to download and enable the subscription. (see `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isSimPortAvailable(kotlin.Int)`)

If there is no available port, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to disable an already-active subscription. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_POLICY_MANAGED_SUBSCRIPTIONS:kotlin.String`

| Parameters ||
|---|---|
| `subscription` | [DownloadableSubscription](https://developer.android.com/reference/kotlin/android/telephony/euicc/DownloadableSubscription)!: the subscription to download. |
| `switchAfterDownload` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, the profile will be activated upon successful download. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: a PendingIntent to launch when the operation completes. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### getAvailableMemoryInBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAvailableMemoryInBytes(): Long
```

Returns the available memory in bytes of the eUICC. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the available memory in bytes. May be `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EUICC_MEMORY_FIELD_UNAVAILABLE:kotlin.Long` if the eUICC is not ready. Check `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isEnabled()` for more information. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` or device doesn't support querying this information from the eUICC. |

### getEid

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEid(): String?
```

Returns the EID identifying the eUICC hardware.

Requires that the calling app has carrier privileges on the active subscription on the current eUICC. A calling app with carrier privileges for one eUICC may not necessarily have access to the EID of another eUICC.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the EID. May be null if the eUICC is not ready. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### getEuiccInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEuiccInfo(): EuiccInfo?
```

Returns information about the eUICC chip/device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccInfo?` | the `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccInfo`. May be null if the eUICC is not ready. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### isEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Whether embedded subscriptions are currently enabled.

Even on devices with the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` feature, embedded subscriptions may be turned off, e.g. because of a carrier restriction from an inserted physical SIM. Therefore, this runtime check should be used before accessing embedded subscription APIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if embedded subscriptions are currently enabled. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### isSimPortAvailable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSimPortAvailable(portIndex: Int): Boolean
```

Returns whether the passing portIndex is available. A port is available if it is active without enabled profile on it or calling app has carrier privilege over the profile installed on the selected port.

From Android U, a port is available if it is active without an enabled profile on it or calling app can activate a new profile on the selected port without any user interaction. Always returns false if the cardId is a physical card.

| Parameters ||
|---|---|
| `portIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): is an enumeration of the ports available on the UICC. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if port is available |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### startResolutionActivity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startResolutionActivity(
    activity: Activity!, 
    requestCode: Int, 
    resultIntent: Intent!, 
    callbackIntent: PendingIntent!
): Unit
```

Start an activity to resolve a user-resolvable error.

If an operation returns `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int`, this method may be called to prompt the user to resolve the issue.

This method may only be called once for a particular error.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: the calling activity (which should be in the foreground). |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an application-specific request code which will be provided to android.app.Activity#onActivityResult upon completion. Note that the operation may still be in progress when the resolution activity completes; it is not fully finished until the callback intent is triggered. |
| `resultIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!: the Intent provided to the initial callback intent which failed with `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int`. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: a PendingIntent to launch when the operation completes. This is trigered upon completion of the original operation that required user resolution. |

| Exceptions ||
|---|---|
| `android.content.IntentSender.SendIntentException` | if called more than once. |

### switchToSubscription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchToSubscription(
    subscriptionId: Int, 
    callbackIntent: PendingIntent!
): Unit
```

Switch to (enable) the given subscription.

Requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or the calling app must be authorized to manage both the currently-active subscription and the subscription to be enabled according to the subscription metadata. Without the former, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to accept the download.

On a multi-active SIM device, requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or a calling app only if the targeted eUICC does not currently have an active subscription or the calling app is authorized to manage the active subscription on the target eUICC, and the calling app is authorized to manage any active subscription on any SIM. Without it, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to accept the download. The caller should also be authorized to manage the subscription to be enabled.

From Android T, devices might support `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String`, the subscription can be installed on different port from the eUICC. Calling apps with carrier privilege (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`) over the currently active subscriptions can use `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)` to specify which port to enable the subscription. Otherwise, use this API to enable the subscription on the eUICC and the platform will internally resolve a port based on following rules:

- always use the default port 0 is eUICC does not support MEP or the apps are not targeting on Android T.
- In SS(Single SIM) mode, if the embedded slot already has an active port, then enable the subscription on this port.
- In SS mode, if the embedded slot is not active, then try to enable the subscription on the default port 0 of eUICC.
- In DSDS mode, find first available port to enable the subscription. (see `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#isSimPortAvailable(kotlin.Int)`)

If there is no available port, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` will be returned in the callback intent to prompt the user to disable an already-active subscription. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the subscription to enable. May be `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#INVALID_SUBSCRIPTION_ID:kotlin.Int` to deactivate the current profile without activating another profile to replace it. Calling apps targeting on android T must use `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)` API for disable profile, port index can be found from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo.html#getPortIndex()`. If it's a disable operation, requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or the calling app must be authorized to manage the active subscription on the target eUICC. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: a PendingIntent to launch when the operation completes. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### switchToSubscription

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchToSubscription(
    subscriptionId: Int, 
    portIndex: Int, 
    callbackIntent: PendingIntent
): Unit
```

Switch to (enable) the given subscription.

Requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or the caller must be having both the carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`) over any currently active subscriptions and the subscription to be enabled according to the subscription metadata. Without the former permissions, an SecurityException is thrown.

If the caller is passing invalid port index, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_ERROR:kotlin.Int` with detailed error code `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#ERROR_INVALID_PORT:kotlin.Int` will be returned. The port index is invalid if one of the following requirements is met:

- index is beyond the range of `https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo.html#getPorts()`.
- In SS(Single SIM) mode, the embedded slot already has an active port with different port index.
- In DSDS mode, if the psim slot is active and the embedded slot already has an active empty port with different port index.

Depending on the target port and permission check, an `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#EMBEDDED_SUBSCRIPTION_RESULT_RESOLVABLE_ERROR:kotlin.Int` might be returned to the callback intent to prompt the user to authorize before the switch. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the subscription to enable. May be `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#INVALID_SUBSCRIPTION_ID:kotlin.Int` to deactivate the current profile without activating another profile to replace it. If it's a disable operation, requires the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission, or the calling app must be authorized to manage the active subscription on the target eUICC. From Android T, multiple enabled profiles is supported. Calling apps targeting on android T must use `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)` API for disable profile, port index can be found from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo.html#getPortIndex()`. |
| `portIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the port to target for the enabled subscription |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#): a PendingIntent to launch when the operation completes. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### updateSubscriptionNickname

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateSubscriptionNickname(
    subscriptionId: Int, 
    nickname: String?, 
    callbackIntent: PendingIntent
): Unit
```

Update the nickname for the given subscription.

Requires that the calling app has carrier privileges according to the metadata of the profile to be updated, or the `android.Manifest.permission#WRITE_EMBEDDED_SUBSCRIPTIONS` permission. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the subscription to update. |
| `nickname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the new nickname to apply. This value may be `null`. |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#): a PendingIntent to launch when the operation completes. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |
