# PhoneStateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneStateListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/PhoneStateListener "View this page in Java") 

```
open class PhoneStateListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.PhoneStateListener](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#) |

| **This class was deprecated in API level 31.**
|
| Use [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback) instead.

A listener class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others.

Override the methods for the state that you wish to receive updates for, and pass your PhoneStateListener object, along with bitwise-or of the LISTEN_ flags to [TelephonyManager.listen()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). Methods are called when the state changes, as well as once on initial registration.

Note that access to some telephony information is permission-protected. Your application won't receive updates for protected information unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the appropriate LISTEN_ flags.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE:kotlin.Int) Listen for changes to active data subId. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_BARRING_INFO](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_BARRING_INFO:kotlin.Int) Listen for Barring Information for the current registered / camped cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_DISCONNECT_CAUSES](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CALL_DISCONNECT_CAUSES:kotlin.Int) Listen for call disconnect causes which contains [DisconnectCause](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause) and the precise disconnect cause. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_FORWARDING_INDICATOR](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CALL_FORWARDING_INDICATOR:kotlin.Int) Listen for changes to the call-forwarding indicator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CALL_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CALL_STATE:kotlin.Int) Listen for changes to the device call state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CELL_INFO](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CELL_INFO:kotlin.Int) Listen for changes to observed cell info. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_CELL_LOCATION](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CELL_LOCATION:kotlin.Int) Listen for changes to the device's cell location. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DATA_ACTIVITY](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_DATA_ACTIVITY:kotlin.Int) Listen for changes to the direction of data traffic on the data connection (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DATA_CONNECTION_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_DATA_CONNECTION_STATE:kotlin.Int) Listen for changes to the data connection state (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_DISPLAY_INFO_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_DISPLAY_INFO_CHANGED:kotlin.Int) Listen for display info changed event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_EMERGENCY_NUMBER_LIST](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_EMERGENCY_NUMBER_LIST:kotlin.Int) Listen for changes to emergency number list based on all active subscriptions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_IMS_CALL_DISCONNECT_CAUSES](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_IMS_CALL_DISCONNECT_CAUSES:kotlin.Int) Listen for IMS call disconnect causes which contains [android.telephony.ims.ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_MESSAGE_WAITING_INDICATOR](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_MESSAGE_WAITING_INDICATOR:kotlin.Int) Listen for changes to the message-waiting indicator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_NONE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_NONE:kotlin.Int) Stop listening for updates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_PRECISE_DATA_CONNECTION_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_PRECISE_DATA_CONNECTION_STATE:kotlin.Int) Listen for [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState) on the data connection (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_REGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_REGISTRATION_FAILURE:kotlin.Int) Listen for Registration Failures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SERVICE_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_SERVICE_STATE:kotlin.Int) Listen for changes to the network service state (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SIGNAL_STRENGTH](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_SIGNAL_STRENGTH:kotlin.Int) Listen for changes to the network signal strength (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_SIGNAL_STRENGTHS](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_SIGNAL_STRENGTHS:kotlin.Int) Listen for changes to the network signal strengths (cellular). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LISTEN_USER_MOBILE_DATA_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_USER_MOBILE_DATA_STATE:kotlin.Int) Listen for changes to the user mobile data state |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PhoneStateListener](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#PhoneStateListener())`()` Create a PhoneStateListener for the Phone with the default subscription. |
| [PhoneStateListener](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#PhoneStateListener(java.util.concurrent.Executor))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`)` Create a PhoneStateListener for the Phone using the specified Executor |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActiveDataSubscriptionIdChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onActiveDataSubscriptionIdChanged(kotlin.Int))`(`subId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when active data subId changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBarringInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onBarringInfoChanged(android.telephony.BarringInfo))`(`barringInfo:` ` [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo)`)` Report updated barring information for the current camped/registered cell. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallDisconnectCauseChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallDisconnectCauseChanged(kotlin.Int,%20kotlin.Int))`(`disconnectCause:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preciseDisconnectCause:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when call disconnect cause changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallForwardingIndicatorChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallForwardingIndicatorChanged(kotlin.Boolean))`(`cfi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the call-forwarding indicator changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallStateChanged(kotlin.Int,%20kotlin.String))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Callback invoked when device call state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCellInfoChanged(kotlin.collections.MutableList))`(`cellInfo:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo)!>!`)` Callback invoked when a observed cell info has changed or new cells have been added or removed on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellLocationChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCellLocationChanged(android.telephony.CellLocation))`(`location:` ` [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation)!`)` Callback invoked when device cell location changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataActivity](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDataActivity(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when data activity state changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataConnectionStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDataConnectionStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when connection state changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataConnectionStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDataConnectionStateChanged(kotlin.Int,%20kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` same as above, but with the network type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDisplayInfoChanged(android.telephony.TelephonyDisplayInfo))`(`telephonyDisplayInfo:` ` [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo)`)` Callback invoked when the display info has changed on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEmergencyNumberListChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onEmergencyNumberListChanged(kotlin.collections.MutableMap))`(`emergencyNumberList:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber)!>!>`)` Callback invoked when the current emergency number list has changed on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImsCallDisconnectCauseChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onImsCallDisconnectCauseChanged(android.telephony.ims.ImsReasonInfo))`(`imsReasonInfo:` ` [ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo)`)` Callback invoked when Ims call disconnect cause changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageWaitingIndicatorChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onMessageWaitingIndicatorChanged(kotlin.Boolean))`(`mwi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the message-waiting indicator changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreciseDataConnectionStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onPreciseDataConnectionStateChanged(android.telephony.PreciseDataConnectionState))`(`dataConnectionState:` ` [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState)`)` Callback providing update about the default/internet data connection on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onRegistrationFailed(android.telephony.CellIdentity,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`cellIdentity:` ` [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity)`, `chosenPlmn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `domain:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `causeCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCauseCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Report that Registration or a Location/Routing/Tracking Area update has failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onServiceStateChanged(android.telephony.ServiceState))`(`serviceState:` ` [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState)!`)` Callback invoked when device service state changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onSignalStrengthChanged(kotlin.Int))`(`asu:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when network signal strength changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthsChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onSignalStrengthsChanged(android.telephony.SignalStrength))`(`signalStrength:` ` [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength)!`)` Callback invoked when network signal strengths changes on the registered subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserMobileDataStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onUserMobileDataStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the user mobile data state has changed on the registered subscription. |

## Constants

### LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_ACTIVE_DATA_SUBSCRIPTION_ID_CHANGE: Int
```

**Deprecated:** *Use [TelephonyCallback.ActiveDataSubscriptionIdListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener) instead.*

Listen for changes to active data subId. Active data subscription is the current subscription used to setup Cellular Internet data. For example, it could be the current active opportunistic subscription in use, or the subscription user selected as default data subscription in DSDS mode. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

 Value: 4194304

**See Also**

- [#onActiveDataSubscriptionIdChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onActiveDataSubscriptionIdChanged(kotlin.Int)) 

### LISTEN_BARRING_INFO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_BARRING_INFO: Int
```

**Deprecated:** *Use [TelephonyCallback.BarringInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener) instead.*

Listen for Barring Information for the current registered / camped cell.

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())).

Also requires the [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission, regardless of whether the calling app has carrier privileges. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 

 Value: -2147483648

**See Also**

- [#onBarringInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onBarringInfoChanged(android.telephony.BarringInfo)) 

### LISTEN_CALL_DISCONNECT_CAUSES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_DISCONNECT_CAUSES: Int
```

**Deprecated:** *Use [TelephonyCallback.CallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallDisconnectCauseListener) instead.*

Listen for call disconnect causes which contains [DisconnectCause](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause) and the precise disconnect cause.

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) 

 Value: 33554432

### LISTEN_CALL_FORWARDING_INDICATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_FORWARDING_INDICATOR: Int
```

**Deprecated:** *Use [TelephonyCallback.CallForwardingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallForwardingIndicatorListener) instead.*

Listen for changes to the call-forwarding indicator. {@more} Requires Permission: [READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

 Value: 8

**See Also**

- [#onCallForwardingIndicatorChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallForwardingIndicatorChanged(kotlin.Boolean)) 

### LISTEN_CALL_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CALL_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.CallStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener) instead.*

Listen for changes to the device call state. {@more} 

 Value: 32

**See Also**

- [#onCallStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCallStateChanged(kotlin.Int,%20kotlin.String)) 

### LISTEN_CELL_INFO

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CELL_INFO: Int
```

**Deprecated:** *Use [TelephonyCallback.CellInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellInfoListener) instead.*

Listen for changes to observed cell info. Listening to this event requires the [Manifest.permission.READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) and [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 

 Value: 1024

**See Also**

- [#onCellInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCellInfoChanged(kotlin.collections.MutableList)) 

### LISTEN_CELL_LOCATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_CELL_LOCATION: Int
```

**Deprecated:** *Use [TelephonyCallback.CellLocationListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener) instead.*

Listen for changes to the device's cell location. Note that this will result in frequent callbacks to the listener. {@more} Requires Permission: [ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

If you need regular location updates but want more control over the update interval or location precision, you can set up a listener through the [location manager](https://developer.android.com/reference/kotlin/android/location/LocationManager.html#) instead. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 

 Value: 16

**See Also**

- [#onCellLocationChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onCellLocationChanged(android.telephony.CellLocation)) 

### LISTEN_DATA_ACTIVITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DATA_ACTIVITY: Int
```

**Deprecated:** *Use [TelephonyCallback.DataActivityListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener) instead.*

Listen for changes to the direction of data traffic on the data connection (cellular). {@more} Example: The status bar uses this to display the appropriate data-traffic icon. 

 Value: 128

**See Also**

- [#onDataActivity](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDataActivity(kotlin.Int)) 

### LISTEN_DATA_CONNECTION_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DATA_CONNECTION_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataConnectionStateListener) instead.*

Listen for changes to the data connection state (cellular). 

 Value: 64

**See Also**

### LISTEN_DISPLAY_INFO_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_DISPLAY_INFO_CHANGED: Int
```

**Deprecated:** *Use [TelephonyCallback.DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener) instead.*

Listen for display info changed event. For clients compiled on Android 11 SDK, requires permission: [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). For clients compiled on Android 12 SDK or newer, [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or carrier privileges is not required anymore. 

 Value: 1048576

**See Also**

- [#onDisplayInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onDisplayInfoChanged(android.telephony.TelephonyDisplayInfo)) 

### LISTEN_EMERGENCY_NUMBER_LIST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_EMERGENCY_NUMBER_LIST: Int
```

**Deprecated:** *Use [TelephonyCallback.EmergencyNumberListListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener) instead.*

Listen for changes to emergency number list based on all active subscriptions.

Requires permission [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

 Value: 16777216

### LISTEN_IMS_CALL_DISCONNECT_CAUSES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_IMS_CALL_DISCONNECT_CAUSES: Int
```

**Deprecated:** *Use [TelephonyCallback.ImsCallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener) instead.*

Listen for IMS call disconnect causes which contains [android.telephony.ims.ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo)

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) 

 Value: 134217728

**See Also**

- [#onImsCallDisconnectCauseChanged(ImsReasonInfo)](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onImsCallDisconnectCauseChanged(android.telephony.ims.ImsReasonInfo)) 

### LISTEN_MESSAGE_WAITING_INDICATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_MESSAGE_WAITING_INDICATOR: Int
```

**Deprecated:** *Use [TelephonyCallback.MessageWaitingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener) instead.*

Listen for changes to the message-waiting indicator. {@more} Requires Permission: [READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())).

Example: The status bar uses this to determine when to display the voicemail icon. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

 Value: 4

**See Also**

- [#onMessageWaitingIndicatorChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onMessageWaitingIndicatorChanged(kotlin.Boolean)) 

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

**Deprecated:** *Use [TelephonyCallback.PreciseDataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener) instead.*

Listen for [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState) on the data connection (cellular).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) 

 Value: 4096

**See Also**

- [#onPreciseDataConnectionStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onPreciseDataConnectionStateChanged(android.telephony.PreciseDataConnectionState)) 

### LISTEN_REGISTRATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_REGISTRATION_FAILURE: Int
```

**Deprecated:** *Use [TelephonyCallback.RegistrationFailedListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.RegistrationFailedListener) instead.*

Listen for Registration Failures. Listen for indications that a registration procedure has failed in either the CS or PS domain. This indication does not necessarily indicate a change of service state, which should be tracked via [LISTEN_SERVICE_STATE](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_SERVICE_STATE:kotlin.Int).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())).

Also requires the [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission, regardless of whether the calling app has carrier privileges. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 

 Value: 1073741824

**See Also**

- [#onRegistrationFailed](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onRegistrationFailed(android.telephony.CellIdentity,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### LISTEN_SERVICE_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SERVICE_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener) instead.*

Listen for changes to the network service state (cellular). 

 Value: 1

**See Also**

- [#onServiceStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onServiceStateChanged(android.telephony.ServiceState))
- [android.telephony.ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState) 

### LISTEN_SIGNAL_STRENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SIGNAL_STRENGTH: Int
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener) instead.*

Listen for changes to the network signal strength (cellular). {@more} 

 Value: 2

**See Also**

- [#onSignalStrengthChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onSignalStrengthChanged(kotlin.Int)) 

### LISTEN_SIGNAL_STRENGTHS

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_SIGNAL_STRENGTHS: Int
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener) instead.*

Listen for changes to the network signal strengths (cellular).

Example: The status bar uses this to control the signal-strength icon. 

 Value: 256

**See Also**

- [#onSignalStrengthsChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onSignalStrengthsChanged(android.telephony.SignalStrength)) 

### LISTEN_USER_MOBILE_DATA_STATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LISTEN_USER_MOBILE_DATA_STATE: Int
```

**Deprecated:** *Use [TelephonyCallback.UserMobileDataStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener) instead.*

Listen for changes to the user mobile data state 

 Value: 524288

**See Also**

- [#onUserMobileDataStateChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onUserMobileDataStateChanged(kotlin.Boolean))

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
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):a non-null Executor that will execute callbacks for the PhoneStateListener. |

## Public methods

### onActiveDataSubscriptionIdChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActiveDataSubscriptionIdChanged(subId: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.ActiveDataSubscriptionIdListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener) instead.*

Callback invoked when active data subId changes. Note, this callback triggers regardless of registered subscription. Requires the READ_PHONE_STATE permission. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):current subscription used to setup Cellular Internet data. For example, it could be the current active opportunistic subscription in use, or the subscription user selected as default data subscription in DSDS mode. |

### onBarringInfoChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBarringInfoChanged(barringInfo: BarringInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.BarringInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener) instead.*

Report updated barring information for the current camped/registered cell.

Barring info is provided for all services applicable to the current camped/registered cell, for the registered PLMN and current access class/access category. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `barringInfo` | [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo):for all services on the current cell. This value cannot be`null`. |

**See Also**

- [android.telephony.BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo) 

### onCallDisconnectCauseChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallDisconnectCauseChanged(
    disconnectCause: Int, 
    preciseDisconnectCause: Int
): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallDisconnectCauseListener) instead.*

Callback invoked when call disconnect cause changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `disconnectCause` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the disconnect cause Value is [android.telephony.DisconnectCause#NOT_VALID](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NOT_VALID:kotlin.Int), [android.telephony.DisconnectCause#NOT_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NOT_DISCONNECTED:kotlin.Int), [android.telephony.DisconnectCause#INCOMING_MISSED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INCOMING_MISSED:kotlin.Int), [android.telephony.DisconnectCause#NORMAL](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NORMAL:kotlin.Int), [android.telephony.DisconnectCause#LOCAL](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LOCAL:kotlin.Int), [android.telephony.DisconnectCause#BUSY](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#BUSY:kotlin.Int), [android.telephony.DisconnectCause#CONGESTION](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CONGESTION:kotlin.Int), [android.telephony.DisconnectCause#MMI](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#MMI:kotlin.Int), [android.telephony.DisconnectCause#INVALID_NUMBER](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INVALID_NUMBER:kotlin.Int), [android.telephony.DisconnectCause#NUMBER_UNREACHABLE](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#NUMBER_UNREACHABLE:kotlin.Int), [android.telephony.DisconnectCause#SERVER_UNREACHABLE](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#SERVER_UNREACHABLE:kotlin.Int), [android.telephony.DisconnectCause#INVALID_CREDENTIALS](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INVALID_CREDENTIALS:kotlin.Int), [android.telephony.DisconnectCause#OUT_OF_NETWORK](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUT_OF_NETWORK:kotlin.Int), [android.telephony.DisconnectCause#SERVER_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#SERVER_ERROR:kotlin.Int), [android.telephony.DisconnectCause#TIMED_OUT](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#TIMED_OUT:kotlin.Int), [android.telephony.DisconnectCause#LOST_SIGNAL](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LOST_SIGNAL:kotlin.Int), [android.telephony.DisconnectCause#LIMIT_EXCEEDED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#LIMIT_EXCEEDED:kotlin.Int), [android.telephony.DisconnectCause#INCOMING_REJECTED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#INCOMING_REJECTED:kotlin.Int), [android.telephony.DisconnectCause#POWER_OFF](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#POWER_OFF:kotlin.Int), [android.telephony.DisconnectCause#OUT_OF_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#OUT_OF_SERVICE:kotlin.Int), [android.telephony.DisconnectCause#ICC_ERROR](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ICC_ERROR:kotlin.Int), [android.telephony.DisconnectCause#CALL_BARRED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CALL_BARRED:kotlin.Int), [android.telephony.DisconnectCause#FDN_BLOCKED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#FDN_BLOCKED:kotlin.Int), [android.telephony.DisconnectCause#CS_RESTRICTED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED:kotlin.Int), [android.telephony.DisconnectCause#CS_RESTRICTED_NORMAL](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED_NORMAL:kotlin.Int), [android.telephony.DisconnectCause#CS_RESTRICTED_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CS_RESTRICTED_EMERGENCY:kotlin.Int), [android.telephony.DisconnectCause#UNOBTAINABLE_NUMBER](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#UNOBTAINABLE_NUMBER:kotlin.Int), [android.telephony.DisconnectCause#CDMA_LOCKED_UNTIL_POWER_CYCLE](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_LOCKED_UNTIL_POWER_CYCLE:kotlin.Int), [android.telephony.DisconnectCause#CDMA_DROP](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_DROP:kotlin.Int), [android.telephony.DisconnectCause#CDMA_INTERCEPT](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_INTERCEPT:kotlin.Int), [android.telephony.DisconnectCause#CDMA_REORDER](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_REORDER:kotlin.Int), [android.telephony.DisconnectCause#CDMA_SO_REJECT](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_SO_REJECT:kotlin.Int), [android.telephony.DisconnectCause#CDMA_RETRY_ORDER](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_RETRY_ORDER:kotlin.Int), [android.telephony.DisconnectCause#CDMA_ACCESS_FAILURE](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_ACCESS_FAILURE:kotlin.Int), [android.telephony.DisconnectCause#CDMA_PREEMPTED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_PREEMPTED:kotlin.Int), [android.telephony.DisconnectCause#CDMA_NOT_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_NOT_EMERGENCY:kotlin.Int), [android.telephony.DisconnectCause#CDMA_ACCESS_BLOCKED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#CDMA_ACCESS_BLOCKED:kotlin.Int), or [android.telephony.DisconnectCause#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause#ERROR_UNSPECIFIED:kotlin.Int) |
| `preciseDisconnectCause` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the precise disconnect cause Value is android.telephony.PreciseDisconnectCause.NOT_VALID, android.telephony.PreciseDisconnectCause.NO_DISCONNECT_CAUSE_AVAILABLE, android.telephony.PreciseDisconnectCause.UNOBTAINABLE_NUMBER, android.telephony.PreciseDisconnectCause.NORMAL, android.telephony.PreciseDisconnectCause.BUSY, android.telephony.PreciseDisconnectCause.NUMBER_CHANGED, android.telephony.PreciseDisconnectCause.STATUS_ENQUIRY, android.telephony.PreciseDisconnectCause.NORMAL_UNSPECIFIED, android.telephony.PreciseDisconnectCause.NO_CIRCUIT_AVAIL, android.telephony.PreciseDisconnectCause.TEMPORARY_FAILURE, android.telephony.PreciseDisconnectCause.SWITCHING_CONGESTION, android.telephony.PreciseDisconnectCause.CHANNEL_NOT_AVAIL, android.telephony.PreciseDisconnectCause.QOS_NOT_AVAIL, android.telephony.PreciseDisconnectCause.BEARER_NOT_AVAIL, android.telephony.PreciseDisconnectCause.ACM_LIMIT_EXCEEDED, android.telephony.PreciseDisconnectCause.CALL_BARRED, android.telephony.PreciseDisconnectCause.FDN_BLOCKED, android.telephony.PreciseDisconnectCause.IMSI_UNKNOWN_IN_VLR, android.telephony.PreciseDisconnectCause.IMEI_NOT_ACCEPTED, android.telephony.PreciseDisconnectCause.CDMA_LOCKED_UNTIL_POWER_CYCLE, android.telephony.PreciseDisconnectCause.CDMA_DROP, android.telephony.PreciseDisconnectCause.CDMA_INTERCEPT, android.telephony.PreciseDisconnectCause.CDMA_REORDER, android.telephony.PreciseDisconnectCause.CDMA_SO_REJECT, android.telephony.PreciseDisconnectCause.CDMA_RETRY_ORDER, android.telephony.PreciseDisconnectCause.CDMA_ACCESS_FAILURE, android.telephony.PreciseDisconnectCause.CDMA_PREEMPTED, android.telephony.PreciseDisconnectCause.CDMA_NOT_EMERGENCY, android.telephony.PreciseDisconnectCause.CDMA_ACCESS_BLOCKED, or android.telephony.PreciseDisconnectCause.ERROR_UNSPECIFIED |

### onCallForwardingIndicatorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallForwardingIndicatorChanged(cfi: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallForwardingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallForwardingIndicatorListener) instead.*

Callback invoked when the call-forwarding indicator changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

### onCallStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCallStateChanged(
    state: Int, 
    phoneNumber: String!
): Unit
```

**Deprecated:** *Use [TelephonyCallback.CallStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener) instead.*

Callback invoked when device call state changes.

Reports the state of Telephony (mobile) calls on the device for the registered subscription.

Note: the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

Note: The state returned here may differ from that returned by [TelephonyManager.getCallState()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getCallState()). Receivers of this callback should be aware that calling [TelephonyManager.getCallState()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getCallState())from within this callback may return a different state than the callback reports. Requires Permission: [READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) for applications targeting API level 31+.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):call state Value is [android.telephony.TelephonyManager#CALL_STATE_IDLE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int), [android.telephony.TelephonyManager#CALL_STATE_RINGING](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int), or [android.telephony.TelephonyManager#CALL_STATE_OFFHOOK](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int) |
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:call phone number. If application does not have [READ_CALL_LOG](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALL_LOG:kotlin.String) permission or carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())), an empty string will be passed as an argument. |

### onCellInfoChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCellInfoChanged(cellInfo: MutableList<CellInfo!>!): Unit
```

**Deprecated:** *Use [TelephonyCallback.CellInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellInfoListener) instead.*

Callback invoked when a observed cell info has changed or new cells have been added or removed on the registered subscription. Note, the registration subId s from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cellInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo)!\>!:is the list of currently visible cells. |

### onCellLocationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCellLocationChanged(location: CellLocation!): Unit
```

**Deprecated:** *Use [TelephonyCallback.CellLocationListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener) instead.*

Callback invoked when device cell location changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 

### onDataActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataActivity(direction: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataActivityListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener) instead.*

Callback invoked when data activity state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
**See Also**

- [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_NONE:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_IN:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_OUT:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_INOUT:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_DORMANT:kotlin.Int) 

### onDataConnectionStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataConnectionStateChanged(state: Int): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataConnectionStateListener) instead.*

Callback invoked when connection state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
**See Also**

- [android.telephony.TelephonyManager#DATA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_DISCONNECTED:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_CONNECTING](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTING:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_CONNECTED](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTED:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_SUSPENDED](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_SUSPENDED:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_HANDOVER_IN_PROGRESS:kotlin.Int) 

### onDataConnectionStateChanged

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDataConnectionStateChanged(
    state: Int, 
    networkType: Int
): Unit
```

**Deprecated:** *Use [TelephonyCallback.DataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataConnectionStateListener) instead.*

same as above, but with the network type. Both called. 

### onDisplayInfoChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisplayInfoChanged(telephonyDisplayInfo: TelephonyDisplayInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener) instead.*

Callback invoked when the display info has changed on the registered subscription.

The [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo) contains status information shown to the user based on carrier policy. For clients compiled on Android 11 SDK, requires permission: [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). For clients compiled on Android 12 SDK or newer, [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) or carrier privileges is not required anymore. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `telephonyDisplayInfo` | [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo):The display information. This value cannot be`null`. |

### onEmergencyNumberListChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onEmergencyNumberListChanged(emergencyNumberList: MutableMap<Int!, MutableList<EmergencyNumber!>!>): Unit
```

**Deprecated:** *Use [TelephonyCallback.EmergencyNumberListListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener) instead.*

Callback invoked when the current emergency number list has changed on the registered subscription. Note, the registered subscription is associated with [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object on which [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int))was called. If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the given subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `emergencyNumberList` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber)!\>!\>:Map associating all active subscriptions on the device with the list of emergency numbers originating from that subscription. If there are no active subscriptions, the map will contain a single entry with [SubscriptionManager.INVALID_SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int) as the key and a list of emergency numbers as the value. If no emergency number information is available, the value will be null. |

### onImsCallDisconnectCauseChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onImsCallDisconnectCauseChanged(imsReasonInfo: ImsReasonInfo): Unit
```

**Deprecated:** *Use [TelephonyCallback.ImsCallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener) instead.*

Callback invoked when Ims call disconnect cause changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `imsReasonInfo` | [ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo): [ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo) contains details on why IMS call failed. This value cannot be`null`. |

### onMessageWaitingIndicatorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageWaitingIndicatorChanged(mwi: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.MessageWaitingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener) instead.*

Callback invoked when the message-waiting indicator changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String) 

### onPreciseDataConnectionStateChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPreciseDataConnectionStateChanged(dataConnectionState: PreciseDataConnectionState): Unit
```

**Deprecated:** *Use [TelephonyCallback.PreciseDataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener) instead.*

Callback providing update about the default/internet data connection on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

Requires permission [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or the calling app has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataConnectionState` | [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState): [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState) This value cannot be`null`. |

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

**Deprecated:** *Use [TelephonyCallback.RegistrationFailedListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.RegistrationFailedListener) instead.*

Report that Registration or a Location/Routing/Tracking Area update has failed.

Indicate whenever a registration procedure, including a location, routing, or tracking area update fails. This includes procedures that do not necessarily result in a change of the modem's registration status. If the modem's registration status changes, that is reflected in the onNetworkStateChanged() and subsequent get{Voice/Data}RegistrationState().

Because registration failures are ephemeral, this callback is not sticky. Registrants will not receive the most recent past value when registering. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cellIdentity` | [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity):the CellIdentity, which must include the globally unique identifier for the cell (for example, all components of the CGI or ECGI). This value cannot be`null`. |
| `chosenPlmn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a 5 or 6 digit alphanumeric PLMN (MCC|MNC) among those broadcast by the cell that was chosen for the failed registration attempt. This value cannot be`null`. |
| `domain` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):DOMAIN_CS, DOMAIN_PS or both in case of a combined procedure. |
| `causeCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the primary failure cause code of the procedure. For GSM/UMTS (MM), values are in TS 24.008 Sec 10.5.95 For GSM/UMTS (GMM), values are in TS 24.008 Sec 10.5.147 For LTE (EMM), cause codes are TS 24.301 Sec 9.9.3.9 For NR (5GMM), cause codes are TS 24.501 Sec 9.11.3.2 Integer.MAX_VALUE if this value is unused. |
| `additionalCauseCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the cause code of any secondary/combined procedure if appropriate. For UMTS, if a combined attach succeeds for PS only, then the GMM cause code shall be included as an additionalCauseCode. For LTE (ESM), cause codes are in TS 24.301 9.9.4.4. Integer.MAX_VALUE if this value is unused. |

### onServiceStateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceStateChanged(serviceState: ServiceState!): Unit
```

**Deprecated:** *Use [TelephonyCallback.ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener) instead.*

Callback invoked when device service state changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). The instance of [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState) passed as an argument here will have various levels of location information stripped from it depending on the location permissions that your app holds. Only apps holding the [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission will receive all the information in [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState), otherwise the cellIdentity will be null if apps only holding the [Manifest.permission.ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) permission. Network operator name in long/short alphanumeric format and numeric id will be null if apps holding neither [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) nor [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String). 
**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_EMERGENCY_ONLY:kotlin.Int)
- [android.telephony.ServiceState#STATE_IN_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_IN_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_OUT_OF_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_POWER_OFF](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_POWER_OFF:kotlin.Int) 

### onSignalStrengthChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSignalStrengthChanged(asu: Int): Unit
```

**Deprecated:** *Use [onSignalStrengthsChanged(android.telephony.SignalStrength)](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#onSignalStrengthsChanged(android.telephony.SignalStrength))*

Callback invoked when network signal strength changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_EMERGENCY_ONLY:kotlin.Int)
- [android.telephony.ServiceState#STATE_IN_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_IN_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_OUT_OF_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_POWER_OFF](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_POWER_OFF:kotlin.Int) 

### onSignalStrengthsChanged

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSignalStrengthsChanged(signalStrength: SignalStrength!): Unit
```

**Deprecated:** *Use [TelephonyCallback.SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener) instead.*

Callback invoked when network signal strengths changes on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 

### onUserMobileDataStateChanged

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUserMobileDataStateChanged(enabled: Boolean): Unit
```

**Deprecated:** *Use [TelephonyCallback.UserMobileDataStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener) instead.*

Callback invoked when the user mobile data state has changed on the registered subscription. Note, the registration subId comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers PhoneStateListener by [TelephonyManager.listen(PhoneStateListener, int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#listen(android.telephony.PhoneStateListener,%20kotlin.Int)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subId. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates whether the current user mobile data state is enabled or disabled. |
