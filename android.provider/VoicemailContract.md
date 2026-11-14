# VoicemailContract

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VoicemailContract

Kotlin| [Java](VoicemailContract.md) 
| --- | --- |

```
open class VoicemailContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.VoicemailContract](VoicemailContract.md) |

The contract between the voicemail provider and applications. Contains definitions for the supported URIs and columns.

The content providers exposes two tables through this interface:

- Voicemails table: This stores the actual voicemail records. The columns and URIs for accessing this table are defined by the [Voicemails](../android/provider/VoicemailContract.Voicemails.md) class.
- Status table: This provides a way for the voicemail source application to convey its current state to the system. The columns and URIS for accessing this table are defined by the [Status](../android/provider/VoicemailContract.Status.md) class.

The minimum permission needed to access this content provider is [android.Manifest.permission#ADD_VOICEMAIL](../android/Manifest.permission.md) or carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](../android.telephony/TelephonyManager.md))).

Voicemails are inserted by what is called as a "voicemail source" application, which is responsible for syncing voicemail data between a remote server and the local voicemail content provider. "voicemail source" application should always set the [PARAM_KEY_SOURCE_PACKAGE](VoicemailContract.md) in the URI to identify its package.

In addition to the [ContentObserver](../android.database/ContentObserver.md) notifications the voicemail provider also generates broadcast intents to notify change for applications that are not active and therefore cannot listen to ContentObserver notifications. Broadcast intents with following actions are generated:

- [ACTION_NEW_VOICEMAIL](VoicemailContract.md) is generated for each new voicemail inserted.
- [Intent.ACTION_PROVIDER_CHANGED](../android.content/Intent.md) is generated for any change made into the database, including new voicemail.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Status](../android/provider/VoicemailContract.Status.md) Defines fields exposed through the /status path of this content provider. |
| | [Voicemails](../android/provider/VoicemailContract.Voicemails.md) Defines fields exposed through the /voicemail path of this content provider. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_FETCH_VOICEMAIL](VoicemailContract.md) Broadcast intent to request a voicemail source to fetch voicemail content of a specific voicemail from the remote server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_NEW_VOICEMAIL](VoicemailContract.md) Broadcast intent when a new voicemail record is inserted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SYNC_VOICEMAIL](VoicemailContract.md) Broadcast intent to request all voicemail sources to perform a sync with the remote server. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](VoicemailContract.md) The authority used by the voicemail provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PHONE_ACCOUNT_HANDLE](VoicemailContract.md) Extra included in [ACTION_SYNC_VOICEMAIL](VoicemailContract.md) broadcast intents to indicate which [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) to sync. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SELF_CHANGE](VoicemailContract.md) Extra included in [Intent.ACTION_PROVIDER_CHANGED](../android.content/Intent.md) broadcast intents to indicate if the receiving package made this change. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PARAM_KEY_SOURCE_PACKAGE](VoicemailContract.md) Parameter key used in the URI to specify the voicemail source package name. |

## Constants

### ACTION_FETCH_VOICEMAIL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_FETCH_VOICEMAIL: String
```

Broadcast intent to request a voicemail source to fetch voicemail content of a specific voicemail from the remote server. The voicemail to fetch is specified by the data uri of the intent.

All voicemail sources are expected to handle this event. After storing the content the application should also set [Voicemails.HAS_CONTENT](../android/provider/VoicemailContract.Voicemails.md) to 1; 

 Value: "android.intent.action.FETCH_VOICEMAIL"

### ACTION_NEW_VOICEMAIL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_NEW_VOICEMAIL: String
```

Broadcast intent when a new voicemail record is inserted. 

 Value: "android.intent.action.NEW_VOICEMAIL"

### ACTION_SYNC_VOICEMAIL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SYNC_VOICEMAIL: String
```

Broadcast intent to request all voicemail sources to perform a sync with the remote server. 

 Value: "android.provider.action.SYNC_VOICEMAIL"

### AUTHORITY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

The authority used by the voicemail provider. 

 Value: "com.android.voicemail"

### EXTRA_PHONE_ACCOUNT_HANDLE

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PHONE_ACCOUNT_HANDLE: String
```

Extra included in [ACTION_SYNC_VOICEMAIL](VoicemailContract.md) broadcast intents to indicate which [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) to sync. 

 Value: "android.provider.extra.PHONE_ACCOUNT_HANDLE"

### EXTRA_SELF_CHANGE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SELF_CHANGE: String
```

Extra included in [Intent.ACTION_PROVIDER_CHANGED](../android.content/Intent.md) broadcast intents to indicate if the receiving package made this change. 

 Value: "com.android.voicemail.extra.SELF_CHANGE"

### PARAM_KEY_SOURCE_PACKAGE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_KEY_SOURCE_PACKAGE: String
```

Parameter key used in the URI to specify the voicemail source package name.

This field must be set in all requests that originate from a voicemail source. 

 Value: "source_package"
