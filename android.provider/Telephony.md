# Telephony

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Telephony

Kotlin| [Java](https://developer.android.com/reference/android/provider/Telephony "View this page in Java") 
| --- | --- |

```
class Telephony
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.Telephony](https://developer.android.com/reference/kotlin/android/provider/Telephony#) |

The Telephony provider contains data related to phone operation, specifically SMS and MMS messages, access to the APN list, including the MMSC to use, and the service state.

**Note:** These APIs are not available on all Android-powered devices. If your app depends on telephony features such as for managing SMS messages, include a [`<uses-feature>`](https://developer.android.com/guide/topics/manifest/uses-feature-element.html) element in your manifest that declares the`"android.hardware.telephony"`hardware feature. Alternatively, you can check for telephony availability at runtime using either android.content.pm.PackageManager#hasSystemFeature.

### Creating an SMS app

Only the default SMS app (selected by the user in system settings) is able to write to the SMS Provider (the tables defined within the`Telephony`class) and only the default SMS app receives the [android.provider.Telephony.Sms.Intents#SMS_DELIVER_ACTION](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents#SMS_DELIVER_ACTION:kotlin.String) broadcast when the user receives an SMS or the [android.provider.Telephony.Sms.Intents#WAP_PUSH_DELIVER_ACTION](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents#WAP_PUSH_DELIVER_ACTION:kotlin.String) broadcast when the user receives an MMS.

Any app that wants to behave as the user's default SMS app must handle the following intents:

- In a broadcast receiver, include an intent filter for [Sms.Intents#SMS_DELIVER_ACTION](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents#SMS_DELIVER_ACTION:kotlin.String)(`"android.provider.Telephony.SMS_DELIVER"`). The broadcast receiver must also require the [android.Manifest.permission#BROADCAST_SMS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_SMS:kotlin.String) permission.

 This allows your app to directly receive incoming SMS messages.
- In a broadcast receiver, include an intent filter for [Sms.Intents#WAP_PUSH_DELIVER_ACTION](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents#WAP_PUSH_DELIVER_ACTION:kotlin.String)} (`"android.provider.Telephony.WAP_PUSH_DELIVER"`) with the MIME type`"application/vnd.wap.mms-message"`. The broadcast receiver must also require the [android.Manifest.permission#BROADCAST_WAP_PUSH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_WAP_PUSH:kotlin.String) permission.

 This allows your app to directly receive incoming MMS messages.
- In your activity that delivers new messages, include an intent filter for [android.content.Intent#ACTION_SENDTO](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SENDTO:kotlin.String)(`"android.intent.action.SENDTO" `) with schemas,`sms:`,`smsto:`,`mms:`, and`mmsto:`.

 This allows your app to receive intents from other apps that want to deliver a message.
- In a service, include an intent filter for [android.telephony.TelephonyManager#ACTION_RESPOND_VIA_MESSAGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#ACTION_RESPOND_VIA_MESSAGE:kotlin.String)(`"android.intent.action.RESPOND_VIA_MESSAGE"`) with schemas,`sms:`,`smsto:`,`mms:`, and`mmsto:`. This service must also require the [android.Manifest.permission#SEND_RESPOND_VIA_MESSAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_RESPOND_VIA_MESSAGE:kotlin.String) permission.

 This allows users to respond to incoming phone calls with an immediate text message using your app.

Other apps that are not selected as the default SMS app can only*read* the SMS Provider, but may also be notified when a new SMS arrives by listening for the [Sms.Intents#SMS_RECEIVED_ACTION](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents#SMS_RECEIVED_ACTION:kotlin.String) broadcast, which is a non-abortable broadcast that may be delivered to multiple apps. This broadcast is intended for apps that---while not selected as the default SMS app---need to read special incoming messages such as to perform phone number verification.

For more information about building SMS apps, read the blog post, [Getting Your SMS Apps Ready for KitKat](http://android-developers.blogspot.com/2013/10/getting-your-sms-apps-ready-for-kitkat.html).

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BaseMmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns) Base columns for tables that contain MMSs. |
| abstract | [CanonicalAddressesColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.CanonicalAddressesColumns) Columns for the "canonical_addresses" table used by MMS and SMS. |
| | [CarrierId](https://developer.android.com/reference/kotlin/android/provider/Telephony.CarrierId) Contains carrier identification information for the current subscriptions. |
| --- | --- |
| | [Carriers](https://developer.android.com/reference/kotlin/android/provider/Telephony.Carriers) Carriers class contains information about APNs, including MMSC information. |
| | [Mms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms) Contains all MMS messages. |
| | [MmsSms](https://developer.android.com/reference/kotlin/android/provider/Telephony.MmsSms) Contains all MMS and SMS messages. |
| --- | --- |
| | [ServiceStateTable](https://developer.android.com/reference/kotlin/android/provider/Telephony.ServiceStateTable) Constants for interfacing with the ServiceStateProvider and the different fields of the [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState.html#) class accessible through the provider. |
| | [Sms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms) Contains all text-based SMS messages. |
| abstract | [TextBasedSmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns) Base columns for tables that contain text-based SMSs. |
| --- | --- |
| | [Threads](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads) Helper functions for the "threads" table used by MMS and SMS. |
| abstract | [ThreadsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns) Columns for the "threads" table used by MMS and SMS. |
