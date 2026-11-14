Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubscriptionManager

```
open class SubscriptionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.SubscriptionManager](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#) |

Subscription manager provides the mobile subscription information. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener` A listener class for monitoring changes to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records of opportunistic subscriptions. |
| open | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener` A listener class for monitoring changes to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SMS_SUBSCRIPTION_CHANGED:kotlin.String` Broadcast Action: The default sms subscription has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SUBSCRIPTION_CHANGED:kotlin.String` Broadcast Action: The default subscription has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_MANAGE_SUBSCRIPTION_PLANS:kotlin.String` Activity Action: Display UI for managing the billing relationship plans between a carrier and a specific subscriber. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_REFRESH_SUBSCRIPTION_PLANS:kotlin.String` Broadcast Action: Request a refresh of the billing relationship plans between a carrier and a specific subscriber. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL:kotlin.Int` Device status is shared whenever possible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL_CONTACTS:kotlin.Int` Device status is shared with all numbers in the user's contacts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_DISABLED:kotlin.Int` Device status is not shared to a remote party. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_SELECTED_CONTACTS:kotlin.Int` Device status is shared with all selected contacts. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_STATUS_SHARING:kotlin.String` TelephonyProvider column name for device to device sharing status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_STATUS_SHARING_SELECTED_CONTACTS:kotlin.String` TelephonyProvider column name for contacts information that allow device to device sharing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DATA_ROAMING_DISABLE:kotlin.Int` Indicates that data roaming is disabled for a subscription |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DATA_ROAMING_ENABLE:kotlin.Int` Indicates that data roaming is enabled for a subscription |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` Indicates the default subscription ID in Telephony. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SLOT_INDEX:kotlin.String` Integer extra to specify SIM slot index. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` Integer extra used with `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SUBSCRIPTION_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SMS_SUBSCRIPTION_CHANGED:kotlin.String` to indicate the subscription which has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SIM_SLOT_INDEX:kotlin.Int` Indicates invalid sim slot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` An invalid subscription identifier |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int` A source of phone number: provided by an app that has carrier privilege. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_IMS:kotlin.Int` A source of phone number: provided by IMS (IP Multimedia Subsystem) implementation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` A source of phone number: provided by the Entitlement Server using the GSMA TS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` A source of phone number: the EF-MSISDN (see 3GPP TS 31.102), or EF-MDN for CDMA (see 3GPP2 C.P0065-B), from UICC application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SERVICE_CAPABILITY_DATA:kotlin.Int` Represents a value indicating the data calling capabilities of a subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SERVICE_CAPABILITY_SMS:kotlin.Int` Represents a value indicating the SMS capabilities of a subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SERVICE_CAPABILITY_VOICE:kotlin.Int` Represents a value indicating the voice calling capabilities of a subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SUBSCRIPTION_TYPE_LOCAL_SIM:kotlin.Int` This constant is to designate a subscription as a Local-SIM Subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SUBSCRIPTION_TYPE_REMOTE_SIM:kotlin.Int` This constant is to designate a subscription as a Remote-SIM Subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_DATA_CENTRIC:kotlin.Int` This subscription is forced to data-centric mode |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_DEFAULT:kotlin.Int` Subscription uses the default setting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_UNKNOWN:kotlin.Int` The usage setting is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#USAGE_SETTING_VOICE_CENTRIC:kotlin.Int` This subscription is forced to voice-centric mode |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#addOnOpportunisticSubscriptionsChangedListener(java.util.concurrent.Executor,%20android.telephony.SubscriptionManager.OnOpportunisticSubscriptionsChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener)` Register for changes to the list of opportunistic subscription records or to the individual records themselves. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#addOnSubscriptionsChangedListener(android.telephony.SubscriptionManager.OnSubscriptionsChangedListener)(listener: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener!)` Register for changes to the list of active `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records or to the individual records themselves. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#addOnSubscriptionsChangedListener(java.util.concurrent.Executor,%20android.telephony.SubscriptionManager.OnSubscriptionsChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener)` Register for changes to the list of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records or to the individual records (active or inactive) themselves. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#addSubscriptionsIntoGroup(kotlin.collections.MutableList,%20android.os.ParcelUuid)(subIdList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>, groupUuid: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)` Add a list of subscriptions into a group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#canManageSubscription(android.telephony.SubscriptionInfo)(info: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!)` Checks whether the app with the given context is authorized to manage the given subscription according to its metadata. |
| open [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#createSubscriptionGroup(kotlin.collections.MutableList)(subIdList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Inform SubscriptionManager that subscriptions in the list are bundled as a group. |
| open static [SubscriptionManager](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#)! | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#from(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\>? | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getAccessibleSubscriptionInfoList()()` Gets the SubscriptionInfo(s) of all embedded subscriptions accessible to the calling app, if any. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveDataSubscriptionId()()` Get active data subscription id. |
| open [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)! | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfo(kotlin.Int)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the active SubscriptionInfo with the input subId. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoCount()()` Get the active subscription count. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoCountMax()()` <br /> |
| open [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)! | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoForSimSlotIndex(kotlin.Int)(slotIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the active SubscriptionInfo associated with the slotIndex |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\>? | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoList()()` Get the SubscriptionInfo(s) of the currently active SIM(s). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getAllSubscriptionInfoList()()` Get all subscription info records from SIMs that are inserted now or previously inserted. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getCompleteActiveSubscriptionInfoList()()` Get both hidden and visible SubscriptionInfo(s) of the currently active SIM(s). |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultDataSubscriptionId()()` Returns the system's default data subscription id. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSmsSubscriptionId()()` Returns the system's default SMS subscription id. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()()` Returns the system's default subscription id. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultVoiceSubscriptionId()()` Returns the system's default voice subscription id. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDeviceToDeviceStatusSharingContacts(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the list of contacts that allow device to device status sharing. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDeviceToDeviceStatusSharingPreference(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the user-chosen device to device status sharing preference |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getOpportunisticSubscriptions()()` Return opportunistic subscriptions that can be visible to the caller. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the phone number for the given `subId`, or an empty string if not available. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int,%20kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the phone number for the given `subscriptionId` and `source`, or an empty string if not available. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSlotIndex(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get slotIndex associated with the subscription. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionId(kotlin.Int)(slotIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the subscription id for specified logical SIM slot index. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionIds(kotlin.Int)(slotIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get an array of subscription ids for the specified logical SIM slot Index. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionPlans(kotlin.Int)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the description of the billing relationship plan between a carrier and a specific subscriber. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!\> | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionsInGroup(android.os.ParcelUuid)(groupUuid: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)` Get subscriptionInfo list of subscriptions that are in the same group of given subId. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isActiveSubscriptionId(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the supplied subscription ID corresponds to a subscription which is actively in use on the device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isNetworkRoaming(kotlin.Int)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the device is considered roaming on the current network for a subscription. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isUsableSubscriptionId(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check if the supplied subscription ID is usable. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isValidSubscriptionId(kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check if the supplied subscription ID is valid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#removeOnOpportunisticSubscriptionsChangedListener(android.telephony.SubscriptionManager.OnOpportunisticSubscriptionsChangedListener)(listener: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener)` Unregister the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener` that is currently listening opportunistic subscriptions change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#removeOnSubscriptionsChangedListener(android.telephony.SubscriptionManager.OnSubscriptionsChangedListener)(listener: https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener!)` Unregister the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#removeSubscriptionsFromGroup(kotlin.collections.MutableList,%20android.os.ParcelUuid)(subIdList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>, groupUuid: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)` Remove a list of subscriptions from their subscription group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setCarrierPhoneNumber(kotlin.Int,%20kotlin.String)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Sets the phone number for the given `subId` for source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setDeviceToDeviceStatusSharingContacts(kotlin.Int,%20kotlin.collections.MutableList)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contacts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Set the list of contacts that allow device to device status sharing for a subscription id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setDeviceToDeviceStatusSharingPreference(kotlin.Int,%20kotlin.Int)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sharing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the device to device status sharing user preference for a subscription id. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setOpportunistic(kotlin.Boolean,%20kotlin.Int)(opportunistic: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set whether a subscription is opportunistic, that is, whether the network it connects to has limited coverage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionOverrideCongested(kotlin.Int,%20kotlin.Boolean,%20kotlin.IntArray,%20kotlin.Long)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, overrideCongested: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, networkTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, expirationDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered congested. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionOverrideCongested(kotlin.Int,%20kotlin.Boolean,%20kotlin.Long)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, overrideCongested: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, expirationDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered congested. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionOverrideUnmetered(kotlin.Int,%20kotlin.Boolean,%20kotlin.IntArray,%20kotlin.Long)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, overrideUnmetered: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, networkTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, expirationDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered unmetered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionOverrideUnmetered(kotlin.Int,%20kotlin.Boolean,%20kotlin.Long)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, overrideUnmetered: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, expirationDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered unmetered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, plans: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan!>)` Set the description of the billing relationship plan between a carrier and a specific subscriber. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList,%20kotlin.Long)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, plans: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan!>, expirationDurationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set the description of the billing relationship plan between a carrier and a specific subscriber. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setTs43PhoneNumber(kotlin.Int,%20kotlin.String)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Sets the phone number for the given `subId` for source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#switchToSubscription(kotlin.Int,%20android.app.PendingIntent)(subId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, callbackIntent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Switch to a certain subscription. |

## Constants

### ACTION_DEFAULT_SMS_SUBSCRIPTION_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEFAULT_SMS_SUBSCRIPTION_CHANGED: String
```

Broadcast Action: The default sms subscription has changed. This has the following extra values:

<br />

`https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` extra indicates the current default sms subscription index

 Value: "android.telephony.action.DEFAULT_SMS_SUBSCRIPTION_CHANGED"

### ACTION_DEFAULT_SUBSCRIPTION_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DEFAULT_SUBSCRIPTION_CHANGED: String
```

Broadcast Action: The default subscription has changed. This has the following extra values:

<br />

The `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` extra indicates the current default subscription index

 Value: "android.telephony.action.DEFAULT_SUBSCRIPTION_CHANGED"

### ACTION_MANAGE_SUBSCRIPTION_PLANS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_SUBSCRIPTION_PLANS: String
```

Activity Action: Display UI for managing the billing relationship plans between a carrier and a specific subscriber.

Carrier apps are encouraged to implement this activity, and the OS will provide an affordance to quickly enter this activity, typically via Settings. This affordance will only be shown when the carrier app is actively providing subscription plan information via `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList)`.

Contains `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` to indicate which subscription the user is interested in.

 Value: "android.telephony.action.MANAGE_SUBSCRIPTION_PLANS"

### ACTION_REFRESH_SUBSCRIPTION_PLANS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REFRESH_SUBSCRIPTION_PLANS: String
```

Broadcast Action: Request a refresh of the billing relationship plans between a carrier and a specific subscriber.

Carrier apps are encouraged to implement this receiver, and the OS will provide an affordance to request a refresh. This affordance will only be shown when the carrier app is actively providing subscription plan information via `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList)`.

Contains `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String` to indicate which subscription the user is interested in.

Receivers should protect themselves by checking that the sender holds the `android.permission.MANAGE_SUBSCRIPTION_PLANS` permission.

 Value: "android.telephony.action.REFRESH_SUBSCRIPTION_PLANS"

### D2D_SHARING_ALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_SHARING_ALL: Int
```

Device status is shared whenever possible.

 Value: 3

### D2D_SHARING_ALL_CONTACTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_SHARING_ALL_CONTACTS: Int
```

Device status is shared with all numbers in the user's contacts.

 Value: 1

### D2D_SHARING_DISABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_SHARING_DISABLED: Int
```

Device status is not shared to a remote party.

 Value: 0

### D2D_SHARING_SELECTED_CONTACTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_SHARING_SELECTED_CONTACTS: Int
```

Device status is shared with all selected contacts.

 Value: 2

### D2D_STATUS_SHARING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_STATUS_SHARING: String
```

TelephonyProvider column name for device to device sharing status.

Type: INTEGER (int)

 Value: "d2d_sharing_status"

### D2D_STATUS_SHARING_SELECTED_CONTACTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val D2D_STATUS_SHARING_SELECTED_CONTACTS: String
```

TelephonyProvider column name for contacts information that allow device to device sharing.

Type: TEXT (String)

 Value: "d2d_sharing_contacts"

### DATA_ROAMING_DISABLE

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ROAMING_DISABLE: Int
```

Indicates that data roaming is disabled for a subscription

 Value: 0

### DATA_ROAMING_ENABLE

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ROAMING_ENABLE: Int
```

Indicates that data roaming is enabled for a subscription

 Value: 1

### DEFAULT_SUBSCRIPTION_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_SUBSCRIPTION_ID: Int
```

Indicates the default subscription ID in Telephony.

 Value: 2147483647

### EXTRA_SLOT_INDEX

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SLOT_INDEX: String
```

Integer extra to specify SIM slot index.

 Value: "android.telephony.extra.SLOT_INDEX"

### EXTRA_SUBSCRIPTION_INDEX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUBSCRIPTION_INDEX: String
```

Integer extra used with `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SUBSCRIPTION_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#ACTION_DEFAULT_SMS_SUBSCRIPTION_CHANGED:kotlin.String` to indicate the subscription which has changed.

 Value: "android.telephony.extra.SUBSCRIPTION_INDEX"

### INVALID_SIM_SLOT_INDEX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_SIM_SLOT_INDEX: Int
```

Indicates invalid sim slot. This can be returned by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSlotIndex(kotlin.Int)`.

 Value: -1

### INVALID_SUBSCRIPTION_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_SUBSCRIPTION_ID: Int
```

An invalid subscription identifier

 Value: -1

### PHONE_NUMBER_SOURCE_CARRIER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_NUMBER_SOURCE_CARRIER: Int
```

A source of phone number: provided by an app that has carrier privilege.

The number is intended to be set by a carrier app knowing the correct number which is, for example, different from the number in `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` for some reason. The number is not available until a carrier app sets one via `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setCarrierPhoneNumber(kotlin.Int,%20kotlin.String)`. The app can update the number with the same API should the number change.

 Value: 2

### PHONE_NUMBER_SOURCE_IMS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_NUMBER_SOURCE_IMS: Int
```

A source of phone number: provided by IMS (IP Multimedia Subsystem) implementation. When IMS service is registered (as indicated by `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback#onRegistered(kotlin.Int)`) the IMS implementation may return P-Associated-Uri SIP headers (RFC 3455). The URIs are the user's public user identities known to the network (see 3GPP TS 24.229 5.4.1.2), and the phone number is typically one of them (see "global number" in 3GPP TS 23.003 13.4).

This source provides the phone number from the last IMS registration. IMS registration may happen on every device reboot or other network condition changes. The number will be updated should the associated URI change after an IMS registration.

 Value: 3

### PHONE_NUMBER_SOURCE_TS43

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_NUMBER_SOURCE_TS43: Int
```

A source of phone number: provided by the Entitlement Server using the GSMA TS.43 standard.

This source is used to retrieve the phone number (MSISDN) from the Entitlement Configuration Server as defined in GSMA TS.43.

Note: Access to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` is restricted to privileged system components (e.g., Settings) or carrier privileged apps.

 Value: 4

### PHONE_NUMBER_SOURCE_UICC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_NUMBER_SOURCE_UICC: Int
```

A source of phone number: the EF-MSISDN (see 3GPP TS 31.102), or EF-MDN for CDMA (see 3GPP2 C.P0065-B), from UICC application.

The availability and accuracy of the number depends on the carrier. The number may be updated by over-the-air update to UICC applications from the carrier, or by other means with physical access to the SIM.

 Value: 1

### SERVICE_CAPABILITY_DATA

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_CAPABILITY_DATA: Int
```

Represents a value indicating the data calling capabilities of a subscription.

 Value: 3

### SERVICE_CAPABILITY_SMS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_CAPABILITY_SMS: Int
```

Represents a value indicating the SMS capabilities of a subscription.

This value identifies whether the subscription supports various sms services. These services can include circuit-switched (CS) SMS, packet-switched (PS) IMS (IP Multimedia Subsystem) SMS, and over-the-top (OTT) SMS options.

Note: The availability of emergency SMS services is not solely dependent on this sms capability. Emergency services may be accessible even if the subscription lacks standard sms capabilities. However, the device's ability to support emergency sms can be influenced by its inherent sms capabilities, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceSmsCapable()`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceSmsCapable()`

### SERVICE_CAPABILITY_VOICE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_CAPABILITY_VOICE: Int
```

Represents a value indicating the voice calling capabilities of a subscription.

This value identifies whether the subscription supports various voice calling services. These services can include circuit-switched (CS) calling, packet-switched (PS) IMS (IP Multimedia Subsystem) calling, and over-the-top (OTT) calling options.

Note: The availability of emergency calling services is not solely dependent on this voice capability. Emergency services may be accessible even if the subscription lacks standard voice capabilities. However, the device's ability to support emergency calls can be influenced by its inherent voice capabilities, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceVoiceCapable()`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isDeviceVoiceCapable()`

### SUBSCRIPTION_TYPE_LOCAL_SIM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBSCRIPTION_TYPE_LOCAL_SIM: Int
```

This constant is to designate a subscription as a Local-SIM Subscription.

A Local-SIM can be a physical SIM inserted into a sim-slot in the device, or eSIM on the device.

 Value: 0

### SUBSCRIPTION_TYPE_REMOTE_SIM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBSCRIPTION_TYPE_REMOTE_SIM: Int
```

This constant is to designate a subscription as a Remote-SIM Subscription.

A Remote-SIM subscription is for a SIM on a phone connected to this device via some connectivity mechanism, for example bluetooth. Similar to Local SIM, this subscription can be used for SMS, Voice and data by proxying data through the connected device. Certain data of the SIM, such as IMEI, are not accessible for Remote SIMs.

A Remote-SIM is available only as long the phone stays connected to this device. When the phone disconnects, Remote-SIM subscription is removed from this device and is no longer known. All data associated with the subscription, such as stored SMS, call logs, contacts etc, are removed from this device.

If the phone re-connects to this device, a new Remote-SIM subscription is created for the phone. The Subscription Id associated with the new subscription is different from the Subscription Id of the previous Remote-SIM subscription created (and removed) for the phone; i.e., new Remote-SIM subscription treats the reconnected phone as a Remote-SIM that was never seen before.

 Value: 1

### USAGE_SETTING_DATA_CENTRIC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SETTING_DATA_CENTRIC: Int
```

This subscription is forced to data-centric mode

Refer to data-centric mode in 3gpp 24.301 sec 4.3 and 3gpp 24.501 sec 4.3. Also refer to "UE's usage setting" as defined in 3gpp 24.301 section 3.1 and 3gpp 23.221 Annex A.

Devices that support `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` and support usage setting configuration must support setting this value via. `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CELLULAR_USAGE_SETTING_INT:kotlin.String`.

 Value: 2

### USAGE_SETTING_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SETTING_DEFAULT: Int
```

Subscription uses the default setting. The value is based upon device capability and the other properties of the subscription. Most subscriptions will default to voice-centric when in a phone. An opportunistic subscription will default to data-centric.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#isOpportunistic()`

### USAGE_SETTING_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SETTING_UNKNOWN: Int
```

The usage setting is unknown. This will be the usage setting returned on devices that do not support querying the or setting the usage setting. It may also be provided by a carrier that wishes to provide a value to avoid making any settings changes.

 Value: -1

### USAGE_SETTING_VOICE_CENTRIC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SETTING_VOICE_CENTRIC: Int
```

This subscription is forced to voice-centric mode

Refer to voice-centric mode in 3gpp 24.301 sec 4.3 and 3gpp 24.501 sec 4.3. Also refer to "UE's usage setting" as defined in 3gpp 24.301 section 3.1 and 3gpp 23.221 Annex A.

Devices that support `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` and support usage setting configuration must support setting this value via `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CELLULAR_USAGE_SETTING_INT:kotlin.String`.

 Value: 1

## Public methods

### addOnOpportunisticSubscriptionsChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnOpportunisticSubscriptionsChangedListener(
    executor: Executor, 
    listener: SubscriptionManager.OnOpportunisticSubscriptionsChangedListener
): Unit
```

Register for changes to the list of opportunistic subscription records or to the individual records themselves. When a change occurs the onOpportunisticSubscriptionsChanged method of the listener will be invoked immediately if there has been a notification.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SubscriptionManager.OnOpportunisticSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener): an instance of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener` with onOpportunisticSubscriptionsChanged overridden. This value cannot be `null`. |

### addOnSubscriptionsChangedListener

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnSubscriptionsChangedListener(listener: SubscriptionManager.OnSubscriptionsChangedListener!): Unit
```

**Deprecated:** *Will get exception if the parameter listener is not initialized with a Looper. Use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#addOnSubscriptionsChangedListener(java.util.concurrent.Executor,%20android.telephony.SubscriptionManager.OnSubscriptionsChangedListener)`.*

Register for changes to the list of active `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records or to the individual records themselves. When a change occurs the onSubscriptionsChanged method of the listener will be invoked immediately if there has been a notification. The onSubscriptionChanged method will also be triggered once initially when calling this function. The callback will be invoked on the looper specified in the listener's constructor.

| Parameters ||
|---|---|
| `listener` | [SubscriptionManager.OnSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener)!: an instance of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener` with onSubscriptionsChanged overridden. |

### addOnSubscriptionsChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnSubscriptionsChangedListener(
    executor: Executor, 
    listener: SubscriptionManager.OnSubscriptionsChangedListener
): Unit
```

Register for changes to the list of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records or to the individual records (active or inactive) themselves. When a change occurs, the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener#onSubscriptionsChanged()` method of the listener will be invoked immediately. The `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener#onSubscriptionsChanged()` method will also be invoked once initially when calling this method.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor that will execute callbacks. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SubscriptionManager.OnSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener): an instance of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener` with `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener#onSubscriptionsChanged()` overridden. This value cannot be `null`. |

### addSubscriptionsIntoGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addSubscriptionsIntoGroup(
    subIdList: MutableList<Int!>, 
    groupUuid: ParcelUuid
): Unit
```

Add a list of subscriptions into a group. See `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#createSubscriptionGroup(kotlin.collections.MutableList)` for more details. Caller will either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` permission or had carrier privilege permission on the subscriptions: `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()` or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#canManageSubscription(android.telephony.SubscriptionInfo)` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subIdList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: list of subId that need adding into the group. This value cannot be `null`. |
| `groupUuid` | [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#): the groupUuid the subscriptions are being added to. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the some subscriptions in the list doesn't exist. |
| `java.lang.IllegalStateException` | if Telephony service is in bad state. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### canManageSubscription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canManageSubscription(info: SubscriptionInfo!): Boolean
```

Checks whether the app with the given context is authorized to manage the given subscription according to its metadata. Only supported for embedded subscriptions (if `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#isEmbedded()` returns true). To check for permissions for non-embedded subscription as well, see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.

| Parameters ||
|---|---|
| `info` | [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo)!: The subscription to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the app is authorized to manage this subscription per its metadata. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

### createSubscriptionGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createSubscriptionGroup(subIdList: MutableList<Int!>): ParcelUuid
```

Inform SubscriptionManager that subscriptions in the list are bundled as a group. It can be multiple primary (non-opportunistic) subscriptions, or one or more primary plus one or more opportunistic subscriptions. This API will always create a new immutable group and assign group UUID to all the subscriptions, regardless whether they are in a group already or not. Grouped subscriptions will have below behaviors: 1) They will share the same user settings. 2) The opportunistic subscriptions in the group is considered invisible and will not return from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoList()`, unless caller has carrier privilege permission of the subscriptions. 3) The opportunistic subscriptions in the group can't be active by itself. If all other non-opportunistic ones are deactivated (unplugged or disabled in Settings), the opportunistic ones will be deactivated automatically. Caller will either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` permission or had carrier privilege permission on the subscriptions: `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()` or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#canManageSubscription(android.telephony.SubscriptionInfo)` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subIdList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: list of subId that will be in the same group. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` | groupUUID a UUID assigned to the subscription group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any of the subscriptions in the list doesn't exist. |
| `java.lang.IllegalStateException` | if Telephony service is in bad state. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### from

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun from(context: Context!): SubscriptionManager!
```

**Deprecated:** *developers should always obtain references directly from `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(java.lang.Class)`.*

### getAccessibleSubscriptionInfoList

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAccessibleSubscriptionInfoList(): MutableList<SubscriptionInfo!>?
```

Gets the SubscriptionInfo(s) of all embedded subscriptions accessible to the calling app, if any.

Only those subscriptions for which the calling app has carrier privileges per the subscription metadata, if any, will be included in the returned list.

The records will be sorted by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSimSlotIndex()` then by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSubscriptionId()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>?` | Sorted list of the current embedded `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records available on the device which are accessible to the caller. - If null is returned the current state is unknown but if a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener` has been registered `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener#onSubscriptionsChanged()` will be invoked in the future. - If the list is empty then there are no `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records currently available. - if the list is non-empty the list is sorted by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSimSlotIndex()` then by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSubscriptionId()`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### getActiveDataSubscriptionId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getActiveDataSubscriptionId(): Int
```

Get active data subscription id. Active data subscription refers to the subscription currently chosen to provide cellular internet connection to the user. This may be different from `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultDataSubscriptionId()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Active data subscription id if any is chosen, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` if not. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener`

### getActiveSubscriptionInfo

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveSubscriptionInfo(subId: Int): SubscriptionInfo!
```

Get the active SubscriptionInfo with the input subId.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique SubscriptionInfo key in database. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!` | SubscriptionInfo, maybe null if its not active. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getActiveSubscriptionInfoCount

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveSubscriptionInfoCount(): Int
```

Get the active subscription count. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current number of active subscriptions. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoList()`

### getActiveSubscriptionInfoCountMax

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveSubscriptionInfoCountMax(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of active subscriptions that will be returned by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoList()` and the value returned by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoCount()`. |

### getActiveSubscriptionInfoForSimSlotIndex

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveSubscriptionInfoForSimSlotIndex(slotIndex: Int): SubscriptionInfo!
```

Get the active SubscriptionInfo associated with the slotIndex

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the slot which the subscription is inserted |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!` | SubscriptionInfo, maybe null if its not active |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getActiveSubscriptionInfoList

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveSubscriptionInfoList(): MutableList<SubscriptionInfo!>?
```

Get the SubscriptionInfo(s) of the currently active SIM(s).

Returned records will be sorted by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSimSlotIndex()` then by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSubscriptionId()`. Beginning with Android SDK 35, this method will never return null.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>?` | a list of the active `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` that is visible to the caller. If an empty list or null is returned, then there are no active subscriptions that are visible to the caller. If the number of active subscriptions available to any caller changes, then this change will be indicated by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener#onSubscriptionsChanged()`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getAllSubscriptionInfoList

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllSubscriptionInfoList(): MutableList<SubscriptionInfo!>
```

Get all subscription info records from SIMs that are inserted now or previously inserted.

If the caller does not have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String` permission, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getNumber()` will return empty string. If the caller does not have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_ICC_AUTH_WITH_DEVICE_IDENTIFIER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getIccId()` will return an empty string, and `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getGroupUuid()` will return `null`.

The carrier app will only get the list of subscriptions that it has carrier privilege on, but will have non-stripped `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` in the list. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>` | List of all `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records from SIMs that are inserted or previously inserted. Sorted by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSimSlotIndex()`, then `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSubscriptionId()`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if callers do not hold the required permission. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getCompleteActiveSubscriptionInfoList

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCompleteActiveSubscriptionInfoList(): MutableList<SubscriptionInfo!>
```

Get both hidden and visible SubscriptionInfo(s) of the currently active SIM(s). The records will be sorted by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSimSlotIndex()` then by `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo#getSubscriptionId()`. Hidden subscriptions refer to those are not meant visible to the users. For example, an opportunistic subscription that is grouped with other subscriptions should remain invisible to users as they are only functionally supplementary to primary ones.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). In the latter case, only records accessible to the calling app are returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>` | Sorted list of the currently available `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo` records on the device. This is similar to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getActiveSubscriptionInfoList()` except that it will return both active and hidden SubscriptionInfos. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getDefaultDataSubscriptionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultDataSubscriptionId(): Int
```

Returns the system's default data subscription id. On a voice only device or on error, will return INVALID_SUBSCRIPTION_ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the default data subscription Id. |

### getDefaultSmsSubscriptionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultSmsSubscriptionId(): Int
```

Returns the system's default SMS subscription id. On a data only device or on error, will return INVALID_SUBSCRIPTION_ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the default SMS subscription Id. |

### getDefaultSubscriptionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultSubscriptionId(): Int
```

Returns the system's default subscription id. For a voice capable device, it will return getDefaultVoiceSubscriptionId. For a data only device, it will return the getDefaultDataSubscriptionId. May return an INVALID_SUBSCRIPTION_ID on error.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the "system" default subscription id. |

### getDefaultVoiceSubscriptionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultVoiceSubscriptionId(): Int
```

Returns the system's default voice subscription id. On a data only device or on error, will return INVALID_SUBSCRIPTION_ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the default voice subscription Id. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getDeviceToDeviceStatusSharingContacts

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceToDeviceStatusSharingContacts(subscriptionId: Int): MutableList<Uri!>
```

Get the list of contacts that allow device to device status sharing.

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Subscription id. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | The list of contacts that allow device to device status sharing. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getDeviceToDeviceStatusSharingPreference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceToDeviceStatusSharingPreference(subscriptionId: Int): Int
```

Returns the user-chosen device to device status sharing preference

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Subscription id of subscription |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The device to device status sharing preference. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL_CONTACTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_SELECTED_CONTACTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getOpportunisticSubscriptions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpportunisticSubscriptions(): MutableList<SubscriptionInfo!>
```

Return opportunistic subscriptions that can be visible to the caller. Opportunistic subscriptions are for opportunistic networks, which are cellular networks with limited capabilities and coverage, for example, CBRS.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>` | the list of opportunistic subscription info. If none exists, an empty list. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getPhoneNumber

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneNumber(subscriptionId: Int): String
```

Returns the phone number for the given `subId`, or an empty string if not available.

This API is suitable for general apps that needs to know the phone number. For specific apps that needs to know the phone number provided by a specific source, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int,%20kotlin.Int)` may be suitable.

This API is built up on `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int,%20kotlin.Int)`, but picks from available sources in the following order: `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_IMS:kotlin.Int`.

The API provides no guarantees of what format the number is in: the format can vary depending on the underlying source and the network etc. Programmatic parsing should be done cautiously, for example, after formatting the number to a consistent format with `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumberToE164(kotlin.String,%20kotlin.String)`.

The availability and correctness of the phone number depends on the underlying source and the network etc. Additional verification is needed to use this number for security-related or other sensitive scenarios.

Note:Access to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` is restricted to privileged system components (e.g., Settings) or carrier privileged apps. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` for the default one. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the phone number, or an empty string if not available. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the telephony process is not currently available. |
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int,%20kotlin.Int)`

### getPhoneNumber

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneNumber(
    subscriptionId: Int, 
    source: Int
): String
```

Returns the phone number for the given `subscriptionId` and `source`, or an empty string if not available.

General apps that need to know the phone number should use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getPhoneNumber(kotlin.Int)` instead. This API may be suitable specific apps that needs to know the phone number from a specific source. For example, a carrier app needs to know exactly what's on `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` and decide if the previously set phone number of source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int` should be updated.

The API provides no guarantees of what format the number is in: the format can vary depending on the `source` and the network etc. Programmatic parsing should be done cautiously, for example, after formatting the number to a consistent format with `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumberToE164(kotlin.String,%20kotlin.String)`.

Note the assumption is that one subscription (which usually means one SIM) has only one phone number. The multiple sources backup each other so hopefully at least one is available. For example, for a carrier that doesn't typically set phone numbers on `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int`, the source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_IMS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` may provide one. Or, a carrier may decide to provide the phone number via source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int` if none of the other sources are available.

The availability and correctness of the phone number depends on the underlying source and the network etc. Additional verification is needed to use this number for security-related or other sensitive scenarios.

Note:Access to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` is restricted to privileged system components (e.g., Settings) or carrier privileged apps. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` for the default one. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the source of the phone number, one of the PHONE_NUMBER_SOURCE_\* constants. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_IMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the phone number, or an empty string if not available. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `source` is invalid. |
| `java.lang.IllegalStateException` | if the telephony process is not currently available. |
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_IMS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int`

### getSlotIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSlotIndex(subscriptionId: Int): Int
```

Get slotIndex associated with the subscription.

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the unique SubscriptionInfo index in database |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | slotIndex as a positive integer or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SIM_SLOT_INDEX:kotlin.Int` if the supplied subscriptionId doesn't have an associated slot index. |

### getSubscriptionId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSubscriptionId(slotIndex: Int): Int
```

Get the subscription id for specified logical SIM slot index.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The logical SIM slot index. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The subscription id. `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` if SIM is absent. If slotIndex is #SLOT_INDEX_FOR_REMOTE_SIM_SUB, the last inserted remote SIM subscription id will be returned. |

### getSubscriptionIds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriptionIds(slotIndex: Int): IntArray?
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getSubscriptionId(kotlin.Int)` instead.*

Get an array of subscription ids for the specified logical SIM slot Index. The maximum size of the array is 1. This API was mistakenly designed to return multiple subscription ids, which is not possible in the current Android telephony architecture.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The logical SIM slot index. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | Subscription id of the active subscription on the specified logical SIM slot index. If SIM is absent on the slot, a single element array of `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` will be returned. `null` if the provided `slotIndex` is not valid. |

### getSubscriptionPlans

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriptionPlans(subId: Int): MutableList<SubscriptionPlan!>
```

Get the description of the billing relationship plan between a carrier and a specific subscriber.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this relationship applies to |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### getSubscriptionsInGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriptionsInGroup(groupUuid: ParcelUuid): MutableList<SubscriptionInfo!>
```

Get subscriptionInfo list of subscriptions that are in the same group of given subId. Caller must have or carrier privilege permission on the subscription. `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

Starting with API level 33, the caller also needs permission to access device identifiers to get the list of subscriptions associated with a group UUID. This method can be invoked if one of the following requirements is met:

- If the app has carrier privilege permission. `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`
- If the app has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permission and access to device identifiers.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `groupUuid` | [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#): of which list of subInfo will be returned. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo!>` | list of subscriptionInfo that belong to the same group, including the given subscription itself. It will return an empty list if no subscription belongs to the group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if Telephony service is in bad state. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### isActiveSubscriptionId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isActiveSubscriptionId(subscriptionId: Int): Boolean
```

Checks if the supplied subscription ID corresponds to a subscription which is actively in use on the device. An active subscription ID is a valid and usable subscription ID. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the supplied subscription ID corresponds to an active subscription; `false` if it does not correspond to an active subscription; or throw a SecurityException if the caller hasn't got the right permission. i |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### isNetworkRoaming

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNetworkRoaming(subId: Int): Boolean
```

Returns true if the device is considered roaming on the current network for a subscription.

Availability: Only when user registered to a network.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The subscription ID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the network for the subscription is roaming, false otherwise |

### isUsableSubscriptionId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isUsableSubscriptionId(subscriptionId: Int): Boolean
```

Check if the supplied subscription ID is usable.

A usable subscription ID is a valid subscription ID, but not necessarily an active subscription ID (see `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isActiveSubscriptionId(kotlin.Int)`). Some subscription APIs require a usable subscription ID, and this is noted in their documentation; otherwise, a subscription ID does not need to be usable for subscription functions, only valid.

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the subscription ID is usable; `false` otherwise. |

### isValidSubscriptionId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isValidSubscriptionId(subscriptionId: Int): Boolean
```

Check if the supplied subscription ID is valid.

A valid subscription ID is not necessarily an active subscription ID (see `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isActiveSubscriptionId(kotlin.Int)`) or an usable subscription ID (see `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#isUsableSubscriptionId(kotlin.Int)`). Unless specifically noted, subscription APIs work with a valid subscription ID.

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The subscription ID. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the supplied subscriptionId is valid; `false` otherwise. |

### removeOnOpportunisticSubscriptionsChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnOpportunisticSubscriptionsChangedListener(listener: SubscriptionManager.OnOpportunisticSubscriptionsChangedListener): Unit
```

Unregister the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener` that is currently listening opportunistic subscriptions change. This is not strictly necessary as the listener will automatically be unregistered if an attempt to invoke the listener fails.

| Parameters ||
|---|---|
| `listener` | [SubscriptionManager.OnOpportunisticSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnOpportunisticSubscriptionsChangedListener): that is to be unregistered. This value cannot be `null`. |

### removeOnSubscriptionsChangedListener

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnSubscriptionsChangedListener(listener: SubscriptionManager.OnSubscriptionsChangedListener!): Unit
```

Unregister the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener`. This is not strictly necessary as the listener will automatically be unregistered if an attempt to invoke the listener fails.

| Parameters ||
|---|---|
| `listener` | [SubscriptionManager.OnSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener)!: that is to be unregistered. |

### removeSubscriptionsFromGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeSubscriptionsFromGroup(
    subIdList: MutableList<Int!>, 
    groupUuid: ParcelUuid
): Unit
```

Remove a list of subscriptions from their subscription group. Caller will either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` permission or has carrier privilege permission on all of the subscriptions provided in `subIdList`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subIdList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: list of subId that need removing from their groups. This value cannot be `null`. |
| `groupUuid` | [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#): The UUID of the subscription group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the some subscriptions in the list doesn't belong the specified group. |
| `java.lang.IllegalStateException` | if Telephony service is in bad state. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#createSubscriptionGroup(kotlin.collections.MutableList)`

### setCarrierPhoneNumber

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCarrierPhoneNumber(
    subscriptionId: Int, 
    number: String
): Unit
```

Sets the phone number for the given `subId` for source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_CARRIER:kotlin.Int`. Sets an empty string to remove the previously set phone number.

The API is suitable for carrier apps to provide a phone number, for example when it's not possible to update `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_UICC:kotlin.Int` directly.

It's recommended that the phone number is formatted to well-known formats, for example, by `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils` `formatNumber*` methods. 
Requires `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` for the default one. |
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the phone number, or an empty string to remove the previously set number. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the telephony process is not currently available. |
| `java.lang.NullPointerException` | if `number` is `null`. |
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setDeviceToDeviceStatusSharingContacts

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDeviceToDeviceStatusSharingContacts(
    subscriptionId: Int, 
    contacts: MutableList<Uri!>
): Unit
```

Set the list of contacts that allow device to device status sharing for a subscription id. The setting app uses this method to indicate with whom they wish to share device to device status information. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The subscription id. |
| `contacts` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The list of contacts that allow device to device status sharing. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setDeviceToDeviceStatusSharingPreference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDeviceToDeviceStatusSharingPreference(
    subscriptionId: Int, 
    sharing: Int
): Unit
```

Set the device to device status sharing user preference for a subscription id. The setting app uses this method to indicate with whom they wish to share device to device status information. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The subscription id. |
| `sharing` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The status sharing preference. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL_CONTACTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_SELECTED_CONTACTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#D2D_SHARING_ALL:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setOpportunistic

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOpportunistic(
    opportunistic: Boolean, 
    subId: Int
): Boolean
```

Set whether a subscription is opportunistic, that is, whether the network it connects to has limited coverage. For example, CBRS. Setting a subscription opportunistic has following impacts: 1) Even if it's active, it will be dormant most of the time. The modem will not try to scan or camp until it knows an available network is nearby to save power. 2) Telephony relies on system app or carrier input to notify nearby available networks. See `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#updateAvailableNetworks(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` for more information. 3) In multi-SIM devices, when the network is nearby and camped, system may automatically switch internet data between it and default data subscription, based on carrier recommendation and its signal strength and metered-ness, etc. Caller will either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or carrier privilege permission of the subscription. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `opportunistic` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether it's an opportunistic subscription. |
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the unique SubscriptionInfo index in database |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation is succeed, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setSubscriptionOverrideCongested

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionOverrideCongested(
    subId: Int, 
    overrideCongested: Boolean, 
    networkTypes: IntArray, 
    expirationDurationMillis: Long
): Unit
```

Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered congested. This will cause the device to delay certain network requests when possible, such as developer jobs that are willing to run in a flexible time window.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this override applies to. |
| `overrideCongested` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set if the subscription should be considered congested. |
| `networkTypes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the network types this override applies to. If no network types are specified, override values will be ignored. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |
| `expirationDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration after which the requested override will be automatically cleared, or `0` to leave in the requested state until explicitly cleared, or the next reboot, whichever happens first. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setSubscriptionOverrideCongested

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionOverrideCongested(
    subId: Int, 
    overrideCongested: Boolean, 
    expirationDurationMillis: Long
): Unit
```

Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered congested. This will cause the device to delay certain network requests when possible, such as developer jobs that are willing to run in a flexible time window.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this override applies to. |
| `overrideCongested` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set if the subscription should be considered congested. |
| `expirationDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration after which the requested override will be automatically cleared, or `0` to leave in the requested state until explicitly cleared, or the next reboot, whichever happens first. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setSubscriptionOverrideUnmetered

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionOverrideUnmetered(
    subId: Int, 
    overrideUnmetered: Boolean, 
    networkTypes: IntArray, 
    expirationDurationMillis: Long
): Unit
```

Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered unmetered. This will be reflected to apps via `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_METERED:kotlin.Int`.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this override applies to. |
| `overrideUnmetered` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set if the billing relationship should be considered unmetered. |
| `networkTypes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the network types this override applies to. If no network types are specified, override values will be ignored. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |
| `expirationDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration after which the requested override will be automatically cleared, or `0` to leave in the requested state until explicitly cleared, or the next reboot, whichever happens first. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setSubscriptionOverrideUnmetered

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionOverrideUnmetered(
    subId: Int, 
    overrideUnmetered: Boolean, 
    expirationDurationMillis: Long
): Unit
```

Temporarily override the billing relationship plan between a carrier and a specific subscriber to be considered unmetered. This will be reflected to apps via `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_METERED:kotlin.Int`.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this override applies to. |
| `overrideUnmetered` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set if the billing relationship should be considered unmetered. |
| `expirationDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration after which the requested override will be automatically cleared, or `0` to leave in the requested state until explicitly cleared, or the next reboot, whichever happens first. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setSubscriptionPlans

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionPlans(
    subId: Int, 
    plans: MutableList<SubscriptionPlan!>
): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#setSubscriptionPlans(kotlin.Int,%20kotlin.collections.MutableList,%20kotlin.Long)` instead.*

Set the description of the billing relationship plan between a carrier and a specific subscriber.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this relationship applies to. An empty list may be sent to clear any existing plans. |
| `plans` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan)!\>: the list of plans. The first plan is always the primary and most important plan. Any additional plans are secondary and may not be displayed or used by decision making logic. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if plans don't meet the requirements defined in `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan`. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setSubscriptionPlans

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubscriptionPlans(
    subId: Int, 
    plans: MutableList<SubscriptionPlan!>, 
    expirationDurationMillis: Long
): Unit
```

Set the description of the billing relationship plan between a carrier and a specific subscriber.

This method is only accessible to the following narrow set of apps:

- The carrier app for this subscriberId, as determined by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`.
- The carrier app explicitly delegated access through `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_PLANS_PACKAGE_OVERRIDE_STRING:kotlin.String`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscriber this relationship applies to. An empty list may be sent to clear any existing plans. |
| `plans` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan)!\>: the list of plans. The first plan is always the primary and most important plan. Any additional plans are secondary and may not be displayed or used by decision making logic. This value cannot be `null`. |
| `expirationDurationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the duration after which the subscription plans will be automatically cleared, or `0` to leave the plans until explicitly cleared, or the next reboot, whichever happens first. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if plans don't meet the requirements defined in `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan`. |
| `java.lang.SecurityException` | if the caller doesn't meet the requirements outlined above. |

### setTs43PhoneNumber

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTs43PhoneNumber(
    subscriptionId: Int, 
    number: String
): Unit
```

Sets the phone number for the given `subId` for source `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#PHONE_NUMBER_SOURCE_TS43:kotlin.Int`. Sets an empty string to remove the previously set phone number.

It's recommended that the phone number is formatted to well-known formats, for example, by `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils` `formatNumber*` methods. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the subscription ID, or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` for the default one. |
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the phone number, or an empty string to remove the previously set number. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the telephony process is not currently available. |
| `java.lang.NullPointerException` | if `number` is `null`. |
| `java.lang.SecurityException` | if the caller doesn't have permissions required. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### switchToSubscription

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchToSubscription(
    subId: Int, 
    callbackIntent: PendingIntent
): Unit
```

**Deprecated:** *this API is a duplicate of `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20android.app.PendingIntent)` and does not support Multiple Enabled Profile(MEP). Apps should use `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20android.app.PendingIntent)` or `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager#switchToSubscription(kotlin.Int,%20kotlin.Int,%20android.app.PendingIntent)` instead.*

Switch to a certain subscription. 
Requires android.Manifest.permission.WRITE_EMBEDDED_SUBSCRIPTIONS. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): sub id |
| `callbackIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#): pending intent that will be sent after operation is done. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |
