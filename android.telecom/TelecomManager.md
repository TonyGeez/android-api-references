Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelecomManager

```
open class TelecomManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telecom.TelecomManager](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#) |

The Android Telecom framework manages audio and video calls on an Android device. It acts as a central switchboard, connecting applications that provide calling capabilities (like SIM-based/telephony calls or VoIP apps) with applications that provide the user interface for calls (like the default Phone app). Key functions include routing calls, managing call states, and integrating various calling services into a consistent user experience. It allows developers to create replacements for the default phone app or integrate their own calling solutions (e.g., VoIP) into the native Android calling system.

Note: The operation of the Telecom framework (this manager class, and other APIs such as `https://developer.android.com/reference/kotlin/android/telecom/InCallService`, `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`) is gated by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String`. It is expected that the Telecom framework is available on ALL devices where "calls" may take place. A call is defined generally as any communication using a microphone and audio output device. This broadly includes phones, tablets, wearables such as watches, and integrated automotive OSes.

Common configurations include phones which will have both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String` and tablets which will only have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String`.

Apps do not instantiate this class directly; instead, they retrieve a reference to an instance through android.content.Context#getSystemService.

Note that access to some telecom information is permission-protected. Your app cannot access the protected information or gain access to protected functionality unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the method descriptions. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` Activity action: Triggers the calling UI and initiates a call back to a previous call made by the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CHANGE_DEFAULT_DIALER:kotlin.String` Activity action: Shows a dialog asking the user whether or not they want to replace the current default Dialer with the one specified in `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CHANGE_PHONE_ACCOUNTS:kotlin.String` The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the settings page used to configure `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` preferences. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CONFIGURE_CALL_LOG_INTEGRATION:kotlin.String` Activity Action: Show the settings for configuring call log integration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CONFIGURE_PHONE_ACCOUNT:kotlin.String` An `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action sent by the telecom framework to start a configuration dialog for a registered `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED:kotlin.String` Broadcast intent action indicating that the current default call screening app has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_DIALER_CHANGED:kotlin.String` Broadcast intent action indicating that the current default dialer has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_INCOMING_CALL:kotlin.String` Activity action: Starts the UI for handing an incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_PHONE_ACCOUNT_REGISTERED:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used indicate that a new phone account was just registered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_PHONE_ACCOUNT_UNREGISTERED:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used indicate that a phone account was just unregistered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_POST_CALL:kotlin.String` Start an activity indicating that the completion of an outgoing call or an incoming call which was not blocked by the `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService`, and which was NOT terminated while the call was in `https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_SHOW_CALL_ACCESSIBILITY_SETTINGS:kotlin.String` The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the call accessibility settings page. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_SHOW_CALL_SETTINGS:kotlin.String` The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the call settings page. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_SHOW_MISSED_CALLS_NOTIFICATION:kotlin.String` Broadcast intent action for letting custom component know to show the missed call notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_SHOW_RESPOND_VIA_SMS_SETTINGS:kotlin.String` The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the respond via SMS settings page. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_VOIP_CALL_LOG_PREFERENCE:kotlin.String` Broadcast intent action indicating that the call log preference is updated by the user. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_PAUSE:kotlin.Char` The dual tone multi-frequency signaling character sent to indicate the dialing system should pause for a predefined period. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DTMF_CHARACTER_WAIT:kotlin.Char` The dual-tone multi-frequency signaling character sent to indicate the dialing system should wait for user confirmation before proceeding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_LONG:kotlin.Int` A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 120 seconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_MEDIUM:kotlin.Int` A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 60 seconds and \< 120 seconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_SHORT:kotlin.Int` A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 3 seconds and \< 60 seconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_VERY_SHORT:kotlin.Int` A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \< 3 seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_BACK_NUMBER:kotlin.String` The number which the party on the other side of the line will see (and use to return the call). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DISCONNECT_CAUSE:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#ACTION_PHONE_STATE_CHANGED:kotlin.String` containing the disconnect code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DISCONNECT_MESSAGE:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#ACTION_PHONE_STATE_CHANGED:kotlin.String` containing the disconnect message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String` A integer value provided for completed calls to indicate the duration of the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_LOG_URI:kotlin.String` Extra URI that is used by a dialer to query the `https://developer.android.com/reference/kotlin/android/provider/CallLog.html#` content provider and associate a missed call notification with a call log entry. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_NETWORK_TYPE:kotlin.String` Optional extra for communicating the call network technology used by a `https://developer.android.com/reference/kotlin/android/telecom/Connection` to Telecom and InCallUI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_SUBJECT:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing a string call subject which will be associated with an outgoing call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_TYPE:kotlin.String` An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#` extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` to specify the desired call type for the callback. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME:kotlin.String` Extra value used to provide the package name for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CHANGE_DEFAULT_DIALER:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_DEFAULT_CALL_SCREENING_APP_COMPONENT_NAME:kotlin.String` Extra value used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED:kotlin.String` broadcast to indicate the ComponentName of the call screening app which has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_DISCONNECT_CAUSE:kotlin.String` A integer value provided for completed calls to indicate the reason for the call disconnection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_HANDLE:kotlin.String` A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` extra, which when set on the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_POST_CALL:kotlin.String` intent, indicates the uri handle(phone number) of the completed call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_HAS_PICTURE:kotlin.String` A boolean extra set on incoming calls to indicate that the call has a picture specified. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_CALL_ADDRESS:kotlin.String` The extra used by a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to provide the handle of the caller that has initiated a new incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_CALL_EXTRAS:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_INCOMING_CALL:kotlin.String` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` which contains metadata about the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_VIDEO_STATE:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` containing an integer that determines the requested video state for an incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_IS_DEFAULT_CALL_SCREENING_APP:kotlin.String` Extra value used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED:kotlin.String` broadcast to indicate whether an app is the default call screening app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_LOCATION:kotlin.String` Extra for the call composer call location, an `https://developer.android.com/reference/kotlin/android/location/Location.html#` parcelable class to represent the geolocation as a latitude and longitude pair. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_NOTIFICATION_COUNT:kotlin.String` The number of calls associated with the notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_NOTIFICATION_MISSED_REASON:kotlin.String` Extra indicating the reason why the call was missed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_NOTIFICATION_PHONE_NUMBER:kotlin.String` The number associated with the missed calls. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_OUTGOING_CALL_EXTRAS:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String` `Intent` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` which contains metadata about the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_OUTGOING_PICTURE:kotlin.String` A ParcelUuid used as a token to represent a picture that was uploaded prior to the call being placed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` The extra used with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String` `Intent` to specify a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` to use when making the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PICTURE_URI:kotlin.String` A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` representing the picture that was downloaded when a call is received or uploaded when a call is placed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PRIORITY:kotlin.String` Extra for the call composer call priority, either `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_NORMAL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_URGENT:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_RTT:kotlin.String` A boolean extra, which when set on the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent or on the bundle passed into `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)`, indicates that the call should be initiated with an RTT session open. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_SPEAKERPHONE:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing a boolean that determines whether the speakerphone should be automatically turned on for an outgoing call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_VIDEO_STATE:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing an integer that determines the desired video state for an outgoing call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_USE_ASSISTED_DIALING:kotlin.String` The boolean indicated by this extra controls whether or not a call is eligible to undergo assisted dialing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_UUID:kotlin.String` Extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` to specify the UUID value representing the call ID returned by `https://developer.android.com/reference/kotlin/android/telecom/CallControl#getCallId()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_VOIP_CALL_LOG_PREFERENCE_STATUS:kotlin.String` Extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_VOIP_CALL_LOG_PREFERENCE:kotlin.String` to specify the value of the VoIP call log preference for the app receiving the broadcast. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#GATEWAY_ORIGINAL_ADDRESS:kotlin.String` An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent extra corresponding to the original address to dial for the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#GATEWAY_PROVIDER_PACKAGE:kotlin.String` An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent extra denoting the package name of the app specifying an alternative gateway for the call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_EXTERNAL_CALLS:kotlin.String` A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` wants to be informed of calls which have the `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String` A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` wants to be informed of calls which have the `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_SELF_MANAGED:kotlin.Int` property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_IN_CALL_SERVICE_CAR_MODE_UI:kotlin.String` A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements an in-call user interface to be used while the device is in car-mode (see `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_CAR:kotlin.Int`). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_IN_CALL_SERVICE_RINGING:kotlin.String` A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements ringing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_IN_CALL_SERVICE_UI:kotlin.String` A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements an in-call user interface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRESENTATION_ALLOWED:kotlin.Int` Indicates that the address or number of a call is allowed to be displayed for caller ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRESENTATION_PAYPHONE:kotlin.Int` Indicates that the address or number of a call belongs to a pay phone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRESENTATION_RESTRICTED:kotlin.Int` Indicates that the address or number of a call is blocked by the other party. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRESENTATION_UNAVAILABLE:kotlin.Int` Indicates that the address or number of a call is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRESENTATION_UNKNOWN:kotlin.Int` Indicates that the address or number of a call is not specified or known by the carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_NORMAL:kotlin.Int` Indicates the call composer call priority is normal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_URGENT:kotlin.Int` Indicates the call composer call priority is urgent. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptHandover(android.net.Uri,%20kotlin.Int,%20android.telecom.PhoneAccountHandle)(srcAddr: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, destAcct: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Called by an app to indicate that it wishes to accept the handover of an ongoing call to a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` it defines. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptRingingCall()()` If there is a ringing incoming call, this method accepts the call on behalf of the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#acceptRingingCall(kotlin.Int)(videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` If there is a ringing incoming call, this method accepts the call on behalf of the user, with the specified video state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addCall(android.telecom.CallAttributes,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver,%20android.telecom.CallControlCallback,%20android.telecom.CallEventCallback)(callAttributes: https://developer.android.com/reference/kotlin/android/telecom/CallAttributes, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, pendingControl: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/telecom/CallControl!, https://developer.android.com/reference/kotlin/android/telecom/CallException!>, handshakes: https://developer.android.com/reference/kotlin/android/telecom/CallControlCallback, events: https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback)` Add a call to the Android system service Telecom. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)(phoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Registers a new incoming call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingConference(android.telecom.PhoneAccountHandle,%20android.os.Bundle)(phoneAccount: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Registers a new incoming conference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#cancelMissedCallsNotification()()` Removes the missed-call notification if one is present and marks missed calls in the call log as read. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#createManageBlockedNumbersIntent()()` Creates the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which can be used with `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` to launch the activity to manage blocked numbers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#endCall()()` Ends the foreground call on the device. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getAdnUriForPhoneAccount(android.telecom.PhoneAccountHandle)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Returns a URI (with the content:// scheme) specific to the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for ADN content retrieval. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getCallCapablePhoneAccounts()()` Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s which can be used to make and receive phone calls. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()()` Used to determine the currently selected default dialer package. |
| open [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultOutgoingPhoneAccount(kotlin.String)(uriScheme: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which will be used to place outgoing calls to addresses with the specified `uriScheme`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getLine1Number(android.telecom.PhoneAccountHandle)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Return the line 1 phone number for given phone account. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!\> | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getOwnSelfManagedPhoneAccounts()()` Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s owned by the calling self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. |
| open [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getPhoneAccount(android.telecom.PhoneAccountHandle)(account: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for a specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount)!\> | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getRegisteredPhoneAccounts()()` This API will return all `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s the caller registered via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!\> | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getSelfManagedPhoneAccounts()()` Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s for all self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s owned by the calling `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#`. |
| open [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getSimCallManager()()` Returns the current SIM call manager. |
| open [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)? | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getSimCallManagerForSubscription(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns current SIM call manager for the Telephony Subscription ID specified. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getSystemDialerPackage()()` Determines the package name of the system-provided default phone app. |
| open [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)? | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getUserSelectedOutgoingPhoneAccount()()` Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which is the user-chosen default for making outgoing phone calls. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getVoiceMailNumber(android.telecom.PhoneAccountHandle)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Return the voicemail number for a given phone account. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#handleMmi(kotlin.String)(dialString: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Processes the specified dial string as an MMI code. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#handleMmi(kotlin.String,%20android.telecom.PhoneAccountHandle)(dialString: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Processes the specified dial string as an MMI code. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#hasManageOngoingCallsPermission()()` Returns whether the caller has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_ONGOING_CALLS:kotlin.String` permission. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isInCall()()` Returns whether there is an ongoing phone call (can be in dialing, ringing, active or holding states) originating from either a manager or self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isInExternalCall()()` Returns whether there is an ongoing phone call (can be in dialing, ringing, active or holding states) that is an external call. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isInManagedCall()()` Returns whether there is an ongoing call originating from a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isIncomingCallPermitted(android.telecom.PhoneAccountHandle)(phoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Determines whether Telecom would permit an incoming call to be added via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` API for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isOutgoingCallPermitted(android.telecom.PhoneAccountHandle)(phoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Determines whether Telecom would permit an outgoing call to be placed via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)` API for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isTtySupported()()` Returns whether TTY is supported on this device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isVoiceMailNumber(android.telecom.PhoneAccountHandle,%20kotlin.String)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return whether a given phone number is the configured voicemail number for a particular phone account. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)(address: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Places a new outgoing call to the provided address using the system telecom service with the specified extras. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)(account: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount!)` Register a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for use by the system that will be stored in Device Encrypted storage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#showInCallScreen(kotlin.Boolean)(showDialpad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Brings the in-call screen to the foreground if there is an ongoing call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#silenceRinger()()` Silences the ringer if a ringing call exists. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#startConference(kotlin.collections.MutableList,%20android.os.Bundle)(participants: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Place a new adhoc conference call with the provided participants using the system telecom service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#unregisterPhoneAccount(android.telecom.PhoneAccountHandle)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!)` Remove a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` registration from the system. |

## Constants

### ACTION_CALL_BACK

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CALL_BACK: String
```

Activity action: Triggers the calling UI and initiates a call back to a previous call made by the application. The specific call to be re-called is identified by the UUID, which must be included as an extra in the intent using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_UUID:kotlin.String`

Note: VoIP apps should register the intent if they need to integrate the call history into the system call logs.

<br />

 Value: "android.telecom.action.CALL_BACK"

### ACTION_CHANGE_DEFAULT_DIALER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANGE_DEFAULT_DIALER: String
```

Activity action: Shows a dialog asking the user whether or not they want to replace the current default Dialer with the one specified in `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME:kotlin.String`. Usage example:

```kotlin
Intent intent = new Intent(TelecomManager.ACTION_CHANGE_DEFAULT_DIALER);
  intent.putExtra(TelecomManager.EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME,
          getActivity().getPackageName());
  startActivity(intent);
  
```

<br />

This is no longer supported since Q, please use `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#createRequestRoleIntent(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_DIALER:kotlin.String` instead.

 Value: "android.telecom.action.CHANGE_DEFAULT_DIALER"

### ACTION_CHANGE_PHONE_ACCOUNTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANGE_PHONE_ACCOUNTS: String
```

The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the settings page used to configure `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` preferences.

 Value: "android.telecom.action.CHANGE_PHONE_ACCOUNTS"

### ACTION_CONFIGURE_CALL_LOG_INTEGRATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONFIGURE_CALL_LOG_INTEGRATION: String
```

Activity Action: Show the settings for configuring call log integration.

This activity allows the user to view and turn off/on the system call logs for available VoIP applications that have integrated with the system's call log.

This activity must be present on a device that supports call log integration.

 Value: "android.telecom.action.CONFIGURE_CALL_LOG_INTEGRATION"

### ACTION_CONFIGURE_PHONE_ACCOUNT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONFIGURE_PHONE_ACCOUNT: String
```

An `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action sent by the telecom framework to start a configuration dialog for a registered `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. There is no default dialog and each app that registers a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` should provide one if desired.

A user can access the list of enabled `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s through the Phone app's settings menu. For each entry, the settings app will add a click action. When triggered, the click-action will start this intent along with the extra `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` to indicate the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` to configure. If the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` package does not register an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` for this intent, then it will not be sent.

 Value: "android.telecom.action.CONFIGURE_PHONE_ACCOUNT"

### ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED: String
```

Broadcast intent action indicating that the current default call screening app has changed.

Note: This intent is NEVER actually broadcast and will be deprecated in the future.

An app that want to know if it holds the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_CALL_SCREENING:kotlin.String` role can use `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#isRoleHeld(kotlin.String)` to confirm if it holds the role or not.

 Value: "android.telecom.action.DEFAULT_CALL_SCREENING_APP_CHANGED"

### ACTION_DEFAULT_DIALER_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEFAULT_DIALER_CHANGED: String
```

Broadcast intent action indicating that the current default dialer has changed. The string extra `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME:kotlin.String` will contain the name of the package that the default dialer was changed to.

 Value: "android.telecom.action.DEFAULT_DIALER_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME:kotlin.String`

### ACTION_INCOMING_CALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_INCOMING_CALL: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` instead.*

Activity action: Starts the UI for handing an incoming call. This intent starts the in-call UI by notifying the Telecom system that an incoming call exists for a specific call service (see `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`). Telecom reads the Intent extras to find and bind to the appropriate `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` which Telecom will ultimately use to control and get information about the call.

Input: get\*Extra field `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` contains the component name of the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` that Telecom should bind to. Telecom will then ask the connection service for more information about the call prior to showing any UI.

 Value: "android.telecom.action.INCOMING_CALL"

### ACTION_PHONE_ACCOUNT_REGISTERED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PHONE_ACCOUNT_REGISTERED: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used indicate that a new phone account was just registered.

The Intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#getExtras()` will contain `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` to indicate which `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` was registered.

Will only be sent to the default dialer app (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`).

 Value: "android.telecom.action.PHONE_ACCOUNT_REGISTERED"

### ACTION_PHONE_ACCOUNT_UNREGISTERED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PHONE_ACCOUNT_UNREGISTERED: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used indicate that a phone account was just unregistered.

The Intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#getExtras()` will contain `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` to indicate which `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` was unregistered.

Will only be sent to the default dialer app (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`).

 Value: "android.telecom.action.PHONE_ACCOUNT_UNREGISTERED"

### ACTION_POST_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_POST_CALL: String
```

Start an activity indicating that the completion of an outgoing call or an incoming call which was not blocked by the `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService`, and which was NOT terminated while the call was in `https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_AUDIO_PROCESSING:kotlin.Int`. The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` extra `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_HANDLE:kotlin.String` will contain the uri handle(phone number) for the call which completed. The integer extra `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_DISCONNECT_CAUSE:kotlin.String` will indicate the reason for the call disconnection. See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_DISCONNECT_CAUSE:kotlin.String` for more information. The integer extra `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String` will indicate the duration of the call. See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String` for more information.

 Value: "android.telecom.action.POST_CALL"

### ACTION_SHOW_CALL_ACCESSIBILITY_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_CALL_ACCESSIBILITY_SETTINGS: String
```

The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the call accessibility settings page.

 Value: "android.telecom.action.SHOW_CALL_ACCESSIBILITY_SETTINGS"

### ACTION_SHOW_CALL_SETTINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_CALL_SETTINGS: String
```

The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the call settings page.

 Value: "android.telecom.action.SHOW_CALL_SETTINGS"

### ACTION_SHOW_MISSED_CALLS_NOTIFICATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_MISSED_CALLS_NOTIFICATION: String
```

Broadcast intent action for letting custom component know to show the missed call notification. If no custom component exists then this is sent to the default dialer which should post a missed-call notification.

 Value: "android.telecom.action.SHOW_MISSED_CALLS_NOTIFICATION"

### ACTION_SHOW_RESPOND_VIA_SMS_SETTINGS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_RESPOND_VIA_SMS_SETTINGS: String
```

The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to show the respond via SMS settings page.

 Value: "android.telecom.action.SHOW_RESPOND_VIA_SMS_SETTINGS"

### ACTION_VOIP_CALL_LOG_PREFERENCE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VOIP_CALL_LOG_PREFERENCE: String
```

Broadcast intent action indicating that the call log preference is updated by the user.

The intent is sent to VoIP applications whose preferences have been affected by the user's choice. Upon receiving this broadcast, the application may re-evaluate its behavior regarding call log entries.

To receive this broadcast, applications must declare a receiver in their manifest file with an intent filter for this action.

 Value: "android.telecom.action.VOIP_CALL_LOG_PREFERENCE"

### DTMF_CHARACTER_PAUSE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DTMF_CHARACTER_PAUSE: Char
```

The dual tone multi-frequency signaling character sent to indicate the dialing system should pause for a predefined period.

 Value: ','

### DTMF_CHARACTER_WAIT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DTMF_CHARACTER_WAIT: Char
```

The dual-tone multi-frequency signaling character sent to indicate the dialing system should wait for user confirmation before proceeding.

 Value: ';'

### DURATION_LONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_LONG: Int
```

A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 120 seconds.

 Value: 3

### DURATION_MEDIUM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_MEDIUM: Int
```

A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 60 seconds and \< 120 seconds.

 Value: 2

### DURATION_SHORT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_SHORT: Int
```

A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \>= 3 seconds and \< 60 seconds.

 Value: 1

### DURATION_VERY_SHORT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_VERY_SHORT: Int
```

A integer value for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_DURATION:kotlin.String`, indicates the duration of the completed call was \< 3 seconds.

 Value: 0

### EXTRA_CALL_BACK_NUMBER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_BACK_NUMBER: String
```

The number which the party on the other side of the line will see (and use to return the call).

`https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s which interact with `https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection`s should only populate this if the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getLine1Number()` value, as that is the user's expected caller ID.

 Value: "android.telecom.extra.CALL_BACK_NUMBER"

### EXTRA_CALL_DISCONNECT_CAUSE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_DISCONNECT_CAUSE: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#ACTION_PHONE_STATE_CHANGED:kotlin.String` containing the disconnect code.

 Value: "android.telecom.extra.CALL_DISCONNECT_CAUSE"

### EXTRA_CALL_DISCONNECT_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_DISCONNECT_MESSAGE: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#ACTION_PHONE_STATE_CHANGED:kotlin.String` containing the disconnect message.

 Value: "android.telecom.extra.CALL_DISCONNECT_MESSAGE"

### EXTRA_CALL_DURATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_DURATION: String
```

A integer value provided for completed calls to indicate the duration of the call.

Allowed values:

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_VERY_SHORT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_SHORT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_MEDIUM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#DURATION_LONG:kotlin.Int`

<br />

 Value: "android.telecom.extra.CALL_DURATION"

### EXTRA_CALL_LOG_URI

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_LOG_URI: String
```

Extra URI that is used by a dialer to query the `https://developer.android.com/reference/kotlin/android/provider/CallLog.html#` content provider and associate a missed call notification with a call log entry.

 Value: "android.telecom.extra.CALL_LOG_URI"

### EXTRA_CALL_NETWORK_TYPE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_NETWORK_TYPE: String
```

Optional extra for communicating the call network technology used by a `https://developer.android.com/reference/kotlin/android/telecom/Connection` to Telecom and InCallUI. `NETWORK_TYPE_*` in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`.

 Value: "android.telecom.extra.CALL_NETWORK_TYPE"

### EXTRA_CALL_SUBJECT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_SUBJECT: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing a string call subject which will be associated with an outgoing call. Should only be specified if the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` supports the capability `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_SUBJECT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_COMPOSER:kotlin.Int`.

 Value: "android.telecom.extra.CALL_SUBJECT"

### EXTRA_CALL_TYPE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_TYPE: String
```

An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#` extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` to specify the desired call type for the callback.

The value must be one of `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#AUDIO_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#VIDEO_CALL:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#MESSAGING:kotlin.Int`.

Type: int

When an application receives an `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` intent, it should check for this extra. If present, the application should attempt to initiate the callback using the specified call type. If this extra is not provided, the application should default to using the original call type associated with the call.

The initiating Dialer app must confirm whether the desired call type is supported by the target application before specifying this extra. Not all apps will support all callback types and it is the caller's responsibility to validate this.

 Value: "android.telecom.extra.CALL_TYPE"

### EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHANGE_DEFAULT_DIALER_PACKAGE_NAME: String
```

Extra value used to provide the package name for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CHANGE_DEFAULT_DIALER:kotlin.String`.

 Value: "android.telecom.extra.CHANGE_DEFAULT_DIALER_PACKAGE_NAME"

### EXTRA_DEFAULT_CALL_SCREENING_APP_COMPONENT_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DEFAULT_CALL_SCREENING_APP_COMPONENT_NAME: String
```

Extra value used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED:kotlin.String` broadcast to indicate the ComponentName of the call screening app which has changed.

Note: This extra is NOT used and will be deprecated in the future.

 Value: "android.telecom.extra.DEFAULT_CALL_SCREENING_APP_COMPONENT_NAME"

### EXTRA_DISCONNECT_CAUSE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISCONNECT_CAUSE: String
```

A integer value provided for completed calls to indicate the reason for the call disconnection.

Allowed values:

- `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int`

<br />

 Value: "android.telecom.extra.DISCONNECT_CAUSE"

### EXTRA_HANDLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HANDLE: String
```

A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` extra, which when set on the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_POST_CALL:kotlin.String` intent, indicates the uri handle(phone number) of the completed call.

 Value: "android.telecom.extra.HANDLE"

### EXTRA_HAS_PICTURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HAS_PICTURE: String
```

A boolean extra set on incoming calls to indicate that the call has a picture specified. Given that image download could take a (short) time, the EXTRA is set immediately upon adding the call to the Dialer app, this allows the Dialer app to reserve space for an image if one is expected. The EXTRA may be unset if the image download ends up failing for some reason.

 Value: "android.telecom.extra.HAS_PICTURE"

### EXTRA_INCOMING_CALL_ADDRESS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INCOMING_CALL_ADDRESS: String
```

The extra used by a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to provide the handle of the caller that has initiated a new incoming call.

 Value: "android.telecom.extra.INCOMING_CALL_ADDRESS"

### EXTRA_INCOMING_CALL_EXTRAS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INCOMING_CALL_EXTRAS: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_INCOMING_CALL:kotlin.String` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` which contains metadata about the call. This `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` will be returned to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`.

 Value: "android.telecom.extra.INCOMING_CALL_EXTRAS"

### EXTRA_INCOMING_VIDEO_STATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INCOMING_VIDEO_STATE: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` containing an integer that determines the requested video state for an incoming call. Valid options: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`.

 Value: "android.telecom.extra.INCOMING_VIDEO_STATE"

### EXTRA_IS_DEFAULT_CALL_SCREENING_APP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_DEFAULT_CALL_SCREENING_APP: String
```

Extra value used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_DEFAULT_CALL_SCREENING_APP_CHANGED:kotlin.String` broadcast to indicate whether an app is the default call screening app.

Note: This extra is NOT used and will be deprecated in the future.

 Value: "android.telecom.extra.IS_DEFAULT_CALL_SCREENING_APP"

### EXTRA_LOCATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LOCATION: String
```

Extra for the call composer call location, an `https://developer.android.com/reference/kotlin/android/location/Location.html#` parcelable class to represent the geolocation as a latitude and longitude pair. Reference: RCC.20 Section 2.4.3.2

 Value: "android.telecom.extra.LOCATION"

### EXTRA_NOTIFICATION_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_COUNT: String
```

The number of calls associated with the notification. If the number is zero then the missed call notification should be dismissed.

 Value: "android.telecom.extra.NOTIFICATION_COUNT"

### EXTRA_NOTIFICATION_MISSED_REASON

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_MISSED_REASON: String
```

Extra indicating the reason why the call was missed. Passed as a long extra in `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_SHOW_MISSED_CALLS_NOTIFICATION:kotlin.String`. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#AUTO_MISSED_EMERGENCY_CALL:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#AUTO_MISSED_MAXIMUM_RINGING:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#AUTO_MISSED_MAXIMUM_DIALING:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#AUTO_MISSED_UNWANTED:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_NO_ANSWER:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_SHORT_RING:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_DND_MODE:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_LOW_RING_VOLUME:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_NO_VIBRATE:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_CALL_SCREENING_SERVICE_SILENCED:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#USER_MISSED_CALL_FILTERS_TIMEOUT:kotlin.Long`

<br />

 Value: "android.telecom.extra.NOTIFICATION_MISSED_REASON"

### EXTRA_NOTIFICATION_PHONE_NUMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_PHONE_NUMBER: String
```

The number associated with the missed calls. This number is only relevant when EXTRA_NOTIFICATION_COUNT is 1.

 Value: "android.telecom.extra.NOTIFICATION_PHONE_NUMBER"

### EXTRA_OUTGOING_CALL_EXTRAS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_OUTGOING_CALL_EXTRAS: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String` `Intent` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` which contains metadata about the call. This `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` will be saved into `Call.Details` and passed to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` when placing the call.

 Value: "android.telecom.extra.OUTGOING_CALL_EXTRAS"

### EXTRA_OUTGOING_PICTURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_OUTGOING_PICTURE: String
```

A ParcelUuid used as a token to represent a picture that was uploaded prior to the call being placed. The value of this extra should be set using the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` obtained from the callback in android.telephony.TelephonyManager#uploadCallComposerPicture.

 Value: "android.telecom.extra.OUTGOING_PICTURE"

### EXTRA_PHONE_ACCOUNT_HANDLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PHONE_ACCOUNT_HANDLE: String
```

The extra used with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String` `Intent` to specify a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` to use when making the call.

Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "android.telecom.extra.PHONE_ACCOUNT_HANDLE"

### EXTRA_PICTURE_URI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICTURE_URI: String
```

A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` representing the picture that was downloaded when a call is received or uploaded when a call is placed. This is a content URI within the call log provider which can be used to open a file descriptor. This could be set a short time after a call is added to the Dialer app if the download/upload is delayed for some reason. The Dialer app will receive a callback via `https://developer.android.com/reference/kotlin/android/telecom/Call.Callback#onDetailsChanged(android.telecom.Call,%20android.telecom.Call.Details)` when this value has changed. Reference: RCC.20 Section 2.4.3.2

 Value: "android.telecom.extra.PICTURE_URI"

### EXTRA_PRIORITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PRIORITY: String
```

Extra for the call composer call priority, either `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_NORMAL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#PRIORITY_URGENT:kotlin.Int`. Reference: RCC.20 Section 2.4.4.2

 Value: "android.telecom.extra.PRIORITY"

### EXTRA_START_CALL_WITH_RTT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_START_CALL_WITH_RTT: String
```

A boolean extra, which when set on the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent or on the bundle passed into `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)`, indicates that the call should be initiated with an RTT session open. See `https://developer.android.com/reference/kotlin/android/telecom/Call.RttCall` for more information on RTT.

 Value: "android.telecom.extra.START_CALL_WITH_RTT"

### EXTRA_START_CALL_WITH_SPEAKERPHONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_START_CALL_WITH_SPEAKERPHONE: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing a boolean that determines whether the speakerphone should be automatically turned on for an outgoing call.

 Value: "android.telecom.extra.START_CALL_WITH_SPEAKERPHONE"

### EXTRA_START_CALL_WITH_VIDEO_STATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_START_CALL_WITH_VIDEO_STATE: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` containing an integer that determines the desired video state for an outgoing call. Valid options: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`.

 Value: "android.telecom.extra.START_CALL_WITH_VIDEO_STATE"

### EXTRA_USE_ASSISTED_DIALING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_USE_ASSISTED_DIALING: String
```

The boolean indicated by this extra controls whether or not a call is eligible to undergo assisted dialing. This extra is stored under `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_OUTGOING_CALL_EXTRAS:kotlin.String`.

The call initiator can use this extra to indicate that a call used assisted dialing to help place the call. This is most commonly used by a Dialer app which provides the ability to automatically add dialing prefixes when placing international calls.

Setting this extra on the outgoing call extras will cause the `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_ASSISTED_DIALING:kotlin.Int` property and `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_ASSISTED_DIALING:kotlin.Int` property to be set on the `https://developer.android.com/reference/kotlin/android/telecom/Connection`/`https://developer.android.com/reference/kotlin/android/telecom/Call` in question. When the call is logged to the call log, the `https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls.html#FEATURES_ASSISTED_DIALING_USED:kotlin.Int` call feature is set to indicate that assisted dialing was used for the call.

 Value: "android.telecom.extra.USE_ASSISTED_DIALING"

### EXTRA_UUID

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_UUID: String
```

Extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` to specify the UUID value representing the call ID returned by `https://developer.android.com/reference/kotlin/android/telecom/CallControl#getCallId()`.

This extra is required when using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` to initiate a callback to a specific call.

Type: String

Applications that support the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` intent should obtain the UUID value by calling `https://developer.android.com/reference/kotlin/android/telecom/CallControl#getCallId()` during the initial call and persist this UUID along with other call-related information. When receiving the UUID via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` intent, the application should retrieve the corresponding call information using the provided UUID and initiate a new call using the stored details.

 Value: "android.telecom.extra.UUID"

### EXTRA_VOIP_CALL_LOG_PREFERENCE_STATUS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VOIP_CALL_LOG_PREFERENCE_STATUS: String
```

Extra used with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_VOIP_CALL_LOG_PREFERENCE:kotlin.String` to specify the value of the VoIP call log preference for the app receiving the broadcast.

This extra is required when using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_VOIP_CALL_LOG_PREFERENCE:kotlin.String` to signal what the preference for an app was changed to.

Type: boolean

Applications that support the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_VOIP_CALL_LOG_PREFERENCE:kotlin.String` will receive broadcast updates for their app when the VoIP call log preference changes. They can use this to determine if their VoIP call log will be logged to the system call log so that caching mechanisms to store call information can be conditionally enforced.

 Value: "android.telecom.extra.VOIP_CALL_LOG_PREFERENCE_STATUS"

### GATEWAY_ORIGINAL_ADDRESS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATEWAY_ORIGINAL_ADDRESS: String
```

An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent extra corresponding to the original address to dial for the call. This is used when an alternative gateway address is provided to recall the original address. The value is a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. (See `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#GATEWAY_PROVIDER_PACKAGE:kotlin.String` for details)

 Value: "android.telecom.extra.GATEWAY_ORIGINAL_ADDRESS"

### GATEWAY_PROVIDER_PACKAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATEWAY_PROVIDER_PACKAGE: String
```

An optional `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent extra denoting the package name of the app specifying an alternative gateway for the call. The value is a string. (The following comment corresponds to the all GATEWAY_\* extras) An app which sends the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent can specify an alternative address to dial which is different from the one specified and displayed to the user. This alternative address is referred to as the gateway address.

 Value: "android.telecom.extra.GATEWAY_PROVIDER_PACKAGE"

### METADATA_INCLUDE_EXTERNAL_CALLS

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_INCLUDE_EXTERNAL_CALLS: String
```

A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` wants to be informed of calls which have the `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` property. An external call is one which a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` knows about, but is not connected to directly. Dialer implementations (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`) which would like to be informed of external calls should set this meta-data to `true` in the manifest registration of their `https://developer.android.com/reference/kotlin/android/telecom/InCallService`. By default, the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` will NOT be informed of external calls.

 Value: "android.telecom.INCLUDE_EXTERNAL_CALLS"

### METADATA_INCLUDE_SELF_MANAGED_CALLS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_INCLUDE_SELF_MANAGED_CALLS: String
```

A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` wants to be informed of calls which have the `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_SELF_MANAGED:kotlin.Int` property. A self-managed call is one which originates from a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` which has chosen to implement its own call user interface. An `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implementation which would like to be informed of external calls should set this meta-data to `true` in the manifest registration of their `https://developer.android.com/reference/kotlin/android/telecom/InCallService`. By default, the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` will NOT be informed about self-managed calls.

An `https://developer.android.com/reference/kotlin/android/telecom/InCallService` which receives self-managed calls is free to view and control the state of calls in the self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. An example use-case is exposing these calls to an automotive device via its companion app.

See also `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_SELF_MANAGED:kotlin.Int`.

 Value: "android.telecom.INCLUDE_SELF_MANAGED_CALLS"

### METADATA_IN_CALL_SERVICE_CAR_MODE_UI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_IN_CALL_SERVICE_CAR_MODE_UI: String
```

A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements an in-call user interface to be used while the device is in car-mode (see `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_CAR:kotlin.Int`).

 Value: "android.telecom.IN_CALL_SERVICE_CAR_MODE_UI"

### METADATA_IN_CALL_SERVICE_RINGING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_IN_CALL_SERVICE_RINGING: String
```

A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements ringing. Dialer implementations (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`) which would also like to override the system provided ringing should set this meta-data to `true` in the manifest registration of their `https://developer.android.com/reference/kotlin/android/telecom/InCallService`.

When `true`, it is the `https://developer.android.com/reference/kotlin/android/telecom/InCallService`'s responsibility to play a ringtone for all incoming calls.

 Value: "android.telecom.IN_CALL_SERVICE_RINGING"

### METADATA_IN_CALL_SERVICE_UI

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_IN_CALL_SERVICE_UI: String
```

A boolean meta-data value indicating whether an `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implements an in-call user interface. Dialer implementations (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`) which would also like to replace the in-call interface should set this meta-data to `true` in the manifest registration of their `https://developer.android.com/reference/kotlin/android/telecom/InCallService`.

 Value: "android.telecom.IN_CALL_SERVICE_UI"

### PRESENTATION_ALLOWED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRESENTATION_ALLOWED: Int
```

Indicates that the address or number of a call is allowed to be displayed for caller ID.

 Value: 1

### PRESENTATION_PAYPHONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRESENTATION_PAYPHONE: Int
```

Indicates that the address or number of a call belongs to a pay phone.

 Value: 4

### PRESENTATION_RESTRICTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRESENTATION_RESTRICTED: Int
```

Indicates that the address or number of a call is blocked by the other party.

 Value: 2

### PRESENTATION_UNAVAILABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRESENTATION_UNAVAILABLE: Int
```

Indicates that the address or number of a call is unavailable.

 Value: 5

### PRESENTATION_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRESENTATION_UNKNOWN: Int
```

Indicates that the address or number of a call is not specified or known by the carrier.

 Value: 3

### PRIORITY_NORMAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_NORMAL: Int
```

Indicates the call composer call priority is normal. Reference: RCC.20 Section 2.4.4.2

 Value: 0

### PRIORITY_URGENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_URGENT: Int
```

Indicates the call composer call priority is urgent. Reference: RCC.20 Section 2.4.4.2

 Value: 1

## Public methods

### acceptHandover

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptHandover(
    srcAddr: Uri!, 
    videoState: Int, 
    destAcct: PhoneAccountHandle!
): Unit
```

Called by an app to indicate that it wishes to accept the handover of an ongoing call to a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` it defines.

A call handover is the process where an ongoing call is transferred from one app (i.e. `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to another app. The user could, for example, choose to continue a mobile network call in a video calling app. The mobile network call via the Telephony stack is referred to as the source of the handover, and the video calling app is referred to as the destination.

When considering a handover scenario the *initiating* device is where a user initiated the handover process (e.g. by calling `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`, and the other device is considered the *receiving* device.

For a full discussion of the handover process and the APIs involved, see `https://developer.android.com/reference/kotlin/android/telecom/Call#handoverTo(android.telecom.PhoneAccountHandle,%20kotlin.Int,%20android.os.Bundle)`.

This method is called from the *receiving* side of a handover to indicate a desire to accept the handover of an ongoing call to another `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` identified by `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` destAcct. For managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s, the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` must have been registered with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` and the user must have enabled the corresponding `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. This can be checked using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getPhoneAccount(android.telecom.PhoneAccountHandle)`. Self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` to handover a call to it.

Once invoked, this method will cause the system to bind to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` associated with the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` destAcct and call (See `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingHandoverConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`).

For a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if either the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` destAcct does not correspond to a registered `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` or the associated `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` is not currently enabled by the user.

For a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if the calling app does not have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`.

| Parameters ||
|---|---|
| `srcAddr` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the ongoing call to handover to the caller's `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. |
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Video state after the handover. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int` |
| `destAcct` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` registered to the calling package. |

### acceptRingingCall

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptRingingCall(): Unit
```

**Deprecated:** *Companion apps for wearable devices should use the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` API instead.*

If there is a ringing incoming call, this method accepts the call on behalf of the user. If the incoming call is a video call, the call will be answered with the same video state as the incoming call requests. This means, for example, that an incoming call requesting `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int` will be answered, accepting that state. If the ringing incoming call is self-managed, this method will only accept the call if the caller of this method is privileged (i.e. system, shell, or root) or system UI. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ANSWER_PHONE_CALLS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

### acceptRingingCall

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptRingingCall(videoState: Int): Unit
```

**Deprecated:** *Companion apps for wearable devices should use the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` API instead.*

If there is a ringing incoming call, this method accepts the call on behalf of the user, with the specified video state. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ANSWER_PHONE_CALLS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired video state to answer the call with. |

### addCall

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCall(
    callAttributes: CallAttributes, 
    executor: Executor, 
    pendingControl: OutcomeReceiver<CallControl!, CallException!>, 
    handshakes: CallControlCallback, 
    events: CallEventCallback
): Unit
```

Add a call to the Android system service Telecom. This allows the system to start tracking an incoming or outgoing call with the specified `https://developer.android.com/reference/kotlin/android/telecom/CallAttributes`. Once a call is added, a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle.html#` notification should be posted and when the call is ready to be disconnected, use `https://developer.android.com/reference/kotlin/android/telecom/CallControl#disconnect(android.telecom.DisconnectCause,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is provided by the `pendingControl#onResult(CallControl)`

**Call Lifecycle** : Your app is given foreground execution priority as long as you have a valid call and are posting a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle.html#` notification. When your application is given foreground execution priority, your app is treated as a foreground service. Foreground execution priority will prevent the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` from killing your application when it is placed the background. Foreground execution priority is removed from your app when all of your app's calls terminate or your app no longer posts a valid notification.

**Note** : Only packages that register with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_TRANSACTIONAL_OPERATIONS:kotlin.Int` can utilize this API. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s that set the capabilities `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SIM_SUBSCRIPTION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_PROVIDER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` are not supported and will cause an exception to be thrown.

**Foreground Service (FGS) Guidance:**

To maintain Telecom's temporary FGS delegation, VoIP apps must use a stable Notification ID for the duration of the call. When transitioning from an incoming to an ongoing call, update the existing notification in place using `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)` instead of canceling the previous notification.

**Usage example:**

```kotlin
// Its up to your app on how you want to wrap the objects. One such implementation can be:
   class MyVoipCall {
     ...
       public CallControlCallEventCallback handshakes = new  CallControlCallback() {
                          ...
                         }
 
       public CallEventCallback events = new CallEventCallback() {
                          ...
                         }
 
       public MyVoipCall(String id){
           ...
       }
   }
 
  MyVoipCall myFirstOutgoingCall = new MyVoipCall("1");
 
  telecomManager.addCall(callAttributes,
                         Runnable::run,
                         new OutcomeReceiver() {
                               public void onResult(CallControl callControl) {
                                  // The call has been added successfully. For demonstration
                                  // purposes, the call is disconnected immediately ...
                                  callControl.disconnect(
                                                  new DisconnectCause(DisconnectCause.LOCAL) )
                               }
                            },
                            myFirstOutgoingCall.handshakes,
                            myFirstOutgoingCall.events);
  
```
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`

| Parameters ||
|---|---|
| `callAttributes` | [CallAttributes](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes): attributes of the new call (incoming or outgoing, address, etc.). This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): execution context to run `https://developer.android.com/reference/kotlin/android/telecom/CallControlCallback` updates on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `pendingControl` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [CallControl](https://developer.android.com/reference/kotlin/android/telecom/CallControl)!, [CallException](https://developer.android.com/reference/kotlin/android/telecom/CallException)!\>: Receives the result of addCall transaction. Upon success, a CallControl object is provided which can be used to do things like disconnect the call that was added. This value cannot be `null`. |
| `handshakes` | [CallControlCallback](https://developer.android.com/reference/kotlin/android/telecom/CallControlCallback): callback that receives **actionable** updates that originate from Telecom. This value cannot be `null`. |
| `events` | [CallEventCallback](https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback): callback that receives **non** -actionable updates that originate from Telecom. This value cannot be `null`. |

### addNewIncomingCall

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addNewIncomingCall(
    phoneAccount: PhoneAccountHandle!, 
    extras: Bundle!
): Unit
```

Registers a new incoming call. A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` should invoke this method when it has an incoming call. For managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s, the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` must have been registered with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` and the user must have enabled the corresponding `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. This can be checked using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getPhoneAccount(android.telecom.PhoneAccountHandle)`. Self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` to add a new incoming call.

Specify the address associated with the incoming call using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_CALL_ADDRESS:kotlin.String`. If an incoming call is from an anonymous source, omit this extra and ensure you specify a valid number presentation via `https://developer.android.com/reference/kotlin/android/telecom/Connection#setAddress(android.net.Uri,%20kotlin.Int)` on the `https://developer.android.com/reference/kotlin/android/telecom/Connection` instance you return in your `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)` implementation.

The incoming call you are adding is assumed to have a video state of `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, unless the extra value `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_VIDEO_STATE:kotlin.String` is specified.

Once invoked, this method will cause the system to bind to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` associated with the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` and request additional information about the call (See `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`) before starting the incoming call UI.

For a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if either the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` does not correspond to a registered `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` or the associated `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` is not currently enabled by the user.

For a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` has `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` and the calling app does not have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`.

**Note** : `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle.html#` notifications should be posted after the call is added to Telecom in order for the notification to be non-dismissible.

| Parameters ||
|---|---|
| `phoneAccount` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: A `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` registered with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: A bundle that will be passed through to `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConnection(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. |

### addNewIncomingConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addNewIncomingConference(
    phoneAccount: PhoneAccountHandle, 
    extras: Bundle
): Unit
```

Registers a new incoming conference. A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` should invoke this method when it has an incoming conference. An incoming `https://developer.android.com/reference/kotlin/android/telecom/Conference` is an adhoc conference call initiated on another device which the user is being invited to join in. For managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s, the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` must have been registered with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` and the user must have enabled the corresponding `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. This can be checked using `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getPhoneAccount(android.telecom.PhoneAccountHandle)`. Self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` to add a new incoming call.

The incoming conference you are adding is assumed to have a video state of `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, unless the extra value `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_INCOMING_VIDEO_STATE:kotlin.String` is specified.

Once invoked, this method will cause the system to bind to the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` associated with the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` and request additional information about the call (See `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`) before starting the incoming call UI.

For a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if either the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` does not correspond to a registered `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` or the associated `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` is not currently enabled by the user.

| Parameters ||
|---|---|
| `phoneAccount` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle): A `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` registered with `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)`. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): A bundle that will be passed through to `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#onCreateIncomingConference(android.telecom.PhoneAccountHandle,%20android.telecom.ConnectionRequest)`. This value cannot be `null`. |

### cancelMissedCallsNotification

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelMissedCallsNotification(): Unit
```

Removes the missed-call notification if one is present and marks missed calls in the call log as read.

Requires that the method-caller be set as the default dialer app.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

### createManageBlockedNumbersIntent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createManageBlockedNumbersIntent(): Intent!
```

Creates the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which can be used with `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` to launch the activity to manage blocked numbers.

The activity will display the UI to manage blocked numbers only if `https://developer.android.com/reference/kotlin/android/provider/BlockedNumberContract.html#canCurrentUserBlockNumbers(android.content.Context)` returns `true` for the current user.

### endCall

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun endCall(): Boolean
```

**Deprecated:** *Companion apps for wearable devices should use the `https://developer.android.com/reference/kotlin/android/telecom/InCallService` API instead. Apps performing call screening should use the `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService` API instead.*

Ends the foreground call on the device.

If there is a single call and it is ringing, calling this method rejects the ringing call. Otherwise, the foreground (active) call is ended preferentially.

Note: this method CANNOT be used to end ongoing emergency calls and will return `false` if an attempt is made to end an emergency call.

Note: If the foreground call on this device is self-managed or transactional, this method will only end the call if the caller of this method is privileged (i.e. system, shell, or root) or system UI. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ANSWER_PHONE_CALLS:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is a call which will be rejected or terminated, `false` otherwise. |

### getAdnUriForPhoneAccount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdnUriForPhoneAccount(accountHandle: PhoneAccountHandle!): Uri!
```

Returns a URI (with the content:// scheme) specific to the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for ADN content retrieval. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The handle for the account to derive an adn query URI for or `null` to return a URI which will use the default account. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The URI (with the content:// scheme) specific to the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for the the content retrieve. |

### getCallCapablePhoneAccounts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallCapablePhoneAccounts(): MutableList<PhoneAccountHandle!>!
```

Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s which can be used to make and receive phone calls. The returned list includes only those accounts which have been explicitly enabled by the user.

For callers only interested in finding all SIMs for voice calls, it is recommended to use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#getActiveSubscriptionInfoList()` instead. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!>!` | A list of `PhoneAccountHandle` objects. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String`

### getDefaultDialerPackage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultDialerPackage(): String!
```

Used to determine the currently selected default dialer package.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | package name for the default dialer package or null if no package has been selected as the default dialer. |

### getDefaultOutgoingPhoneAccount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultOutgoingPhoneAccount(uriScheme: String!): PhoneAccountHandle!
```

Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which will be used to place outgoing calls to addresses with the specified `uriScheme`. This `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` will always be a member of the list which is returned from invoking `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getCallCapablePhoneAccounts()`. The specific account returned depends on the following priorities:

- If the user-selected default `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` supports the specified scheme, it will be returned.
- If there exists only one `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` that supports the specified scheme, it will be returned.

<br />

If no `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` fits the criteria above, this method will return `null`.

For callers only interested in finding the default SIM for voice calls, it is recommended to use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#getDefaultVoiceSubscriptionId()` instead. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `uriScheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The URI scheme. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!` | The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` corresponding to the account to be used. |

### getLine1Number

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLine1Number(accountHandle: PhoneAccountHandle!): String!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#getPhoneNumber(kotlin.Int)` instead, which takes a Telephony Subscription ID that can be retrieved with the `accountHandle` from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSubscriptionId(android.telecom.PhoneAccountHandle)`.*

Return the line 1 phone number for given phone account.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SMS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String`, or that the caller is the default SMS app for any API level. `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` for apps targeting SDK API level 29 and below.

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The handle for the account retrieve a number for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string representation of the line 1 phone number. |

### getOwnSelfManagedPhoneAccounts

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOwnSelfManagedPhoneAccounts(): MutableList<PhoneAccountHandle!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s owned by the calling self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`.

Self-Managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s have a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.

Requires permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`

A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if a caller lacks the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String` permission. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!>` | A list of `PhoneAccountHandle` objects. This value cannot be `null`. |

### getPhoneAccount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneAccount(account: PhoneAccountHandle!): PhoneAccount!
```

Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for a specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. Object includes resources which can be used in a user interface. Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String` for applications targeting API level 31+.

| Parameters ||
|---|---|
| `account` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount!` | The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` object. |

### getRegisteredPhoneAccounts

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegisteredPhoneAccounts(): MutableList<PhoneAccount!>
```

This API will return all `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s the caller registered via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)`. If a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` appears to be missing from the list, Telecom has either unregistered the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` (for cleanup purposes) or the caller registered the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` under a different user and does not have the android.Manifest.permission#INTERACT_ACROSS_USERS permission. **Note:** This API will only return `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s registered by the same app. For system Dialers that need all the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s registered by every application, see #getAllPhoneAccounts().

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount!>` | all the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s registered by the caller. This value cannot be `null`. |

### getSelfManagedPhoneAccounts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSelfManagedPhoneAccounts(): MutableList<PhoneAccountHandle!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`s for all self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s owned by the calling `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#`.

Self-Managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s have a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.

Requires permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, or that the caller is the default dialer app.

A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if a called is not the default dialer, or lacks the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permission. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!>` | A list of `PhoneAccountHandle` objects. This value cannot be `null`. |

### getSimCallManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimCallManager(): PhoneAccountHandle!
```

Returns the current SIM call manager. Apps must be prepared for this method to return `null`, indicating that there currently exists no SIM call manager `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for the default voice subscription.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!` | The phone account handle of the current sim call manager for the default voice subscription. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#getDefaultVoiceSubscriptionId()`

### getSimCallManagerForSubscription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimCallManagerForSubscription(subscriptionId: Int): PhoneAccountHandle?
```

Returns current SIM call manager for the Telephony Subscription ID specified. Apps must be prepared for this method to return `null`, indicating that there currently exists no SIM call manager `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for the subscription specified.

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Telephony Subscription ID that the SIM call manager should be queried for. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle?` | The phone account handle of the current sim call manager. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#getActiveSubscriptionInfoList()`

### getSystemDialerPackage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemDialerPackage(): String?
```

Determines the package name of the system-provided default phone app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | package name for the system dialer package or `null` if no system dialer is preloaded. |

### getUserSelectedOutgoingPhoneAccount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserSelectedOutgoingPhoneAccount(): PhoneAccountHandle?
```

Return the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which is the user-chosen default for making outgoing phone calls. This `PhoneAccount` will always be a member of the list which is returned from calling `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getCallCapablePhoneAccounts()`

Apps must be prepared for this method to return `null`, indicating that there currently exists no user-chosen default `PhoneAccount`.

The default dialer has access to use this method. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle?` | The user outgoing phone account selected by the user, or `null` if there is no user selected outgoing `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. |

### getVoiceMailNumber

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVoiceMailNumber(accountHandle: PhoneAccountHandle!): String!
```

Return the voicemail number for a given phone account. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The handle for the phone account. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The voicemail number for the phone account, and `null` if one has not been configured. |

### handleMmi

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun handleMmi(dialString: String!): Boolean
```

Processes the specified dial string as an MMI code. MMI codes are any sequence of characters entered into the dialpad that contain a "\*" or "#". Some of these sequences launch special behavior through handled by Telephony. This method uses the default subscription.

Requires that the method-caller be set as the system dialer app.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

| Parameters ||
|---|---|
| `dialString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The digits to dial. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the digits were processed as an MMI code, false otherwise. |

### handleMmi

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun handleMmi(
    dialString: String!, 
    accountHandle: PhoneAccountHandle!
): Boolean
```

Processes the specified dial string as an MMI code. MMI codes are any sequence of characters entered into the dialpad that contain a "\*" or "#". Some of these sequences launch special behavior through handled by Telephony.

Requires that the method-caller be set as the system dialer app.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

| Parameters ||
|---|---|
| `dialString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The digits to dial. |
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The handle for the account the MMI code should apply to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the digits were processed as an MMI code, false otherwise. |

### hasManageOngoingCallsPermission

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasManageOngoingCallsPermission(): Boolean
```

Returns whether the caller has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_ONGOING_CALLS:kotlin.String` permission. The permission can be obtained by associating with a physical wearable device via the `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` API as a companion app. If the caller app has the permission, it has `https://developer.android.com/reference/kotlin/android/telecom/InCallService` access to manage ongoing calls.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the caller has `https://developer.android.com/reference/kotlin/android/telecom/InCallService` access for companion app; `false` otherwise. |

### isInCall

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInCall(): Boolean
```

Returns whether there is an ongoing phone call (can be in dialing, ringing, active or holding states) originating from either a manager or self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is an ongoing call in either a managed or self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, `false` otherwise. |

### isInExternalCall

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInExternalCall(): Boolean
```

Returns whether there is an ongoing phone call (can be in dialing, ringing, active or holding states) that is an external call.

External calls take place on another dveice. They do not retain audio focus or result in call audio routing operations. For example, a wearable device may provide a UI for a call which takes place on the user's phone for the purpose of controlling the call or potentially pulling it to the wearable; such a call is external.

Calls with `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` are external. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is an ongoing call that is external, `false` otherwise. |

### isInManagedCall

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInManagedCall(): Boolean
```

Returns whether there is an ongoing call originating from a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. An ongoing call can be in dialing, ringing, active or holding states.

If you also need to know if there are ongoing self-managed calls, use `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#isInCall()` instead. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is an ongoing call in a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`, `false` otherwise. |

### isIncomingCallPermitted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isIncomingCallPermitted(phoneAccountHandle: PhoneAccountHandle!): Boolean
```

Determines whether Telecom would permit an incoming call to be added via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addNewIncomingCall(android.telecom.PhoneAccountHandle,%20android.os.Bundle)` API for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`.

A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` may not add a call for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` in the following situations:

- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` does not have property `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` set (i.e. it is a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`), and the active or held call limit has been reached.
- There is an ongoing emergency call.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` the call will be added for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if telecom will permit an incoming call to be added, `false` otherwise. |

### isOutgoingCallPermitted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOutgoingCallPermitted(phoneAccountHandle: PhoneAccountHandle!): Boolean
```

Determines whether Telecom would permit an outgoing call to be placed via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)` API for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`.

A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` may not place a call for the specified `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` in the following situations:

- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` does not have property `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` set (i.e. it is a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`), and the active, held or ringing call limit has been reached.
- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` has property `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` set (i.e. it is a self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` and there is an ongoing call in another `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`.
- There is an ongoing emergency call.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` the call will be added for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if telecom will permit an outgoing call to be placed, `false` otherwise. |

### isTtySupported

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTtySupported(): Boolean
```

Returns whether TTY is supported on this device. 
Requires android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

### isVoiceMailNumber

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVoiceMailNumber(
    accountHandle: PhoneAccountHandle!, 
    number: String!
): Boolean
```

Return whether a given phone number is the configured voicemail number for a particular phone account. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The handle for the account to check the voicemail number against |
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The number to look up. |

### placeCall

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun placeCall(
    address: Uri!, 
    extras: Bundle!
): Unit
```

Places a new outgoing call to the provided address using the system telecom service with the specified extras. This method is equivalent to placing an outgoing call using `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String`, except that the outgoing call will always be sent via the system telecom service. If method-caller is either the user selected default dialer app or preloaded system dialer app, then emergency calls will also be allowed. Placing a call via a managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` requires permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String` Usage example:

```kotlin
Uri uri = Uri.fromParts("tel", "12345", null);
  Bundle extras = new Bundle();
  extras.putBoolean(TelecomManager.EXTRA_START_CALL_WITH_SPEAKERPHONE, true);
  telecomManager.placeCall(uri, extras);
  
```
The following keys are supported in the supplied extras.

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_OUTGOING_CALL_EXTRAS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_SPEAKERPHONE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_VIDEO_STATE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_TYPE:kotlin.String`

<br />

An app which implements the self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` API uses `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#placeCall(android.net.Uri,%20android.os.Bundle)` to inform Telecom of a new outgoing call. A self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` must include `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` to specify its associated `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle`. Self-managed `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`s require permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`.

**Note:** If this method is used to place an emergency call, it is not guaranteed that the call will be placed on the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` provided in the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` extra (if specified) and may be placed on another `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` with the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_PLACE_EMERGENCY_CALLS:kotlin.Int` capability, depending on external factors, such as network conditions and Modem/SIM status.

**Note** : `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle.html#` notifications should be posted after the call is placed in order for the notification to be non-dismissible.

**Note**: Call Forwarding MMI codes can only be dialed by applications that are configured as the user defined default dialer or system dialer role. If a call containing a call forwarding MMI code is placed by an application that is not in one of these roles, the dialer will be launched with a UI showing the MMI code already populated so that the user can confirm the action before the call is placed.

**Note** : The dialer application may set the URI parameter of address to specify a call log record. This allows the dialer to launch a related application to initiate a callback for a specific call log entry. The dialer must have the READ_CALL_LOGS permission to access call log records. The ContentUri for a specific call log record can be obtained by android.content.ContentUri#withAppendedId(CallLog.Calls.CONTENT_URI,callLogId), where callLogId is the `https://developer.android.com/reference/kotlin/android/provider/BaseColumns.html#_ID:kotlin.String` of the call log record. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_OWN_CALLS:kotlin.String`

| Parameters ||
|---|---|
| `address` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The address to make the call to. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Bundle of extras to use with the call. |

### registerPhoneAccount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerPhoneAccount(account: PhoneAccount!): Unit
```

Register a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` for use by the system that will be stored in Device Encrypted storage. When registering `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`s, existing registrations will be overwritten if the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` matches that of a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` which is already registered. Once registered, the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` is listed to the user as an option when placing calls. The user may still need to enable the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` within the phone app settings before the account is usable.

Note: Each package is limited to 10 `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` registrations.

A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if an app tries to register a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` where the package name specified within `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getComponentName()` does not match the package name of the app.

A `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if an app tries to register a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` when the upper bound limit, 10, has already been reached.

| Parameters ||
|---|---|
| `account` | [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount)!: The complete `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if: 1. the caller cannot modify phone state and the phone account doesn't belong to the calling user. 2. the caller is registering a self-managed phone and either they are not allowed to manage their own calls or if the account is call capable, a connection manager, or a sim account. 3. the caller is registering a sim account without the ability to do so. 4. the caller is registering a multi-user phone account but isn't a system app. 5. the account can make SIM-based voice calls but the caller cannot register sim accounts or isn't a sim call manager. 6. the account defines the EXTRA_SKIP_CALL_FILTERING extra but the caller isn't able to modify the phone state. 7. the caller is registering an account for a different user but isn't able to interact across users. 8. if simultaneous calling is available and the phone account package name doesn't correspond to the simultaneous calling accounts associated with this phone account. |
| `java.lang.UnsupportedOperationException` | if the caller cannot modify phone state and the device does not have the Telecom feature. |

### showInCallScreen

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showInCallScreen(showDialpad: Boolean): Unit
```

Brings the in-call screen to the foreground if there is an ongoing call. If there is currently no ongoing call, then this method does nothing.

Requires that the method-caller be set as the system dialer app or have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permission.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `showDialpad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Brings up the in-call dialpad as part of showing the in-call screen. |

### silenceRinger

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun silenceRinger(): Unit
```

Silences the ringer if a ringing call exists.

This method can only be relied upon to stop the ringtone for a call if the ringtone has already started playing. It is intended to handle use-cases such as silencing a ringing call when the user presses the volume button during ringing.

If this method is called prior to when the ringtone begins playing, the ringtone will not be silenced. As such it is not intended as a means to avoid playing of a ringtone.

A dialer app which wants to have more control over ringtone playing should declare `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_IN_CALL_SERVICE_RINGING:kotlin.String` in the manifest entry for their `https://developer.android.com/reference/kotlin/android/telecom/InCallService` implementation to indicate that the app wants to be responsible for playing the ringtone for all incoming calls.

Requires permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the app fills the dialer role (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

### startConference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startConference(
    participants: MutableList<Uri!>, 
    extras: Bundle
): Unit
```

Place a new adhoc conference call with the provided participants using the system telecom service. This method doesn't support placing of emergency calls. An adhoc conference call is established by providing a list of addresses to `TelecomManager#startConference(List<Uri>, int videoState)` where the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` is responsible for connecting all indicated participants to a conference simultaneously. This is in contrast to conferences formed by merging calls together (e.g. using `https://developer.android.com/reference/kotlin/android/telecom/Call#mergeConference()`). The following keys are supported in the supplied extras.

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_SPEAKERPHONE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_START_CALL_WITH_VIDEO_STATE:kotlin.String`

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String`

<br />

| Parameters ||
|---|---|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: List of participants to start conference with. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): Bundle of extras to use with the call. This value cannot be `null`. |

### unregisterPhoneAccount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterPhoneAccount(accountHandle: PhoneAccountHandle!): Unit
```

Remove a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` registration from the system.

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: A `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle` for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` to unregister. |
