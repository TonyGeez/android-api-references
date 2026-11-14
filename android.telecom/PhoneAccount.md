Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneAccount

```
class PhoneAccount : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.PhoneAccount](PhoneAccount.md) |

Represents a distinct method to place or receive a phone call. Apps which can place calls and want those calls to be integrated into the dialer and in-call UI should build an instance of this class and register it with the system using TelecomManager.

TelecomManager uses registered PhoneAccounts to present the user with alternative options when placing a phone call. When building a PhoneAccount, the app should supply a valid PhoneAccountHandle that references the connection service implementation Telecom will use to interact with the app.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.Builder` Helper class for creating a PhoneAccount. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_ADHOC_CONFERENCE_CALLING:kotlin.Int` An adhoc conference call is established by providing a list of addresses to `TelecomManager#startConference(List<Uri>, int videoState)` where the ConnectionService is responsible for connecting all indicated participants to a conference simultaneously. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_COMPOSER:kotlin.Int` Flag indicating whether this PhoneAccount is capable of supporting the call composer functionality for enriched calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_PROVIDER:kotlin.Int` Flag indicating that this `PhoneAccount` can make phone calls in place of traditional SIM-based telephony calls. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_SUBJECT:kotlin.Int` Flag indicating that this `PhoneAccount` supports a subject for Calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CHANGE_RTT_CALL_TO_AUDIO_CALL:kotlin.Int` Flag indicating that this PhoneAccount is capable of changing an RTT (Real-time text) call to a voice call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` Flag indicating that this `PhoneAccount` can act as a connection manager for other connections. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_OPT_OUT_OF_PREMIUM_NETWORK:kotlin.Int` Flag indicating that this PhoneAccount should be opted out of automatic requests for premium network capabilities. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_PLACE_EMERGENCY_CALLS:kotlin.Int` Flag indicating that this `PhoneAccount` is capable of placing emergency calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_RTT:kotlin.Int` Flag indicating that this PhoneAccount is capable of making a call with an RTT (Real-time text) session. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int` Flag indicating that this PhoneAccount is responsible for managing its own Connections. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SIM_SUBSCRIPTION:kotlin.Int` Flag indicating that this `PhoneAccount` represents a built-in PSTN SIM subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_CALL_STREAMING:kotlin.Int` Flag indicating that this voip app PhoneAccount supports the call streaming session to stream call audio to another remote device via streaming app. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_TRANSACTIONAL_OPERATIONS:kotlin.Int` Flag indicating that this PhoneAccount supports the transactional addCall API for adding calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VIDEO_CALLING:kotlin.Int` Flag indicating that this PhoneAccount supports video calling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS:kotlin.Int` Flag indicating that this PhoneAccount provides SIM-based voice calls, potentially as an over-the-top solution such as wi-fi calling. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int` Flag indicating that this `PhoneAccount` is currently able to place video calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING_RELIES_ON_PRESENCE:kotlin.Int` Flag indicating that for this `PhoneAccount`, the ability to make a video call to a number relies on presence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VOICE_CALLING_AVAILABLE:kotlin.Int` Flag indicating that this PhoneAccount is *currently* able to place SIM-based voice calls, similar to `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_ADD_SELF_MANAGED_CALLS_TO_INCALLSERVICE:kotlin.String` Boolean PhoneAccount extras key (see getExtras) which indicates whether a Self-managed PhoneAccount want to expose its calls to all InCallService which declares the metadata `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_ALWAYS_USE_VOIP_AUDIO_MODE:kotlin.String` Boolean PhoneAccount extras key (see getExtras) which indicates that all calls from this PhoneAccount should be treated as VoIP calls rather than cellular calls by the Telecom audio handling logic. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_CALL_SUBJECT_CHARACTER_ENCODING:kotlin.String` PhoneAccount extras key (see getExtras) which determines the character encoding to be used when determining the length of messages. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_CALL_SUBJECT_MAX_LENGTH:kotlin.String` PhoneAccount extras key (see getExtras) which determines the maximum permitted length of a call subject specified via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_SUBJECT:kotlin.String` extra on an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_LOG_SELF_MANAGED_CALLS:kotlin.String` Boolean PhoneAccount extras key (see getExtras) which indicates whether a Self-Managed PhoneAccount should log its calls to the call log. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_FROM:kotlin.String` Boolean PhoneAccount extras key (see getExtras) which indicates whether this PhoneAccount is capable of supporting a request to handover a connection from this PhoneAccount to another PhoneAccount. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_TO:kotlin.String` Boolean PhoneAccount extras key (see getExtras) which indicates whether this PhoneAccount is capable of supporting a request to handover a connection (see `android.telecom.Call#handoverTo()`) to this PhoneAccount from a PhoneAccount specifying `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_FROM:kotlin.String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#LOW_BATTERY_ALERT_DISABLED:kotlin.Int` Default value indicating that the low battery alert feature is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#NO_HIGHLIGHT_COLOR:kotlin.Int` Indicating no hightlight color is set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#NO_RESOURCE_ID:kotlin.Int` Indicating no resource ID is set. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_SIP:kotlin.String` URI scheme for SIP URIs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_TEL:kotlin.String` URI scheme for telephone number URIs. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_VOICEMAIL:kotlin.String` URI scheme for voicemail URIs. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| static [PhoneAccount.Builder](../android/telecom/PhoneAccount.Builder.md)! | builder <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [PhoneAccountHandle](PhoneAccountHandle.md)! | getAccountHandle The unique identifier of this `PhoneAccount`. |
| [Uri](../android.net/Uri.md)! | getAddress The address (e.g., a phone number) associated with this |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCapabilities The capabilities of this `PhoneAccount`. |
| --- | --- |
| [Bundle](../android.os/Bundle.md)! | getExtras The extras associated with this `PhoneAccount`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHighlightColor A highlight color to use in displaying information about this `PhoneAccount`. |
| [Icon](../android.graphics.drawable/Icon.md)! | getIcon The icon to represent this `PhoneAccount`. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getLabel A short label describing a `PhoneAccount`. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getShortDescription A short paragraph describing this `PhoneAccount`. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PhoneAccountHandle](PhoneAccountHandle.md)!\> | getSimultaneousCallingRestriction If a restriction is set (see hasSimultaneousCallingRestriction), this method returns the Set of PhoneAccountHandles that are allowed to support calls simultaneously with this PhoneAccount. |
| --- | --- |
| [Uri](../android.net/Uri.md)! | getSubscriptionAddress The raw callback number used for this `PhoneAccount`, as distinct from getAddress. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getSupportedUriSchemes The URI schemes supported by this `PhoneAccount`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasCapabilities Determines if this `PhoneAccount` has a capabilities specified by the passed in bit mask. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSimultaneousCallingRestriction Whether or not this PhoneAccount contains a simultaneous calling restriction on it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEnabled Indicates whether the user has enabled this `PhoneAccount` or not. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | supportsUriScheme Determines if the PhoneAccount supports calls to/from addresses with a specified URI scheme. |
| [PhoneAccount.Builder](../android/telecom/PhoneAccount.Builder.md)! | toBuilder Returns a builder initialized with the current PhoneAccount instance. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PhoneAccount](PhoneAccount.md)!\> | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CAPABILITY_ADHOC_CONFERENCE_CALLING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_ADHOC_CONFERENCE_CALLING: Int
```

An adhoc conference call is established by providing a list of addresses to `TelecomManager#startConference(List<Uri>, int videoState)` where the ConnectionService is responsible for connecting all indicated participants to a conference simultaneously. This is in contrast to conferences formed by merging calls together (e.g. using mergeConference).

 Value: 16384

### CAPABILITY_CALL_COMPOSER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CALL_COMPOSER: Int
```

Flag indicating whether this PhoneAccount is capable of supporting the call composer functionality for enriched calls.

 Value: 32768

### CAPABILITY_CALL_PROVIDER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CALL_PROVIDER: Int
```

Flag indicating that this `PhoneAccount` can make phone calls in place of traditional SIM-based telephony calls. This account will be treated as a distinct method for placing calls alongside the traditional SIM-based telephony stack. This flag is distinct from `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` in that it is not allowed to manage or place calls from the built-in telephony stack.

See getCapabilities

<br />

 Value: 2

### CAPABILITY_CALL_SUBJECT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CALL_SUBJECT: Int
```

Flag indicating that this `PhoneAccount` supports a subject for Calls. This means a caller is able to specify a short subject line for an outgoing call. A capable receiving device displays the call subject on the incoming call screen.

See getCapabilities

 Value: 64

### CAPABILITY_CHANGE_RTT_CALL_TO_AUDIO_CALL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CHANGE_RTT_CALL_TO_AUDIO_CALL: Int
```

Flag indicating that this PhoneAccount is capable of changing an RTT (Real-time text) call to a voice call.

When set, the in-call app will display the "change to voice" option.

Only applicable for a phone account with `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_RTT:kotlin.Int`.

 Value: 1048576

### CAPABILITY_CONNECTION_MANAGER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CONNECTION_MANAGER: Int
```

Flag indicating that this `PhoneAccount` can act as a connection manager for other connections. The ConnectionService associated with this `PhoneAccount` will be allowed to manage phone calls including using its own proprietary phone-call implementation (like VoIP calling) to make calls instead of the telephony stack.

When a user opts to place a call using the SIM-based telephony stack, the ConnectionService associated with this `PhoneAccount` will be attempted first if the user has explicitly selected it to be used as the default connection manager.

See getCapabilities

 Value: 1

### CAPABILITY_OPT_OUT_OF_PREMIUM_NETWORK

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_OPT_OUT_OF_PREMIUM_NETWORK: Int
```

Flag indicating that this PhoneAccount should be opted out of automatic requests for premium network capabilities.

By default, the system may automatically request a premium network slice (such as a slice for unified communications) on behalf of an application with android.telecom.Call#PROPERTY_IS_TRANSACTIONAL, when a call is being established. Setting this capability would allow an application to opt-out of this behaviour and manage its own network requests, giving it more granular control over its networking.

This is intended for applications with sophisticated, custom network management logic that prefer to handle their own network requests rather than relying on the system's automatic behavior.

 Value: 2097152

**See Also**

- getCapabilities

### CAPABILITY_PLACE_EMERGENCY_CALLS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_PLACE_EMERGENCY_CALLS: Int
```

Flag indicating that this `PhoneAccount` is capable of placing emergency calls. By default all PSTN `PhoneAccount`s are capable of placing emergency calls.

See getCapabilities

 Value: 16

### CAPABILITY_RTT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_RTT: Int
```

Flag indicating that this PhoneAccount is capable of making a call with an RTT (Real-time text) session. When set, Telecom will attempt to open an RTT session on outgoing calls that specify that they should be placed with an RTT session , and the in-call app will be displayed with text entry fields for RTT. Likewise, the in-call app can request that an RTT session be opened during a call if this bit is set.

 Value: 4096

### CAPABILITY_SELF_MANAGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SELF_MANAGED: Int
```

**Deprecated:** *VoIP applications that want to integrate with the Telecom framework should transition to the new Telecom VoIP APIs which are wrapped by the*

Flag indicating that this PhoneAccount is responsible for managing its own Connections. This type of PhoneAccount is ideal for use with standalone calling apps which do not wish to use the default phone app for Connection UX, but which want to leverage the call and audio routing capabilities of the Telecom framework.

When set, Connections created by the self-managed ConnectionService will not be surfaced to implementations of the InCallService API. Thus it is the responsibility of a self-managed ConnectionService to provide a user interface for its Connections.

Self-managed Connections will, however, be displayed on connected Bluetooth devices.

 Value: 2048

### CAPABILITY_SIM_SUBSCRIPTION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SIM_SUBSCRIPTION: Int
```

Flag indicating that this `PhoneAccount` represents a built-in PSTN SIM subscription.

Only the Android framework can register a `PhoneAccount` having this capability.

See getCapabilities

 Value: 4

### CAPABILITY_SUPPORTS_CALL_STREAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_CALL_STREAMING: Int
```

Flag indicating that this voip app PhoneAccount supports the call streaming session to stream call audio to another remote device via streaming app.

 Value: 524288

**See Also**

- getCapabilities

### CAPABILITY_SUPPORTS_TRANSACTIONAL_OPERATIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_TRANSACTIONAL_OPERATIONS: Int
```

Flag indicating that this PhoneAccount supports the transactional addCall API for adding calls.

An app that declares this capability is indicating its support for a newer, more flexible call registration mechanism. When this capability is set on a PhoneAccount, the Telecom framework will amend its capabilities to include `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`. This allows the app to manage its own call UI and lifecycle, while still integrating with the Android system for audio routing and call management.

This capability should **only** be added if your application is using the addCall method to report new incoming and outgoing calls. If your app uses the legacy methods addNewIncomingCall or placeCall, this capability **must not** be used.

 Value: 262144

**See Also**

- addCall
- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`
- getCapabilities

### CAPABILITY_SUPPORTS_VIDEO_CALLING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VIDEO_CALLING: Int
```

Flag indicating that this PhoneAccount supports video calling. This is not an indication that the PhoneAccount is currently able to make a video call, but rather that it has the ability to make video calls (but not necessarily at this time).

Whether a PhoneAccount can make a video call is ultimately controlled by `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int`, which indicates whether the PhoneAccount is currently capable of making a video call. Consider a case where, for example, a PhoneAccount supports making video calls (e.g. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VIDEO_CALLING:kotlin.Int`), but a current lack of network connectivity prevents video calls from being made (e.g. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int`).

See getCapabilities

 Value: 1024

### CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS: Int
```

Flag indicating that this PhoneAccount provides SIM-based voice calls, potentially as an over-the-top solution such as wi-fi calling.

Similar to `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VIDEO_CALLING:kotlin.Int`, this capability indicates this PhoneAccount has the ability to make voice calls (but not necessarily at this time). Whether this PhoneAccount can make a voice call is ultimately controlled by `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VOICE_CALLING_AVAILABLE:kotlin.Int`, which indicates whether this PhoneAccount is currently capable of making a voice call. Consider a case where, for example, a PhoneAccount supports making voice calls (e.g. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS:kotlin.Int`), but a current lack of network connectivity prevents voice calls from being made (e.g. `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VOICE_CALLING_AVAILABLE:kotlin.Int`).

In order to declare this capability, this PhoneAccount must also declare `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SIM_SUBSCRIPTION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` and satisfy the associated requirements.

 Value: 65536

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VOICE_CALLING_AVAILABLE:kotlin.Int`
- getCapabilities

### CAPABILITY_VIDEO_CALLING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_VIDEO_CALLING: Int
```

Flag indicating that this `PhoneAccount` is currently able to place video calls.

See also `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VIDEO_CALLING:kotlin.Int` which indicates whether the `PhoneAccount` supports placing video calls.

See getCapabilities

 Value: 8

### CAPABILITY_VIDEO_CALLING_RELIES_ON_PRESENCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_VIDEO_CALLING_RELIES_ON_PRESENCE: Int
```

Flag indicating that for this `PhoneAccount`, the ability to make a video call to a number relies on presence. Should only be set if the `PhoneAccount` also has `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int`.

Note: As of Android 12, using the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns.html#CARRIER_PRESENCE_VT_CAPABLE:kotlin.Int` bit on the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns.html#CARRIER_PRESENCE:kotlin.String` column to indicate whether a contact's phone number supports video calling has been deprecated and should only be used on devices where `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_USE_RCS_PRESENCE_BOOL:kotlin.String` is set. On newer devices, applications must use `https://developer.android.com/reference/kotlin/android/telephony/ims/RcsUceAdapter.html#` instead to determine whether or not a contact's phone number supports carrier video calling.

See getCapabilities

 Value: 256

### CAPABILITY_VOICE_CALLING_AVAILABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_VOICE_CALLING_AVAILABLE: Int
```

Flag indicating that this PhoneAccount is *currently* able to place SIM-based voice calls, similar to `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_VIDEO_CALLING:kotlin.Int`.

See also `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS:kotlin.Int`, which indicates whether the `PhoneAccount` supports placing SIM-based voice calls or not.

In order to declare this capability, this PhoneAccount must also declare `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SIM_SUBSCRIPTION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int` and satisfy the associated requirements.

 Value: 131072

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SUPPORTS_VOICE_CALLING_INDICATIONS:kotlin.Int`
- getCapabilities

### EXTRA_ADD_SELF_MANAGED_CALLS_TO_INCALLSERVICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ADD_SELF_MANAGED_CALLS_TO_INCALLSERVICE: String
```

Boolean PhoneAccount extras key (see getExtras) which indicates whether a Self-managed PhoneAccount want to expose its calls to all InCallService which declares the metadata `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String`.

 Value: "android.telecom.extra.ADD_SELF_MANAGED_CALLS_TO_INCALLSERVICE"

### EXTRA_ALWAYS_USE_VOIP_AUDIO_MODE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ALWAYS_USE_VOIP_AUDIO_MODE: String
```

Boolean PhoneAccount extras key (see getExtras) which indicates that all calls from this PhoneAccount should be treated as VoIP calls rather than cellular calls by the Telecom audio handling logic.

 Value: "android.telecom.extra.ALWAYS_USE_VOIP_AUDIO_MODE"

### EXTRA_CALL_SUBJECT_CHARACTER_ENCODING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_SUBJECT_CHARACTER_ENCODING: String
```

PhoneAccount extras key (see getExtras) which determines the character encoding to be used when determining the length of messages. The user interface can use this when determining the number of characters the user may type in a call subject. If empty-string, the call subject message size limit will be enforced on a 1:1 basis. That is, each character will count towards the messages size limit as a single character. If a character encoding is specified, the message size limit will be based on the number of bytes in the message per the specified encoding. See `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_CALL_SUBJECT_MAX_LENGTH:kotlin.String` for more information on the call subject maximum length.

 Value: "android.telecom.extra.CALL_SUBJECT_CHARACTER_ENCODING"

### EXTRA_CALL_SUBJECT_MAX_LENGTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_SUBJECT_MAX_LENGTH: String
```

PhoneAccount extras key (see getExtras) which determines the maximum permitted length of a call subject specified via the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_CALL_SUBJECT:kotlin.String` extra on an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String` intent. Ultimately a ConnectionService is responsible for enforcing the maximum call subject length when sending the message, however this extra is provided so that the user interface can proactively limit the length of the call subject as the user types it.

 Value: "android.telecom.extra.CALL_SUBJECT_MAX_LENGTH"

### EXTRA_LOG_SELF_MANAGED_CALLS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LOG_SELF_MANAGED_CALLS: String
```

**Deprecated:** *Register `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#ACTION_CALL_BACK:kotlin.String` instead.*

Boolean PhoneAccount extras key (see getExtras) which indicates whether a Self-Managed PhoneAccount should log its calls to the call log. Self-Managed PhoneAccounts are responsible for their own notifications, so the system will not create a notification when a missed call is logged.

By default, Self-Managed PhoneAccounts do not log their calls to the call log. Setting this extra to `true` provides a means for them to log their calls.

Note: Only calls where the getHandle getScheme is `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_SIP:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#SCHEME_TEL:kotlin.String` will be logged at the current time.

 Value: "android.telecom.extra.LOG_SELF_MANAGED_CALLS"

### EXTRA_SUPPORTS_HANDOVER_FROM

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUPPORTS_HANDOVER_FROM: String
```

Boolean PhoneAccount extras key (see getExtras) which indicates whether this PhoneAccount is capable of supporting a request to handover a connection from this PhoneAccount to another PhoneAccount. (see `android.telecom.Call#handoverTo()`) which specifies `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_TO:kotlin.String`.

A handover request is initiated by the user from the default dialer app to indicate a desire to handover a call from one PhoneAccount/ConnectionService to another.

 Value: "android.telecom.extra.SUPPORTS_HANDOVER_FROM"

### EXTRA_SUPPORTS_HANDOVER_TO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUPPORTS_HANDOVER_TO: String
```

Boolean PhoneAccount extras key (see getExtras) which indicates whether this PhoneAccount is capable of supporting a request to handover a connection (see `android.telecom.Call#handoverTo()`) to this PhoneAccount from a PhoneAccount specifying `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#EXTRA_SUPPORTS_HANDOVER_FROM:kotlin.String`.

A handover request is initiated by the user from the default dialer app to indicate a desire to handover a call from one PhoneAccount/ConnectionService to another.

 Value: "android.telecom.extra.SUPPORTS_HANDOVER_TO"

### LOW_BATTERY_ALERT_DISABLED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOW_BATTERY_ALERT_DISABLED: Int
```

Default value indicating that the low battery alert feature is disabled.

 Value: -1

### NO_HIGHLIGHT_COLOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_HIGHLIGHT_COLOR: Int
```

Indicating no hightlight color is set.

 Value: 0

### NO_RESOURCE_ID

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_RESOURCE_ID: Int
```

Indicating no resource ID is set.

 Value: -1

### SCHEME_SIP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEME_SIP: String
```

URI scheme for SIP URIs.

 Value: "sip"

### SCHEME_TEL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEME_TEL: String
```

URI scheme for telephone number URIs.

 Value: "tel"

### SCHEME_VOICEMAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEME_VOICEMAIL: String
```

URI scheme for voicemail URIs.

 Value: "voicemail"

## Public methods

### builder

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun builder(
    accountHandle: PhoneAccountHandle!, 
    label: CharSequence!
): PhoneAccount.Builder!
```

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAccountHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccountHandle(): PhoneAccountHandle!
```

The unique identifier of this `PhoneAccount`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!` | A `PhoneAccountHandle`. |

### getAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): Uri!
```

The address (e.g., a phone number) associated with this `PhoneAccount`. This represents the destination from which outgoing calls using this `PhoneAccount` will appear to come, if applicable, and the destination to which incoming calls using this `PhoneAccount` may be addressed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | A address expressed as a `Uri`, for example, a phone number. |

### getCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCapabilities(): Int
```

The capabilities of this `PhoneAccount`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bit field of flags describing this `PhoneAccount`'s capabilities. |

### getExtras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle!
```

The extras associated with this `PhoneAccount`.

A ConnectionService may provide implementation specific information about the PhoneAccount via the extras.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The extras. |

### getHighlightColor

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighlightColor(): Int
```

A highlight color to use in displaying information about this `PhoneAccount`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A hexadecimal color value. |

### getIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIcon(): Icon!
```

The icon to represent this `PhoneAccount`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#!` | The icon. |

### getLabel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLabel(): CharSequence!
```

A short label describing a `PhoneAccount`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | A label for this `PhoneAccount`. |

### getShortDescription

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShortDescription(): CharSequence!
```

A short paragraph describing this `PhoneAccount`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | A description for this `PhoneAccount`. |

### getSimultaneousCallingRestriction

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSimultaneousCallingRestriction(): MutableSet<PhoneAccountHandle!>
```

If a restriction is set (see hasSimultaneousCallingRestriction), this method returns the Set of PhoneAccountHandles that are allowed to support calls simultaneously with this PhoneAccount.

If this PhoneAccount is busy with one or more ongoing calls, a restriction is set on this PhoneAccount (see hasSimultaneousCallingRestriction to check), and a new incoming or outgoing call is received or placed on a PhoneAccount that is not in this Set, Telecom will reject or cancel the pending call in favor of keeping the ongoing call alive.

Note: Simultaneous calling restrictions can only be placed on PhoneAccounts that were registered by the same application. Simultaneous calling across applications is always possible as long as the Connection supports hold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!>` | the Set of PhoneAccountHandles that this PhoneAccount supports simultaneous calls with. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If there is no restriction set on this PhoneAccount and this method is called. Whether or not there is a restriction can be checked using hasSimultaneousCallingRestriction. |

### getSubscriptionAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubscriptionAddress(): Uri!
```

The raw callback number used for this `PhoneAccount`, as distinct from getAddress. For the majority of `PhoneAccount`s this should be registered as `null`. It is used by the system for SIM-based `PhoneAccount` registration where setLine1NumberForDisplay has been used to alter the callback number.

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The subscription number, suitable for display to the user. |

### getSupportedUriSchemes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedUriSchemes(): MutableList<String!>!
```

The URI schemes supported by this `PhoneAccount`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | The URI schemes. |

### hasCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCapabilities(capability: Int): Boolean
```

Determines if this `PhoneAccount` has a capabilities specified by the passed in bit mask.

| Parameters ||
|---|---|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The capabilities to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the phone account has the capability. |

### hasSimultaneousCallingRestriction

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasSimultaneousCallingRestriction(): Boolean
```

Whether or not this PhoneAccount contains a simultaneous calling restriction on it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this PhoneAccount contains a simultaneous calling restriction, `false` if it does not. Use getSimultaneousCallingRestriction to query which other PhoneAccounts support simultaneous calling with this one. |

**See Also**

- getSimultaneousCallingRestriction

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabled(): Boolean
```

Indicates whether the user has enabled this `PhoneAccount` or not. This value is only populated for `PhoneAccount`s returned by getPhoneAccount.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the account is enabled by the user, `false` otherwise. |

### supportsUriScheme

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun supportsUriScheme(uriScheme: String!): Boolean
```

Determines if the PhoneAccount supports calls to/from addresses with a specified URI scheme.

| Parameters ||
|---|---|
| `uriScheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The URI scheme to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `PhoneAccount` supports calls to/from addresses with the specified URI scheme. |

### toBuilder

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toBuilder(): PhoneAccount.Builder!
```

Returns a builder initialized with the current PhoneAccount instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.Builder!` | The builder. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PhoneAccount!>
```
