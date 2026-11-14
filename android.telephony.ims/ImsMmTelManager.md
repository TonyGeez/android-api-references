# ImsMmTelManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsMmTelManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/ImsMmTelManager "View this page in Java") 
| --- | --- |

```
open class ImsMmTelManager : RegistrationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#) |

A manager for the MmTel (Multimedia Telephony) feature of an IMS network, given an associated subscription. Allows a user to query the IMS MmTel feature information for a subscription, register for registration and MmTel capability status callbacks, as well as query/modify user settings for the associated subscription. Use [android.telephony.ims.ImsManager#getImsMmTelManager(int)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getImsMmTelManager(kotlin.Int))to get an instance of this manager. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback) Receives IMS capability status updates from the ImsService. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_MODE_CELLULAR_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_CELLULAR_PREFERRED:kotlin.Int) Prefer registering for IMS over LTE if LTE signal quality is high enough. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_MODE_WIFI_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_ONLY:kotlin.Int) Register for IMS over IWLAN if WiFi signal quality is high enough. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_MODE_WIFI_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_PREFERRED:kotlin.Int) Prefer registering for IMS over IWLAN if possible if WiFi signal quality is high enough. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [RegistrationManager](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_NOT_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int) <br /> The IMS service is currently not registered to the carrier network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int) <br /> The IMS service is currently registered to the carrier network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERING](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int) <br /> The IMS service is currently in the process of registering to the carrier network. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRegistrationTransportType](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#getRegistrationTransportType(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `transportTypeCallback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVoWiFiModeSetting](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#getVoWiFiModeSetting())`()` Returns the user's voice over WiFi Roaming mode setting associated with the device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAdvancedCallingSettingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isAdvancedCallingSettingEnabled())`()` Query the user's setting for "Advanced Calling" or "Enhanced 4G LTE", which is used to enable MmTel IMS features, depending on the carrier configuration for the current subscription. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCrossSimCallingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isCrossSimCallingEnabled())`()` This configuration is meaningful only on dual sim device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTtyOverVolteEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isTtyOverVolteEnabled())`()` <br /> Requires android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVoWiFiRoamingSettingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isVoWiFiRoamingSettingEnabled())`()` Returns the user's voice over WiFi roaming setting associated with the current subscription. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVoWiFiSettingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isVoWiFiSettingEnabled())`()` <br /> Requires android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVtSettingEnabled](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#isVtSettingEnabled())`()` The user's setting for whether or not they have enabled the "Video Calling" setting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerImsRegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#registerImsRegistrationCallback(java.util.concurrent.Executor,%20android.telephony.ims.RegistrationManager.RegistrationCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `c:` ` [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback)`)` Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#registerImsStateCallback(java.util.concurrent.Executor,%20android.telephony.ims.ImsStateCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback)`)` Register a new callback, which is used to notify the registrant of changes to the state of the underlying IMS service that is attached to telephony to implement IMS functionality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerMmTelCapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#registerMmTelCapabilityCallback(java.util.concurrent.Executor,%20android.telephony.ims.ImsMmTelManager.CapabilityCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `c:` ` [ImsMmTelManager.CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback)`)` Registers a [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback) with the system, which will provide MmTel service availability updates for the subscription specified in [ImsManager#getImsMmTelManager(int)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getImsMmTelManager(kotlin.Int)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterImsRegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#unregisterImsRegistrationCallback(android.telephony.ims.RegistrationManager.RegistrationCallback))`(`c:` ` [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback)`)` Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#unregisterImsStateCallback(android.telephony.ims.ImsStateCallback))`(`callback:` ` [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback)`)` Unregisters a previously registered callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterMmTelCapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#unregisterMmTelCapabilityCallback(android.telephony.ims.ImsMmTelManager.CapabilityCallback))`(`c:` ` [ImsMmTelManager.CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback)`)` Removes an existing MmTel [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback). |

## Constants

### WIFI_MODE_CELLULAR_PREFERRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_MODE_CELLULAR_PREFERRED: Int
```

Prefer registering for IMS over LTE if LTE signal quality is high enough. 

 Value: 1

### WIFI_MODE_WIFI_ONLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_MODE_WIFI_ONLY: Int
```

Register for IMS over IWLAN if WiFi signal quality is high enough. Do not hand over to LTE registration if signal quality degrades. 

 Value: 0

### WIFI_MODE_WIFI_PREFERRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_MODE_WIFI_PREFERRED: Int
```

Prefer registering for IMS over IWLAN if possible if WiFi signal quality is high enough. 

 Value: 2

## Public methods

### getRegistrationTransportType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRegistrationTransportType(
    executor: Executor, 
    transportTypeCallback: Consumer<Int!>
): Unit
```

Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). Access by profile owners is deprecated and will be removed in a future release. Gets the Transport Type associated with the current IMS registration. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `transportTypeCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:This value cannot be`null`. Value is android.telephony.AccessNetworkConstants.TRANSPORT_TYPE_INVALID, [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WWAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WWAN:kotlin.Int), or [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WLAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WLAN:kotlin.Int) |

### getVoWiFiModeSetting

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVoWiFiModeSetting(): Int
```

Returns the user's voice over WiFi Roaming mode setting associated with the device.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The Voice over WiFi Mode preference set by the user, which can be one of the following: - [WIFI_MODE_WIFI_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_ONLY:kotlin.Int)- [WIFI_MODE_CELLULAR_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_CELLULAR_PREFERRED:kotlin.Int)- [WIFI_MODE_WIFI_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_PREFERRED:kotlin.Int) Value is android.telephony.ims.ImsMmTelManager.WIFI_MODE_UNKNOWN, [android.telephony.ims.ImsMmTelManager#WIFI_MODE_WIFI_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_ONLY:kotlin.Int), [android.telephony.ims.ImsMmTelManager#WIFI_MODE_CELLULAR_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_CELLULAR_PREFERRED:kotlin.Int), or [android.telephony.ims.ImsMmTelManager#WIFI_MODE_WIFI_PREFERRED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#WIFI_MODE_WIFI_PREFERRED:kotlin.Int) |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### isAdvancedCallingSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAdvancedCallingSettingEnabled(): Boolean
```

Query the user's setting for "Advanced Calling" or "Enhanced 4G LTE", which is used to enable MmTel IMS features, depending on the carrier configuration for the current subscription. If this setting is enabled, IMS voice and video telephony over IWLAN/LTE will be enabled as long as the carrier has provisioned these services for the specified subscription. Other IMS services (SMS/UT) are not affected by this user setting and depend on carrier requirements.

Note: If the carrier configuration for advanced calling is not editable or hidden, this method will always return the default value.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user's setting for advanced calling is enabled, false otherwise. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager#KEY_CARRIER_VOLTE_PROVISIONING_REQUIRED_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_CARRIER_VOLTE_PROVISIONING_REQUIRED_BOOL:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_EDITABLE_ENHANCED_4G_LTE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_EDITABLE_ENHANCED_4G_LTE_BOOL:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_HIDE_ENHANCED_4G_LTE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_HIDE_ENHANCED_4G_LTE_BOOL:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_ENHANCED_4G_LTE_ON_BY_DEFAULT_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_ENHANCED_4G_LTE_ON_BY_DEFAULT_BOOL:kotlin.String)
- [android.telephony.CarrierConfigManager#KEY_CARRIER_VOLTE_AVAILABLE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_CARRIER_VOLTE_AVAILABLE_BOOL:kotlin.String) 

### isCrossSimCallingEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCrossSimCallingEnabled(): Boolean
```

This configuration is meaningful only on dual sim device. If enabled, this will result in the device setting up IMS of all other active subscriptions over the INTERNET APN of the primary default data subscription when any of those subscriptions are roaming or out of service and if wifi is not available for VoWifi. This feature will be disabled if [CarrierConfigManager.KEY_CARRIER_CROSS_SIM_IMS_AVAILABLE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_CARRIER_CROSS_SIM_IMS_AVAILABLE_BOOL:kotlin.String) is set to false.

Following are the conditions in which system will try to register IMS over cross sim

- Wifi is not available, one SIM is roaming and the default data SIM is in home network. Then roaming SIM IMS will be registered over INTERNET APN of the default data subscription
- Wifi is not available, one SIM is out of service and the default data SIM is in home network. Then out of service SIM IMS will be registered over INTERNET APN of the default data subscription

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user's setting for Voice over Cross SIM is enabled and false if it is not |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the IMS service associated with this subscription is not available or the IMS service is not available. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### isTtyOverVolteEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTtyOverVolteEnabled(): Boolean
```

<br />

Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if TTY over VoLTE is supported This API requires one of the following: - The caller holds the READ_PRECISE_PHONE_STATE permission. - If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission. - The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription. The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

**See Also**

- [android.telephony.CarrierConfigManager#KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_CARRIER_VOLTE_TTY_SUPPORTED_BOOL:kotlin.String) 

### isVoWiFiRoamingSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isVoWiFiRoamingSettingEnabled(): Boolean
```

Returns the user's voice over WiFi roaming setting associated with the current subscription.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user's setting for Voice over WiFi while roaming is enabled, false if disabled. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### isVoWiFiSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isVoWiFiSettingEnabled(): Boolean
```

<br />

Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user's setting for Voice over WiFi is enabled and false if it is not. This API requires one of the following: - The caller holds the READ_PRECISE_PHONE_STATE permission. - If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission. - The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription. The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### isVtSettingEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isVtSettingEnabled(): Boolean
```

The user's setting for whether or not they have enabled the "Video Calling" setting.

Note: If the carrier configuration for advanced calling is not editable or hidden, this method will always return the default value.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the user's "Video Calling" setting is currently enabled. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the subscription associated with this operation is not active (SIM is not inserted, ESIM inactive) or invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have [PackageManager.FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String). |

### registerImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerImsRegistrationCallback(
    executor: Executor, 
    c: RegistrationManager.RegistrationCallback
): Unit
```

Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). Registers a [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) with the system. Use 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `c` | [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the`ImsService`associated with the subscription is not available. This can happen if the service crashed, for example. See [ImsException.getCode()](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for a more detailed reason. |

### registerImsStateCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerImsStateCallback(
    executor: Executor, 
    callback: ImsStateCallback
): Unit
```

Register a new callback, which is used to notify the registrant of changes to the state of the underlying IMS service that is attached to telephony to implement IMS functionality. If the manager is created for the [SubscriptionManager.DEFAULT_SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#DEFAULT_SUBSCRIPTION_ID:kotlin.Int), this throws an [ImsException](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException).

Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the Executor that will be used to call the [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback). This value cannot be`null`. |
| `callback` | [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback):The callback instance being registered. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | in the case that the callback can not be registered. See [ImsException.getCode](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for more information on when this is called. |

### registerMmTelCapabilityCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerMmTelCapabilityCallback(
    executor: Executor, 
    c: ImsMmTelManager.CapabilityCallback
): Unit
```

Registers a [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback) with the system, which will provide MmTel service availability updates for the subscription specified in [ImsManager#getImsMmTelManager(int)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager#getImsMmTelManager(kotlin.Int)). Use [SubscriptionManager.OnSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener.html#) to listen to subscription changed events and call [unregisterMmTelCapabilityCallback(android.telephony.ims.ImsMmTelManager.CapabilityCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#unregisterMmTelCapabilityCallback(android.telephony.ims.ImsMmTelManager.CapabilityCallback))to clean up.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. When the callback is registered, it will initiate the callback c to be called with the current capabilities. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor the callback events should be run on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `c` | [ImsMmTelManager.CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback):The MmTel [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback) to be registered. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the`ImsService`associated with the subscription is not available. This can happen if the service crashed, for example. See [ImsException.getCode()](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for a more detailed reason. |

**See Also**

- [#unregisterMmTelCapabilityCallback(CapabilityCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#unregisterMmTelCapabilityCallback(android.telephony.ims.ImsMmTelManager.CapabilityCallback)) 

### unregisterImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterImsRegistrationCallback(c: RegistrationManager.RegistrationCallback): Unit
```

Requires Permission: [READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) or that the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())). Access by profile owners is deprecated and will be removed in a future release. Removes an existing [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback). When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback):This value cannot be`null`. |

### unregisterImsStateCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterImsStateCallback(callback: ImsStateCallback): Unit
```

Unregisters a previously registered callback.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback):The callback instance to be unregistered. This value cannot be`null`. |

### unregisterMmTelCapabilityCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterMmTelCapabilityCallback(c: ImsMmTelManager.CapabilityCallback): Unit
```

Removes an existing MmTel [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback). When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op.

This API requires one of the following:

- The caller holds the READ_PRECISE_PHONE_STATE permission.
- If the caller is the device or profile owner, the caller holds the [Manifest.permission.READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) permission.
- The caller has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges())) on any active subscription.

The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Access by profile owners is deprecated and will be removed in a future release. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [ImsMmTelManager.CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback):The MmTel [CapabilityCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager.CapabilityCallback) to be removed. This value cannot be`null`. |

**See Also**

- [#registerMmTelCapabilityCallback(Executor, CapabilityCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager#registerMmTelCapabilityCallback(java.util.concurrent.Executor,%20android.telephony.ims.ImsMmTelManager.CapabilityCallback))
