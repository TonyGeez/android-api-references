# RcsUceAdapter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RcsUceAdapter

Kotlin| [Java](../android/telephony/ims/RcsUceAdapter.md) 
| --- | --- |

```
open class RcsUceAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.RcsUceAdapter](../android/telephony/ims/RcsUceAdapter.md) |

Manages RCS User Capability Exchange for the subscription specified. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUceSettingEnabled](../android/telephony/ims/RcsUceAdapter.md))`()` The setting for whether or not the user has opted in to the automatic refresh of the RCS capabilities associated with the contacts in the user's contact address book. |

## Public methods

### isUceSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUceSettingEnabled(): Boolean
```

The setting for whether or not the user has opted in to the automatic refresh of the RCS capabilities associated with the contacts in the user's contact address book. By default, this setting is disabled and must be enabled after the user has seen the opt-in dialog shown by [ImsRcsManager.ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN](../android/telephony/ims/ImsRcsManager.md).

If this feature is enabled, the device will periodically share the phone numbers of all of the contacts in the user's address book with the carrier to refresh the RCS capabilities cache associated with those contacts as the local cache becomes stale.

This setting will only enable this feature if [android.telephony.CarrierConfigManager.Ims#KEY_RCS_BULK_CAPABILITY_EXCHANGE_BOOL](../android/telephony/CarrierConfigManager.Ims.md) is also enabled.

Note: This setting does not affect whether or not the device publishes its service capabilities if the subscription supports presence publication. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user has opted in for automatic refresh of the RCS capabilities of their contacts, false otherwise. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this instance of [RcsUceAdapter](../android/telephony/ims/RcsUceAdapter.md) is valid, but the ImsService associated with the subscription is not available. This can happen if the ImsService has crashed, for example, or if the subscription becomes inactive. See [ImsException.getCode()](../android/telephony/ims/ImsException.md))for more information on the error codes. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android/content/pm/PackageManager.md). |
