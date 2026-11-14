Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionService

```
abstract class ConnectionService : Service
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.content.Context](../android.content/Context.md) ||||
| | ↳ | [android.content.ContextWrapper](../android.content/ContextWrapper.md) |||
| | | ↳ | [android.app.Service](../android.app/Service.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.telecom.ConnectionService](ConnectionService.md) |

An abstract service that should be implemented by any apps which either:

1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`.
2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`.

Once implemented, the needs to take the following steps so that Telecom will bind to it:

<br />

1. *Registration in AndroidManifest.xml* 

```kotlin
<service android:name="com.example.package.MyConnectionService"
     android:label="@string/some_label_for_my_connection_service"
     android:permission="android.permission.BIND_TELECOM_CONNECTION_SERVICE">
   <intent-filter>
    <action android:name="android.telecom.ConnectionService" />
   </intent-filter>
  </service>
  
```

2. *Registration of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager`.* 
See `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` and `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` for more information.

System managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`s must be enabled by the user in the phone app settings before Telecom will bind to them. Self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`s must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` permission in their manifest before Telecom will bind to them.

Once registered and enabled by the user in the phone app settings or granted permission, telecom will bind to a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` implementation when it wants that `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` to place a call or the service has indicated that is has an incoming call through `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)`. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` can then expect a call to `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` wherein it should provide a new instance of a `https://developer.android.com/reference/kotlin/android/telecom/Connection` object. It is through this `https://developer.android.com/reference/kotlin/android/telecom/Connection` object that telecom receives state updates and the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` receives call-commands such as answer, reject, hold and disconnect.

When there are no more live calls, telecom will unbind from the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`.

# Self-Managed Connection Services

NOTE: VoIP applications that want to integrate with the Telecom framework should transition to the new Telecom VoIP APIs which are wrapped by the [ConnectionService](https://developer.android.com/reference/androidx/core/telecom/CallsManager>Core
Telecom</a> Jetpack library.
<p>
A VoIP app can implement a <code><a docref=) to ensure that its calls are integrated into the Android platform. There are numerous benefits to using the Telecom APIs for a VoIP app:

- Call concurrency is handled - the user is able to swap between calls in different apps and on the mobile network.
- Simplified audio routing - the platform provides your app with a unified list of the audio routes which are available (e.g. `https://developer.android.com/reference/kotlin/android/telecom/Connection#onAvailableCallEndpointsChanged(kotlin.collections.MutableList)`) and a standardized way to switch audio routes (e.g. `https://developer.android.com/reference/kotlin/android/telecom/Connection#requestCallEndpointChange(android.telecom.CallEndpoint,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` ).
- Bluetooth integration - your calls will be visible on and controllable via bluetooth devices (e.g. car head units and headsets).
- Companion device integration - wearable devices such as watches which implement an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` can optionally subscribe to see self-managed calls. Similar to a bluetooth headunit, wearables will typically render your call using a generic call UX and provide the user with basic call controls such as hangup, answer, reject.
- Automotive calling experiences - Android supports automotive optimized experiences which provides a means for calls to be controlled and viewed in an automobile; these experiences are capable of leveraging call metadata provided by your app.

## Registering a Phone Account

Before your app can handle incoming or outgoing calls through Telecom it needs to register a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with Telecom indicating to the platform that your app is capable of calling.

Your app should create a new instance of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which meets the following requirements:

- Has `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` (set using `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.Builder#setCapabilities(kotlin.Int)`). This indicates to Telecom that your app will report calls but that it provides a primary UI for the calls by itself.
- Provide a unique identifier for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` via the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getId()` attribute. As per the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` documentation, you should NOT use an identifier which contains PII or other sensitive information. A typical choice is a UUID.

Your app should register the new `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with Telecom using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)`. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s persist across reboot. You can use `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getOwnSelfManagedPhoneAccounts()` to confirm the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` you registered. Your app should generally only register a single `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`.

## Implementing ConnectionService

Your app uses `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)` to start new outgoing calls and `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` to report new incoming calls. Calling these APIs causes the Telecom stack to bind to your app's `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` implementation. Telecom will either inform your app that it cannot handle a call request at the current time (i.e. there could be an ongoing emergency call, which means your app is not allowed to handle calls at the current time), or it will ask your app to create a new instance of `https://developer.android.com/reference/kotlin/android/telecom/Connection` to represent a call in your app. Your app should implement the following `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` methods:

- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - called by Telecom to ask your app to make a new `https://developer.android.com/reference/kotlin/android/telecom/Connection` to represent an outgoing call your app requested via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)`.
- \<`https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - called by Telecom to inform your app that a call it reported via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)` cannot be handled at this time. Your app should NOT place a call at the current time.
- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - called by Telecom to ask your app to make a new `https://developer.android.com/reference/kotlin/android/telecom/Connection` to represent an incoming call your app reported via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)`.
- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - called by Telecom to inform your app that an incoming call it reported via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` cannot be handled at this time. Your app should NOT post a new incoming call notification and should silently reject the call.

## Implementing a Connection

Your app should extend the `https://developer.android.com/reference/kotlin/android/telecom/Connection` class to represent calls in your app. When you create new instances of your `https://developer.android.com/reference/kotlin/android/telecom/Connection`, you should ensure the following properties are set on the new `https://developer.android.com/reference/kotlin/android/telecom/Connection` instance returned by your `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`:

- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setAddress(android.net.Uri,%20kotlin.Int)` - the identifier for the other party. For apps that user phone numbers the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` can be a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_TEL:kotlin.String` URI representing the phone number.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setCallerDisplayName(kotlin.String,%20kotlin.Int)` - the display name of the other party. This is what will be shown on Bluetooth devices and other calling surfaces such as wearable devices. This is particularly important for calls that do not use a phone number to identify the caller or called party.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setConnectionProperties(kotlin.Int)` - ensure you set `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_SELF_MANAGED:kotlin.Int` to identify to the platform that the call is handled by your app.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setConnectionCapabilities(kotlin.Int)` - if your app supports making calls inactive (i.e. holding calls) you should get `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_HOLD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_HOLD:kotlin.Int` to indicate to the platform that you calls can potentially be held for concurrent calling scenarios.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setAudioModeIsVoip(kotlin.Boolean)` - set to `true` to ensure that the platform knows your call is a VoIP call.
- For newly created `https://developer.android.com/reference/kotlin/android/telecom/Connection` instances, do NOT change the state of your call using `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()`, `https://developer.android.com/reference/kotlin/android/telecom/Connection#setOnHold()` until the call is added to Telecom (ie you have returned it via `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`).

## How to Place Outgoing Calls

When your app wants to place an outgoing call it calls `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)`. You should specify a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to identify who the call is being placed to, and specify the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` associated with the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` you registered for your app using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` in the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter.

Telecom will bind to your app's `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` implementation and call either:

- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getAddress()` will match the address you specified when placing the call. You should return a new instance of your app's `https://developer.android.com/reference/kotlin/android/telecom/Connection` class to represent the outgoing call.
- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - your app should not place the call at this time; the call should be cancelled and the user informed that the call cannot be placed.

New outgoing calls will start in a `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DIALING:kotlin.Int` state. This state indicates that your app is in the process of connecting the call to the other party.

Once the other party answers the call (or it is set up successfully), your app should call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()` to inform Telecom that the call is now active.

## How to Add Incoming Calls

When your app receives an incoming call, it should call `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)`. Set the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` parameter to the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` associated with your app's `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`.

Telecom will bind to your app's `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` implementation and call either:

- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - You should return a new instance of your app's `https://developer.android.com/reference/kotlin/android/telecom/Connection` class to represent the incoming call.
- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` - your app should not receive the call at this time; the call should be rejected silently; the user may be informed of a missed call.

New incoming calls will start with a `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` state. This state indicates that your app has a new incoming call pending. Telecom will NOT play a ringtone or post a notification for your app. It is up to your app to post an incoming call notification with an associated ringtone. Telecom will call `https://developer.android.com/reference/kotlin/android/telecom/Connection#onShowIncomingCallUi()` on the `https://developer.android.com/reference/kotlin/android/telecom/Connection` when your app can post its incoming call notification. See `https://developer.android.com/reference/kotlin/android/telecom/Connection#onShowIncomingCallUi()` for more information on how to post the notification.

Your incoming call notification (or full screen UI) will typically have an "answer" and "decline" action which the user chooses. When your app receives the "answer" or "decline" `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`, you should must call either `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()` to inform Telecom that the call was answered, or `https://developer.android.com/reference/kotlin/android/telecom/Connection#setDisconnected(android.telecom.DisconnectCause)` to inform Telecom that the call was rejected. If the call was rejected, supply an instance of `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` with `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int`, and then call `https://developer.android.com/reference/kotlin/android/telecom/Connection#destroy()`.

In addition to handling requests to answer or decline the call via notification actions, your app should also be implement the `https://developer.android.com/reference/kotlin/android/telecom/Connection#onAnswer(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#onAnswer()` methods on the `https://developer.android.com/reference/kotlin/android/telecom/Connection`. These will be raised if the user answers your call via a Bluetooth device or another device like a wearable or automotive calling UX. In response, your app should call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()` to inform Telecom that the call was answered.

Additionally, your app should implement `https://developer.android.com/reference/kotlin/android/telecom/Connection#onReject()` to handle requests to reject the call which are raised via Bluetooth or other calling surfaces. Your app should call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setDisconnected(android.telecom.DisconnectCause)` and supply an instance of `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` with `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` in this case.

## Ending Calls

When an ongoing active call (incoming or outgoing) has ended, your app is responsible for informing Telecom that the call ended.

Your app calls:

- `https://developer.android.com/reference/kotlin/android/telecom/Connection#setDisconnected(android.telecom.DisconnectCause)` - this informs Telecom that the call has terminated. You should provide a new instance of `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` with either `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` to indicate where the call disconnection took place. `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` indicates that the call terminated in your app on the current device (i.e. via user action), where `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` indicates that the call terminates on the remote device.
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#destroy()` - this informs Telecom that your call instance can be cleaned up. You should always call this when you are finished with a call.

Similar to answering incoming calls, requests to disconnect your call may originate from outside your app. You can handle these by implementing `https://developer.android.com/reference/kotlin/android/telecom/Connection#onDisconnect()`. Your app should call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setDisconnected(android.telecom.DisconnectCause)` with an instance of `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause` and reason `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` to indicate to Telecom that your app has disconnected the call as requested based on the user's request.

## Holding and Unholding Calls

When your app specifies `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_HOLD:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_HOLD:kotlin.Int` on your `https://developer.android.com/reference/kotlin/android/telecom/Connection` instance, it is telling Telecom that your calls can be placed into a suspended, or "held" state if required. If your app supports holding its calls, it will be possible for the user to switch between calls in your app and holdable calls in another app or on the mobile network. If your app does not support holding its calls, you may receive a request to disconnect the call from Telecom if the user opts to answer an incoming call in another app or on the mobile network; this ensures that the user can only be in one call at a time.

Your app is free to change a call between the held and active state using `https://developer.android.com/reference/kotlin/android/telecom/Connection#setOnHold()` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()`.

Your app may receive a request from Telecom to hold or unhold a call via `https://developer.android.com/reference/kotlin/android/telecom/Connection#onHold()` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#onUnhold()`. Telecom can ask your app to hold or unhold its `https://developer.android.com/reference/kotlin/android/telecom/Connection` either if the user requests this action through another calling surface such as Bluetooth, or if the user answers or switches to a call in a different app or on the mobile network.

When your app receives an `https://developer.android.com/reference/kotlin/android/telecom/Connection#onHold()` it must call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setOnHold()` to inform Telecom that the call has been held successfully.

When your app receives an `https://developer.android.com/reference/kotlin/android/telecom/Connection#onUnhold()` it must call `https://developer.android.com/reference/kotlin/android/telecom/Connection#setActive()` to inform Telecom that the call has been resumed successfully.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#SERVICE_INTERFACE:kotlin.String` The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that must be declared as handled by the service. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCESSIBILITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#` for giving the user feedback for UI events through the registered event listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACCOUNT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global system state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ADVANCED_PROTECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APPWIDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` for accessing AppWidgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_FUNCTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager.html#` for executing app functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_INTERACTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager.html#` for managing app interactions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_OPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` for tracking application operations on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#APP_SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#` for indexing and querying app data managed by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUDIO_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#` for handling management of volume, ringer modes and audio routing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#AUTOFILL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`

Flag for #bindService: indicates that the client application binding to this service considers the service to be more important than the app itself. When set, the platform will try to have the out of memory killer kill the app before it kills the service it is bound to, though this is not guaranteed to be the case.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`

Flag for #bindService: If binding from an activity, allow the target service's process importance to be raised based on whether the activity is visible to the user, regardless whether another flag is used to reduce the amount that the client process's overall importance is used to impact it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_ACTIVITY_STARTS:kotlin.Int`

Flag for #bindService: If binding from an app that is visible, the bound service is allowed to start an activity from background. This was the default behavior before SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`. Since then, the default behavior changed to disallow the bound service to start a background activity even if the app bound to it is in foreground, unless this flag is specified when binding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`

Flag for #bindService: allow the process hosting the bound service to go through its normal memory management. It will be treated more like a running service, allowing the system to (temporarily) expunge the process if low on memory or for some other whim it may have, and being more aggressive about making it a candidate to be killed (and restarted) if running for a long time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int`

Flag for #bindService: automatically create the service as long as the binding exists. Note that while this will create the service, its `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method will still only be called due to an explicit call to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. Even without that, though, this still provides you with access to the service object while the service is created.

Note that prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, not supplying this flag would also impact how important the system consider's the target service's process to be. When set, the only way for it to be raised was by binding from a service in which case it will only be important when that activity is in the foreground. Now to achieve this behavior you must explicitly supply the new flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. For compatibility, old applications that don't specify `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` will automatically have the flags `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` set for them in order to achieve the same result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_DEBUG_UNBIND:kotlin.Int`

Flag for #bindService: include debugging help for mismatched calls to unbind. When this flag is set, the callstack of the following `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` call is retained, to be printed if a later incorrect unbind call is made. Note that doing this requires retaining information about the binding that was made for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`

Flag for #bindService: The service being bound is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#externalService:kotlin.Int` service. This binds the service into the calling application's package, rather than the package in which the service is declared.

When using this flag, the code for the service being bound will execute under the calling application's package name and user ID. Because the service must be an isolated process, it will not have direct access to the application's data, though. The purpose of this flag is to allow applications to provide services that are attributed to the app using the service, rather than the application providing the service.
*This flag is NOT compatible with `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`. If you need to use `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`, you must use `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long` instead.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long`

Works in the same way as `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`, but it's defined as a `long` value that is compatible to `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`

Flag for #bindService: this service is very important to the client, so should be brought to the foreground process level when the client is. Normally a process can only be raised to the visibility level by a client, even if that client is in the foreground.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_INCLUDE_CAPABILITIES:kotlin.Int`

Flag for #bindService: If binding from an app that has specific capabilities due to its foreground state such as an activity or foreground service, then this flag will allow the bound app to get the same capabilities, as long as it has the required permissions as well. If binding from a top app and its target SDK version is at or above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the app needs to explicitly use BIND_INCLUDE_CAPABILITIES flag to pass all capabilities to the service so the other app can have while-in-use access such as location, camera, microphone from background. If binding from a top app and its target SDK version is below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, BIND_INCLUDE_CAPABILITIES is implicit.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`

Flag for #bindService: don't allow this binding to raise the target service's process to the foreground scheduling priority. It will still be raised to at least the same memory priority as the client (so that its process will not be killable in any situation where the client is not killable), but for CPU scheduling purposes it may be left in the background. This only has an impact in the situation where the binding client is a foreground process and the target service is in a background process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

Flag for #bindService: If binding from an app that is visible or user-perceptible, lower the target service's importance to below the perceptible level. This allows the system to (temporarily) expunge the bound process from memory to make room for more important user-perceptible processes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_PACKAGE_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process, but only with other isolated services from the same package that declare the same process name.

Specifying this flag allows multiple isolated services defined in the same package to be running in a single shared isolated process. This shared isolated process must be specified since this flag will not work with the default application process.

This flag is different from `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` since it only allows binding services from the same package in the same shared isolated process. This also means the shared package isolated process is global, and not scoped to each potential calling app.

The shared isolated process instance is identified by the "android:process" attribute defined by the service. This flag cannot be used without this attribute set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process. Specifying this flag allows multiple isolated services to be running in a single shared isolated process. The shared isolated process instance is identified by the instanceName parameter in `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)`. Subsequent calls to #bindIsolatedService with the same instanceName will cause the isolated service to be co-located in the same shared isolated process. Note that the shared isolated process is scoped to the calling app; once created, only the calling app can bind additional isolated services into the shared process. However, the services themselves can come from different APKs and therefore different vendors. Only services that set the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowSharedIsolatedProcess:kotlin.Int` attribute to `true` are allowed to be bound into a shared isolated process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`

Flag for #bindService: don't impact the scheduling or memory management priority of the target service's hosting process. Allows the service's process to be managed on the background LRU list just like a regular application process in the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BIOMETRIC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#` for handling biometric and PIN/pattern/password authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLOB_STORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.html#` for contributing and accessing data blobs from the blob store maintained by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BLUETOOTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager.html#` for using Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#BUGREPORT_SERVICE:kotlin.String`

Service to capture a bugreport.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAMERA_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#` for interacting with camera devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CAPTIONING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.html#` for obtaining captioning properties and listening for changes in captioning preferences.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CARRIER_CONFIG_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#` for reading carrier configuration values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CHOOSER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager.html#`.

**Note:** This service is not available on Wear OS, Android TV, or Android Auto devices. On these form factors, calls to `getSystemService` for this service will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CLIPBOARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#` for accessing and modifying the contents of the global clipboard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#COMPANION_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` for managing companion devices

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_DIAGNOSTICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager.html#` for performing network connectivity diagnostics as well as receiving network connectivity information from the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONSUMER_IR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.html#` for transmitting infrared signals from the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTACT_KEYS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager.html#` to managing contact keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTENT_RESTRICTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_IGNORE_SECURITY:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: ignore any security restrictions on the Context being requested, allowing it to always be loaded. For use with `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` to allow code to be loaded into a process even when it isn't safe to do so. Use with extreme care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: include the application code with the context. This means loading code into the caller's process, so that `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` can be used to instantiate the application's classes. Setting this flags imposes security restrictions on what application context you can access; if the requested application can not be safely loaded into your process, java.lang.SecurityException will be thrown. If this flag is not set, there will be no restrictions on the packages that can be loaded, but `https://developer.android.com/reference/kotlin/android/content/Context.html#getClassLoader()` will always return the default system class loader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_RESTRICTED:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)`: a restricted context may disable specific features. For instance, a View associated with a restricted context would ignore particular XML attributes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CREDENTIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` to authenticate a user to your app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#CROSS_PROFILE_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps.html#` for cross profile operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

The default device ID, which is the ID of the primary (non-virtual) device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_INVALID:kotlin.Int`

Invalid device ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_LOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` for working with global device policy management.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` to handle display hashes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` for interacting with display devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` to retrieve approval and user state for declared web domains.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#DROPBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#` instance for recording diagnostic logs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#EUICC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager.html#` to manage the device eUICC (embedded SIM).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_INTEGRITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/FileIntegrityManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#FILE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/FileManager.html#` for handling file operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GAME_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GameManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing the hardware properties service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HEALTHCONNECT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#HID_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager.html#` for interacting with HID devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for accessing input methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#` for interacting with input devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for encrypting Sockets or Networks with IPSec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` instance for managing occasional background tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYCHAIN_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/KeyChainManager.html#` for managing KeyChain certificates and grants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYSTORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager.html#` for accessing [Android Keystore](../privacy-and-security/keystore.md) functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAUNCHER_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#` for querying and monitoring launchable apps across profiles of a user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCALE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/LocaleManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_COMMUNICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager.html#` for managing `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_METRICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager.html#` for interacting with media metrics on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_PROJECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager.html#` instance for managing media projection sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_QUALITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.html#` for standardize picture and audio API parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_ROUTER_SERVICE:kotlin.String`

Use with #getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` for controlling and managing routing of media.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_SESSION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.html#` for managing media Sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MEMORY_BUDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.html#` for monitoring memory budgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MIDI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#` for accessing the MIDI service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_APPEND:kotlin.Int`

File creation mode: for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)`, if the file already exists then write data to the end of the existing file instead of erasing it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`

Database open flag: when set, the database is opened with write-ahead logging enabled by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_MULTI_PROCESS:kotlin.Int`

SharedPreference loading flag: when set, the file on disk will be checked for modification even if the shared preferences instance is already loaded in this process. This behavior is sometimes desired in cases where the application has multiple processes, all writing to the same SharedPreferences file. Generally there are better forms of communication between processes, though.

This was the legacy (but undocumented) behavior in and before Gingerbread (Android 2.3) and this flag is implied when targeting such releases. For applications targeting SDK versions *greater than* Android 2.3, this flag must be explicitly set if desired.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int`

Database open flag: when set, the database is opened without support for localized collators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_PRIVATE:kotlin.Int`

File creation mode: the default mode, where the created file can only be accessed by the calling application (or all applications sharing the same user ID).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_READABLE:kotlin.Int`

File creation mode: allow all other applications to have read access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode throws a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_WORLD_WRITEABLE:kotlin.Int`

File creation mode: allow all other applications to have write access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve the service that plays multisensory feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NFC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/nfc/NfcManager.html#` for using NFC.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NPU_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#NSD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.html#` for handling management of network service discovery

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#OVERLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager.html#` for managing overlay packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PCC_SANDBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PEOPLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to access a `https://developer.android.com/reference/kotlin/android/app/people/PeopleManager.html#` to interact with your published conversations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERFORMANCE_HINT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.html#` for accessing the performance hinting service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/persistentdata/PersistentDataBlockManager.html#` instance for interacting with a storage device that lives across factory resets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management, including "wake locks," which let you keep the device on while you're running long tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PRINT_SERVICE:kotlin.String`

`https://developer.android.com/reference/kotlin/android/print/PrintManager.html#` for printing and managing printers and print tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#PROFILING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/os/ProfilingManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=true"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver cannot receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=false"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from Instant Apps.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#RESTRICTIONS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager.html#` for retrieving application restrictions and requesting permissions for restricted operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#ROLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#` for managing roles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SATELLITE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager.html#` for accessing satellite functionality.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling searches.

`https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int` does not support `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SECURITY_STATE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager.html#` for accessing the security state manager service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SENSOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` for accessing sensors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SERIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialManager.html#` for access to serial ports.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#` for accessing the launcher shortcut service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STATUS_BAR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/StatusBarManager.html#` for interacting with the status bar and quick settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#` for accessing system storage functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#STORAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/StorageStatsManager.html#` for accessing system storage statistics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#SYSTEM_HEALTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager.html#` for accessing system health (battery, power, memory, etc) metrics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELECOM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager` to manage telecom-related features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_IMS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager.html#` for parsing phone numbers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#` for handling management the telephony features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#` for handling management the telephony subscriptions of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TETHERING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.html#` for managing tethering functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_CLASSIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager.html#` for text classification services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textservice/TextServicesManager.html#` for accessing text services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TIME_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/time/TimeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_AD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.html#` for interacting with TV client-side advertisement services on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager.html#` for interacting with TV inputs on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#TV_INTERACTIVE_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.html#` for interacting with TV interactive applications on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#` for querying device usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#` for access to USB devices (as a USB host) and for controlling this device's behavior as a USB device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#USER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for managing users on devices that support multiple users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibration hardware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VIRTUAL_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.html#` for managing virtual devices. On devices without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` system feature the `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#VPN_MANAGEMENT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` to manage profiles for the platform built-in VPN.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a com.android.server.WallpaperService for accessing wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WEB_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for handling management of Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for handling management of Wi-Fi peer-to-peer connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_RTT_RANGING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager.html#` for ranging devices with wifi.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for handling management of Wi-Fi access.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` for accessing the system's window manager.

<br />

From class `https://developer.android.com/reference/kotlin/android/app/Service.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_CONTINUATION_MASK:kotlin.Int`

Bits returned by `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` describing how to continue the service if it is killed. May be `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#START_NOT_STICKY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_FLAG_REDELIVERY:kotlin.Int`

This flag is set in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` if the Intent is a re-delivery of a previously delivered intent, because the service had previously returned `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int` but had been killed before calling `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` for that Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_FLAG_RETRY:kotlin.Int`

This flag is set in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` if the Intent is a retry because the original attempt never got to or returned from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_NOT_STICKY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), and there are no new start intents to deliver to it, then take the service out of the started state and don't recreate until a future explicit call to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. The service will not receive a `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` call with a null Intent because it will not be restarted if there are no pending Intents to deliver.

This mode makes sense for things that want to do some work as a result of being started, but can be stopped when under memory pressure and will explicit start themselves again later to do more work. An example of such a service would be one that polls for data from a server: it could schedule an alarm to poll every N minutes by having the alarm start its service. When its `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` is called from the alarm, it schedules a new alarm for N minutes later, and spawns a thread to do its networking. If its process is killed while doing that check, the service will not be restarted until the alarm goes off.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_REDELIVER_INTENT:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), then it will be scheduled for a restart and the last delivered Intent re-delivered to it again via `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`. This Intent will remain scheduled for redelivery until the service calls `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` with the start ID provided to `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`. The service will not receive a `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` call with a null Intent because it will only be restarted if it is not finished processing all Intents sent to it (and any such pending events will be delivered at the point of restart).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: if this service's process is killed while it is started (after returning from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`), then leave it in the started state but don't retain this delivered intent. Later the system will try to re-create the service. Because it is in the started state, it will guarantee to call `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` after creating the new service instance; if there are not any pending start commands to be delivered to the service, it will be called with a null intent object, so you must take care to check for this.

This mode makes sense for things that will be explicitly started and stopped to run for arbitrary periods of time, such as a service performing background music playback.

Since Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or above are disallowed to start a foreground service from the background, but the restriction doesn't impact *restarts* of a sticky foreground service. However, when apps start a sticky foreground service from the background, the same restriction still applies.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`

Constant to return from `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`: compatibility version of `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int` that does not guarantee that `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` will be called again after being killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_DETACH:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: if set, the notification previously supplied to #startForeground will be detached from the service's lifecycle. The notification will remain shown even after the service is stopped and destroyed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_LEGACY:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: equivalent to passing `false` to the legacy API `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_REMOVE:kotlin.Int`

Selector for `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`: if supplied, the notification previously supplied to #startForeground will be cancelled and removed from display.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#ConnectionService()()` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#addConference(android.telecom.Conference)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference!)` Adds a new conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#addConferenceFromConnection(android.telecom.Conference,%20android.telecom.Connection)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference, originalConnection: https://developer.android.com/reference/kotlin/android/telecom/Connection)` This is used to make a `https://developer.android.com/reference/kotlin/android/telecom/Connection` become a `https://developer.android.com/reference/kotlin/android/telecom/Conference` when the remote party merges calls together. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#addExistingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.Connection)(phoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, connection: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Adds a connection created by the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and informs telecom of the new connection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#conferenceRemoteConnections(android.telecom.RemoteConnection,%20android.telecom.RemoteConnection)(remoteConnection1: https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection!, remoteConnection2: https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection!)` Indicates to the relevant `RemoteConnectionService` that the specified `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection`s should be merged into a conference call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#connectionServiceFocusReleased()()` Call to inform Telecom that your `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has released call resources (e.g microphone, camera). |
| [RemoteConference](RemoteConference.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#createRemoteIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle?, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest?)` Ask some other `ConnectionService` to create a `RemoteConference` given an incoming request. |
| --- | --- |
| [RemoteConnection](RemoteConnection.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#createRemoteIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest)` Ask some other `ConnectionService` to create a `RemoteConnection` given an incoming request. |
| [RemoteConference](RemoteConference.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#createRemoteOutgoingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle?, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest?)` Ask some other `ConnectionService` to create a `RemoteConference` given an outgoing request. |
| [RemoteConnection](RemoteConnection.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#createRemoteOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest)` Ask some other `ConnectionService` to create a `RemoteConnection` given an outgoing request. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Conference](Conference.md)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#getAllConferences()()` Returns all the active `Conference`s for which this `ConnectionService` has taken responsibility. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Connection](Connection.md)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#getAllConnections()()` Returns all the active `Connection`s for which this `ConnectionService` has taken responsibility. |
| [IBinder](../android.os/IBinder.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onBind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Return the communication channel to the service. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConference(android.telecom.Connection,%20android.telecom.Connection)(connection1: https://developer.android.com/reference/kotlin/android/telecom/Connection!, connection2: https://developer.android.com/reference/kotlin/android/telecom/Connection!)` Conference two specified connections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConferenceAdded(android.telecom.Conference)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference)` Called when a conference is added. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConferenceRemoved(android.telecom.Conference)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference)` Called when a conference is removed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionAdded(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection)` Called when a connection is added. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionRemoved(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection)` Called when a connection is removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionServiceFocusGained()()` Called when the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has gained the call focus. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionServiceFocusLost()()` Called when the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has lost the call focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateConferenceComplete(android.telecom.Conference)(conference: https://developer.android.com/reference/kotlin/android/telecom/Conference)` Called by Telecom after the `https://developer.android.com/reference/kotlin/android/telecom/Conference` returned by `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` has been added to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and sent to Telecom. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateConnectionComplete(android.telecom.Connection)(connection: https://developer.android.com/reference/kotlin/android/telecom/Connection)` Called by Telecom after the `https://developer.android.com/reference/kotlin/android/telecom/Connection` returned by `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` has been added to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and sent to Telecom. |
| --- | --- |
| open [Conference](Conference.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest)` Create a `Conference` given an incoming request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConferenceFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle?, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest?)` Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Conference` was denied. |
| open [Connection](Connection.md)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Create a `Connection` given an incoming request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Connection` was denied. |
| open [Connection](Connection.md)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingHandoverConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(fromPhoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Called by Telecom to request that a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` creates an instance of an incoming handover `https://developer.android.com/reference/kotlin/android/telecom/Connection`. |
| open [Conference](Conference.md)? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest)` Create a `Conference` given an outgoing request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConferenceFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest)` Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Conference` was denied. |
| open [Connection](Connection.md)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Create a `Connection` given an outgoing request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnectionFailed(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(connectionManagerPhoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Connection` was denied. |
| --- | --- |
| open [Connection](Connection.md)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingHandoverConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)(fromPhoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!)` Called by Telecom to request that a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` creates an instance of an outgoing handover `https://developer.android.com/reference/kotlin/android/telecom/Connection`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onHandoverFailed(android.telecom.ConnectionRequest,%20kotlin.Int)(request: https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest!, error: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called by Telecom in response to a `TelecomManager#acceptHandover()` invocation which failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onRemoteConferenceAdded(android.telecom.RemoteConference)(conference: https://developer.android.com/reference/kotlin/android/telecom/RemoteConference!)` Indicates that a remote conference has been created for existing `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection`s. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onRemoteExistingConnectionAdded(android.telecom.RemoteConnection)(connection: https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection!)` Called when an existing connection is added remotely. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onUnbind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Called when all clients have disconnected from a particular interface published by the service. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/app/Service.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#attachBaseContext(android.content.Context)(newBase: https://developer.android.com/reference/kotlin/android/content/Context.html#!)`

Set the base context for this ContextWrapper. All calls will then be delegated to the base context. Throws IllegalStateException if a base context has already been set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)`

Print the Service's state into the given stream. This gets invoked if you run "adb shell dumpsys activity service \<yourservicename\>" (note that for this command to work, the service must be running, and you must specify a fully-qualified service name). This is distinct from "dumpsys \<servicename\>", which only works for named system services and which invokes the `https://developer.android.com/reference/kotlin/android/os/IBinder.html#dump(java.io.FileDescriptor,%20kotlin.Array)` method on the `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` interface registered with ServiceManager.

<br />

`https://developer.android.com/reference/kotlin/android/app/Application.html#!` `https://developer.android.com/reference/kotlin/android/app/Service.html#getApplication()()`

Return the application that owns this service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#getForegroundServiceType()()`

If the service has become a foreground service by calling `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` or `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/app/Service.html#getForegroundServiceType()` returns the current foreground service type.

If there is no foregroundServiceType specified in manifest, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` is returned.

If the service is not a foreground service, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int` is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onCreate()()`

Called by the system when the service is first created. Do not call this method directly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onDestroy()()`

Called by the system to notify a Service that it is no longer used and is being removed. The service should clean up any resources it holds (threads, registered receivers, etc) at this point. Upon return, there will be no more calls in to this Service object and it is effectively dead. Do not call this method directly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onRebind(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Called when new clients have connected to the service, after it had previously been notified that all had disconnected in its `https://developer.android.com/reference/kotlin/android/app/Service.html#onUnbind(android.content.Intent)`. This will only be called if the implementation of `https://developer.android.com/reference/kotlin/android/app/Service.html#onUnbind(android.content.Intent)` was overridden to return true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called by the system every time a client explicitly starts the service by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, providing the arguments it supplied and a unique integer token representing the start request. Do not call this method directly.

For backwards compatibility, the default implementation calls `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)` and returns either `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Service.html#START_STICKY_COMPATIBILITY:kotlin.Int`.

Note that the system calls this on your service's main thread. A service's main thread is the same thread where UI operations take place for Activities running in the same process. You should always avoid stalling the main thread's event loop. When doing long-running operations, network calls, or heavy disk I/O, you should kick off a new thread, or use `https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTaskRemoved(android.content.Intent)(rootIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

This is called if the service is currently running and the user has removed a task that comes from the service's application. If you have set `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FLAG_STOP_WITH_TASK:kotlin.Int` then you will not receive this callback; instead, the service will simply be stopped.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Callback called on timeout for `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int`. See `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` for more details.

If the foreground service of type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` doesn't finish even after it's timed out, the app will be declared an ANR after a short grace period of several seconds.

Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)` will also be called when a foreground service of type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` times out. Developers do not need to implement both of the callbacks on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and onwards.

Note, even though `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SHORT_SERVICE:kotlin.Int` was added on Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, it can be also used on on prior android versions (just like other new foreground service types can be used). However, because `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` did not exist on prior versions, it will never called on such versions. Because of this, developers must make sure to stop the foreground service even if `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int)` is not called on such versions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTimeout(kotlin.Int,%20kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fgsType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Callback called when a particular foreground service type has timed out.

This callback is meant to give the app a small grace period of a few seconds to finish the foreground service of the associated type - if it fails to do so, the app will crash.

The foreground service of the associated type can be stopped within the time limit by `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` or their overloads. `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` can be used as well, which demotes the service to a "background" service, which will soon be stopped by the system.

The specific time limit for each type (if one exists) is mentioned in the documentation for that foreground service type. See `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_DATA_SYNC:kotlin.Int` for example.

Note: time limits are restricted to a rolling 24-hour window - for example, if a foreground service type has a time limit of 6 hours, that time counter begins as soon as the foreground service starts. This time limit will only be reset once every 24 hours or if the app comes into the foreground state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, notification: https://developer.android.com/reference/kotlin/android/app/Notification.html#!)`

If your service is started (running through `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`), then also make this service run in the foreground, supplying the ongoing notification to be shown to the user while in this state. By default started services are background, meaning that their process won't be given foreground CPU scheduling (unless something else in that process is foreground) and, if the system needs to kill them to reclaim more memory (such as to display a large page in a web browser), they can be killed without too much harm. You use #startForeground if killing your service would be disruptive to the user, such as if your service is performing background music playback, so the user would notice if their music stopped playing.

Note that calling this method does *not* put the service in the started state itself, even though the name sounds like it. You must always call `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent)` first to tell the system it should keep the service running, and then use this method to tell it to keep it running harder.

Apps targeting API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` or later must request the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FOREGROUND_SERVICE:kotlin.String` in order to use this API.

Apps built with SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or later can specify the foreground service types using attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` in service element of manifest file. The value of attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` can be multiple flags ORed together.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](https://developer.android.com/about/versions/12/behavior-changes-12) for more details.

<br />

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher are not allowed to start foreground services without specifying a valid foreground service type in the manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`. See [Behavior changes: Apps targeting Android 14](https://developer.android.com/about/versions/14/behavior-changes-14) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, notification: https://developer.android.com/reference/kotlin/android/app/Notification.html#, foregroundServiceType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

An overloaded version of `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` with additional foregroundServiceType parameter.

Apps built with SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or later can specify the foreground service types using attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` in service element of manifest file. The value of attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int` can be multiple flags ORed together.

The foregroundServiceType parameter must be a subset flags of what is specified in manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`, if not, an IllegalArgumentException is thrown. Specify foregroundServiceType parameter as `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MANIFEST:kotlin.Int` to use all flags that is specified in manifest attribute foregroundServiceType.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](https://developer.android.com/about/versions/12/behavior-changes-12) for more details.

<br />

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher are not allowed to start foreground services without specifying a valid foreground service type in the manifest attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int`, and the parameter `foregroundServiceType` here must not be the `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_NONE:kotlin.Int`. See [Behavior changes: Apps targeting Android 14](https://developer.android.com/about/versions/14/behavior-changes-14) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Boolean)(removeNotification: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Legacy version of `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)(notificationBehavior: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove this service from foreground state, allowing it to be killed if more memory is needed. This does not stop the service from running (for that you use `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()` or related methods), just takes it out of the foreground state.

If `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_REMOVE:kotlin.Int` is supplied, the service's associated notification will be cancelled immediately.

If `https://developer.android.com/reference/kotlin/android/app/Service.html#STOP_FOREGROUND_DETACH:kotlin.Int` is supplied, the service's association with the notification will be severed. If the notification had not yet been shown, due to foreground-service notification deferral policy, it is immediately posted when `stopForeground(STOP_FOREGROUND_DETACH)` is called. In all cases, the notification remains shown even after this service is stopped fully and destroyed.

If `zero` is passed as the argument, the result will be the legacy behavior as defined prior to Android L: the notification will remain posted until the service is fully stopped, at which time it will automatically be cancelled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf()()`

Stop the service, if it was previously started. This is the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` for this particular service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Old version of `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelfResult(kotlin.Int)` that doesn't return a result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelfResult(kotlin.Int)(startId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Stop the service if the most recent time it was started was startId. This is the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` for this particular service but allows you to safely avoid stopping if there is a start request from a client that you haven't yet seen in `https://developer.android.com/reference/kotlin/android/app/Service.html#onStart(android.content.Intent,%20kotlin.Int)`.

*Be careful about ordering of your calls to this function.*. If you call this function with the most-recently received ID before you have called it for previously received IDs, the service will be immediately stopped anyway. If you may end up processing IDs out of order (such as by dispatching them on separate threads), then you are responsible for stopping them in the same order you received them.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. In other words, you can use this to bind to a service that has specified `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` and, in addition to the existing behavior of running in an isolated process, you can also through the arguments here have the system bring up multiple concurrent processes hosting their own instances of that service. The instanceName you provide here identifies the different instances, and you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)` to tell the system how it should manage each of these instances.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Connects to an application service, creating it if needed. This defines a dependency between your application and the service. The given conn will receive the service object when it is created and be told if it dies and restarts. The service will be considered required by the system only for as long as the calling context exists. For example, if this Context is an Activity that is stopped, the service will not be required to continue running until the Activity is resumed.

If the service does not support binding, it may return `null` from its `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)` method. If it does, then the ServiceConnection's `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onNullBinding(android.content.ComponentName)` method will be invoked instead of `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onServiceConnected(android.content.ComponentName,%20android.os.IBinder)`.

**Note:** This method *cannot* be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component. A pattern you can use to communicate from a BroadcastReceiver to a Service is to call `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)` with the arguments containing the command to be sent, with the service calling its `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` method when done executing that command. See the API demo App/Service/Service Start Arguments Controller for an illustration of this. It is okay, however, to use this method from a BroadcastReceiver that has been registered with #registerReceiver, since the lifetime of this BroadcastReceiver is tied to another object (the one that registered it).

This method only accepts a int type flag, to pass in a long type flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` with executor to control ServiceConnection callbacks.

This method only accepts a 32 bits flag, to pass in a 64 bits flag, call `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`

Binds to a service in the given `user` in the same manner as #bindService.

Requires that one of the following conditions are met:

- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS_FULL`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is the same package as the `service` (determined by its component's package) and the Android version is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is in same profile group as the given `user`
- caller has `android.Manifest.permission.INTERACT_ACROSS_PROFILES` and is in same profile group as the given `user` and is the same package as the `service`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC *or you* have been granted a particular permission. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingPermission(kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingOrSelfUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether the calling process of an IPC you are handling has been granted a particular permission. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkCallingOrSelfPermission(kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a specific URI. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkCallingUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the calling process and uid has been granted permission to access a list of URIs. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkContentUriPermissionFull(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific content URI.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, this method checks for general access to the URI's content provider, as well as explicitly granted permissions.

Note, this check will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for non-content URIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether the given permission is allowed for a particular process and user ID running in the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Determine whether *you* have been granted a particular permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a specific URI. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Check both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and #checkUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Determine whether a particular process and uid has been granted permission to access a list of URIs. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail. **Note:** On SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, calling this method from a secondary-user's context will incorrectly return `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` for all {code uris}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#clearWallpaper()()`

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createAttributionContext(kotlin.String)(attributionTag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Return a new Context object for the current Context but attribute to a different tag. In complex apps attribution tagging can be used to distinguish between separate logical parts.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createConfigurationContext(android.content.res.Configuration)(overrideConfiguration: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContext(android.content.ContextParams)(contextParams: https://developer.android.com/reference/kotlin/android/content/ContextParams.html#)`

Creates a context with specific properties and behaviors.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createContextForSplit(kotlin.String)(splitName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Return a new Context object for the given split name. The new Context has a ClassLoader and Resources object that can access the split's and all of its dependencies' code/resources. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same split) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceContext(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a new `Context` object from the current context but with device association given by the `deviceId`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

Applications that run on virtual devices may use this method to access the default device capabilities and functionality (by passing `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`. Similarly, applications running on the default device may access the functionality of virtual devices.

Note that the newly created instance will be associated with the same display as the parent Context, regardless of the device ID passed here.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDeviceProtectedStorageContext()()`

Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both *before and after* the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged.

If the underlying device does not have the ability to store device-protected and credential-protected data using different keys, then both storage areas will become available at the same time. They remain as two distinct storage locations on disk, and only the window of availability changes.

Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createDisplayContext(android.view.Display)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#)`

Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

**Note:** This `Context` is **not** expected to be updated with new configuration if the underlying display configuration changes and the cached `Resources` it returns could be stale. It is suggested to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener.html#` to listen for changes and re-create an instance if necessary.

This `Context` is **not** a UI context, do not use it to access UI components or obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` instance.

To obtain an instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` configured to show windows on the given display, call `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` on the returned display context, then call `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)` on the returned window context.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createPackageContext(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a new Context object for the given application name. This Context is the same as what the named application gets when it is launched, containing the same resources and class loader. Each call to this method returns a new instance of a Context object; Context objects are not shared, however they share common state (Resources, ClassLoader, etc) so the Context instance itself is fairly lightweight.

Throws `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#` if there is no application with the given package name.

Throws `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the Context requested can not be loaded into the caller's process for security reasons (see `https://developer.android.com/reference/kotlin/android/content/Context.html#CONTEXT_INCLUDE_CODE:kotlin.Int` for more information}.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(android.view.Display,%20kotlin.Int,%20android.os.Bundle)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity.html#` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, but the `display` is passed in, instead of implicitly using the `https://developer.android.com/reference/kotlin/android/content/Context.html#getDisplay()`.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#createWindowContext(kotlin.Int,%20android.os.Bundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Creates a Context for a non-activity window.

A window context is a context that can be used to add non-activity windows, such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`. A window context must be created from a context that has an associated `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)`.

The window context is created with the appropriate `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` for the area of the display that the windows created with it can occupy; it must be used when `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` views, such that they can be inflated with proper `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#`. Below is a sample code to **add an application overlay window on the primary display:**

```kotlin
...
  final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createDisplayContext(primaryDisplay)
          .createWindowContext(TYPE_APPLICATION_OVERLAY, null);
  final View overlayView = Inflater.from(windowContext).inflate(someLayoutXml, null);
 
  // WindowManager.LayoutParams initialization
  ...
  // The types used in addView and createWindowContext must match.
  mParams.type = TYPE_APPLICATION_OVERLAY;
  ...
 
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

This context's configuration and resources are adjusted to an area of the display where the windows with provided type will be added. **Note that all windows associated with the same context will have an affinity and can only be moved together between different displays or areas on a display.** If there is a need to add different window types, or non-associated windows, separate Contexts should be used.

Creating a window context is an expensive operation. Misuse of this API may lead to a huge performance drop. The best practice is to use the same window context when possible. An approach is to create one window context with specific window type and display and use it everywhere it's needed.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to receive configuration changes for existing token by overriding the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` of the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` passed in `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`. This is useful when an application needs to attach its window to an existing activity for window token sharing use-case.

Note that the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` didn't have this capability. This is a no-op for the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.
Below is sample code to **attach an existing token to a window context:**

```kotlin
final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createWindowContext(primaryDisplay,
          TYPE_APPLICATION, null);
 
  // Get an existing token.
  final IBinder existingToken = activity.getWindow().getAttributes().token;
 
  // The types used in addView() and createWindowContext() must match.
  final WindowManager.LayoutParams params = new WindowManager.LayoutParams(TYPE_APPLICATION);
  params.token = existingToken;
 
  // After WindowManager#addView(), the server side will extract the provided token from
  // LayoutParams#token (existingToken in the sample code), and switch to propagate
  // configuration changes from the node associated with the provided token.
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to listen to its `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerComponentCallbacks(android.content.ComponentCallbacks)`, while other kinds of `https://developer.android.com/reference/kotlin/android/content/Context.html#` will register the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to `https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()`. Note that window context only propagate `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)` callback. `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` or other callbacks in `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` won't be invoked.

Note that using `https://developer.android.com/reference/kotlin/android/app/Application.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` context for UI-related queries may result in layout or continuity issues on devices with variable screen sizes (e.g. foldables) or in multi-window modes, since these non-UI contexts may not reflect the `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` changes for the visual container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#databaseList()()`

Returns an array of strings naming the private databases associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteDatabase(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing private SQLiteDatabase associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteFile(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete the given private file associated with this Context's application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#deleteSharedPreferences(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Delete an existing shared preferences file.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingPermission(kotlin.String,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw the SecurityException. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)` to avoid this protection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw a SecurityException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#enforceUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Enforce both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context.html#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` and #enforceUriPermission in one call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#fileList()()`

Returns an array of strings naming the private files associated with this Context's application package.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationContext()()`

Return the context of the single, global Application object of the current process. This generally should only be used if you need a Context whose lifecycle is separate from the current context, that is tied to the lifetime of the process rather than the current component.

Consider for example how this interacts with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`:

- If used from an Activity context, the receiver is being registered within that activity. This means that you are expected to unregister before the activity is done being destroyed; in fact if you do not do so, the framework will clean up your leaked registration as it removes the activity and log an error. Thus, if you use the Activity context to register a receiver that is static (global to the process, not associated with an Activity instance) then that registration will be removed on you at whatever point the activity you used is destroyed.

- If used from the Context returned here, the receiver is being registered with the global state associated with your application. Thus it will never be unregistered for you. This is necessary if the receiver is associated with static data, not a particular component. However using the ApplicationContext elsewhere can easily lead to serious leaks if you forget to unregister, unbind, etc.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getApplicationInfo()()`

Return the full application info for this context's package.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAssets()()`

Returns an AssetManager instance for the application's package.

**Note:** Implementations of this method should return an AssetManager instance that is consistent with the Resources instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getResources()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/AttributionSource.html#` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionSource()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getAttributionTag()()`

Attribution can be used in complex apps to logically separate parts of the app. E.g. a blogging app might also have a instant messaging app built in. In this case two separate tags can for used each sub-feature.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()()`

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem.

The system will automatically delete files in this directory as disk space is needed elsewhere on the device. The system will always delete older files first, as reported by `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()`. If desired, you can exert more control over how files are deleted using `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)`.

Apps are strongly encouraged to keep their usage of cache space below the quota returned by `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#getCacheQuotaBytes(java.util.UUID)`. If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

Note that your cache quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getClassLoader()()`

Return a class loader you can use to retrieve classes in this package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getCodeCacheDir()()`

Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code.

The system will delete any files stored in this location both when your specific application is upgraded, and when the entire platform is upgraded.

This location is optimal for storing compiled or optimized code generated by your application at runtime.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getContentResolver()()`

Return a ContentResolver instance for your application's package.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDataDir()()`

Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. Apps should not use this path directly; they should instead use `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDir(kotlin.String,%20kotlin.Int)`, or other storage APIs on this class.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDatabasePath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDeviceId()()`

Gets the device ID this context is associated with. Applications can use this method to determine whether they are running on a virtual device and identify that device. The device ID of the host device is `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int`

If the underlying device ID is changed by the system, for example, when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is moved to a different virtual device, applications can register to listen to changes by calling `https://developer.android.com/reference/kotlin/android/content/Context.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`.

This method will only return a reliable value for this instance if it was created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)`, or if this instance is a UI or Display Context. Contexts created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceContext(kotlin.Int)` will have an explicit device association, which will never change, even if the underlying device is closed or is removed. UI Contexts and Display Contexts are already associated with a display, so if the device association is not explicitly given, `https://developer.android.com/reference/kotlin/android/content/Context.html#getDeviceId()` will return the ID of the device associated with the associated display. The system can assign an arbitrary device id value for Contexts not logically associated with a device.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDir(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve, creating if needed, a new directory in which the application can place its own custom data files. You can use the returned File object to create and access files in this directory. Note that files created through a File object will only be accessible by your own application; you can only set the mode of the entire directory, not of individual files.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

<br />

`https://developer.android.com/reference/kotlin/android/view/Display.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getDisplay()()`

Get the display this context is associated with. Applications should use this method with `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context associated with a `https://developer.android.com/reference/kotlin/android/view/Display.html#` via `https://developer.android.com/reference/kotlin/android/content/Context.html#createDisplayContext(android.view.Display)` to get a display object associated with a Context, or `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)` to get a display object by id.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDir()()`

Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalCacheDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getCacheDir()`.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDir(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. These files are internal to the applications, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

Here is an example of typical code to manipulate a file in an application's shared storage:

If you supply a non-null type to this function, the returned file will be a path to a sub-directory of the given type. Though these files are not automatically scanned by the media scanner, you can explicitly add them to the media database with `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#scanFile(android.content.Context,%20kotlin.Array,%20kotlin.Array,%20android.media.MediaScannerConnection.OnScanCompletedListener)`. Note that this is not the same as `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, which provides directories of media shared by all applications. The directories returned here are owned by the application, and their contents will be removed when the application is uninstalled. Unlike `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, the directory returned here will be automatically created for you.

Here is an example of typical code to manipulate a picture in an application's shared storage and add it to the media database:

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalFilesDirs(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`, etc.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getExternalMediaDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. These files are scanned and made available to other apps through `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#`.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDirs(kotlin.String)` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFileStreamPath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns the absolute path on the filesystem where a file created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getFilesDir()()`

Returns the absolute path to the directory on the filesystem where files created with `https://developer.android.com/reference/kotlin/android/content/Context.html#openFileOutput(kotlin.String,%20kotlin.Int)` are stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainExecutor()()`

Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. This is the thread used to dispatch calls to application components (activities, services, etc).

<br />

`https://developer.android.com/reference/kotlin/android/os/Looper.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainLooper()()`

Return the Looper for the main thread of the current process. This is the thread used to dispatch calls to application components (activities, services, etc).

By definition, this method returns the same result as would be obtained by calling `https://developer.android.com/reference/kotlin/android/os/Looper.html#getMainLooper()`.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getNoBackupFilesDir()()`

Returns the absolute path to the directory on the filesystem similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()`. The difference is that files placed under this directory will be excluded from automatic backup to remote storage. See `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#` for a full discussion of the automatic backup mechanism in Android.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

<br />

`https://developer.android.com/reference/kotlin/java/io/File.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDir()()`

Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, this directory may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the path that this method returns. However, starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, to read the OBB expansion files, you must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission in the app manifest and ask for permission at runtime as follows:

`<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" android:maxSdkVersion="23" />`

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission is not required, so don't ask for this permission at runtime. To handle both cases, your app must first try to read the OBB file, and if it fails, you must request `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission at runtime.

The following code snippet shows how to do this:

```kotlin
File obb = new File(obb_filename);
  boolean open_failed = false;
 
  try {
      BufferedReader br = new BufferedReader(new FileReader(obb));
      open_failed = false;
      ReadObbFile(br);
  } catch (IOException e) {
      open_failed = true;
  }
 
  if (open_failed) {
      // request READ_EXTERNAL_STORAGE permission before reading OBB file
      ReadObbFileWithPermission();
  }
  
```
On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), multiple users may share the same OBB storage location. Applications should ensure that multiple instances running under different users don't interfere with each other.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getObbDirs()()`

Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, these directories may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getOpPackageName()()`

Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` calls from this context, so that app ops manager's uid verification will work with the name.

This is not generally intended for third party application developers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageCodePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains application's primary code and assets.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageManager()()`

Return PackageManager instance to find global package information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageName()()`

Return the name of this application's package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getPackageResourcePath()()`

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains the application's primary resources.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

<br />

`https://developer.android.com/reference/kotlin/android/content/ContextParams.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getParams()()`

Return the set of parameters which this Context was created with, if it was created via `https://developer.android.com/reference/kotlin/android/content/Context.html#createContext(android.content.ContextParams)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getResources()()`

Returns a Resources instance for the application's package.

**Note:** Implementations of this method should return a Resources instance that is consistent with the AssetManager instance returned by `https://developer.android.com/reference/kotlin/android/content/Context.html#getAssets()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSharedPreferences(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. Only one instance of the SharedPreferences object is returned to any callers for the same name, meaning they will see each other's edits as soon as they are made.

This method is thread-safe.

If the preferences directory does not already exist, it will be created when this method is called.

If a preferences file by this name does not exist, it will be created when you retrieve an editor (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#edit()`) and then commit changes (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#commit()` or `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#apply()`).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSystemService(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context.html#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context.html#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context.html#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context.html#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context.html#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context.html#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling search.

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_MANAGER_SERVICE:kotlin.String` ("vibrator_manager")
: A `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

`https://developer.android.com/reference/kotlin/android/content/Context.html#MULTISENSORY_MANAGER_SERVICE:kotlin.String` ("multisensory_manager")
: A `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager.html#` for delivering audio-haptic feedback in the Multisensory Design System

`https://developer.android.com/reference/kotlin/android/content/Context.html#VIBRATOR_SERVICE:kotlin.String` ("vibrator")
: A `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibrator hardware.

`https://developer.android.com/reference/kotlin/android/content/Context.html#CONNECTIVITY_SERVICE:kotlin.String` ("connectivity")
: A `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

`https://developer.android.com/reference/kotlin/android/content/Context.html#IPSEC_SERVICE:kotlin.String` ("ipsec")
: A `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for managing IPSec on sockets and networks.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String` ("wifi")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for management of Wi-Fi connectivity. On releases before Android 7, it should only be obtained from an application context, and not from any other derived context to avoid memory leaks within the calling process.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String` ("wifiaware")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for management of Wi-Fi Aware discovery and connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String` ("wifip2p")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for management of Wi-Fi Direct connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context.html#INPUT_METHOD_SERVICE:kotlin.String` ("input_method")
: An `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for management of input methods.

`https://developer.android.com/reference/kotlin/android/content/Context.html#UI_MODE_SERVICE:kotlin.String` ("uimode")
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context.html#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context.html#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context.html#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage statistics.

`https://developer.android.com/reference/kotlin/android/content/Context.html#HARDWARE_PROPERTIES_SERVICE:kotlin.String` ("hardware_properties")
: A `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing hardware properties.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DOMAIN_VERIFICATION_SERVICE:kotlin.String` ("domain_verification")
: A `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#` for accessing web domain approval state.

`https://developer.android.com/reference/kotlin/android/content/Context.html#DISPLAY_HASH_SERVICE:kotlin.String` ("display_hash")
: A `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` for management of display hashes.

`https://developer.android.com/reference/kotlin/android/content/Context.html#AUTHENTICATION_POLICY_SERVICE:kotlin.String` ("authentication_policy")
: A `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#` for managing authentication related policies on the device.

<br />

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getSystemServiceName(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>)`

Gets the name of the system-level service that is represented by the specified class.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getTheme()()`

Return the Theme object associated with this Context.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumHeight()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getWallpaperDesiredMinimumWidth()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(toPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. This can be used to grant specific, temporary permissions, typically in response to user interaction (such as the user opening an attachment that you would like someone else to display).

Normally you should use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` with the Intent being used to start an activity instead of this function directly. If you use this function directly, you should be sure to call #revokeUriPermission when the target should no longer be allowed to access it.

To succeed, the content provider owning the Uri must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isDeviceProtectedStorage()()`

Indicates if the storage APIs of this Context are backed by device-protected storage.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isRestricted()()`

Indicates whether this Context is restricted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#isUiContext()()`

Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`. Accessing UI components from non-UI contexts throws `https://developer.android.com/reference/kotlin/android/os/strictmode/Violation.html#` if `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectIncorrectContextUse()` is enabled.

Examples of UI contexts are an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, a context created from `https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle)` or `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`

Note that even if it is allowed programmatically, it is not suggested to override this method to bypass `https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation.html#` verification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveDatabaseFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing database file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as migrating to device protected storage.

The database must be closed before being moved.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#moveSharedPreferencesFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Move an existing shared preferences file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as moving to device protected storage.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileInput(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Open a private file associated with this Context's application package for reading.

<br />

`https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openFileOutput(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Open a private file associated with this Context's application package for writing. Creates the file if it doesn't already exist.

No additional permissions are required for the calling app to read or write the returned file.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!)`

Open a new private SQLiteDatabase associated with this Context's application package. Create the database file if it doesn't exist.

<br />

`https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)`

Open a new private SQLiteDatabase associated with this Context's application package. Creates the database file if it doesn't exist.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#peekWallpaper()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#)`

Rebind an application service with updated bind service flags

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)` when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be registered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` to the base application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system.

The callback can be called when an app is moved to a different device and the `Context` is not explicitly associated with a specific device.

When an application receives a device id update callback, this Context is guaranteed to also have an updated display ID(if any) and `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#`.

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!)`

Register a BroadcastReceiver to be run in the main activity thread. The receiver will be called with any broadcast Intent that matches filter, in the main application thread.

The system may broadcast Intents that are "sticky" -- these stay around after the broadcast has finished, to be sent to any later registrations. If your IntentFilter matches one of these sticky Intents, that Intent will be returned by this function **and** sent to your receiver as if it had just been broadcast.

There may be multiple sticky Intents that match filter, in which case each of these will be sent to receiver. In this case, only one of these can be returned directly by the function; which of these that is returned is arbitrarily decided by the system.

If you know the Intent you are registering for is sticky, you can supply null for your receiver. In this case, no receiver is registered -- the function simply returns the sticky Intent that matches filter. In the case of multiple matches, the same rules as described above apply.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` to register a receiver with flags.

Note: this method *cannot be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` component;* that is, from a BroadcastReceiver that is declared in an application's manifest. It is okay, however, to call this method from another BroadcastReceiver that has itself been registered at run time with #registerReceiver, since the lifetime of such a registered BroadcastReceiver is tied to the object that registered it.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. By default Instant Apps cannot interact with receivers in other applications, this allows you to expose a receiver that Instant Apps can interact with.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. This allows you to enforce permissions on who can broadcast intents to your receiver, or have the receiver run in a different thread than the main application thread.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context.html#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)` to register a receiver with flags.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)` for more information.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#removeStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#removeStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String` permission in order to use this API. If you do not hold that permission, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeSelfPermissionsOnKill(kotlin.collections.MutableCollection)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Triggers the revocation of one or more permissions for the calling package. A package is only able to revoke runtime permissions. If a permission is not currently granted, it is ignored and will not get revoked (even if later granted by the user). Ultimately, you should never make assumptions about a permission status as users may grant or revoke them at any time.

Background permissions which have no corresponding foreground permission still granted once the revocation is effective will also be revoked.

The revocation happens asynchronously and kills all processes running in the calling UID. It will be triggered once it is safe to do so. In particular, it will not be triggered as long as the package remains in the foreground, or has any active manifest components (e.g. when another app is accessing a content provider in the package).

If you want to revoke the permissions right away, you could call `System.exit()` in `Handler.postDelayed` with a delay to allow completion of async IPC, But `System.exit()` could affect other apps that are accessing your app at the moment. For example, apps accessing a content provider in your app will all crash.

Note that the settings UI shows a permission group as granted as long as at least one permission in the group is granted. If you want the user to observe the revocation in the settings, you should revoke every permission in the target group. To learn the current list of permissions in a group, you may use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPlatformPermissionsForGroup(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. This list of permissions may evolve over time, so it is recommended to check whether it contains any permission you wish to retain before trying to revoke an entire group.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove all permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` or *any other* mechanism. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, if you did not have regular permission access to a Uri, but had received access to it through a specific Uri permission grant, you could not revoke that grant with this function and a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` would be thrown. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this function will not throw a security exception, but will remove whatever permission grants to the Uri had been given to the app (or none).

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)`, this method impacts all permission grants matching the given Uri, for any package they had been granted to, through any mechanism this had happened (such as indirectly through the clipboard, activity launch, service start, etc). That means this can be potentially dangerous to use, as it can revoke grants that another app could be strongly expecting to stick around.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)`, this method will *only* revoke permissions that had been explicitly granted through `https://developer.android.com/reference/kotlin/android/content/Context.html#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` and only for the package specified. Any matching grants that have happened through other mechanisms (clipboard, activity launching, service starting, etc) will not be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Broadcast the given intent to all interested BroadcastReceivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent,%20kotlin.String)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Perform a `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcast(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Perform a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendBroadcast(android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called. Note that the sticky data stored is only the data you initially supply to the broadcast, not the result of any changes made by the receivers.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#sendStickyOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Version of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setTheme(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the base theme for this context. Note that this should be called before any views are instantiated in the Context (for example before calling android.app.Activity#setContentView or android.view.LayoutInflater#inflate).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#setWallpaper(java.io.InputStream)(data: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets whether you should show UI with rationale before requesting a permission. If the permission does not exist on this SDK level or is not visible to this app, the method will return `false`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivities(kotlin.Array,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivities(kotlin.Array,%20android.os.Bundle)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch multiple new activities. This is generally the same as calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the first Intent in the array, that activity during its creation calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` for the second entry, etc. Note that unlike that approach, generally none of the activities except the last in the array will be created at this point, but rather will be created when the user first visits them (due to pressing back from the activity on top).

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found for *any* given Intent. In this case the state of the activity stack is undefined (some Intents in the list may be on it, some not), so you probably want to avoid such situations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Launch a new activity. You will not receive any information about when the activity exits.

Note that if this method is being called from outside of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` Context, then the Intent must include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag. This is because, without being started from an existing Activity, there is no existing task in which to place the new activity and thus it needs to be placed in its own separate task.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` if there was no Activity found to run the given Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startForegroundService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Similar to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, but with an implicit promise that the Service will call `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` once it begins running. The service is given an amount of time comparable to the ANR interval to do this, otherwise the system will automatically crash the process, in which case an internal exception `ForegroundServiceDidNotStartInTimeException` is logged on logcat on devices running SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later. On older Android versions, an internal exception `RemoteServiceException` is logged instead, with a corresponding message.

Unlike the ordinary `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`, this method can be used at any time, regardless of whether the app hosting the service is in a foreground state.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startInstrumentation(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, profileFile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#` class. The given Instrumentation component will be run by killing its target application (if currently running), starting the target process, instantiating the instrumentation component, and then letting it drive the application.

This function is not synchronous -- it returns as soon as the instrumentation has started and while it is running.

Instrumentation is normally only allowed to run against a package that is either unsigned or signed with a signature that the the instrumentation package is also signed with (ensuring the target trusts the instrumentation).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Same as `https://developer.android.com/reference/kotlin/android/content/Context.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Like `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)`, but taking a IntentSender to start. If the IntentSender is for an activity, that activity will be started as if you had called the regular `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be started. The Intent should either contain the complete class name of a specific service implementation to start, or a specific package name to target. If the Intent is less specified, it logs a warning about this. In this case any of the multiple matching services may be used. If this service is not already running, it will be instantiated and started (creating a process for it if needed); if it is running then it remains running.

Every call to this method will result in a corresponding call to the target service's `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method, with the intent given here. This provides a convenient way to submit jobs to a service without having to bind and call on to its interface.

Using startService() overrides the default service lifetime that is managed by #bindService: it requires the service to remain running until `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` is called, regardless of whether any clients are connected to it. Note that calls to startService() do not nest: no matter how many times you call startService(), a single call to `https://developer.android.com/reference/kotlin/android/content/Context.html#stopService(android.content.Intent)` will stop it.

The system attempts to keep running services around as much as possible. The only time they should be stopped is if the current foreground application is using so many resources that the service needs to be killed. If any errors happen in the service's process, it will automatically be restarted.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to start the given service.

**Note:** Each call to startService() results in significant work done by the system to manage service lifecycle surrounding the processing of the intent, which can take multiple milliseconds of CPU time. Due to this cost, startService() should not be used for frequent intent delivery to a service, and only for scheduling significant work. Use #bindService for high frequency calls.
Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher are not allowed to start background services from the background. See [Background Execution Limits](../about/versions/oreo/background.md) for more details.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#stopService(android.content.Intent)(name: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Request that a given application service be stopped. If the service is not running, nothing happens. Otherwise it is stopped. Note that calls to startService() are not counted -- this stops the service no matter how many times it was started.

If the service is running as a foreground service when it is stopped, its associated notification will be removed. To avoid this, apps can use `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` to decouple the notification from the service's lifecycle before stopping it.

Note that if a stopped service still has `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#` objects bound to it with the `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int` set, it will not be destroyed until all of these bindings are removed. See the `https://developer.android.com/reference/kotlin/android/app/Service.html#` documentation for more details on a service's lifecycle.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to stop the given service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unbindService(android.content.ServiceConnection)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

Disconnect from an application service. You will no longer receive calls as the service is restarted, and the service is now allowed to stop at any time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#!)`

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#attachBaseContext(android.content.Context)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterDeviceIdChangeListener(java.util.function.IntConsumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)`

Removes a device ID changed listener from the Context. It's a no-op if the listener is not already registered.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#unregisterReceiver(android.content.BroadcastReceiver)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#!)`

Unregister a previously registered BroadcastReceiver. *All* filters that have been registered for this BroadcastReceiver will be removed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceBindings(kotlin.collections.MutableCollection)(params: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/content/Context.UpdateBindingParams.html#!>)`

Perform a batch update of existing bindings. Existing bindings can be rebound with an updated set of flags, or unbound. Only flags returned from `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()` may be added or removed.

This API behaves as if the `https://developer.android.com/reference/kotlin/android/content/Context.html#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` and `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` API are called in the same order as the params are iterated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#, group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, importance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. This doesn't modify the original bind flags that were passed in when binding, but adjusts how the process will be managed in some cases based on those flags. Currently only works on isolated processes (will be ignored for non-isolated processes).

Note that this call does not take immediate effect, but will be applied the next time the impacted process is adjusted for some other reason. Typically you would call this before then calling a new #bindIsolatedService on the service of interest, with that binding causing the process to be shuffled accordingly.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/Context.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#)`

See `https://developer.android.com/reference/kotlin/android/content/Context.html#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColor(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getColorStateList(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color state list associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/content/Context.html#getDrawable(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a drawable object associated with a particular resource ID and styled for the current theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getString(kotlin.Int,%20kotlin.Any)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Returns a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Return the handle to a system-level service by class.

Currently available classes are: `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#`, `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#`, `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#`, `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`, `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#`, `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#`, `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`, `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#`, `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#`, `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#`, `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager.html#`, `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context.html#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context.html#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#getText(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#getUpdateableFlags()()`

Gets the list of bind flags that may be updated (i.e. added or removed) for an existing connection. Includes:

- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_FOREGROUND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ABOVE_CLIENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_WAIVE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_IMPORTANT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_NOT_PERCEPTIBLE:kotlin.Int`

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#` `https://developer.android.com/reference/kotlin/android/content/Context.html#obtainStyledAttributes(kotlin.IntArray)(attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#obtainStyledAttributes(kotlin.IntArray)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeSelfPermissionOnKill(kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Triggers the asynchronous revocation of a runtime permission. If the permission is not currently granted, nothing happens (even if later granted by the user).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcastWithMultiplePermissions(android.content.Intent,%20kotlin.Array)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, receiverPermissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an array of required permissions to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` for more information on Intent broadcasts.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

## Constants

### SERVICE_INTERFACE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_INTERFACE: String
```

The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that must be declared as handled by the service.

 Value: "android.telecom.ConnectionService"

## Public constructors

### ConnectionService

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConnectionService()
```

## Public methods

### addConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addConference(conference: Conference!): Unit
```

Adds a new conference call. When a conference call is created either as a result of an explicit request via `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConference(android.telecom.Connection,%20android.telecom.Connection)` or otherwise, the connection service should supply an instance of `https://developer.android.com/reference/kotlin/android/telecom/Conference` by invoking this method. A conference call provided by this method will persist until `https://developer.android.com/reference/kotlin/android/telecom/Conference#destroy()` is invoked on the conference instance.

| Parameters ||
|---|---|
| `conference` | [Conference](Conference.md)!: The new conference object. |

### addConferenceFromConnection

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addConferenceFromConnection(
    conference: Conference, 
    originalConnection: Connection
): Unit
```

This is used to make a `https://developer.android.com/reference/kotlin/android/telecom/Connection` become a `https://developer.android.com/reference/kotlin/android/telecom/Conference` when the remote party merges calls together. In prior API revisions, the `https://developer.android.com/reference/kotlin/android/telecom/Connection` would be disconnected and re-added as a `https://developer.android.com/reference/kotlin/android/telecom/Conference`; this method accomplishes that in a single step and maintains attributes such as the call duration associated with the `https://developer.android.com/reference/kotlin/android/telecom/Connection`.

| Parameters ||
|---|---|
| `conference` | [Conference](Conference.md): The new conference object. This value cannot be `null`. |
| `originalConnection` | [Connection](Connection.md): The original connection object. This value cannot be `null`. |

### addExistingConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addExistingConnection(
    phoneAccountHandle: PhoneAccountHandle!, 
    connection: Connection!
): Unit
```

Adds a connection created by the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and informs telecom of the new connection.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](PhoneAccountHandle.md)!: The phone account handle for the connection. |
| `connection` | [Connection](Connection.md)!: The connection to add. |

### conferenceRemoteConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun conferenceRemoteConnections(
    remoteConnection1: RemoteConnection!, 
    remoteConnection2: RemoteConnection!
): Unit
```

Indicates to the relevant `RemoteConnectionService` that the specified `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection`s should be merged into a conference call.

If the conference request is successful, the method `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onRemoteConferenceAdded(android.telecom.RemoteConference)` will be invoked.

| Parameters ||
|---|---|
| `remoteConnection1` | [RemoteConnection](RemoteConnection.md)!: The first of the remote connections to conference. |
| `remoteConnection2` | [RemoteConnection](RemoteConnection.md)!: The second of the remote connections to conference. |

### connectionServiceFocusReleased

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectionServiceFocusReleased(): Unit
```

Call to inform Telecom that your `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has released call resources (e.g microphone, camera).

The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` will be disconnected when it failed to call this method within 5 seconds after `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionServiceFocusLost()` is called.
**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onConnectionServiceFocusLost()`

### createRemoteIncomingConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRemoteIncomingConference(
    connectionManagerPhoneAccount: PhoneAccountHandle?, 
    request: ConnectionRequest?
): RemoteConference?
```

Ask some other `ConnectionService` to create a `RemoteConference` given an incoming request. This is used by `ConnectionService`s that are registered with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_ADHOC_CONFERENCE_CALLING:kotlin.Int`.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)?: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value may be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)?: Details about the incoming conference call. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConference?` | The `RemoteConference` object to satisfy this call, or `null` to not handle the call. |

### createRemoteIncomingConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRemoteIncomingConnection(
    connectionManagerPhoneAccount: PhoneAccountHandle, 
    request: ConnectionRequest
): RemoteConnection?
```

Ask some other `ConnectionService` to create a `RemoteConnection` given an incoming request. This is used by `ConnectionService`s that are registered with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` and want to be able to manage SIM-based incoming calls.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md): See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value cannot be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md): Details about the incoming call. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection?` | The `Connection` object to satisfy this call, or `null` to not handle the call. |

### createRemoteOutgoingConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRemoteOutgoingConference(
    connectionManagerPhoneAccount: PhoneAccountHandle?, 
    request: ConnectionRequest?
): RemoteConference?
```

Ask some other `ConnectionService` to create a `RemoteConference` given an outgoing request. This is used by `ConnectionService`s that are registered with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_ADHOC_CONFERENCE_CALLING:kotlin.Int`.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)?: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value may be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)?: Details about the outgoing conference call. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConference?` | The `RemoteConference` object to satisfy this call, or `null` to not handle the call. |

### createRemoteOutgoingConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRemoteOutgoingConnection(
    connectionManagerPhoneAccount: PhoneAccountHandle, 
    request: ConnectionRequest
): RemoteConnection?
```

Ask some other `ConnectionService` to create a `RemoteConnection` given an outgoing request. This is used by `ConnectionService`s that are registered with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` and want to be able to use the SIM-based `ConnectionService` to place its outgoing calls.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md): See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value cannot be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md): Details about the outgoing call. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection?` | The `Connection` object to satisfy this call, or `null` to not handle the call. |

### getAllConferences

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllConferences(): MutableCollection<Conference!>!
```

Returns all the active `Conference`s for which this `ConnectionService` has taken responsibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/telecom/Conference!>!` | A collection of `Conference`s created by this `ConnectionService`. |

### getAllConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllConnections(): MutableCollection<Connection!>!
```

Returns all the active `Connection`s for which this `ConnectionService` has taken responsibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/telecom/Connection!>!` | A collection of `Connection`s created by this `ConnectionService`. |

### onBind

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun onBind(intent: Intent!): IBinder?
```

Return the communication channel to the service. May return null if clients can not bind to the service. The returned `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` is usually for a complex interface that has been [described using aidl](https://developer.android.com/guide/components/aidl.html).

*Note that unlike other application components, calls on to the IBinder interface returned here may not happen on the main thread of the process* . More information about the main thread can be found in [Processes and Threads](https://developer.android.com/guide/topics/fundamentals/processes-and-threads.html).

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md)!: The Intent that was used to bind to this service, as given to android.content.Context#bindService. Note that any extras that were included with the Intent at that point will *not* be seen here. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#?` | Return an IBinder through which clients can call on to the service. |

### onConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConference(
    connection1: Connection!, 
    connection2: Connection!
): Unit
```

Conference two specified connections. Invoked when the user has made a request to merge the specified connections into a conference call. In response, the connection service should create an instance of `https://developer.android.com/reference/kotlin/android/telecom/Conference` and pass it into `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#addConference(android.telecom.Conference)`.

| Parameters ||
|---|---|
| `connection1` | [Connection](Connection.md)!: A connection to merge into a conference call. |
| `connection2` | [Connection](Connection.md)!: A connection to merge into a conference call. |

### onConferenceAdded

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConferenceAdded(conference: Conference): Unit
```

Called when a conference is added.

| Parameters ||
|---|---|
| `conference` | [Conference](Conference.md): This value cannot be `null`. |

### onConferenceRemoved

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConferenceRemoved(conference: Conference): Unit
```

Called when a conference is removed.

| Parameters ||
|---|---|
| `conference` | [Conference](Conference.md): This value cannot be `null`. |

### onConnectionAdded

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionAdded(connection: Connection): Unit
```

Called when a connection is added.

| Parameters ||
|---|---|
| `connection` | [Connection](Connection.md): This value cannot be `null`. |

### onConnectionRemoved

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionRemoved(connection: Connection): Unit
```

Called when a connection is removed.

| Parameters ||
|---|---|
| `connection` | [Connection](Connection.md): This value cannot be `null`. |

### onConnectionServiceFocusGained

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionServiceFocusGained(): Unit
```

Called when the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has gained the call focus. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` can acquire the call resources at this time.

### onConnectionServiceFocusLost

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionServiceFocusLost(): Unit
```

Called when the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` has lost the call focus. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` should release the call resources and invokes `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#connectionServiceFocusReleased()` to inform telecom that it has released the call resources.

### onCreateConferenceComplete

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateConferenceComplete(conference: Conference): Unit
```

Called by Telecom after the `https://developer.android.com/reference/kotlin/android/telecom/Conference` returned by `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` has been added to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and sent to Telecom.

| Parameters ||
|---|---|
| `conference` | [Conference](Conference.md): the `https://developer.android.com/reference/kotlin/android/telecom/Conference` which was added to Telecom. This value cannot be `null`. |

### onCreateConnectionComplete

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateConnectionComplete(connection: Connection): Unit
```

Called by Telecom after the `https://developer.android.com/reference/kotlin/android/telecom/Connection` returned by `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` or `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` has been added to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` and sent to Telecom.

| Parameters ||
|---|---|
| `connection` | [Connection](Connection.md): the `https://developer.android.com/reference/kotlin/android/telecom/Connection` which was added to Telecom. This value cannot be `null`. |

### onCreateIncomingConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateIncomingConference(
    connectionManagerPhoneAccount: PhoneAccountHandle, 
    request: ConnectionRequest
): Conference?
```

Create a `Conference` given an incoming request. This is used to attach to an incoming conference call initiated via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingConference(android.telecom.PhoneAccountHandle,%20android.os.Bundle)`.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md): See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value cannot be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md): Details about the incoming conference call. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Conference?` | The `Conference` object to satisfy this call. If the conference attempt is failed, the return value will be a result of an invocation of `https://developer.android.com/reference/kotlin/android/telecom/Connection#createFailedConnection(android.telecom.DisconnectCause)`. Return `null` if the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` cannot handle the call. |

### onCreateIncomingConferenceFailed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateIncomingConferenceFailed(
    connectionManagerPhoneAccount: PhoneAccountHandle?, 
    request: ConnectionRequest?
): Unit
```

Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Conference` was denied.

Used when a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` attempts to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Conference`, but Telecom has determined that the call cannot be allowed at this time. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` is responsible for silently rejecting the new incoming `https://developer.android.com/reference/kotlin/android/telecom/Conference`.

See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isIncomingCallPermitted(android.telecom.PhoneAccountHandle)` for more information.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)?: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value may be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)?: The incoming connection request. This value may be `null`. |

### onCreateIncomingConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateIncomingConnection(
    connectionManagerPhoneAccount: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Connection!
```

Create a `Connection` given an incoming request. This is used to attach to existing incoming calls.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)!: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: Details about the incoming call. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection!` | The `Connection` object to satisfy this call, or `null` to not handle the call. |

### onCreateIncomingConnectionFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateIncomingConnectionFailed(
    connectionManagerPhoneAccount: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Unit
```

Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Connection` was denied.

Used when a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` attempts to create a new incoming `https://developer.android.com/reference/kotlin/android/telecom/Connection`, but Telecom has determined that the call cannot be allowed at this time. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` is responsible for silently rejecting the new incoming `https://developer.android.com/reference/kotlin/android/telecom/Connection`.

See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isIncomingCallPermitted(android.telecom.PhoneAccountHandle)` for more information.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)!: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: The incoming connection request. |

### onCreateIncomingHandoverConnection

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateIncomingHandoverConnection(
    fromPhoneAccountHandle: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Connection!
```

Called by Telecom to request that a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` creates an instance of an incoming handover `https://developer.android.com/reference/kotlin/android/telecom/Connection`.

A call handover is the process where an ongoing call is transferred from one app (i.e. `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` to another app. The user could, for example, choose to continue a mobile network call in a video calling app. The mobile network call via the Telephony stack is referred to as the source of the handover, and the video calling app is referred to as the destination.

When considering a handover scenario the *initiating* device is where a user initiated the handover process (e.g. by calling `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`, and the other device is considered the *receiving* device.

This method is called on the destination app on the *receiving* device when the destination app calls `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptHandover(android.net.Uri,%20kotlin.Int,%20android.telecom.PhoneAccountHandle)` to accept an incoming handover from the *initiating* device.

For a full discussion of the handover process and the APIs involved, see `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`.

Implementations of this method should return an instance of `https://developer.android.com/reference/kotlin/android/telecom/Connection` which represents the handover. The code below shows an example of how this is done.

```kotlin
<code>public Connection onCreateIncomingHandoverConnection(PhoneAccountHandle
      fromPhoneAccountHandle, ConnectionRequest request) {
    // Given that your app requested to accept the handover, you should not return null here.
    MyConnection connection = new MyConnection();
    connection.setAddress(request.getAddress(), TelecomManager.PRESENTATION_ALLOWED);
    connection.setVideoState(request.getVideoState());
    return connection;
  }
  </code>
```

| Parameters ||
|---|---|
| `fromPhoneAccountHandle` | [PhoneAccountHandle](PhoneAccountHandle.md)!: `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` associated with the ConnectionService which needs to handover the call. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: Details about the call which needs to be handover. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection!` | `https://developer.android.com/reference/kotlin/android/telecom/Connection` instance corresponding to the handover call. |

### onCreateOutgoingConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateOutgoingConference(
    connectionManagerPhoneAccount: PhoneAccountHandle, 
    request: ConnectionRequest
): Conference?
```

Create a `Conference` given an outgoing request. This is used to initiate new outgoing conference call requested via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#startConference(kotlin.collections.MutableList,%20android.os.Bundle)`.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md): The connection manager account to use for managing this call. If this parameter is not `null`, it means that this `ConnectionService` has registered one or more `PhoneAccount`s having `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int`. This parameter will contain one of these `PhoneAccount`s, while the `request` will contain another (usually but not always distinct) `PhoneAccount` to be used for actually making the connection. If this parameter is `null`, it means that this `ConnectionService` is being asked to make a direct connection. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getAccountHandle()` of parameter `request` will be a `PhoneAccount` registered by this `ConnectionService` to use for making the connection. |
| `request` | [ConnectionRequest](ConnectionRequest.md): Details about the outgoing call. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Conference?` | The `Conference` object to satisfy this call. If the conference attempt is failed, the return value will be a result of an invocation of `https://developer.android.com/reference/kotlin/android/telecom/Connection#createFailedConnection(android.telecom.DisconnectCause)`. Return `null` if the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` cannot handle the call. |

### onCreateOutgoingConferenceFailed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateOutgoingConferenceFailed(
    connectionManagerPhoneAccount: PhoneAccountHandle, 
    request: ConnectionRequest
): Unit
```

Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Conference` was denied.

Used when a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` attempts to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Conference`, but Telecom has determined that the call cannot be placed at this time. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` is responisible for informing the user that the `https://developer.android.com/reference/kotlin/android/telecom/Conference` cannot be made at this time.

See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isOutgoingCallPermitted(android.telecom.PhoneAccountHandle)` for more information.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md): See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value cannot be `null`. |
| `request` | [ConnectionRequest](ConnectionRequest.md): The outgoing connection request. This value cannot be `null`. |

### onCreateOutgoingConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateOutgoingConnection(
    connectionManagerPhoneAccount: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Connection!
```

Create a `Connection` given an outgoing request. This is used to initiate new outgoing calls.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)!: The connection manager account to use for managing this call. If this parameter is not `null`, it means that this `ConnectionService` has registered one or more `PhoneAccount`s having `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int`. This parameter will contain one of these `PhoneAccount`s, while the `request` will contain another (usually but not always distinct) `PhoneAccount` to be used for actually making the connection. If this parameter is `null`, it means that this `ConnectionService` is being asked to make a direct connection. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getAccountHandle()` of parameter `request` will be a `PhoneAccount` registered by this `ConnectionService` to use for making the connection. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: Details about the outgoing call. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection!` | The `Connection` object to satisfy this call, or the result of an invocation of `https://developer.android.com/reference/kotlin/android/telecom/Connection#createFailedConnection(android.telecom.DisconnectCause)` to not handle the call. |

### onCreateOutgoingConnectionFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateOutgoingConnectionFailed(
    connectionManagerPhoneAccount: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Unit
```

Called by Telecom to inform the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` that its request to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Connection` was denied.

Used when a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` attempts to create a new outgoing `https://developer.android.com/reference/kotlin/android/telecom/Connection`, but Telecom has determined that the call cannot be placed at this time. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` is responisible for informing the user that the `https://developer.android.com/reference/kotlin/android/telecom/Connection` cannot be made at this time.

See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isOutgoingCallPermitted(android.telecom.PhoneAccountHandle)` for more information.

| Parameters ||
|---|---|
| `connectionManagerPhoneAccount` | [PhoneAccountHandle](PhoneAccountHandle.md)!: See description at `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateOutgoingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: The outgoing connection request. |

### onCreateOutgoingHandoverConnection

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateOutgoingHandoverConnection(
    fromPhoneAccountHandle: PhoneAccountHandle!, 
    request: ConnectionRequest!
): Connection!
```

Called by Telecom to request that a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` creates an instance of an outgoing handover `https://developer.android.com/reference/kotlin/android/telecom/Connection`.

A call handover is the process where an ongoing call is transferred from one app (i.e. `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` to another app. The user could, for example, choose to continue a mobile network call in a video calling app. The mobile network call via the Telephony stack is referred to as the source of the handover, and the video calling app is referred to as the destination.

When considering a handover scenario the *initiating* device is where a user initiated the handover process (e.g. by calling `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`, and the other device is considered the *receiving* device.

This method is called on the destination `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` on *initiating* device when the user initiates a handover request from one app to another. The user request originates in the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` via `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`.

For a full discussion of the handover process and the APIs involved, see `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`.

Implementations of this method should return an instance of `https://developer.android.com/reference/kotlin/android/telecom/Connection` which represents the handover. If your app does not wish to accept a handover to it at this time, you can return `null`. The code below shows an example of how this is done.

```kotlin
<code>public Connection onCreateIncomingHandoverConnection(PhoneAccountHandle
      fromPhoneAccountHandle, ConnectionRequest request) {
    if (!isHandoverAvailable()) {
        return null;
    }
    MyConnection connection = new MyConnection();
    connection.setAddress(request.getAddress(), TelecomManager.PRESENTATION_ALLOWED);
    connection.setVideoState(request.getVideoState());
    return connection;
  }
  </code>
```

| Parameters ||
|---|---|
| `fromPhoneAccountHandle` | [PhoneAccountHandle](PhoneAccountHandle.md)!: `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` associated with the ConnectionService which needs to handover the call. |
| `request` | [ConnectionRequest](ConnectionRequest.md)!: Details about the call to handover. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection!` | `https://developer.android.com/reference/kotlin/android/telecom/Connection` instance corresponding to the handover call. |

### onHandoverFailed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHandoverFailed(
    request: ConnectionRequest!, 
    error: Int
): Unit
```

Called by Telecom in response to a `TelecomManager#acceptHandover()` invocation which failed.

For a full discussion of the handover process and the APIs involved, see `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`

| Parameters ||
|---|---|
| `request` | [ConnectionRequest](ConnectionRequest.md)!: Details about the call which failed to handover. |
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Reason for handover failure. Will be one of the. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#HANDOVER_FAILURE_DEST_APP_REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#HANDOVER_FAILURE_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#HANDOVER_FAILURE_USER_REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#HANDOVER_FAILURE_ONGOING_EMERGENCY_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#HANDOVER_FAILURE_UNKNOWN:kotlin.Int` |

### onRemoteConferenceAdded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRemoteConferenceAdded(conference: RemoteConference!): Unit
```

Indicates that a remote conference has been created for existing `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection`s. When this method is invoked, this `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#` should create its own representation of the conference call and send it to telecom using `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#addConference(android.telecom.Conference)`.

This is only relevant to `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#`s which are registered with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int`.

| Parameters ||
|---|---|
| `conference` | [RemoteConference](RemoteConference.md)!: The remote conference call. |

### onRemoteExistingConnectionAdded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRemoteExistingConnectionAdded(connection: RemoteConnection!): Unit
```

Called when an existing connection is added remotely.

| Parameters ||
|---|---|
| `connection` | [RemoteConnection](RemoteConnection.md)!: The existing connection which was added. |

### onUnbind

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUnbind(intent: Intent!): Boolean
```

Called when all clients have disconnected from a particular interface published by the service. The default implementation does nothing and returns false.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md)!: The Intent that was used to bind to this service, as given to android.content.Context#bindService. Note that any extras that were included with the Intent at that point will *not* be seen here. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Return true if you would like to have the service's `https://developer.android.com/reference/kotlin/android/app/Service.html#onRebind(android.content.Intent)` method later called when new clients bind to it. |
