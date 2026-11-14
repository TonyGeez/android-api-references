# ProvisioningManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProvisioningManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/ProvisioningManager "View this page in Java") 

```
open class ProvisioningManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.ims.ProvisioningManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#) |

Manages IMS provisioning and configuration parameters, as well as callbacks for apps to listen to changes in these configurations. IMS provisioning keys are defined per carrier or OEM using OMA-DM or other provisioning applications and may vary. It is up to the carrier and OEM applications to ensure that the correct provisioning keys are being used when integrating with a vendor's ImsService. Use [android.telephony.ims.ImsManager#getProvisioningManager(int)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getProvisioningManager(kotlin.Int))to get an instance of this manager. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback) Callback for IMS provisioning feature changes. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getProvisioningStatusForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#getProvisioningStatusForCapability(kotlin.Int,%20kotlin.Int))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the provisioning status for the IMS MmTel capability specified. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRcsProvisioningStatusForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#getRcsProvisioningStatusForCapability(kotlin.Int,%20kotlin.Int))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the provisioning status for the IMS RCS capability specified. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProvisioningRequiredForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#isProvisioningRequiredForCapability(kotlin.Int,%20kotlin.Int))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether provisioning for the MMTEL capability and IMS registration technology specified is required or not |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRcsProvisioningRequiredForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#isRcsProvisioningRequiredForCapability(kotlin.Int,%20kotlin.Int))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether provisioning for the RCS capability and IMS registration technology specified is required or not |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerFeatureProvisioningChangedCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#registerFeatureProvisioningChangedCallback(java.util.concurrent.Executor,%20android.telephony.ims.ProvisioningManager.FeatureProvisioningCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [ProvisioningManager.FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback)`)` Register a new [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback), which is used to listen for IMS feature provisioning updates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProvisioningStatusForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#setProvisioningStatusForCapability(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isProvisioned:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the provisioning status for the IMS MmTel capability using the specified subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRcsProvisioningStatusForCapability](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#setRcsProvisioningStatusForCapability(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isProvisioned:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the provisioning status for the IMS RCS capability using the specified subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterFeatureProvisioningChangedCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#unregisterFeatureProvisioningChangedCallback(android.telephony.ims.ProvisioningManager.FeatureProvisioningCallback))`(`callback:` ` [ProvisioningManager.FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback)`)` Unregisters a previously registered [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback) instance. |

## Public methods

### getProvisioningStatusForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvisioningStatusForCapability(
    capability: Int, 
    tech: Int
): Boolean
```

Get the provisioning status for the IMS MmTel capability specified. If provisioning is not required for the queried`capability`and`tech`combination specified, this method will always return`true`.

Requires Permission:

- android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE,
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER:kotlin.Int), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device is provisioned for the capability or does not require provisioning, false if the capability does require provisioning and has not been provisioned yet. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE:kotlin.String) 

### getRcsProvisioningStatusForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRcsProvisioningStatusForCapability(
    capability: Int, 
    tech: Int
): Boolean
```

Get the provisioning status for the IMS RCS capability specified. If provisioning is not required for the queried`capability`or if the device does not support IMS this method will always return`true`.

Requires Permission:

- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_NONE:kotlin.Int), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE:kotlin.Int), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device is provisioned for the capability or does not require provisioning, false if the capability does require provisioning and has not been provisioned yet. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE:kotlin.String) 

### isProvisioningRequiredForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isProvisioningRequiredForCapability(
    capability: Int, 
    tech: Int
): Boolean
```

Indicates whether provisioning for the MMTEL capability and IMS registration technology specified is required or not

Requires Permission:

- android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE,
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER:kotlin.Int), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if provisioning is required for the MMTEL capability and IMS registration technology specified, false if it is not required or if the device does not support IMS. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### isRcsProvisioningRequiredForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRcsProvisioningRequiredForCapability(
    capability: Int, 
    tech: Int
): Boolean
```

Indicates whether provisioning for the RCS capability and IMS registration technology specified is required or not

Requires Permission:

- android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE,
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_NONE:kotlin.Int), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE:kotlin.Int), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if provisioning is required for the RCS capability and IMS registration technology specified, false if it is not required or if the device does not support IMS. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### registerFeatureProvisioningChangedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerFeatureProvisioningChangedCallback(
    executor: Executor, 
    callback: ProvisioningManager.FeatureProvisioningCallback
): Unit
```

Register a new [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback), which is used to listen for IMS feature provisioning updates.

When the subscription associated with this callback is removed (SIM removed, ESIM swap,etc...), this callback will automatically be removed.

Requires Permission:

- android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE,
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor that the callback methods will be called on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [ProvisioningManager.FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback):The callback instance being registered. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the service crashed, for example. See [ImsException.getCode()](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for a more detailed reason. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### setProvisioningStatusForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProvisioningStatusForCapability(
    capability: Int, 
    tech: Int, 
    isProvisioned: Boolean
): Unit
```

Set the provisioning status for the IMS MmTel capability using the specified subscription. Provisioning may or may not be required, depending on the carrier configuration. If provisioning is not required for the carrier associated with this subscription or the device does not support the capability/technology combination specified, this operation will be a no-op.

Requires Permission:

- [android.Manifest.permission#MODIFY_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String),
- or that the calling app has carrier privileges (see
- [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#MODIFY_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isProvisioned` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the device is provisioned for UT over IMS, false otherwise. |
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS:kotlin.Int), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER:kotlin.Int), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE:kotlin.String) 

### setRcsProvisioningStatusForCapability

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRcsProvisioningStatusForCapability(
    capability: Int, 
    tech: Int, 
    isProvisioned: Boolean
): Unit
```

Set the provisioning status for the IMS RCS capability using the specified subscription. Provisioning may or may not be required, depending on the carrier configuration. If provisioning is not required for the carrier associated with this subscription or the device does not support the capability/technology combination specified, this operation will be a no-op.

Requires Permission:

- [android.Manifest.permission#MODIFY_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#MODIFY_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isProvisioned` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the device is provisioned for the RCS capability specified, false otherwise. |
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_NONE:kotlin.Int), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE:kotlin.Int), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE:kotlin.Int) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NONE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_LTE:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM:kotlin.Int), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_NR:kotlin.Int), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](https://developer.android.com/reference/kotlin/android/telephony/ims/stub/ImsRegistrationImplBase#REGISTRATION_TECH_3G:kotlin.Int) |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE:kotlin.String) 

### unregisterFeatureProvisioningChangedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterFeatureProvisioningChangedCallback(callback: ProvisioningManager.FeatureProvisioningCallback): Unit
```

Unregisters a previously registered [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback) instance. When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ProvisioningManager.FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback):The existing [FeatureProvisioningCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback) to be removed. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [#registerFeatureProvisioningChangedCallback(Executor, FeatureProvisioningCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/ProvisioningManager#registerFeatureProvisioningChangedCallback(java.util.concurrent.Executor,%20android.telephony.ims.ProvisioningManager.FeatureProvisioningCallback))
