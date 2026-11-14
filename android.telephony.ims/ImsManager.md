# ImsManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsManager

Kotlin| [Java](ImsManager.md) 
| --- | --- |

```
open class ImsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ImsManager](ImsManager.md) |

Provides access to information about Telephony IMS services on the device. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WFC_IMS_REGISTRATION_ERROR](ImsManager.md) An intent action indicating that IMS registration for WiFi calling has resulted in an error. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE](ImsManager.md) An extra key corresponding to a [CharSequence](../java.lang/CharSequence.md) value which contains the carrier specific message to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WFC_REGISTRATION_FAILURE_TITLE](ImsManager.md) An extra key corresponding to a [CharSequence](../java.lang/CharSequence.md) value which contains the carrier specific title to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. |
| --- | --- |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ImsMmTelManager](ImsMmTelManager.md) | [getImsMmTelManager](ImsManager.md))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of ImsMmTelManager for the subscription id specified. |
| open [ImsRcsManager](ImsRcsManager.md) | [getImsRcsManager](ImsManager.md))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of ImsRcsManager for the subscription id specified. |
| open [ProvisioningManager](ProvisioningManager.md) | [getProvisioningManager](ImsManager.md))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of [ProvisioningManager](ProvisioningManager.md) for the subscription id specified. |
| --- | --- |

## Constants

### ACTION_WFC_IMS_REGISTRATION_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WFC_IMS_REGISTRATION_ERROR: String
```

An intent action indicating that IMS registration for WiFi calling has resulted in an error. Contains error information that should be displayed to the user.

This intent will contain the following extra key/value pairs: [EXTRA_WFC_REGISTRATION_FAILURE_TITLE](ImsManager.md) and [EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE](ImsManager.md), which contain carrier specific error information that should be displayed to the user.

Usage: This intent is sent as an ordered broadcast. If the settings application is going to show the error information specified to the user, it should respond to [android.content.BroadcastReceiver#setResultCode(int)](../android.content/BroadcastReceiver.md))with [android.app.Activity#RESULT_CANCELED](../android.app/Activity.md), which will signal to the framework that the event was handled. If the framework does not receive a response to the ordered broadcast, it will then show a notification to the user indicating that there was a registration failure. 

 Value: "android.telephony.ims.action.WFC_IMS_REGISTRATION_ERROR"

### EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE: String
```

An extra key corresponding to a [CharSequence](../java.lang/CharSequence.md) value which contains the carrier specific message to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. 

 Value: "android.telephony.ims.extra.WFC_REGISTRATION_FAILURE_MESSAGE"

### EXTRA_WFC_REGISTRATION_FAILURE_TITLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WFC_REGISTRATION_FAILURE_TITLE: String
```

An extra key corresponding to a [CharSequence](../java.lang/CharSequence.md) value which contains the carrier specific title to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. 

 Value: "android.telephony.ims.extra.WFC_REGISTRATION_FAILURE_TITLE"

## Public methods

### getImsMmTelManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImsMmTelManager(subscriptionId: Int): ImsMmTelManager
```

Create an instance of ImsMmTelManager for the subscription id specified.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the subscription that this ImsMmTelManager will use. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ImsMmTelManager](ImsMmTelManager.md) | a ImsMmTelManager instance with the specific subscription ID. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription is invalid. |

### getImsRcsManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImsRcsManager(subscriptionId: Int): ImsRcsManager
```

Create an instance of ImsRcsManager for the subscription id specified.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the subscription that this ImsRcsManager will use. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ImsRcsManager](ImsRcsManager.md) | a ImsRcsManager instance with the specific subscription ID. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription is invalid. |

### getProvisioningManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvisioningManager(subscriptionId: Int): ProvisioningManager
```

Create an instance of [ProvisioningManager](ProvisioningManager.md) for the subscription id specified.

Provides a ProvisioningManager instance to carrier apps to update carrier provisioning information, as well as provides a callback so that apps can listen for changes in MMTEL/RCS provisioning

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the subscription that this ProvisioningManager will use. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [ProvisioningManager](ProvisioningManager.md) | a ProvisioningManager instance with the specific subscription ID. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription is invalid. |
