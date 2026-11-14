# ProvisioningManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProvisioningManager

Kotlin| [Java](ProvisioningManager.md) 
| --- | --- |

```
open class ProvisioningManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ProvisioningManager](ProvisioningManager.md) |

Manages IMS provisioning and configuration parameters, as well as callbacks for apps to listen to changes in these configurations. IMS provisioning keys are defined per carrier or OEM using OMA-DM or other provisioning applications and may vary. It is up to the carrier and OEM applications to ensure that the correct provisioning keys are being used when integrating with a vendor's ImsService. Use [android.telephony.ims.ImsManager#getProvisioningManager(int)](ImsManager.md))to get an instance of this manager. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md) Callback for IMS provisioning feature changes. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getProvisioningStatusForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the provisioning status for the IMS MmTel capability specified. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRcsProvisioningStatusForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the provisioning status for the IMS RCS capability specified. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProvisioningRequiredForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether provisioning for the MMTEL capability and IMS registration technology specified is required or not |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRcsProvisioningRequiredForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether provisioning for the RCS capability and IMS registration technology specified is required or not |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerFeatureProvisioningChangedCallback](ProvisioningManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [ProvisioningManager.FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md)`)` Register a new [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md), which is used to listen for IMS feature provisioning updates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProvisioningStatusForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isProvisioned:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the provisioning status for the IMS MmTel capability using the specified subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRcsProvisioningStatusForCapability](ProvisioningManager.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tech:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isProvisioned:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the provisioning status for the IMS RCS capability using the specified subscription. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterFeatureProvisioningChangedCallback](ProvisioningManager.md))`(`callback:` ` [ProvisioningManager.FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md)`)` Unregisters a previously registered [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md) instance. |

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
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device is provisioned for the capability or does not require provisioning, false if the capability does require provisioning and has not been provisioned yet. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE](../android/telephony/CarrierConfigManager.Ims.md) 

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

- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](ImsRcsManager.md), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](ImsRcsManager.md), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](ImsRcsManager.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device is provisioned for the capability or does not require provisioning, false if the capability does require provisioning and has not been provisioned yet. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE](../android/telephony/CarrierConfigManager.Ims.md) 

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
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if provisioning is required for the MMTEL capability and IMS registration technology specified, false if it is not required or if the device does not support IMS. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

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
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](ImsRcsManager.md), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](ImsRcsManager.md), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](ImsRcsManager.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if provisioning is required for the RCS capability and IMS registration technology specified, false if it is not required or if the device does not support IMS. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

### registerFeatureProvisioningChangedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerFeatureProvisioningChangedCallback(
    executor: Executor, 
    callback: ProvisioningManager.FeatureProvisioningCallback
): Unit
```

Register a new [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md), which is used to listen for IMS feature provisioning updates.

When the subscription associated with this callback is removed (SIM removed, ESIM swap,etc...), this callback will automatically be removed.

Requires Permission:

- android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE,
- [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor that the callback methods will be called on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [ProvisioningManager.FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md):The callback instance being registered. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the service crashed, for example. See [ImsException.getCode()](ImsException.md))for a more detailed reason. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

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

- [android.Manifest.permission#MODIFY_PHONE_STATE](../android/Manifest.permission.md),
- or that the calling app has carrier privileges (see
- [TelephonyManager.hasCarrierPrivileges](../android.telephony/TelephonyManager.md))).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#MODIFY_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isProvisioned` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the device is provisioned for UT over IMS, false otherwise. |
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VOICE](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_VIDEO](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_UT](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_SMS](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md), and [android.telephony.ims.feature.MmTelFeature.MmTelCapabilities#CAPABILITY_TYPE_CALL_COMPOSER_BUSINESS_ONLY](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |
| --- | --- |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_MMTEL_REQUIRES_PROVISIONING_BUNDLE](../android/telephony/CarrierConfigManager.Ims.md) 

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

- [android.Manifest.permission#MODIFY_PHONE_STATE](../android/Manifest.permission.md),
- or that the caller has carrier privileges (see [TelephonyManager.hasCarrierPrivileges()](../android.telephony/TelephonyManager.md))).

<br />

This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires [android.Manifest.permission#MODIFY_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isProvisioned` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the device is provisioned for the RCS capability specified, false otherwise. |
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_NONE](ImsRcsManager.md), [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE](ImsRcsManager.md), and [android.telephony.ims.ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE](ImsRcsManager.md) |
| `tech` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NONE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_LTE](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_IWLAN](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_CROSS_SIM](../android.telephony.ims.stub/ImsRegistrationImplBase.md), [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_NR](../android.telephony.ims.stub/ImsRegistrationImplBase.md), or [android.telephony.ims.stub.ImsRegistrationImplBase#REGISTRATION_TECH_3G](../android.telephony.ims.stub/ImsRegistrationImplBase.md) |
| --- | --- |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

**See Also**

- [android.telephony.CarrierConfigManager.Ims#KEY_RCS_REQUIRES_PROVISIONING_BUNDLE](../android/telephony/CarrierConfigManager.Ims.md) 

### unregisterFeatureProvisioningChangedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterFeatureProvisioningChangedCallback(callback: ProvisioningManager.FeatureProvisioningCallback): Unit
```

Unregisters a previously registered [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md) instance. When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ProvisioningManager.FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md):The existing [FeatureProvisioningCallback](../android/telephony/ims/ProvisioningManager.FeatureProvisioningCallback.md) to be removed. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md). |

**See Also**

- [#registerFeatureProvisioningChangedCallback(Executor, FeatureProvisioningCallback)](ProvisioningManager.md))
