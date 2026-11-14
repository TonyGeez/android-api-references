# RcsUceAdapter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RcsUceAdapter

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/RcsUceAdapter "View this page in Java") 
| --- | --- |

```
open class RcsUceAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.RcsUceAdapter](https://developer.android.com/reference/kotlin/android/telephony/ims/RcsUceAdapter#) |

Manages RCS User Capability Exchange for the subscription specified. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUceSettingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/RcsUceAdapter#isUceSettingEnabled())`()` The setting for whether or not the user has opted in to the automatic refresh of the RCS capabilities associated with the contacts in the user's contact address book. |

## Public methods

### isUceSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUceSettingEnabled(): Boolean
```

The setting for whether or not the user has opted in to the automatic refresh of the RCS capabilities associated with the contacts in the user's contact address book. By default, this setting is disabled and must be enabled after the user has seen the opt-in dialog shown by [ImsRcsManager.ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN:kotlin.String).

If this feature is enabled, the device will periodically share the phone numbers of all of the contacts in the user's address book with the carrier to refresh the RCS capabilities cache associated with those contacts as the local cache becomes stale.

This setting will only enable this feature if [android.telephony.CarrierConfigManager.Ims#KEY_RCS_BULK_CAPABILITY_EXCHANGE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_RCS_BULK_CAPABILITY_EXCHANGE_BOOL:kotlin.String) is also enabled.

Note: This setting does not affect whether or not the device publishes its service capabilities if the subscription supports presence publication. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user has opted in for automatic refresh of the RCS capabilities of their contacts, false otherwise. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this instance of [RcsUceAdapter](https://developer.android.com/reference/kotlin/android/telephony/ims/RcsUceAdapter#) is valid, but the ImsService associated with the subscription is not available. This can happen if the ImsService has crashed, for example, or if the subscription becomes inactive. See [ImsException.getCode()](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for more information on the error codes. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |
