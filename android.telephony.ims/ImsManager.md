# ImsManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/ImsManager "View this page in Java") 

```
open class ImsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.ims.ImsManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#) |

Provides access to information about Telephony IMS services on the device. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WFC_IMS_REGISTRATION_ERROR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#ACTION_WFC_IMS_REGISTRATION_ERROR:kotlin.String) An intent action indicating that IMS registration for WiFi calling has resulted in an error. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE:kotlin.String) An extra key corresponding to a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) value which contains the carrier specific message to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WFC_REGISTRATION_FAILURE_TITLE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#EXTRA_WFC_REGISTRATION_FAILURE_TITLE:kotlin.String) An extra key corresponding to a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) value which contains the carrier specific title to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager) | [getImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getImsMmTelManager(kotlin.Int))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of ImsMmTelManager for the subscription id specified. |
| open [ImsRcsManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager) | [getImsRcsManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getImsRcsManager(kotlin.Int))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of ImsRcsManager for the subscription id specified. |
| open [ProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager) | [getProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getProvisioningManager(kotlin.Int))`(`subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an instance of [ProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager) for the subscription id specified. |

## Constants

### ACTION_WFC_IMS_REGISTRATION_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WFC_IMS_REGISTRATION_ERROR: String
```

An intent action indicating that IMS registration for WiFi calling has resulted in an error. Contains error information that should be displayed to the user.

This intent will contain the following extra key/value pairs: [EXTRA_WFC_REGISTRATION_FAILURE_TITLE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#EXTRA_WFC_REGISTRATION_FAILURE_TITLE:kotlin.String) and [EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE:kotlin.String), which contain carrier specific error information that should be displayed to the user.

Usage: This intent is sent as an ordered broadcast. If the settings application is going to show the error information specified to the user, it should respond to [android.content.BroadcastReceiver#setResultCode(int)](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultCode(kotlin.Int))with [android.app.Activity#RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int), which will signal to the framework that the event was handled. If the framework does not receive a response to the ordered broadcast, it will then show a notification to the user indicating that there was a registration failure. 

 Value: "android.telephony.ims.action.WFC_IMS_REGISTRATION_ERROR"

### EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WFC_REGISTRATION_FAILURE_MESSAGE: String
```

An extra key corresponding to a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) value which contains the carrier specific message to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. 

 Value: "android.telephony.ims.extra.WFC_REGISTRATION_FAILURE_MESSAGE"

### EXTRA_WFC_REGISTRATION_FAILURE_TITLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WFC_REGISTRATION_FAILURE_TITLE: String
```

An extra key corresponding to a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) value which contains the carrier specific title to be displayed as part of the message shown to the user when there is an error registering for WiFi calling. 

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
| [ImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager) | a ImsMmTelManager instance with the specific subscription ID. This value cannot be`null`. |

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
| [ImsRcsManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager) | a ImsRcsManager instance with the specific subscription ID. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription is invalid. |

### getProvisioningManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvisioningManager(subscriptionId: Int): ProvisioningManager
```

Create an instance of [ProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager) for the subscription id specified.

Provides a ProvisioningManager instance to carrier apps to update carrier provisioning information, as well as provides a callback so that apps can listen for changes in MMTEL/RCS provisioning

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the subscription that this ProvisioningManager will use. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [ProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager) | a ProvisioningManager instance with the specific subscription ID. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription is invalid. |
