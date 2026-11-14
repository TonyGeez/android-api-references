# SipManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipManager

Kotlin | [Java](../android/net/sip/SipManager.md) 
| --- | --- |

```
open class SipManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipManager](../android/net/sip/SipManager.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](../android/net/sip/SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Provides APIs for SIP tasks, such as initiating SIP connections, and provides access to related SIP services. This class is the starting point for any SIP actions. You can acquire an instance of it with [newInstance()](../android/net/sip/SipManager.md)).

<br />

The APIs in this class allows you to:

- Create a [SipSession](../android/net/sip/SipSession.md) to get ready for making calls or listen for incoming calls. See [createSipSession()](../android/net/sip/SipManager.md)) and [getSessionFor()](../android/net/sip/SipManager.md)).
- Initiate and receive generic SIP calls or audio-only SIP calls. Generic SIP calls may be video, audio, or other, and are initiated with #open. Audio-only SIP calls should be handled with a [SipAudioCall](../android/net/sip/SipAudioCall.md), which you can acquire with #makeAudioCall and [takeAudioCall()](../android/net/sip/SipManager.md)).
- Register and unregister with a SIP service provider, with [register()](../android/net/sip/SipManager.md)) and [unregister()](../android/net/sip/SipManager.md)).
- Verify session connectivity, with [isOpened()](../android/net/sip/SipManager.md)) and [isRegistered()](../android/net/sip/SipManager.md)).

**Note:** Not all Android-powered devices support VOIP calls using SIP. You should always call [isVoipSupported()](../android/net/sip/SipManager.md)) to verify that the device supports VOIP calling and [isApiSupported()](../android/net/sip/SipManager.md)) to verify that the device supports the SIP APIs. Your application must also request the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) and [android.Manifest.permission#USE_SIP](../android/Manifest.permission.md) permissions.
|
| ### Developer Guides
|
| For more information about using SIP, read the [Session Initiation Protocol](https://developer.android.com/guide/topics/network/sip.html) developer guide.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CALL_ID](../android/net/sip/SipManager.md) Key to retrieve the call ID from an incoming call intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_OFFER_SD](../android/net/sip/SipManager.md) Key to retrieve the offered session description from an incoming call intent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INCOMING_CALL_RESULT_CODE](../android/net/sip/SipManager.md) The result code to be sent back with the incoming call [PendingIntent](../android/app/PendingIntent.md). |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/sip/SipManager.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Closes the specified profile to not make/receive calls. |
| open [SipSession](../android/net/sip/SipSession.md)! | [createSipSession](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `listener:` ` [SipSession.Listener](../android/net/sip/SipSession.Listener.md)!`)` Creates a [SipSession](../android/net/sip/SipSession.md) with the specified profile. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCallId](../android/net/sip/SipManager.md))`(`incomingCallIntent:` ` [Intent](../android/content/Intent.md)!`)` Gets the call ID from the specified incoming call broadcast intent. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOfferSessionDescription](../android/net/sip/SipManager.md))`(`incomingCallIntent:` ` [Intent](../android/content/Intent.md)!`)` Gets the offer session description from the specified incoming call broadcast intent. |
| open [SipSession](../android/net/sip/SipSession.md)! | [getSessionFor](../android/net/sip/SipManager.md))`(`incomingCallIntent:` ` [Intent](../android/content/Intent.md)!`)` Gets the [SipSession](../android/net/sip/SipSession.md) that handles the incoming call. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isApiSupported](../android/net/sip/SipManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns true if the SIP API is supported by the system. |
| --- | --- |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIncomingCallIntent](../android/net/sip/SipManager.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` Checks if the intent is an incoming call broadcast intent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpened](../android/net/sip/SipManager.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks if the specified profile is opened in the SIP service for making and/or receiving calls. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](../android/net/sip/SipManager.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks if the SIP service has successfully registered the profile to the SIP provider (specified in the profile) for receiving calls. |
| --- | --- |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSipWifiOnly](../android/net/sip/SipManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns true if SIP is only available on WIFI. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVoipSupported](../android/net/sip/SipManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns true if the system supports SIP-based VOIP API. |
| open [SipAudioCall](../android/net/sip/SipAudioCall.md)! | [makeAudioCall](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `peerProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `listener:` ` [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to make a call. |
| --- | --- |
| open [SipAudioCall](../android/net/sip/SipAudioCall.md)! | [makeAudioCall](../android/net/sip/SipManager.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `peerProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to make an audio call. |
| open static [SipManager](../android/net/sip/SipManager.md)! | [newInstance](../android/net/sip/SipManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates a manager instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [open](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`)` Opens the profile for making generic SIP calls. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [open](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `incomingCallPendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`, `listener:` ` [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!`)` Opens the profile for making calls and/or receiving generic SIP calls. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [register](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `expiryTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `listener:` ` [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!`)` Manually registers the profile to the corresponding SIP provider for receiving calls. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRegistrationListener](../android/net/sip/SipManager.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!`)` Sets the listener to listen to registration events. |
| --- | --- |
| open [SipAudioCall](../android/net/sip/SipAudioCall.md)! | [takeAudioCall](../android/net/sip/SipManager.md))`(`incomingCallIntent:` ` [Intent](../android/content/Intent.md)!`, `listener:` ` [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!`)` Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to take an incoming call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregister](../android/net/sip/SipManager.md))`(`localProfile:` ` [SipProfile](../android/net/sip/SipProfile.md)!`, `listener:` ` [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!`)` Manually unregisters the profile from the corresponding SIP provider for stop receiving further calls. |

## Constants

### EXTRA_CALL_ID

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CALL_ID: String
```

**Deprecated:** *Deprecated in Java.*

Key to retrieve the call ID from an incoming call intent. 

 Value: "android:sipCallID"

**See Also**

- [#open(SipProfile, PendingIntent, SipRegistrationListener)](../android/net/sip/SipManager.md)) 

### EXTRA_OFFER_SD

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_OFFER_SD: String
```

**Deprecated:** *Deprecated in Java.*

Key to retrieve the offered session description from an incoming call intent. 

 Value: "android:sipOfferSD"

**See Also**

- [#open(SipProfile, PendingIntent, SipRegistrationListener)](../android/net/sip/SipManager.md)) 

### INCOMING_CALL_RESULT_CODE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCOMING_CALL_RESULT_CODE: Int
```

**Deprecated:** *Deprecated in Java.*

The result code to be sent back with the incoming call [PendingIntent](../android/app/PendingIntent.md). 

 Value: 101

**See Also**

- [#open(SipProfile, PendingIntent, SipRegistrationListener)](../android/net/sip/SipManager.md))

## Public methods

### close

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(localProfileUri: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Closes the specified profile to not make/receive calls. All the resources that were allocated to the profile are also released.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URI of the profile to close |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### createSipSession

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSipSession(
    localProfile: SipProfile!, 
    listener: SipSession.Listener!
): SipSession!
```

**Deprecated:** *Deprecated in Java.*

Creates a [SipSession](../android/net/sip/SipSession.md) with the specified profile. Use other methods, if applicable, instead of interacting with [SipSession](../android/net/sip/SipSession.md) directly.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile the session is associated with |
| `listener` | [SipSession.Listener](../android/net/sip/SipSession.Listener.md)!: to listen to SIP session events |

### getCallId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCallId(incomingCallIntent: Intent!): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the call ID from the specified incoming call broadcast intent.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| `incomingCallIntent` | [Intent](../android/content/Intent.md)!: the incoming call broadcast intent |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the call ID or null if the intent does not contain it |

### getOfferSessionDescription

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getOfferSessionDescription(incomingCallIntent: Intent!): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the offer session description from the specified incoming call broadcast intent.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| `incomingCallIntent` | [Intent](../android/content/Intent.md)!: the incoming call broadcast intent |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the offer session description or null if the intent does not have it |

### getSessionFor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionFor(incomingCallIntent: Intent!): SipSession!
```

**Deprecated:** *Deprecated in Java.*

Gets the [SipSession](../android/net/sip/SipSession.md) that handles the incoming call. For audio calls, consider to use [SipAudioCall](../android/net/sip/SipAudioCall.md) to handle the incoming call. See [takeAudioCall](../android/net/sip/SipManager.md)). Note that the method may be called only once for the same intent. For subsequent calls on the same intent, the method returns null.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| `incomingCallIntent` | [Intent](../android/content/Intent.md)!: the incoming call broadcast intent |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SipSession](../android/net/sip/SipSession.md)! | the session object that handles the incoming call |

### isApiSupported

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isApiSupported(context: Context!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the SIP API is supported by the system. 

### isIncomingCallIntent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isIncomingCallIntent(intent: Intent!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the intent is an incoming call broadcast intent.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android/content/Intent.md)!: the intent in question |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the intent is an incoming call broadcast intent |

### isOpened

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpened(localProfileUri: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the specified profile is opened in the SIP service for making and/or receiving calls.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URI of the profile in question |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the profile is enabled to receive calls |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### isRegistered

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRegistered(localProfileUri: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the SIP service has successfully registered the profile to the SIP provider (specified in the profile) for receiving calls. Returning true from this method also implies the profile is opened ([isOpened](../android/net/sip/SipManager.md))).

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URI of the profile in question |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the profile is registered to the SIP provider; false if the profile has not been opened in the SIP service or the SIP service has not yet successfully registered the profile to the SIP provider |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### isSipWifiOnly

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSipWifiOnly(context: Context!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if SIP is only available on WIFI. 

### isVoipSupported

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isVoipSupported(context: Context!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the system supports SIP-based VOIP API. 

### makeAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun makeAudioCall(
    localProfile: SipProfile!, 
    peerProfile: SipProfile!, 
    listener: SipAudioCall.Listener!, 
    timeout: Int
): SipAudioCall!
```

**Deprecated:** *Deprecated in Java.*

Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to make a call. The attempt will be timed out if the call is not established within `timeout` seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md)) will be called.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to make the call from |
| `peerProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to make the call to |
| `listener` | [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!: to listen to the call events from [SipAudioCall](../android/net/sip/SipAudioCall.md); can be null |
| --- | --- |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the timeout value in seconds. Default value (defined by SIP protocol) is used if `timeout` is zero or negative. |

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SipAudioCall](../android/net/sip/SipAudioCall.md)! | a [SipAudioCall](../android/net/sip/SipAudioCall.md) object |

| Exceptions ||
|--------------------------------|-------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md))
- [#isVoipSupported](../android/net/sip/SipManager.md)) 

### makeAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun makeAudioCall(
    localProfileUri: String!, 
    peerProfileUri: String!, 
    listener: SipAudioCall.Listener!, 
    timeout: Int
): SipAudioCall!
```

**Deprecated:** *Deprecated in Java.*

Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to make an audio call. The attempt will be timed out if the call is not established within `timeout` seconds and [onError(SipAudioCall, SipErrorCode.TIME_OUT, String)](../android/net/sip/SipAudioCall.Listener.md)) will be called.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: URI of the SIP profile to make the call from |
| `peerProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: URI of the SIP profile to make the call to |
| `listener` | [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!: to listen to the call events from [SipAudioCall](../android/net/sip/SipAudioCall.md); can be null |
| --- | --- |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the timeout value in seconds. Default value (defined by SIP protocol) is used if `timeout` is zero or negative. |

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SipAudioCall](../android/net/sip/SipAudioCall.md)! | a [SipAudioCall](../android/net/sip/SipAudioCall.md) object |

| Exceptions ||
|--------------------------------|-------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error or VOIP API is not supported by the device |

**See Also**

- [android.net.sip.SipAudioCall.Listener#onError](../android/net/sip/SipAudioCall.Listener.md))
- [#isVoipSupported](../android/net/sip/SipManager.md)) 

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(context: Context!): SipManager!
```

**Deprecated:** *Deprecated in Java.*

Creates a manager instance. Returns null if SIP API is not supported.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!: application context for creating the manager object |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [SipManager](../android/net/sip/SipManager.md)! | the manager instance or null if SIP API is not supported |

### open

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun open(localProfile: SipProfile!): Unit
```

**Deprecated:** *Deprecated in Java.*

Opens the profile for making generic SIP calls. The caller may make subsequent calls through #makeAudioCall. If one also wants to receive calls on the profile, use [open(android.net.sip.SipProfile,android.app.PendingIntent,android.net.sip.SipRegistrationListener)](../android/net/sip/SipManager.md)) instead.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to make calls from |

| Exceptions ||
|--------------------------------|-------------------------------------------------------------------------------------------|
| `android.net.sip.SipException` | if the profile contains incorrect settings or calling the SIP service results in an error |

### open

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun open(
    localProfile: SipProfile!, 
    incomingCallPendingIntent: PendingIntent!, 
    listener: SipRegistrationListener!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Opens the profile for making calls and/or receiving generic SIP calls. The caller may make subsequent calls through #makeAudioCall. If the auto-registration option is enabled in the profile, the SIP service will register the profile to the corresponding SIP provider periodically in order to receive calls from the provider. When the SIP service receives a new call, it will send out an intent with the provided action string. The intent contains a call ID extra and an offer session description string extra. Use [getCallId](../android/net/sip/SipManager.md)) and [getOfferSessionDescription](../android/net/sip/SipManager.md)) to retrieve those extras.

| Parameters ||
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to receive incoming calls for |
| `incomingCallPendingIntent` | [PendingIntent](../android/app/PendingIntent.md)!: When an incoming call is received, the SIP service will call [PendingIntent.send(Context, int, Intent)](../android/app/PendingIntent.md)) to send back the intent to the caller with [INCOMING_CALL_RESULT_CODE](../android/net/sip/SipManager.md) as the result code and the intent to fill in the call ID and session description information. It cannot be null. |
| `listener` | [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!: to listen to registration events; can be null |
| --- | --- |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if `incomingCallPendingIntent` is null |
| `android.net.sip.SipException` | if the profile contains incorrect settings or calling the SIP service results in an error |

**See Also**

- [#getCallId](../android/net/sip/SipManager.md))
- [#getOfferSessionDescription](../android/net/sip/SipManager.md))
- [#takeAudioCall](../android/net/sip/SipManager.md))
- [#isIncomingCallIntent](../android/net/sip/SipManager.md))
- [#getCallId](../android/net/sip/SipManager.md))
- [#getOfferSessionDescription](../android/net/sip/SipManager.md)) 

### register

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun register(
    localProfile: SipProfile!, 
    expiryTime: Int, 
    listener: SipRegistrationListener!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Manually registers the profile to the corresponding SIP provider for receiving calls. [open(android.net.sip.SipProfile,android.app.PendingIntent,android.net.sip.SipRegistrationListener)](../android/net/sip/SipManager.md)) is still needed to be called at least once in order for the SIP service to notify the caller with the [android.app.PendingIntent](../android/app/PendingIntent.md) when an incoming call is received.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to register with |
| `expiryTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): registration expiration time (in seconds) |
| `listener` | [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!: to listen to the registration events |
| --- | --- |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### setRegistrationListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRegistrationListener(
    localProfileUri: String!, 
    listener: SipRegistrationListener!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to listen to registration events. No effect if the profile has not been opened to receive calls (see [open(android.net.sip.SipProfile,android.app.PendingIntent,android.net.sip.SipRegistrationListener)](../android/net/sip/SipManager.md))).

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URI of the profile |
| `listener` | [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!: to listen to registration events; can be null |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### takeAudioCall

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeAudioCall(
    incomingCallIntent: Intent!, 
    listener: SipAudioCall.Listener!
): SipAudioCall!
```

**Deprecated:** *Deprecated in Java.*

Creates a [SipAudioCall](../android/net/sip/SipAudioCall.md) to take an incoming call. Before the call is returned, the listener will receive a [SipAudioCall.Listener.onRinging](../android/net/sip/SipAudioCall.Listener.md)) callback.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `incomingCallIntent` | [Intent](../android/content/Intent.md)!: the incoming call broadcast intent |
| `listener` | [SipAudioCall.Listener](../android/net/sip/SipAudioCall.Listener.md)!: to listen to the call events from [SipAudioCall](../android/net/sip/SipAudioCall.md); can be null |

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [SipAudioCall](../android/net/sip/SipAudioCall.md)! | a [SipAudioCall](../android/net/sip/SipAudioCall.md) object |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |

### unregister

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregister(
    localProfile: SipProfile!, 
    listener: SipRegistrationListener!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Manually unregisters the profile from the corresponding SIP provider for stop receiving further calls. This may interference with the auto registration process in the SIP service if the auto-registration option in the profile is enabled.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localProfile` | [SipProfile](../android/net/sip/SipProfile.md)!: the SIP profile to register with |
| `listener` | [SipRegistrationListener](../android/net/sip/SipRegistrationListener.md)!: to listen to the registration events |

| Exceptions ||
|--------------------------------|------------------------------------------------|
| `android.net.sip.SipException` | if calling the SIP service results in an error |
