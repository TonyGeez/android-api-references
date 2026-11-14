# SubscriptionInfo

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubscriptionInfo

Kotlin| [Java](../android/telephony/SubscriptionInfo.md) 
| --- | --- |

```
open class SubscriptionInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SubscriptionInfo](../android/telephony/SubscriptionInfo.md) |

A Parcelable class for Subscription Information.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bitmap](../android/graphics/Bitmap.md)! | [createIconBitmap](../android/telephony/SubscriptionInfo.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates and returns an icon`Bitmap`to represent this`SubscriptionInfo`in a user interface. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/SubscriptionInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardId](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCarrierId](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getCarrierName](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCountryIso](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataRoaming](../android/telephony/SubscriptionInfo.md))`()` Whether user enables data roaming for this subscription or not. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDisplayName](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [ParcelUuid](../android/os/ParcelUuid.md)? | [getGroupUuid](../android/telephony/SubscriptionInfo.md))`()` Used in scenarios where different subscriptions are bundled as a group. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getIccId](../android/telephony/SubscriptionInfo.md))`()` Returns the ICC ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIconTint](../android/telephony/SubscriptionInfo.md))`()` A highlight color to use in displaying information about this`PhoneAccount`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMcc](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMccString](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMnc](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMncString](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNumber](../android/telephony/SubscriptionInfo.md))`()` Returns the number of this subscription. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPortIndex](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getServiceCapabilities](../android/telephony/SubscriptionInfo.md))`()` Retrieves the service capabilities for the current subscription. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSimSlotIndex](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionType](../android/telephony/SubscriptionInfo.md))`()` This method returns the type of a subscription. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUsageSetting](../android/telephony/SubscriptionInfo.md))`()` Get the usage setting for this subscription. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmbedded](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOnlyNonTerrestrialNetwork](../android/telephony/SubscriptionInfo.md))`()` Check if the subscription is exclusively for non-terrestrial networks. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpportunistic](../android/telephony/SubscriptionInfo.md))`()` An opportunistic subscription connects to a network that is limited in functionality and / or coverage. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/SubscriptionInfo.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/SubscriptionInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SubscriptionInfo](../android/telephony/SubscriptionInfo.md)!\> | [CREATOR](../android/telephony/SubscriptionInfo.md) <br /> |

## Public methods

### createIconBitmap

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createIconBitmap(context: Context!): Bitmap!
```

Creates and returns an icon`Bitmap`to represent this`SubscriptionInfo`in a user interface.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:A`Context`to get the`DisplayMetrics`s from. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)! | A bitmap icon for this`SubscriptionInfo`. |

### describeContents

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCardId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCardId(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The card ID of the SIM card which contains the subscription. |

**See Also**

- [android.telephony.UiccCardInfo#getCardId()](../android/telephony/UiccCardInfo.md)) 

### getCarrierId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCarrierId(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The carrier id of this subscription carrier. |

**See Also**

- [android.telephony.TelephonyManager#getSimCarrierId()](../android/telephony/TelephonyManager.md)) 

### getCarrierName

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCarrierName(): CharSequence!
```

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The name displayed to the user that identifies subscription provider name. This name is the SPN displayed in status bar and many other places. Can't be renamed by the user. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getDisplayName()> 

### getCountryIso

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCountryIso(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The ISO country code. Empty if not available. |

### getDataRoaming

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataRoaming(): Int
```

Whether user enables data roaming for this subscription or not. Either [SubscriptionManager.DATA_ROAMING_ENABLE](../android/telephony/SubscriptionManager.md) or [SubscriptionManager.DATA_ROAMING_DISABLE](../android/telephony/SubscriptionManager.md). 

### getDisplayName

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(): CharSequence!
```

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The name displayed to the user that identifies this subscription. This name is used in Settings page and can be renamed by the user. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getCarrierName()> 

### getGroupUuid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupUuid(): ParcelUuid?
```

Used in scenarios where different subscriptions are bundled as a group. It's typically a primary and an opportunistic subscription. (see [isOpportunistic()](../android/telephony/SubscriptionInfo.md))) Such that those subscriptions will have some affiliated behaviors such as opportunistic subscription may be invisible to the user.

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | Group UUID a String of group UUID if it belongs to a group. Otherwise`null`. |

### getIccId

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIccId(): String!
```

Returns the ICC ID. Starting with API level 29 Security Patch 2021-04-05, returns the ICC ID if the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission, has carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))), or is a device owner or profile owner that has been granted the READ_PHONE_STATE permission. The profile owner is an app that owns a managed profile on the device; for more details see [Work profiles](https://developer.android.com/work/managed-profiles). Profile owner access is deprecated and will be removed in a future release.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ICC ID, or an empty string if one of these requirements is not met |

### getIconTint

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTint(): Int
```

A highlight color to use in displaying information about this`PhoneAccount`.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A hexadecimal color value. |

### getMcc

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMcc(): Int
```

**Deprecated:** *Use [getMccString()](../android/telephony/SubscriptionInfo.md))instead.*

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The mobile country code. |

### getMccString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMccString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The mobile country code. This value may be`null`. |

### getMnc

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMnc(): Int
```

**Deprecated:** *Use [getMncString()](../android/telephony/SubscriptionInfo.md))instead.*

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The mobile network code. |

### getMncString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMncString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The mobile network code. This value may be`null`. |

### getNumber

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumber(): String!
```

**Deprecated:** *use [SubscriptionManager.getPhoneNumber(int)](../android/telephony/SubscriptionManager.md))instead, which takes a [subscription ID](../android/telephony/SubscriptionInfo.md)).*

Returns the number of this subscription. Starting with API level 30, returns the number of this subscription if the calling app meets at least one of the following requirements:

- If the calling app's target SDK is API level 29 or lower and the app has been granted the READ_PHONE_STATE permission.
- If the calling app has been granted any of READ_PRIVILEGED_PHONE_STATE, READ_PHONE_NUMBERS, or READ_SMS.
- If the calling app has carrier privileges (see [android.telephony.TelephonyManager#hasCarrierPrivileges](../android/telephony/TelephonyManager.md))).
- If the calling app is the default SMS role holder.

<br />

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the number of this subscription, or an empty string if none of the requirements are met. |

### getPortIndex

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPortIndex(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The port index of the SIM card which contains the subscription. |

### getServiceCapabilities

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServiceCapabilities(): MutableSet<Int!>
```

Retrieves the service capabilities for the current subscription.

These capabilities are hint to system components and applications, allowing them to enhance user experience. For instance, a Dialer application can inform the user that the current subscription is incapable of making voice calls if the voice service is not available.

Correct usage of these service capabilities must also consider the device's overall service capabilities. For example, even if the subscription supports voice calls, a voice call might not be feasible on a device that only supports data services. To determine the device's capabilities for voice and SMS services, refer to`TelephonyManager#isDeviceVoiceCapable()`and`TelephonyManager#isDeviceSmsCapable()`.

Emergency service availability may not directly correlate with the subscription or device's general service capabilities. In some cases, emergency calls might be possible even if the subscription or device does not typically support voice services.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!> | A set of integer representing the subscription's service capabilities, defined by`SubscriptionManager#SERVICE_CAPABILITY_VOICE`,`SubscriptionManager#SERVICE_CAPABILITY_SMS`and`SubscriptionManager#SERVICE_CAPABILITY_DATA`. This value cannot be`null`. Value is [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_VOICE](../android/telephony/SubscriptionManager.md), [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_SMS](../android/telephony/SubscriptionManager.md), or [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_DATA](../android/telephony/SubscriptionManager.md) |

**See Also**

- [android.telephony.TelephonyManager#isDeviceVoiceCapable()](../android/telephony/TelephonyManager.md))
- [android.telephony.TelephonyManager#isDeviceSmsCapable()](../android/telephony/TelephonyManager.md))
- [android.telephony.CarrierConfigManager#KEY_CELLULAR_SERVICE_CAPABILITIES_INT_ARRAY](../android/telephony/CarrierConfigManager.md)
- [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_VOICE](../android/telephony/SubscriptionManager.md)
- [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_SMS](../android/telephony/SubscriptionManager.md)
- [android.telephony.SubscriptionManager#SERVICE_CAPABILITY_DATA](../android/telephony/SubscriptionManager.md) 

### getSimSlotIndex

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSimSlotIndex(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the SIM slot that currently contains the subscription and not necessarily unique and maybe [SubscriptionManager.INVALID_SIM_SLOT_INDEX](../android/telephony/SubscriptionManager.md) if unknown or the subscription is inactive. |

### getSubscriptionId

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionId(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The subscription ID. |

### getSubscriptionType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionType(): Int
```

This method returns the type of a subscription. It can be [SubscriptionManager.SUBSCRIPTION_TYPE_LOCAL_SIM](../android/telephony/SubscriptionManager.md) or [SubscriptionManager.SUBSCRIPTION_TYPE_REMOTE_SIM](../android/telephony/SubscriptionManager.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of the subscription. Value is [android.telephony.SubscriptionManager#SUBSCRIPTION_TYPE_LOCAL_SIM](../android/telephony/SubscriptionManager.md), or [android.telephony.SubscriptionManager#SUBSCRIPTION_TYPE_REMOTE_SIM](../android/telephony/SubscriptionManager.md) |

### getUsageSetting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUsageSetting(): Int
```

Get the usage setting for this subscription.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The usage setting used for this subscription. Value is [android.telephony.SubscriptionManager#USAGE_SETTING_UNKNOWN](../android/telephony/SubscriptionManager.md), [android.telephony.SubscriptionManager#USAGE_SETTING_DEFAULT](../android/telephony/SubscriptionManager.md), [android.telephony.SubscriptionManager#USAGE_SETTING_VOICE_CENTRIC](../android/telephony/SubscriptionManager.md), or [android.telephony.SubscriptionManager#USAGE_SETTING_DATA_CENTRIC](../android/telephony/SubscriptionManager.md) |

### hashCode

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isEmbedded

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmbedded(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the subscription is from eSIM. |

### isOnlyNonTerrestrialNetwork

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOnlyNonTerrestrialNetwork(): Boolean
```

Check if the subscription is exclusively for non-terrestrial networks.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it is a non-terrestrial network subscription,`false`otherwise. |

### isOpportunistic

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpportunistic(): Boolean
```

An opportunistic subscription connects to a network that is limited in functionality and / or coverage.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether subscription is opportunistic. |

### toString

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SubscriptionInfo!>
```
