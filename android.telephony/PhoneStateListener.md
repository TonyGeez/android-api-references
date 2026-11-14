# PhoneStateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneStateListener

Kotlin| [Java](PhoneStateListener.md) 
| --- | --- |

```
open class PhoneStateListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.PhoneStateListener](PhoneStateListener.md) |

| **This class was deprecated in API level 31.**
|
| Use [TelephonyCallback](TelephonyCallback.md) instead.

A listener class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others.

Override the methods for the state that you wish to receive updates for, and pass your PhoneStateListener object, along with bitwise-or of the LISTEN_ flags to [TelephonyManager.listen()](TelephonyManager.md)). Methods are called when the state changes, as well as once on initial registration.

Note that access to some telephony information is permission-protected. Your application won't receive updates for protected information unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the appropriate LISTEN_ flags.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE](PhoneStateListener.md) Listen for changes to active data subId. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_BARRING_INFO](PhoneStateListener.md) Listen for Barring Information for the current registered / camped cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_DISCONNECT_CAUSES](PhoneStateListener.md) Listen for call disconnect causes which contains [DisconnectCause](DisconnectCause.md) and the precise disconnect cause. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_FORWARDING_INDICATOR](PhoneStateListener.md) Listen for changes to the call-forwarding indicator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_STATE](PhoneStateListener.md) Listen for changes to the device call state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CELL_INFO](PhoneStateListener.md) Listen for changes to observed cell info. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CELL_LOCATION](PhoneStateListener.md) Listen for changes to the device's cell location. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DATA_ACTIVITY](PhoneStateListener.md) Listen for changes to the direction of data traffic on the data connection (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DATA_CONNECTION_STATE](PhoneStateListener.md) Listen for changes to the data connection state (cellular). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DISPLAY_INFO_CHANGED](PhoneStateListener.md) Listen for display info changed event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_EMERGENCY_NUMBER_LIST](PhoneStateListener.md) Listen for changes to emergency number list based on all active subscriptions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_IMS_CALL_DISCONNECT_CAUSES](PhoneStateListener.md) Listen for IMS call disconnect causes which contains [android.telephony.ims.ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_MESSAGE_WAITING_INDICATOR](PhoneStateListener.md) Listen for changes to the message-waiting indicator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_NONE](PhoneStateListener.md) Stop listening for updates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_PRECISE_DATA_CONNECTION_STATE](PhoneStateListener.md) Listen for [PreciseDataConnectionState](PreciseDataConnectionState.md) on the data connection (cellular). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_REGISTRATION_FAILURE](PhoneStateListener.md) Listen for Registration Failures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SERVICE_STATE](PhoneStateListener.md) Listen for changes to the network service state (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SIGNAL_STRENGTH](PhoneStateListener.md) Listen for changes to the network signal strength (cellular). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SIGNAL_STRENGTHS](PhoneStateListener.md) Listen for changes to the network signal strengths (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_USER_MOBILE_DATA_STATE](PhoneStateListener.md) Listen for changes to the user mobile data state |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PhoneStateListener](PhoneStateListener.md))`()` Create a PhoneStateListener for the Phone with the default subscription. |
| [PhoneStateListener](PhoneStateListener.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`)` Create a PhoneStateListener for the Phone using the specified Executor |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActiveDataSubscriptionIdChanged](PhoneStateListener.md))`(`subId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when active data subId changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBarringInfoChanged](PhoneStateListener.md))`(`barringInfo:` ` [BarringInfo](BarringInfo.md)`)` Report updated barring information for the current camped/registered cell. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallDisconnectCauseChanged](PhoneStateListener.md))`(`disconnectCause:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preciseDisconnectCause:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when call disconnect cause changes on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallForwardingIndicatorChanged](PhoneStateListener.md))`(`cfi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the call-forwarding indicator changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallStateChanged](PhoneStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Callback invoked when device call state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellInfoChanged](PhoneStateListener.md))`(`cellInfo:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CellInfo](CellInfo.md)!>!`)` Callback invoked when a observed cell info has changed or new cells have been added or removed on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellLocationChanged](PhoneStateListener.md))`(`location:` ` [CellLocation](CellLocation.md)!`)` Callback invoked when device cell location changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataActivity](PhoneStateListener.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when data activity state changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataConnectionStateChanged](PhoneStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when connection state changes on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataConnectionStateChanged](PhoneStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` same as above, but with the network type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayInfoChanged](PhoneStateListener.md))`(`telephonyDisplayInfo:` ` [TelephonyDisplayInfo](TelephonyDisplayInfo.md)`)` Callback invoked when the display info has changed on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEmergencyNumberListChanged](PhoneStateListener.md))`(`emergencyNumberList:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EmergencyNumber](../android.telephony.emergency/EmergencyNumber.md)!>!>`)` Callback invoked when the current emergency number list has changed on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImsCallDisconnectCauseChanged](PhoneStateListener.md))`(`imsReasonInfo:` ` [ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md)`)` Callback invoked when Ims call disconnect cause changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageWaitingIndicatorChanged](PhoneStateListener.md))`(`mwi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the message-waiting indicator changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreciseDataConnectionStateChanged](PhoneStateListener.md))`(`dataConnectionState:` ` [PreciseDataConnectionState](PreciseDataConnectionState.md)`)` Callback providing update about the default/internet data connection on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](PhoneStateListener.md))`(`cellIdentity:` ` [CellIdentity](CellIdentity.md)`, `chosenPlmn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `domain:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `causeCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCauseCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Report that Registration or a Location/Routing/Tracking Area update has failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceStateChanged](PhoneStateListener.md))`(`serviceState:` ` [ServiceState](ServiceState.md)!`)` Callback invoked when device service state changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthChanged](PhoneStateListener.md))`(`asu:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when network signal strength changes on the registered subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthsChanged](PhoneStateListener.md))`(`signalStrength:` ` [SignalStrength](SignalStrength.md)!`)` Callback invoked when network signal strengths changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserMobileDataStateChanged](PhoneStateListener.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the user mobile data state has changed on the registered subscription. |

## Constants

### LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE: Int
```

**Deprecated:** *Use [TelephonyCallback.ActiveDataSubscriptionIdListener](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) instead.*

Listen for changes to active data subId. Active data subscription is the current subscription used to setup Cellular Internet data. For example, it could be the current active opportunistic subscription in use, or the subscription user selected as default data subscription in DSDS mode. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 4194304

**See Also**

- [#onActiveDataSubscriptionIdChanged](PhoneStateListener.md)) 

### LISTEN_BARRING_INFO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_BARRING_INFO: Int
```

**Deprecated:** *Use [TelephonyCallback.BarringInfoListener](../android/telephony/TelephonyCallback.BarringInfoListener.md) instead.*

Listen for Barring Information for the current registered / camped cell.

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))).

Also requires the [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission, regardless of whether the calling app has carrier privileges. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 

 Value: -2147483648

**See Also**

- [#onBarringInfoChanged](PhoneStateListener.md)) 

### LISTEN_CALL_DISCONNECT_CAUSES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_DISCONNECT_CAUSES: Int
```

**Deprecated:** *Use [TelephonyCallback.CallDisconnectCauseListener](../android/telephony/TelephonyCallback.CallDisconnectCauseListener.md) instead.*

Listen for call disconnect causes which contains [DisconnectCause](DisconnectCause.md) and the precise disconnect cause.

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 33554432

### LISTEN_CALL_FORWARDING_INDICATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_FORWARDING_INDICATOR: Int
```

**Deprecated:** *Use [TelephonyCallback.CallForwardingIndicatorListener](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) instead.*

Listen for changes to the call-forwarding indicator. {@more} Requires Permission: [READ_PHONE_STATE](../android/Manifest.permission.md) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 8

**See Also**

- [#onCallForwardingIndicatorChanged](PhoneStateListener.md)) 

### LISTEN_CALL_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.CallStateListener](../android/telephony/TelephonyCallback.CallStateListener.md) instead.*

Listen for changes to the device call state. {@more} 

 Value: 32

**See Also**

- [#onCallStateChanged](PhoneStateListener.md)) 

### LISTEN_CELL_INFO

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CELL_INFO: Int
```

**Deprecated:** *Use [TelephonyCallback.CellInfoListener](../android/telephony/TelephonyCallback.CellInfoListener.md) instead.*

Listen for changes to observed cell info. Listening to this event requires the [Manifest.permission.READ_PHONE_STATE](../android/Manifest.permission.md) and [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 

 Value: 1024

**See Also**

- [#onCellInfoChanged](PhoneStateListener.md)) 

### LISTEN_CELL_LOCATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CELL_LOCATION: Int
```

**Deprecated:** *Use [TelephonyCallback.CellLocationListener](../android/telephony/TelephonyCallback.CellLocationListener.md) instead.*

Listen for changes to the device's cell location. Note that this will result in frequent callbacks to the listener. {@more} Requires Permission: [ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

If you need regular location updates but want more control over the update interval or location precision, you can set up a listener through the [location manager](../android.location/LocationManager.md) instead. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 

 Value: 16

**See Also**

- [#onCellLocationChanged](PhoneStateListener.md)) 

### LISTEN_DATA_ACTIVITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DATA_ACTIVITY: Int
```

**Deprecated:** *Use [TelephonyCallback.DataActivityListener](../android/telephony/TelephonyCallback.DataActivityListener.md) instead.*

Listen for changes to the direction of data traffic on the data connection (cellular). {@more} Example: The status bar uses this to display the appropriate data-traffic icon. 

 Value: 128

**See Also**

- [#onDataActivity](PhoneStateListener.md)) 

### LISTEN_DATA_CONNECTION_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DATA_CONNECTION_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) instead.*

Listen for changes to the data connection state (cellular). 

 Value: 64

**See Also**

### LISTEN_DISPLAY_INFO_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DISPLAY_INFO_CHANGED: Int
```

**Deprecated:** *Use [TelephonyCallback.DisplayInfoListener](../android/telephony/TelephonyCallback.DisplayInfoListener.md) instead.*

Listen for display info changed event. For clients compiled on Android 11 SDK, requires permission: [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). For clients compiled on Android 12 SDK or newer, [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or carrier privileges is not required anymore. 

 Value: 1048576

**See Also**

- [#onDisplayInfoChanged](PhoneStateListener.md)) 

### LISTEN_EMERGENCY_NUMBER_LIST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_EMERGENCY_NUMBER_LIST: Int
```

**Deprecated:** *Use [TelephonyCallback.EmergencyNumberListListener](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) instead.*

Listen for changes to emergency number list based on all active subscriptions.

Requires permission [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 16777216

### LISTEN_IMS_CALL_DISCONNECT_CAUSES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_IMS_CALL_DISCONNECT_CAUSES: Int
```

**Deprecated:** *Use [TelephonyCallback.ImsCallDisconnectCauseListener](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md) instead.*

Listen for IMS call disconnect causes which contains [android.telephony.ims.ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md)

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 134217728

**See Also**

- [#onImsCallDisconnectCauseChanged(ImsReasonInfo)](PhoneStateListener.md)) 

### LISTEN_MESSAGE_WAITING_INDICATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_MESSAGE_WAITING_INDICATOR: Int
```

**Deprecated:** *Use [TelephonyCallback.MessageWaitingIndicatorListener](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) instead.*

Listen for changes to the message-waiting indicator. {@more} Requires Permission: [READ_PHONE_STATE](../android/Manifest.permission.md) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))).

Example: The status bar uses this to determine when to display the voicemail icon. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 4

**See Also**

- [#onMessageWaitingIndicatorChanged](PhoneStateListener.md)) 

### LISTEN_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_NONE: Int
```

**Deprecated:** *Deprecated in Java.*

Stop listening for updates. The PhoneStateListener is not tied to any subscription and unregistered for any update. 

 Value: 0

### LISTEN_PRECISE_DATA_CONNECTION_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_PRECISE_DATA_CONNECTION_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.PreciseDataConnectionStateListener](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) instead.*

Listen for [PreciseDataConnectionState](PreciseDataConnectionState.md) on the data connection (cellular).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) 

 Value: 4096

**See Also**

- [#onPreciseDataConnectionStateChanged](PhoneStateListener.md)) 

### LISTEN_REGISTRATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_REGISTRATION_FAILURE: Int
```

**Deprecated:** *Use [TelephonyCallback.RegistrationFailedListener](../android/telephony/TelephonyCallback.RegistrationFailedListener.md) instead.*

Listen for Registration Failures. Listen for indications that a registration procedure has failed in either the CS or PS domain. This indication does not necessarily indicate a change of service state, which should be tracked via [LISTEN_SERVICE_STATE](PhoneStateListener.md).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))).

Also requires the [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission, regardless of whether the calling app has carrier privileges. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 

 Value: 1073741824

**See Also**

- [#onRegistrationFailed](PhoneStateListener.md)) 

### LISTEN_SERVICE_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SERVICE_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md) instead.*

Listen for changes to the network service state (cellular). 

 Value: 1

**See Also**

- [#onServiceStateChanged](PhoneStateListener.md))
- [android.telephony.ServiceState](ServiceState.md) 

### LISTEN_SIGNAL_STRENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SIGNAL_STRENGTH: Int
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) instead.*

Listen for changes to the network signal strength (cellular). {@more} 

 Value: 2

**See Also**

- [#onSignalStrengthChanged](PhoneStateListener.md)) 

### LISTEN_SIGNAL_STRENGTHS

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SIGNAL_STRENGTHS: Int
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) instead.*

Listen for changes to the network signal strengths (cellular).

Example: The status bar uses this to control the signal-strength icon. 

 Value: 256

**See Also**

- [#onSignalStrengthsChanged](PhoneStateListener.md)) 

### LISTEN_USER_MOBILE_DATA_STATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_USER_MOBILE_DATA_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.UserMobileDataStateListener](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) instead.*

Listen for changes to the user mobile data state 

 Value: 524288

**See Also**

- [#onUserMobileDataStateChanged](PhoneStateListener.md))

## Public constructors

### PhoneStateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PhoneStateListener()
```

Create a PhoneStateListener for the Phone with the default subscription. This class requires Looper.myLooper() not return null. 

### PhoneStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PhoneStateListener(executor: Executor)
```

Create a PhoneStateListener for the Phone using the specified Executor

Create a PhoneStateListener with a specified Executor for handling necessary callbacks. The Executor must not be null.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):a non-null Executor that will execute callbacks for the PhoneStateListener. |

## Public methods

### onActiveDataSubscriptionIdChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActiveDataSubscriptionIdChanged(subId: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.ActiveDataSubscriptionIdListener](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) instead.*

Callback invoked when active data subId changes. Note, this callback triggers regardless of registered subscription. Requires the READ_PHONE_STATE permission. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):current subscription used to setup Cellular Internet data. For example, it could be the current active opportunistic subscription in use, or the subscription user selected as default data subscription in DSDS mode. |

### onBarringInfoChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBarringInfoChanged(barringInfo: BarringInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.BarringInfoListener](../android/telephony/TelephonyCallback.BarringInfoListener.md) instead.*

Report updated barring information for the current camped/registered cell.

Barring info is provided for all services applicable to the current camped/registered cell, for the registered PLMN and current access class/access category. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `barringInfo` | [BarringInfo](BarringInfo.md):for all services on the current cell. This value cannot be`null`. |

**See Also**

- [android.telephony.BarringInfo](BarringInfo.md) 

### onCallDisconnectCauseChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallDisconnectCauseChanged(
    disconnectCause: Int, 
    preciseDisconnectCause: Int
): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallDisconnectCauseListener](../android/telephony/TelephonyCallback.CallDisconnectCauseListener.md) instead.*

Callback invoked when call disconnect cause changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disconnectCause` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the disconnect cause Value is [android.telephony.DisconnectCause#NOT_VALID](DisconnectCause.md), [android.telephony.DisconnectCause#NOT_DISCONNECTED](DisconnectCause.md), [android.telephony.DisconnectCause#INCOMING_MISSED](DisconnectCause.md), [android.telephony.DisconnectCause#NORMAL](DisconnectCause.md), [android.telephony.DisconnectCause#LOCAL](DisconnectCause.md), [android.telephony.DisconnectCause#BUSY](DisconnectCause.md), [android.telephony.DisconnectCause#CONGESTION](DisconnectCause.md), [android.telephony.DisconnectCause#MMI](DisconnectCause.md), [android.telephony.DisconnectCause#INVALID_NUMBER](DisconnectCause.md), [android.telephony.DisconnectCause#NUMBER_UNREACHABLE](DisconnectCause.md), [android.telephony.DisconnectCause#SERVER_UNREACHABLE](DisconnectCause.md), [android.telephony.DisconnectCause#INVALID_CREDENTIALS](DisconnectCause.md), [android.telephony.DisconnectCause#OUT_OF_NETWORK](DisconnectCause.md), [android.telephony.DisconnectCause#SERVER_ERROR](DisconnectCause.md), [android.telephony.DisconnectCause#TIMED_OUT](DisconnectCause.md), [android.telephony.DisconnectCause#LOST_SIGNAL](DisconnectCause.md), [android.telephony.DisconnectCause#LIMIT_EXCEEDED](DisconnectCause.md), [android.telephony.DisconnectCause#INCOMING_REJECTED](DisconnectCause.md), [android.telephony.DisconnectCause#POWER_OFF](DisconnectCause.md), [android.telephony.DisconnectCause#OUT_OF_SERVICE](DisconnectCause.md), [android.telephony.DisconnectCause#ICC_ERROR](DisconnectCause.md), [android.telephony.DisconnectCause#CALL_BARRED](DisconnectCause.md), [android.telephony.DisconnectCause#FDN_BLOCKED](DisconnectCause.md), [android.telephony.DisconnectCause#CS_RESTRICTED](DisconnectCause.md), [android.telephony.DisconnectCause#CS_RESTRICTED_NORMAL](DisconnectCause.md), [android.telephony.DisconnectCause#CS_RESTRICTED_EMERGENCY](DisconnectCause.md), [android.telephony.DisconnectCause#UNOBTAINABLE_NUMBER](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_LOCKED_UNTIL_POWER_CYCLE](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_DROP](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_INTERCEPT](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_REORDER](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_SO_REJECT](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_RETRY_ORDER](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_ACCESS_FAILURE](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_PREEMPTED](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_NOT_EMERGENCY](DisconnectCause.md), [android.telephony.DisconnectCause#CDMA_ACCESS_BLOCKED](DisconnectCause.md), or [android.telephony.DisconnectCause#ERROR_UNSPECIFIED](DisconnectCause.md) |
| `preciseDisconnectCause` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the precise disconnect cause Value is android.telephony.PreciseDisconnectCause.NOT_VALID, android.telephony.PreciseDisconnectCause.NO_DISCONNECT_CAUSE_AVAILABLE, android.telephony.PreciseDisconnectCause.UNOBTAINABLE_NUMBER, android.telephony.PreciseDisconnectCause.NORMAL, android.telephony.PreciseDisconnectCause.BUSY, android.telephony.PreciseDisconnectCause.NUMBER_CHANGED, android.telephony.PreciseDisconnectCause.STATUS_ENQUIRY, android.telephony.PreciseDisconnectCause.NORMAL_UNSPECIFIED, android.telephony.PreciseDisconnectCause.NO_CIRCUIT_AVAIL, android.telephony.PreciseDisconnectCause.TEMPORARY_FAILURE, android.telephony.PreciseDisconnectCause.SWITCHING_CONGESTION, android.telephony.PreciseDisconnectCause.CHANNEL_NOT_AVAIL, android.telephony.PreciseDisconnectCause.QOS_NOT_AVAIL, android.telephony.PreciseDisconnectCause.BEARER_NOT_AVAIL, android.telephony.PreciseDisconnectCause.ACM_LIMIT_EXCEEDED, android.telephony.PreciseDisconnectCause.CALL_BARRED, android.telephony.PreciseDisconnectCause.FDN_BLOCKED, android.telephony.PreciseDisconnectCause.IMSI_UNKNOWN_IN_VLR, android.telephony.PreciseDisconnectCause.IMEI_NOT_ACCEPTED, android.telephony.PreciseDisconnectCause.CDMA_LOCKED_UNTIL_POWER_CYCLE, android.telephony.PreciseDisconnectCause.CDMA_DROP, android.telephony.PreciseDisconnectCause.CDMA_INTERCEPT, android.telephony.PreciseDisconnectCause.CDMA_REORDER, android.telephony.PreciseDisconnectCause.CDMA_SO_REJECT, android.telephony.PreciseDisconnectCause.CDMA_RETRY_ORDER, android.telephony.PreciseDisconnectCause.CDMA_ACCESS_FAILURE, android.telephony.PreciseDisconnectCause.CDMA_PREEMPTED, android.telephony.PreciseDisconnectCause.CDMA_NOT_EMERGENCY, android.telephony.PreciseDisconnectCause.CDMA_ACCESS_BLOCKED, or android.telephony.PreciseDisconnectCause.ERROR_UNSPECIFIED |

### onCallForwardingIndicatorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallForwardingIndicatorChanged(cfi: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallForwardingIndicatorListener](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) instead.*

Callback invoked when the call-forwarding indicator changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

### onCallStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallStateChanged(
    state: Int, 
    phoneNumber: String!
): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallStateListener](../android/telephony/TelephonyCallback.CallStateListener.md) instead.*

Callback invoked when device call state changes.

Reports the state of Telephony (mobile) calls on the device for the registered subscription.

Note: the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

Note: The state returned here may differ from that returned by [TelephonyManager.getCallState()](TelephonyManager.md)). Receivers of this callback should be aware that calling [TelephonyManager.getCallState()](TelephonyManager.md))from within this callback may return a different state than the callback reports. Requires Permission: [READ_PHONE_STATE](../android/Manifest.permission.md) for applications targeting API level 31+.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):call state Value is [android.telephony.TelephonyManager#CALL_STATE_IDLE](TelephonyManager.md), [android.telephony.TelephonyManager#CALL_STATE_RINGING](TelephonyManager.md), or [android.telephony.TelephonyManager#CALL_STATE_OFFHOOK](TelephonyManager.md) |
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:call phone number. If application does not have [READ_CALL_LOG](../android/Manifest.permission.md) permission or carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))), an empty string will be passed as an argument. |

### onCellInfoChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCellInfoChanged(cellInfo: MutableList<CellInfo!>!): Unit
```

**Deprecated:** *Use [TelephonyCallback.CellInfoListener](../android/telephony/TelephonyCallback.CellInfoListener.md) instead.*

Callback invoked when a observed cell info has changed or new cells have been added or removed on the registered subscription. Note, the registration subId s from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cellInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellInfo](CellInfo.md)!\>!:is the list of currently visible cells. |

### onCellLocationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCellLocationChanged(location: CellLocation!): Unit
```

**Deprecated:** *Use [TelephonyCallback.CellLocationListener](../android/telephony/TelephonyCallback.CellLocationListener.md) instead.*

Callback invoked when device cell location changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 

### onDataActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataActivity(direction: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataActivityListener](../android/telephony/TelephonyCallback.DataActivityListener.md) instead.*

Callback invoked when data activity state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
**See Also**

- [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](TelephonyManager.md) 

### onDataConnectionStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataConnectionStateChanged(state: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) instead.*

Callback invoked when connection state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
**See Also**

- [android.telephony.TelephonyManager#DATA_DISCONNECTED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTING](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_SUSPENDED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](TelephonyManager.md) 

### onDataConnectionStateChanged

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataConnectionStateChanged(
    state: Int, 
    networkType: Int
): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) instead.*

same as above, but with the network type. Both called. 

### onDisplayInfoChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisplayInfoChanged(telephonyDisplayInfo: TelephonyDisplayInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.DisplayInfoListener](../android/telephony/TelephonyCallback.DisplayInfoListener.md) instead.*

Callback invoked when the display info has changed on the registered subscription.

The [TelephonyDisplayInfo](TelephonyDisplayInfo.md) contains status information shown to the user based on carrier policy. For clients compiled on Android 11 SDK, requires permission: [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). For clients compiled on Android 12 SDK or newer, [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) or carrier privileges is not required anymore. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `telephonyDisplayInfo` | [TelephonyDisplayInfo](TelephonyDisplayInfo.md):The display information. This value cannot be`null`. |

### onEmergencyNumberListChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onEmergencyNumberListChanged(emergencyNumberList: MutableMap<Int!, MutableList<EmergencyNumber!>!>): Unit
```

**Deprecated:** *Use [TelephonyCallback.EmergencyNumberListListener](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) instead.*

Callback invoked when the current emergency number list has changed on the registered subscription. Note, the registered subscription is associated with [TelephonyManager](TelephonyManager.md) object on which [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md))was called. If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the given subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `emergencyNumberList` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](../android.telephony.emergency/EmergencyNumber.md)!\>!\>:Map associating all active subscriptions on the device with the list of emergency numbers originating from that subscription. If there are no active subscriptions, the map will contain a single entry with [SubscriptionManager.INVALID_SUBSCRIPTION_ID](SubscriptionManager.md) as the key and a list of emergency numbers as the value. If no emergency number information is available, the value will be null. |

### onImsCallDisconnectCauseChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onImsCallDisconnectCauseChanged(imsReasonInfo: ImsReasonInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.ImsCallDisconnectCauseListener](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md) instead.*

Callback invoked when Ims call disconnect cause changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `imsReasonInfo` | [ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md): [ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md) contains details on why IMS call failed. This value cannot be`null`. |

### onMessageWaitingIndicatorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageWaitingIndicatorChanged(mwi: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.MessageWaitingIndicatorListener](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) instead.*

Callback invoked when the message-waiting indicator changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md) 

### onPreciseDataConnectionStateChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPreciseDataConnectionStateChanged(dataConnectionState: PreciseDataConnectionState): Unit
```

**Deprecated:** *Use [TelephonyCallback.PreciseDataConnectionStateListener](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) instead.*

Callback providing update about the default/internet data connection on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataConnectionState` | [PreciseDataConnectionState](PreciseDataConnectionState.md): [PreciseDataConnectionState](PreciseDataConnectionState.md) This value cannot be`null`. |

### onRegistrationFailed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRegistrationFailed(
    cellIdentity: CellIdentity, 
    chosenPlmn: String, 
    domain: Int, 
    causeCode: Int, 
    additionalCauseCode: Int
): Unit
```

**Deprecated:** *Use [TelephonyCallback.RegistrationFailedListener](../android/telephony/TelephonyCallback.RegistrationFailedListener.md) instead.*

Report that Registration or a Location/Routing/Tracking Area update has failed.

Indicate whenever a registration procedure, including a location, routing, or tracking area update fails. This includes procedures that do not necessarily result in a change of the modem's registration status. If the modem's registration status changes, that is reflected in the onNetworkStateChanged() and subsequent get{Voice/Data}RegistrationState().

Because registration failures are ephemeral, this callback is not sticky. Registrants will not receive the most recent past value when registering. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cellIdentity` | [CellIdentity](CellIdentity.md):the CellIdentity, which must include the globally unique identifier for the cell (for example, all components of the CGI or ECGI). This value cannot be`null`. |
| `chosenPlmn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a 5 or 6 digit alphanumeric PLMN (MCC|MNC) among those broadcast by the cell that was chosen for the failed registration attempt. This value cannot be`null`. |
| `domain` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):DOMAIN_CS, DOMAIN_PS or both in case of a combined procedure. |
| --- | --- |
| `causeCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the primary failure cause code of the procedure. For GSM/UMTS (MM), values are in TS 24.008 Sec 10.5.95 For GSM/UMTS (GMM), values are in TS 24.008 Sec 10.5.147 For LTE (EMM), cause codes are TS 24.301 Sec 9.9.3.9 For NR (5GMM), cause codes are TS 24.501 Sec 9.11.3.2 Integer.MAX_VALUE if this value is unused. |
| `additionalCauseCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cause code of any secondary/combined procedure if appropriate. For UMTS, if a combined attach succeeds for PS only, then the GMM cause code shall be included as an additionalCauseCode. For LTE (ESM), cause codes are in TS 24.301 9.9.4.4. Integer.MAX_VALUE if this value is unused. |

### onServiceStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceStateChanged(serviceState: ServiceState!): Unit
```

**Deprecated:** *Use [TelephonyCallback.ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md) instead.*

Callback invoked when device service state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). The instance of [ServiceState](ServiceState.md) passed as an argument here will have various levels of location information stripped from it depending on the location permissions that your app holds. Only apps holding the [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission will receive all the information in [ServiceState](ServiceState.md), otherwise the cellIdentity will be null if apps only holding the [Manifest.permission.ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) permission. Network operator name in long/short alphanumeric format and numeric id will be null if apps holding neither [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) nor [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md). 
**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](ServiceState.md)
- [android.telephony.ServiceState#STATE_IN_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_POWER_OFF](ServiceState.md) 

### onSignalStrengthChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSignalStrengthChanged(asu: Int): Unit
```

**Deprecated:** *Use [onSignalStrengthsChanged(android.telephony.SignalStrength)](PhoneStateListener.md))*

Callback invoked when network signal strength changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](ServiceState.md)
- [android.telephony.ServiceState#STATE_IN_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_POWER_OFF](ServiceState.md) 

### onSignalStrengthsChanged

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSignalStrengthsChanged(signalStrength: SignalStrength!): Unit
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) instead.*

Callback invoked when network signal strengths changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 

### onUserMobileDataStateChanged

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUserMobileDataStateChanged(enabled: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.UserMobileDataStateListener](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) instead.*

Callback invoked when the user mobile data state has changed on the registered subscription. Note, the registration subId comes from [TelephonyManager](TelephonyManager.md) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates whether the current user mobile data state is enabled or disabled. |
