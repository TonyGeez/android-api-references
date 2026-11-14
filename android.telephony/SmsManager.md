Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SmsManager

```
class SmsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SmsManager](SmsManager.md) |

Manages SMS operations such as sending data, text, and pdu SMS messages. Get this object by calling the static method getDefault. To create an instance of SmsManager associated with a specific subscription ID, call getSmsManagerForSubscriptionId. This is typically used for devices that support multiple active subscriptions at once.

For information about how to behave as the default SMS app on Android 4.4 (API level 19) and higher, see `https://developer.android.com/reference/kotlin/android/provider/Telephony.html#`. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager.FinancialSmsCallback` callback for providing asynchronous sms messages for financial app. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#EXTRA_MMS_DATA:kotlin.String` Intent extra name for MMS sending result data in byte array type |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#EXTRA_MMS_HTTP_STATUS:kotlin.String` Intent extra name for HTTP status code for MMS HTTP failure in integer type |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_ALIAS_ENABLED:kotlin.String` Whether alias is enabled (boolean type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_ALIAS_MAX_CHARS:kotlin.String` Max alias character count (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_ALIAS_MIN_CHARS:kotlin.String` Min alias character count (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_ALLOW_ATTACH_AUDIO:kotlin.String` Whether audio is allowed to be attached for MMS messages (boolean type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_APPEND_TRANSACTION_ID:kotlin.String` Whether to append transaction id to MMS WAP Push M-Notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_EMAIL_GATEWAY_NUMBER:kotlin.String` Email gateway number (String type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_GROUP_MMS_ENABLED:kotlin.String` Whether group MMS is enabled for the current carrier (boolean type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_HTTP_PARAMS:kotlin.String` A list of HTTP headers to add to MMS HTTP request, separated by "|" (String type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_HTTP_SOCKET_TIMEOUT:kotlin.String` MMS HTTP socket timeout in milliseconds (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MAX_IMAGE_HEIGHT:kotlin.String` Max MMS image height (int type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MAX_IMAGE_WIDTH:kotlin.String` Max MMS image width (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MAX_MESSAGE_SIZE:kotlin.String` Max MMS message size in bytes (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MESSAGE_TEXT_MAX_SIZE:kotlin.String` Max message text size (int type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MMS_DELIVERY_REPORT_ENABLED:kotlin.String` Whether MMS delivery report is enabled (boolean type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MMS_ENABLED:kotlin.String` Whether MMS is enabled for the current carrier (boolean type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MMS_READ_REPORT_ENABLED:kotlin.String` Whether MMS read report is enabled (boolean type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_MULTIPART_SMS_ENABLED:kotlin.String` Whether multipart SMS is enabled (boolean type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_NAI_SUFFIX:kotlin.String` The suffix to append to the NAI header value for MMS HTTP request (String type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_NOTIFY_WAP_MMSC_ENABLED:kotlin.String` If this is enabled, M-NotifyResp. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_RECIPIENT_LIMIT:kotlin.String` Limit of recipients of MMS messages (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES:kotlin.String` Whether multipart SMS should be sent as separate messages |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SHOW_CELL_BROADCAST_APP_LINKS:kotlin.String` If true, show the cell broadcast (amber alert) in the SMS settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SMS_DELIVERY_REPORT_ENABLED:kotlin.String` Whether SMS delivery report is enabled (boolean type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD:kotlin.String` Some carriers require SMS to be converted into MMS when text length reaches this threshold (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SMS_TO_MMS_TEXT_THRESHOLD:kotlin.String` When the number of parts of a multipart SMS reaches this threshold, it should be converted into an MMS (int type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SUBJECT_MAX_LENGTH:kotlin.String` Max message subject length (int type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SUPPORT_HTTP_CHARSET_HEADER:kotlin.String` Whether the carrier MMSC supports charset field in Content-Type header. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_SUPPORT_MMS_CONTENT_DISPOSITION:kotlin.String` Whether content-disposition field should be expected in an MMS PDU (boolean type) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_UA_PROF_TAG_NAME:kotlin.String` The name of the UA Prof URL HTTP header for MMS HTTP request (String type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_UA_PROF_URL:kotlin.String` The UA Profile URL header value for MMS HTTP request (String type) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_CONFIG_USER_AGENT:kotlin.String` The User-Agent header value for MMS HTTP request (String type) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_CONFIGURATION_ERROR:kotlin.Int` The carrier-dependent configuration values could not be loaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_DATA_DISABLED:kotlin.Int` Data is disabled for the MMS APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_HTTP_FAILURE:kotlin.Int` An error occurred during the HTTP client setup. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_INACTIVE_SUBSCRIPTION:kotlin.Int` The subscription id for the send/download is inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_INVALID_APN:kotlin.Int` ApnException occurred during MMS network setup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_INVALID_SUBSCRIPTION_ID:kotlin.Int` The subscription id for the send/download is invalid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_IO_ERROR:kotlin.Int` An I/O error occurred reading the PDU. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_MMS_DISABLED_BY_CARRIER:kotlin.Int` MMS is disabled by a carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_NO_DATA_NETWORK:kotlin.Int` There is neither Wi-Fi nor mobile data network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_RETRY:kotlin.Int` An error occurred while retrying sending/downloading the MMS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_UNABLE_CONNECT_MMS:kotlin.Int` An error occurred during the MMS connection setup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#MMS_ERROR_UNSPECIFIED:kotlin.Int` Unspecific MMS error occurred during send/download. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_BLUETOOTH_DISCONNECTED:kotlin.Int` Failed sending via bluetooth because bluetooth disconnected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_CANCELLED:kotlin.Int` Failed because the operation was cancelled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ENCODING_ERROR:kotlin.Int` Failed because of an encoding error |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_FDN_CHECK_FAILURE:kotlin.Int` Failed because FDN is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_GENERIC_FAILURE:kotlin.Int` Generic failure cause |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_LIMIT_EXCEEDED:kotlin.Int` Failed because we reached the sending queue limit. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_NONE:kotlin.Int` No error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_NO_SERVICE:kotlin.Int` Failed because service is currently unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_NULL_PDU:kotlin.Int` Failed because no pdu provided |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_RADIO_OFF:kotlin.Int` Failed because radio was explicitly turned off |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED:kotlin.Int` Failed because the user has denied this app ever send premium short codes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_ERROR_SHORT_CODE_NOT_ALLOWED:kotlin.Int` Failed because user denied the sending of this short code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INTERNAL_ERROR:kotlin.Int` Failed because of an internal error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INVALID_ARGUMENTS:kotlin.Int` Failed because of invalid arguments |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INVALID_BLUETOOTH_ADDRESS:kotlin.Int` Failed sending via bluetooth because the bluetooth device address is invalid |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INVALID_SMSC_ADDRESS:kotlin.Int` Failed because of an invalid smsc address |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INVALID_SMS_FORMAT:kotlin.Int` Failed because the sms format is not valid |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_INVALID_STATE:kotlin.Int` Failed because of an invalid state |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_MODEM_ERROR:kotlin.Int` Failed because of a modem error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NETWORK_ERROR:kotlin.Int` Failed because of a network error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NETWORK_REJECT:kotlin.Int` Failed because of network rejection |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NO_BLUETOOTH_SERVICE:kotlin.Int` Failed sending via bluetooth because the bluetooth service is not available |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NO_DEFAULT_SMS_APP:kotlin.Int` Set by BroadcastReceiver to indicate there's no default sms app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NO_MEMORY:kotlin.Int` Failed because there is no memory |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_NO_RESOURCES:kotlin.Int` Failed because there are no resources |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_OPERATION_NOT_ALLOWED:kotlin.Int` Failed because the operation is not allowed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RADIO_NOT_AVAILABLE:kotlin.Int` Failed because the radio was not available |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_DISPATCH_FAILURE:kotlin.Int` SMS receive dispatch failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_INJECTED_NULL_PDU:kotlin.Int` SMS receive injected null PDU. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_NULL_MESSAGE_FROM_RIL:kotlin.Int` SMS received null message from the radio interface layer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_RUNTIME_EXCEPTION:kotlin.Int` SMS receive encountered runtime exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_SQL_EXCEPTION:kotlin.Int` SMS receive encountered an SQL exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_URI_EXCEPTION:kotlin.Int` SMS receive an exception parsing a uri. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RECEIVE_WHILE_ENCRYPTED:kotlin.Int` SMS short code received while the phone is in encrypted state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_REMOTE_EXCEPTION:kotlin.Int` Set by BroadcastReceiver to indicate a remote exception while handling a message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_REQUEST_NOT_SUPPORTED:kotlin.Int` Failed because the request is not supported |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_ABORTED:kotlin.Int` Operation aborted |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_ACCESS_BARRED:kotlin.Int` Access is barred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_BLOCKED_DUE_TO_CALL:kotlin.Int` SMS is blocked due to call control, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_CANCELLED:kotlin.Int` The request has been cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_DEVICE_IN_USE:kotlin.Int` Operation cannot be performed because the device is currently in use |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_ENCODING_ERR:kotlin.Int` The SMS message was not encoded properly. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_GENERIC_ERROR:kotlin.Int` A RIL error occurred during the SMS send. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INTERNAL_ERR:kotlin.Int` The modem encountered an unexpected error scenario while handling the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_ARGUMENTS:kotlin.Int` The radio received invalid arguments in the request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_MODEM_STATE:kotlin.Int` The radio cannot process the request in the current modem state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_RESPONSE:kotlin.Int` A RIL internal error when one of the RIL layers receives an unrecognized response from a lower layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_SIM_STATE:kotlin.Int` Cannot process the request in current SIM state |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_SMSC_ADDRESS:kotlin.Int` The specified SMSC address was invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_SMS_FORMAT:kotlin.Int` The radio returned an error indicating invalid sms format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_INVALID_STATE:kotlin.Int` The radio returned an unexpected request for the current state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_MODEM_ERR:kotlin.Int` The vendor RIL received an unexpected or incorrect response. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NETWORK_ERR:kotlin.Int` The radio received an error from the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NETWORK_NOT_READY:kotlin.Int` The network is not ready to perform the request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NETWORK_REJECT:kotlin.Int` The sms request was rejected by the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NO_MEMORY:kotlin.Int` The radio didn't have sufficient memory to process the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NO_NETWORK_FOUND:kotlin.Int` Network cannot be found |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NO_RESOURCES:kotlin.Int` There are insufficient resources to process the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NO_SMS_TO_ACK:kotlin.Int` ACK received when there is no SMS to ack |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_NO_SUBSCRIPTION:kotlin.Int` Device does not have subscription |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_OPERATION_NOT_ALLOWED:kotlin.Int` The radio reports the request is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_RADIO_NOT_AVAILABLE:kotlin.Int` The radio did not start or is resetting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_REQUEST_NOT_SUPPORTED:kotlin.Int` The request was not supported by the radio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_REQUEST_RATE_LIMITED:kotlin.Int` The radio denied the operation due to overly-frequent requests. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED:kotlin.Int` 1X voice and SMS are not allowed simultaneously. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_ABSENT:kotlin.Int` The radio failed to set the location where the CDMA subscription can be retrieved because the SIM or RUIM is absent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_BUSY:kotlin.Int` SIM is busy |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_ERROR:kotlin.Int` Received error from SIM card |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_FULL:kotlin.Int` The target EF is full |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_PIN2:kotlin.Int` Operation requires SIM PIN2 to be entered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SIM_PUK2:kotlin.Int` Operation requires SIM PUK2 to be entered |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SMS_SEND_FAIL_RETRY:kotlin.Int` The radio failed to send the sms and needs to retry. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SUBSCRIPTION_NOT_AVAILABLE:kotlin.Int` Fail to find CDMA subscription from specified location |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_RIL_SYSTEM_ERR:kotlin.Int` The radio encountered a platform or system error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_SMS_BLOCKED_DURING_EMERGENCY:kotlin.Int` Failed sending during an emergency call |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_SMS_SEND_FAILED_AFTER_MAX_RETRY:kotlin.Int` Indicates that the SMS sending operation failed because all allowed retry attempts were exhausted without successfully sending the message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_SMS_SEND_RETRY_FAILED:kotlin.Int` Failed to send an sms retry |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_SYSTEM_ERROR:kotlin.Int` Failed because of a system error |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_UNEXPECTED_EVENT_STOP_SENDING:kotlin.Int` Failed sending because the user denied or canceled the dialog displayed for a premium shortcode sms or rate-limited sms. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_USER_NOT_ALLOWED:kotlin.Int` User is not associated with the subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_CALL_BARRING:kotlin.Int` RP-Cause Value for Call Barring |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_CONGESTION:kotlin.Int` RP-Cause Value for SMS Failure due to Congestion in network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_DESTINATION_OUT_OF_ORDER:kotlin.Int` RP-Cause Value for Destination is Out of Order |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_FACILITY_NOT_IMPLEMENTED:kotlin.Int` RP-Cause Value when network does not provide the received service |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_FACILITY_NOT_SUBSCRIBED:kotlin.Int` RP-Cause Value when SMS Facilty is not subscribed by Reote device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_FACILITY_REJECTED:kotlin.Int` RP-Cause Value when SMS Facility if Rejected by Operator |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_INFORMATION_ELEMENT_NON_EXISTENT:kotlin.Int` RP-Cause Value when network does not provide the received service |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_INTERWORKING_UNSPECIFIED:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_INVALID_MANDATORY_INFORMATION:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_INVALID_MESSAGE_REFERENCE_VALUE:kotlin.Int` RP-Cause Value when RP-MessageRefere |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_MESSAGE_INCOMPATIBLE_WITH_PROTOCOL_STATE:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_MESSAGE_TYPE_NON_EXISTENT:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_NETWORK_OUT_OF_ORDER:kotlin.Int` RP-Cause Value when network is out of order |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_OPERATOR_DETERMINED_BARRING:kotlin.Int` RP-Cause for Operator Barring |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_PROTOCOL_ERROR:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_RESERVED:kotlin.Int` RP-Cause value for Reserved Number |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_RESOURCES_UNAVAILABLE:kotlin.Int` RP-Cause Value when Network Resources are unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_SEMANTICALLY_INCORRECT_MESSAGE:kotlin.Int` RP-Cause Value when network does not provide the received service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_SHORT_MESSAGE_TRANSFER_REJECTED:kotlin.Int` RP-Cause Value for Message Transfer Rejected by Network |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_TEMPORARY_FAILURE:kotlin.Int` RP-Cause Value For Temporary failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_UNALLOCATED_NUMBER:kotlin.Int` Unallocated Number Cause |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_UNIDENTIFIED_SUBSCRIBER:kotlin.Int` RP-Cause Value when Subscriber is not Identified |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#SMS_RP_CAUSE_UNKNOWN_SUBSCRIBER:kotlin.Int` RP-Cause Value when Subscriber is not Identified |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#STATUS_ON_ICC_FREE:kotlin.Int` Free space (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#STATUS_ON_ICC_READ:kotlin.Int` Received and read (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#STATUS_ON_ICC_SENT:kotlin.Int` Stored and sent (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#STATUS_ON_ICC_UNREAD:kotlin.Int` Received and unread (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#STATUS_ON_ICC_UNSENT:kotlin.Int` Stored and unsent (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27). |
| --- | --- |

| Public methods ||
|---|---|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | createAppSpecificSmsToken Create a single use app specific incoming SMS request for the calling package. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | createAppSpecificSmsTokenWithPackageInfo Create a single use app specific incoming SMS request for the calling package. |
| [SmsManager](SmsManager.md) | createForSubscriptionId Get the instance of the SmsManager associated with a particular subscription ID. |
| --- | --- |
| [ArrayList](../java.util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | divideMessage Divide a message text into several fragments, none bigger than the maximum SMS message size. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | downloadMultimediaMessage Download an MMS message from carrier by a given location URL |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | downloadMultimediaMessage Download an MMS message from carrier by a given location URL Same as downloadMultimediaMessage, but adds an optional messageId. |
| --- | --- |
| [Bundle](../android.os/Bundle.md) | getCarrierConfigValues Get carrier-dependent MMS configuration values. |
| static [SmsManager](SmsManager.md)! | getDefault Get the SmsManager associated with the default subscription id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDefaultSmsSubscriptionId Get default sms subscription id. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSmsCapacityOnIcc Gets the total capacity of SMS storage on the SIM card. |
| static [SmsManager](SmsManager.md)! | getSmsManagerForSubscriptionId Get the instance of the SmsManager associated with a particular subscription ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getSmsMessagesForFinancialApp Get SMS messages for the calling financial app. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getSmscAddress Gets the SMSC address from (U)SIM. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSubscriptionId Get the associated subscription id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | injectSmsPdu Inject an SMS PDU into the android application framework. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendDataMessage Send a data based SMS to a specific application port. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendMultimediaMessage Send an MMS message |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendMultimediaMessage Send an MMS message Same as sendMultimediaMessage, but adds an optional messageId. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendMultipartTextMessage Send a multi-part text based SMS. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendMultipartTextMessage Similar method as #sendMultipartTextMessage(String, String, ArrayList, ArrayList, ArrayList) With an additional argument. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendMultipartTextMessage Send a multi-part text based SMS. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendTextMessage Send a text based SMS. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendTextMessage Send a text based SMS. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendTextMessageWithoutPersisting Send a text based SMS without writing it into the SMS Provider. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setSmscAddress Sets the SMSC address on (U)SIM. |

## Constants

### EXTRA_MMS_DATA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MMS_DATA: String
```

Intent extra name for MMS sending result data in byte array type

 Value: "android.telephony.extra.MMS_DATA"

### EXTRA_MMS_HTTP_STATUS

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MMS_HTTP_STATUS: String
```

Intent extra name for HTTP status code for MMS HTTP failure in integer type

 Value: "android.telephony.extra.MMS_HTTP_STATUS"

### MMS_CONFIG_ALIAS_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_ALIAS_ENABLED: String
```

Whether alias is enabled (boolean type)

 Value: "aliasEnabled"

### MMS_CONFIG_ALIAS_MAX_CHARS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_ALIAS_MAX_CHARS: String
```

Max alias character count (int type)

 Value: "aliasMaxChars"

### MMS_CONFIG_ALIAS_MIN_CHARS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_ALIAS_MIN_CHARS: String
```

Min alias character count (int type)

 Value: "aliasMinChars"

### MMS_CONFIG_ALLOW_ATTACH_AUDIO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_ALLOW_ATTACH_AUDIO: String
```

Whether audio is allowed to be attached for MMS messages (boolean type)

 Value: "allowAttachAudio"

### MMS_CONFIG_APPEND_TRANSACTION_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_APPEND_TRANSACTION_ID: String
```

Whether to append transaction id to MMS WAP Push M-Notification.ind's content location URI when constructing the download URL of a new MMS (boolean type)

 Value: "enabledTransID"

### MMS_CONFIG_EMAIL_GATEWAY_NUMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_EMAIL_GATEWAY_NUMBER: String
```

Email gateway number (String type)

 Value: "emailGatewayNumber"

### MMS_CONFIG_GROUP_MMS_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_GROUP_MMS_ENABLED: String
```

Whether group MMS is enabled for the current carrier (boolean type)

 Value: "enableGroupMms"

### MMS_CONFIG_HTTP_PARAMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_HTTP_PARAMS: String
```

A list of HTTP headers to add to MMS HTTP request, separated by "|" (String type)
| --- | --- |

 Value: "httpParams"

### MMS_CONFIG_HTTP_SOCKET_TIMEOUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_HTTP_SOCKET_TIMEOUT: String
```

MMS HTTP socket timeout in milliseconds (int type)

 Value: "httpSocketTimeout"

### MMS_CONFIG_MAX_IMAGE_HEIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MAX_IMAGE_HEIGHT: String
```

Max MMS image height (int type)

 Value: "maxImageHeight"

### MMS_CONFIG_MAX_IMAGE_WIDTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MAX_IMAGE_WIDTH: String
```

Max MMS image width (int type)

 Value: "maxImageWidth"

### MMS_CONFIG_MAX_MESSAGE_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MAX_MESSAGE_SIZE: String
```

Max MMS message size in bytes (int type)

 Value: "maxMessageSize"

### MMS_CONFIG_MESSAGE_TEXT_MAX_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MESSAGE_TEXT_MAX_SIZE: String
```

Max message text size (int type)

 Value: "maxMessageTextSize"

### MMS_CONFIG_MMS_DELIVERY_REPORT_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MMS_DELIVERY_REPORT_ENABLED: String
```

Whether MMS delivery report is enabled (boolean type)

 Value: "enableMMSDeliveryReports"

### MMS_CONFIG_MMS_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MMS_ENABLED: String
```

Whether MMS is enabled for the current carrier (boolean type)

 Value: "enabledMMS"

### MMS_CONFIG_MMS_READ_REPORT_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MMS_READ_REPORT_ENABLED: String
```

Whether MMS read report is enabled (boolean type)

 Value: "enableMMSReadReports"

### MMS_CONFIG_MULTIPART_SMS_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_MULTIPART_SMS_ENABLED: String
```

Whether multipart SMS is enabled (boolean type)

 Value: "enableMultipartSMS"

### MMS_CONFIG_NAI_SUFFIX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_NAI_SUFFIX: String
```

The suffix to append to the NAI header value for MMS HTTP request (String type)

 Value: "naiSuffix"

### MMS_CONFIG_NOTIFY_WAP_MMSC_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_NOTIFY_WAP_MMSC_ENABLED: String
```

If this is enabled, M-NotifyResp.ind should be sent to the WAP Push content location instead of the default MMSC (boolean type)

 Value: "enabledNotifyWapMMSC"

### MMS_CONFIG_RECIPIENT_LIMIT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_RECIPIENT_LIMIT: String
```

Limit of recipients of MMS messages (int type)

 Value: "recipientLimit"

### MMS_CONFIG_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SEND_MULTIPART_SMS_AS_SEPARATE_MESSAGES: String
```

Whether multipart SMS should be sent as separate messages

 Value: "sendMultipartSmsAsSeparateMessages"

### MMS_CONFIG_SHOW_CELL_BROADCAST_APP_LINKS

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SHOW_CELL_BROADCAST_APP_LINKS: String
```

If true, show the cell broadcast (amber alert) in the SMS settings. Some carriers don't want this shown. (Boolean type)

 Value: "config_cellBroadcastAppLinks"

### MMS_CONFIG_SMS_DELIVERY_REPORT_ENABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SMS_DELIVERY_REPORT_ENABLED: String
```

Whether SMS delivery report is enabled (boolean type)

 Value: "enableSMSDeliveryReports"

### MMS_CONFIG_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SMS_TO_MMS_TEXT_LENGTH_THRESHOLD: String
```

Some carriers require SMS to be converted into MMS when text length reaches this threshold (int type)

 Value: "smsToMmsTextLengthThreshold"

### MMS_CONFIG_SMS_TO_MMS_TEXT_THRESHOLD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SMS_TO_MMS_TEXT_THRESHOLD: String
```

When the number of parts of a multipart SMS reaches this threshold, it should be converted into an MMS (int type)

 Value: "smsToMmsTextThreshold"

### MMS_CONFIG_SUBJECT_MAX_LENGTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SUBJECT_MAX_LENGTH: String
```

Max message subject length (int type)

 Value: "maxSubjectLength"

### MMS_CONFIG_SUPPORT_HTTP_CHARSET_HEADER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SUPPORT_HTTP_CHARSET_HEADER: String
```

Whether the carrier MMSC supports charset field in Content-Type header. If this is false, then we don't add "charset" to "Content-Type"

 Value: "supportHttpCharsetHeader"

### MMS_CONFIG_SUPPORT_MMS_CONTENT_DISPOSITION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_SUPPORT_MMS_CONTENT_DISPOSITION: String
```

Whether content-disposition field should be expected in an MMS PDU (boolean type)

 Value: "supportMmsContentDisposition"

### MMS_CONFIG_UA_PROF_TAG_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_UA_PROF_TAG_NAME: String
```

The name of the UA Prof URL HTTP header for MMS HTTP request (String type)

 Value: "uaProfTagName"

### MMS_CONFIG_UA_PROF_URL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_UA_PROF_URL: String
```

The UA Profile URL header value for MMS HTTP request (String type)

 Value: "uaProfUrl"

### MMS_CONFIG_USER_AGENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_CONFIG_USER_AGENT: String
```

The User-Agent header value for MMS HTTP request (String type)

 Value: "userAgent"

### MMS_ERROR_CONFIGURATION_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_CONFIGURATION_ERROR: Int
```

The carrier-dependent configuration values could not be loaded.

 Value: 7

### MMS_ERROR_DATA_DISABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_DATA_DISABLED: Int
```

Data is disabled for the MMS APN.

 Value: 11

### MMS_ERROR_HTTP_FAILURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_HTTP_FAILURE: Int
```

An error occurred during the HTTP client setup.

 Value: 4

### MMS_ERROR_INACTIVE_SUBSCRIPTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_INACTIVE_SUBSCRIPTION: Int
```

The subscription id for the send/download is inactive.

 Value: 10

### MMS_ERROR_INVALID_APN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_INVALID_APN: Int
```

ApnException occurred during MMS network setup.

 Value: 2

### MMS_ERROR_INVALID_SUBSCRIPTION_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_INVALID_SUBSCRIPTION_ID: Int
```

The subscription id for the send/download is invalid.

 Value: 9

### MMS_ERROR_IO_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_IO_ERROR: Int
```

An I/O error occurred reading the PDU.

 Value: 5

### MMS_ERROR_MMS_DISABLED_BY_CARRIER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_MMS_DISABLED_BY_CARRIER: Int
```

MMS is disabled by a carrier.

 Value: 12

### MMS_ERROR_NO_DATA_NETWORK

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_NO_DATA_NETWORK: Int
```

There is neither Wi-Fi nor mobile data network.

 Value: 8

### MMS_ERROR_RETRY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_RETRY: Int
```

An error occurred while retrying sending/downloading the MMS.

 Value: 6

### MMS_ERROR_UNABLE_CONNECT_MMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_UNABLE_CONNECT_MMS: Int
```

An error occurred during the MMS connection setup.

 Value: 3

### MMS_ERROR_UNSPECIFIED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MMS_ERROR_UNSPECIFIED: Int
```

Unspecific MMS error occurred during send/download.

 Value: 1

### RESULT_BLUETOOTH_DISCONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_BLUETOOTH_DISCONNECTED: Int
```

Failed sending via bluetooth because bluetooth disconnected

 Value: 27

### RESULT_CANCELLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_CANCELLED: Int
```

Failed because the operation was cancelled

 Value: 23

### RESULT_ENCODING_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ENCODING_ERROR: Int
```

Failed because of an encoding error

 Value: 18

### RESULT_ERROR_FDN_CHECK_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_FDN_CHECK_FAILURE: Int
```

Failed because FDN is enabled.

 Value: 6

### RESULT_ERROR_GENERIC_FAILURE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_GENERIC_FAILURE: Int
```

Generic failure cause

 Value: 1

### RESULT_ERROR_LIMIT_EXCEEDED

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_LIMIT_EXCEEDED: Int
```

Failed because we reached the sending queue limit.

 Value: 5

### RESULT_ERROR_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_NONE: Int
```

No error.

 Value: 0

### RESULT_ERROR_NO_SERVICE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_NO_SERVICE: Int
```

Failed because service is currently unavailable

 Value: 4

### RESULT_ERROR_NULL_PDU

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_NULL_PDU: Int
```

Failed because no pdu provided

 Value: 3

### RESULT_ERROR_RADIO_OFF

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_RADIO_OFF: Int
```

Failed because radio was explicitly turned off

 Value: 2

### RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED: Int
```

Failed because the user has denied this app ever send premium short codes.

 Value: 8

### RESULT_ERROR_SHORT_CODE_NOT_ALLOWED

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_SHORT_CODE_NOT_ALLOWED: Int
```

Failed because user denied the sending of this short code.

 Value: 7

### RESULT_INTERNAL_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INTERNAL_ERROR: Int
```

Failed because of an internal error

 Value: 21

### RESULT_INVALID_ARGUMENTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_ARGUMENTS: Int
```

Failed because of invalid arguments

 Value: 11

### RESULT_INVALID_BLUETOOTH_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_BLUETOOTH_ADDRESS: Int
```

Failed sending via bluetooth because the bluetooth device address is invalid

 Value: 26

### RESULT_INVALID_SMSC_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_SMSC_ADDRESS: Int
```

Failed because of an invalid smsc address

 Value: 19

### RESULT_INVALID_SMS_FORMAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_SMS_FORMAT: Int
```

Failed because the sms format is not valid

 Value: 14

### RESULT_INVALID_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_STATE: Int
```

Failed because of an invalid state

 Value: 12

### RESULT_MODEM_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_MODEM_ERROR: Int
```

Failed because of a modem error

 Value: 16

### RESULT_NETWORK_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NETWORK_ERROR: Int
```

Failed because of a network error

 Value: 17

### RESULT_NETWORK_REJECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NETWORK_REJECT: Int
```

Failed because of network rejection

 Value: 10

### RESULT_NO_BLUETOOTH_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NO_BLUETOOTH_SERVICE: Int
```

Failed sending via bluetooth because the bluetooth service is not available

 Value: 25

### RESULT_NO_DEFAULT_SMS_APP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NO_DEFAULT_SMS_APP: Int
```

Set by BroadcastReceiver to indicate there's no default sms app.

 Value: 32

### RESULT_NO_MEMORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NO_MEMORY: Int
```

Failed because there is no memory

 Value: 13

### RESULT_NO_RESOURCES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NO_RESOURCES: Int
```

Failed because there are no resources

 Value: 22

### RESULT_OPERATION_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OPERATION_NOT_ALLOWED: Int
```

Failed because the operation is not allowed

 Value: 20

### RESULT_RADIO_NOT_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RADIO_NOT_AVAILABLE: Int
```

Failed because the radio was not available

 Value: 9

### RESULT_RECEIVE_DISPATCH_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_DISPATCH_FAILURE: Int
```

SMS receive dispatch failure.

 Value: 500

### RESULT_RECEIVE_INJECTED_NULL_PDU

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_INJECTED_NULL_PDU: Int
```

SMS receive injected null PDU.

 Value: 501

### RESULT_RECEIVE_NULL_MESSAGE_FROM_RIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_NULL_MESSAGE_FROM_RIL: Int
```

SMS received null message from the radio interface layer.

 Value: 503

### RESULT_RECEIVE_RUNTIME_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_RUNTIME_EXCEPTION: Int
```

SMS receive encountered runtime exception.

 Value: 502

### RESULT_RECEIVE_SQL_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_SQL_EXCEPTION: Int
```

SMS receive encountered an SQL exception.

 Value: 505

### RESULT_RECEIVE_URI_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_URI_EXCEPTION: Int
```

SMS receive an exception parsing a uri.

 Value: 506

### RESULT_RECEIVE_WHILE_ENCRYPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RECEIVE_WHILE_ENCRYPTED: Int
```

SMS short code received while the phone is in encrypted state.

 Value: 504

### RESULT_REMOTE_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_REMOTE_EXCEPTION: Int
```

Set by BroadcastReceiver to indicate a remote exception while handling a message.

 Value: 31

### RESULT_REQUEST_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_REQUEST_NOT_SUPPORTED: Int
```

Failed because the request is not supported

 Value: 24

### RESULT_RIL_ABORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_ABORTED: Int
```

Operation aborted

 Value: 137

### RESULT_RIL_ACCESS_BARRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_ACCESS_BARRED: Int
```

Access is barred.

 Value: 122

### RESULT_RIL_BLOCKED_DUE_TO_CALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_BLOCKED_DUE_TO_CALL: Int
```

SMS is blocked due to call control, e.g., resource unavailable in the SMR entity.

 Value: 123

### RESULT_RIL_CANCELLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_CANCELLED: Int
```

The request has been cancelled.

 Value: 119

### RESULT_RIL_DEVICE_IN_USE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_DEVICE_IN_USE: Int
```

Operation cannot be performed because the device is currently in use

 Value: 136

### RESULT_RIL_ENCODING_ERR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_ENCODING_ERR: Int
```

The SMS message was not encoded properly.

 Value: 109

### RESULT_RIL_GENERIC_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_GENERIC_ERROR: Int
```

A RIL error occurred during the SMS send.

 Value: 124

### RESULT_RIL_INTERNAL_ERR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INTERNAL_ERR: Int
```

The modem encountered an unexpected error scenario while handling the request.

 Value: 113

### RESULT_RIL_INVALID_ARGUMENTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_ARGUMENTS: Int
```

The radio received invalid arguments in the request.

 Value: 104

### RESULT_RIL_INVALID_MODEM_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_MODEM_STATE: Int
```

The radio cannot process the request in the current modem state.

 Value: 115

### RESULT_RIL_INVALID_RESPONSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_RESPONSE: Int
```

A RIL internal error when one of the RIL layers receives an unrecognized response from a lower layer.

 Value: 125

### RESULT_RIL_INVALID_SIM_STATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_SIM_STATE: Int
```

Cannot process the request in current SIM state

 Value: 130

### RESULT_RIL_INVALID_SMSC_ADDRESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_SMSC_ADDRESS: Int
```

The specified SMSC address was invalid.

 Value: 110

### RESULT_RIL_INVALID_SMS_FORMAT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_SMS_FORMAT: Int
```

The radio returned an error indicating invalid sms format.

 Value: 107

### RESULT_RIL_INVALID_STATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_INVALID_STATE: Int
```

The radio returned an unexpected request for the current state.

 Value: 103

### RESULT_RIL_MODEM_ERR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_MODEM_ERR: Int
```

The vendor RIL received an unexpected or incorrect response.

 Value: 111

### RESULT_RIL_NETWORK_ERR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NETWORK_ERR: Int
```

The radio received an error from the network.

 Value: 112

### RESULT_RIL_NETWORK_NOT_READY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NETWORK_NOT_READY: Int
```

The network is not ready to perform the request.

 Value: 116

### RESULT_RIL_NETWORK_REJECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NETWORK_REJECT: Int
```

The sms request was rejected by the network.

 Value: 102

### RESULT_RIL_NO_MEMORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NO_MEMORY: Int
```

The radio didn't have sufficient memory to process the request.

 Value: 105

### RESULT_RIL_NO_NETWORK_FOUND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NO_NETWORK_FOUND: Int
```

Network cannot be found

 Value: 135

### RESULT_RIL_NO_RESOURCES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NO_RESOURCES: Int
```

There are insufficient resources to process the request.

 Value: 118

### RESULT_RIL_NO_SMS_TO_ACK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NO_SMS_TO_ACK: Int
```

ACK received when there is no SMS to ack

 Value: 131

### RESULT_RIL_NO_SUBSCRIPTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_NO_SUBSCRIPTION: Int
```

Device does not have subscription

 Value: 134

### RESULT_RIL_OPERATION_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_OPERATION_NOT_ALLOWED: Int
```

The radio reports the request is not allowed.

 Value: 117

### RESULT_RIL_RADIO_NOT_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_RADIO_NOT_AVAILABLE: Int
```

The radio did not start or is resetting.

 Value: 100

### RESULT_RIL_REQUEST_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_REQUEST_NOT_SUPPORTED: Int
```

The request was not supported by the radio.

 Value: 114

### RESULT_RIL_REQUEST_RATE_LIMITED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_REQUEST_RATE_LIMITED: Int
```

The radio denied the operation due to overly-frequent requests.

 Value: 106

### RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED: Int
```

1X voice and SMS are not allowed simultaneously.

 Value: 121

### RESULT_RIL_SIM_ABSENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_ABSENT: Int
```

The radio failed to set the location where the CDMA subscription can be retrieved because the SIM or RUIM is absent.

 Value: 120

### RESULT_RIL_SIM_BUSY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_BUSY: Int
```

SIM is busy

 Value: 132

### RESULT_RIL_SIM_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_ERROR: Int
```

Received error from SIM card

 Value: 129

### RESULT_RIL_SIM_FULL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_FULL: Int
```

The target EF is full

 Value: 133

### RESULT_RIL_SIM_PIN2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_PIN2: Int
```

Operation requires SIM PIN2 to be entered

 Value: 126

### RESULT_RIL_SIM_PUK2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SIM_PUK2: Int
```

Operation requires SIM PUK2 to be entered

 Value: 127

### RESULT_RIL_SMS_SEND_FAIL_RETRY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SMS_SEND_FAIL_RETRY: Int
```

The radio failed to send the sms and needs to retry.

 Value: 101

### RESULT_RIL_SUBSCRIPTION_NOT_AVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SUBSCRIPTION_NOT_AVAILABLE: Int
```

Fail to find CDMA subscription from specified location

 Value: 128

### RESULT_RIL_SYSTEM_ERR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RIL_SYSTEM_ERR: Int
```

The radio encountered a platform or system error.

 Value: 108

### RESULT_SMS_BLOCKED_DURING_EMERGENCY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SMS_BLOCKED_DURING_EMERGENCY: Int
```

Failed sending during an emergency call

 Value: 29

### RESULT_SMS_SEND_FAILED_AFTER_MAX_RETRY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SMS_SEND_FAILED_AFTER_MAX_RETRY: Int
```

Indicates that the SMS sending operation failed because all allowed retry attempts were exhausted without successfully sending the message.

This is distinct from `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_SMS_SEND_RETRY_FAILED:kotlin.Int`, which signals a single failed retry attempt where further retries might still be scheduled. In contrast, `RESULT_SMS_SEND_FAILED_AFTER_MAX_RETRY` signifies that the maximum retry limit has been surpassed, and no more attempts will be made for this SMS message.

 Value: 138

### RESULT_SMS_SEND_RETRY_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SMS_SEND_RETRY_FAILED: Int
```

Failed to send an sms retry

 Value: 30

### RESULT_SYSTEM_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SYSTEM_ERROR: Int
```

Failed because of a system error

 Value: 15

### RESULT_UNEXPECTED_EVENT_STOP_SENDING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNEXPECTED_EVENT_STOP_SENDING: Int
```

Failed sending because the user denied or canceled the dialog displayed for a premium shortcode sms or rate-limited sms.

 Value: 28

### RESULT_USER_NOT_ALLOWED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_USER_NOT_ALLOWED: Int
```

User is not associated with the subscription.

 Value: 33

### SMS_RP_CAUSE_CALL_BARRING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_CALL_BARRING: Int
```

RP-Cause Value for Call Barring

 Value: 10

### SMS_RP_CAUSE_CONGESTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_CONGESTION: Int
```

RP-Cause Value for SMS Failure due to Congestion in network

 Value: 42

### SMS_RP_CAUSE_DESTINATION_OUT_OF_ORDER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_DESTINATION_OUT_OF_ORDER: Int
```

RP-Cause Value for Destination is Out of Order

 Value: 27

### SMS_RP_CAUSE_FACILITY_NOT_IMPLEMENTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_FACILITY_NOT_IMPLEMENTED: Int
```

RP-Cause Value when network does not provide the received service

 Value: 69

### SMS_RP_CAUSE_FACILITY_NOT_SUBSCRIBED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_FACILITY_NOT_SUBSCRIBED: Int
```

RP-Cause Value when SMS Facilty is not subscribed by Reote device

 Value: 50

### SMS_RP_CAUSE_FACILITY_REJECTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_FACILITY_REJECTED: Int
```

RP-Cause Value when SMS Facility if Rejected by Operator

 Value: 29

### SMS_RP_CAUSE_INFORMATION_ELEMENT_NON_EXISTENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_INFORMATION_ELEMENT_NON_EXISTENT: Int
```

RP-Cause Value when network does not provide the received service

 Value: 99

### SMS_RP_CAUSE_INTERWORKING_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_INTERWORKING_UNSPECIFIED: Int
```

RP-Cause Value when network does not provide the received service

 Value: 127

### SMS_RP_CAUSE_INVALID_MANDATORY_INFORMATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_INVALID_MANDATORY_INFORMATION: Int
```

RP-Cause Value when network does not provide the received service

 Value: 96

### SMS_RP_CAUSE_INVALID_MESSAGE_REFERENCE_VALUE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_INVALID_MESSAGE_REFERENCE_VALUE: Int
```

RP-Cause Value when RP-MessageRefere

 Value: 81

### SMS_RP_CAUSE_MESSAGE_INCOMPATIBLE_WITH_PROTOCOL_STATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_MESSAGE_INCOMPATIBLE_WITH_PROTOCOL_STATE: Int
```

RP-Cause Value when network does not provide the received service

 Value: 98

### SMS_RP_CAUSE_MESSAGE_TYPE_NON_EXISTENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_MESSAGE_TYPE_NON_EXISTENT: Int
```

RP-Cause Value when network does not provide the received service

 Value: 97

### SMS_RP_CAUSE_NETWORK_OUT_OF_ORDER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_NETWORK_OUT_OF_ORDER: Int
```

RP-Cause Value when network is out of order

 Value: 38

### SMS_RP_CAUSE_OPERATOR_DETERMINED_BARRING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_OPERATOR_DETERMINED_BARRING: Int
```

RP-Cause for Operator Barring

 Value: 8

### SMS_RP_CAUSE_PROTOCOL_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_PROTOCOL_ERROR: Int
```

RP-Cause Value when network does not provide the received service

 Value: 111

### SMS_RP_CAUSE_RESERVED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_RESERVED: Int
```

RP-Cause value for Reserved Number

 Value: 11

### SMS_RP_CAUSE_RESOURCES_UNAVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_RESOURCES_UNAVAILABLE: Int
```

RP-Cause Value when Network Resources are unavailable

 Value: 47

### SMS_RP_CAUSE_SEMANTICALLY_INCORRECT_MESSAGE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_SEMANTICALLY_INCORRECT_MESSAGE: Int
```

RP-Cause Value when network does not provide the received service

 Value: 95

### SMS_RP_CAUSE_SHORT_MESSAGE_TRANSFER_REJECTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_SHORT_MESSAGE_TRANSFER_REJECTED: Int
```

RP-Cause Value for Message Transfer Rejected by Network

 Value: 21

### SMS_RP_CAUSE_TEMPORARY_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_TEMPORARY_FAILURE: Int
```

RP-Cause Value For Temporary failure

 Value: 41

### SMS_RP_CAUSE_UNALLOCATED_NUMBER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_UNALLOCATED_NUMBER: Int
```

Unallocated Number Cause

 Value: 1

### SMS_RP_CAUSE_UNIDENTIFIED_SUBSCRIBER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_UNIDENTIFIED_SUBSCRIBER: Int
```

RP-Cause Value when Subscriber is not Identified

 Value: 28

### SMS_RP_CAUSE_UNKNOWN_SUBSCRIBER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SMS_RP_CAUSE_UNKNOWN_SUBSCRIBER: Int
```

RP-Cause Value when Subscriber is not Identified

 Value: 30

### STATUS_ON_ICC_FREE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ON_ICC_FREE: Int
```

Free space (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27).

 Value: 0

### STATUS_ON_ICC_READ

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ON_ICC_READ: Int
```

Received and read (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27).

 Value: 1

### STATUS_ON_ICC_SENT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ON_ICC_SENT: Int
```

Stored and sent (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27).

 Value: 5

### STATUS_ON_ICC_UNREAD

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ON_ICC_UNREAD: Int
```

Received and unread (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27).

 Value: 3

### STATUS_ON_ICC_UNSENT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_ON_ICC_UNSENT: Int
```

Stored and unsent (TS 51.011 10.5.3 / 3GPP2 C.S0023 3.4.27).

 Value: 7

## Public methods

### createAppSpecificSmsToken

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createAppSpecificSmsToken(intent: PendingIntent!): String!
```

Create a single use app specific incoming SMS request for the calling package. This method returns a token that if included in a subsequent incoming SMS message will cause `intent` to be sent with the SMS data. The token is only good for one use, after an SMS has been received containing the token all subsequent SMS messages with the token will be routed as normal. An app can only have one request at a time, if the app already has a request pending it will be replaced with a new request.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Token to include in an SMS message. The token will be 11 characters long. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the intent is null. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

**See Also**

- getMessagesFromIntent

### createAppSpecificSmsTokenWithPackageInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createAppSpecificSmsTokenWithPackageInfo(
    prefixes: String?, 
    intent: PendingIntent
): String?
```

Create a single use app specific incoming SMS request for the calling package. This method returns a token that if included in a subsequent incoming SMS message, and the SMS message has a prefix from the given prefixes list, the provided `intent` will be sent with the SMS data to the calling package. The token is only good for one use within a reasonable amount of time. After an SMS has been received containing the token all subsequent SMS messages with the token will be routed as normal. An app can only have one request at a time, if the app already has a request pending it will be replaced with a new request.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `prefixes` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: this is a list of prefixes string separated by REGEX_PREFIX_DELIMITER. The matching SMS message should have at least one of the prefixes in the beginning of the message. This value may be `null`. |
| `intent` | [PendingIntent](../android.app/PendingIntent.md): this intent is sent when the matching SMS message is received. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | Token to include in an SMS message. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### createForSubscriptionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createForSubscriptionId(subId: Int): SmsManager
```

Get the instance of the SmsManager associated with a particular subscription ID.

**Note:** Constructing an SmsManager in this manner will never cause an SMS disambiguation dialog to appear, unlike getDefault.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an SMS subscription ID, typically accessed using SubscriptionManager |

| Return ||
|---|---|
| SmsManager | the instance of the SmsManager associated with subscription. This value cannot be `null`. |

**See Also**

- getActiveSubscriptionInfoList
- getDefaultSmsSubscriptionId

### divideMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun divideMessage(text: String!): ArrayList<String!>!
```

Divide a message text into several fragments, none bigger than the maximum SMS message size. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the original message. Must not be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an `ArrayList` of strings that, in order, comprise the original message. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if text is null. |

### downloadMultimediaMessage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun downloadMultimediaMessage(
    context: Context!, 
    locationUrl: String!, 
    contentUri: Uri!, 
    configOverrides: Bundle!, 
    downloadedIntent: PendingIntent!
): Unit
```

Download an MMS message from carrier by a given location URL

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail downloading the MMS message because no suitable default subscription could be found. In this case, if `downloadedIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_NO_DEFAULT_SMS_APP`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: application context |
| `locationUrl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the location URL of the MMS message to be downloaded, usually obtained from the MMS WAP push notification |
| `contentUri` | [Uri](../android.net/Uri.md)!: the content uri to which the downloaded pdu will be written |
| --- | --- |
| `configOverrides` | [Bundle](../android.os/Bundle.md)!: the carrier-specific messaging configuration values to override for downloading the message. |
| `downloadedIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is downloaded, or the download is failed The result code will be `Activity.RESULT_OK` for success or one of these errors: `MMS_ERROR_UNSPECIFIED` `MMS_ERROR_INVALID_APN` `MMS_ERROR_UNABLE_CONNECT_MMS` `MMS_ERROR_HTTP_FAILURE` `MMS_ERROR_IO_ERROR` `MMS_ERROR_RETRY` `MMS_ERROR_CONFIGURATION_ERROR` `MMS_ERROR_NO_DATA_NETWORK` `MMS_ERROR_INVALID_SUBSCRIPTION_ID` `MMS_ERROR_INACTIVE_SUBSCRIPTION` `MMS_ERROR_DATA_DISABLED` `MMS_ERROR_MMS_DISABLED_BY_CARRIER` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if locationUrl or contentUri is empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### downloadMultimediaMessage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun downloadMultimediaMessage(
    context: Context, 
    locationUrl: String, 
    contentUri: Uri, 
    configOverrides: Bundle?, 
    downloadedIntent: PendingIntent?, 
    messageId: Long
): Unit
```

Download an MMS message from carrier by a given location URL Same as downloadMultimediaMessage, but adds an optional messageId.

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail downloading the MMS message because no suitable default subscription could be found. In this case, if `downloadedIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_NO_DEFAULT_SMS_APP`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): application context. This value cannot be `null`. |
| `locationUrl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the location URL of the MMS message to be downloaded, usually obtained from the MMS WAP push notification. This value cannot be `null`. |
| `contentUri` | [Uri](../android.net/Uri.md): the content uri to which the downloaded pdu will be written. This value cannot be `null`. |
| --- | --- |
| `configOverrides` | [Bundle](../android.os/Bundle.md)?: the carrier-specific messaging configuration values to override for downloading the message. This value may be `null`. |
| `downloadedIntent` | [PendingIntent](../android.app/PendingIntent.md)?: if not NULL this `PendingIntent` is broadcast when the message is downloaded, or the download is failed The result code will be `Activity.RESULT_OK` for success or one of these errors: `MMS_ERROR_UNSPECIFIED` `MMS_ERROR_INVALID_APN` `MMS_ERROR_UNABLE_CONNECT_MMS` `MMS_ERROR_HTTP_FAILURE` `MMS_ERROR_IO_ERROR` `MMS_ERROR_RETRY` `MMS_ERROR_CONFIGURATION_ERROR` `MMS_ERROR_NO_DATA_NETWORK` `MMS_ERROR_INVALID_SUBSCRIPTION_ID` `MMS_ERROR_INACTIVE_SUBSCRIPTION` `MMS_ERROR_DATA_DISABLED` `MMS_ERROR_MMS_DISABLED_BY_CARRIER` . This value may be `null`. |
| `messageId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): an id that uniquely identifies the message requested to be downloaded. Used for logging and diagnostics purposes. The id may be 0. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if locationUrl or contentUri is empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getCarrierConfigValues

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierConfigValues(): Bundle
```

Get carrier-dependent MMS configuration values.

**Note:** This method is intended for internal use by carrier applications or the Telephony framework and will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | the bundle key/values pairs that contains MMS configuration values or an empty Bundle if they cannot be found. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getDefault

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefault(): SmsManager!
```

**Deprecated:** *Use android.content.Context#getSystemService instead*

Get the SmsManager associated with the default subscription id. The instance will always be associated with the default subscription id, even if the default subscription id changes.

**Note:** For devices that support multiple active subscriptions at a time, SmsManager will track the subscription set by the user as the default SMS subscription. If the user has not set a default, SmsManager may start an activity to kick off a subscription disambiguation dialog. Most operations will not complete until the user has chosen the subscription that will be associated with the operation. If the user cancels the dialog without choosing a subscription, one of the following will happen, depending on the target SDK version of the application. For compatibility purposes, if the target SDK level is \<= 28, telephony will still send the SMS over the first available subscription. If the target SDK level is \> 28, the operation will fail to complete.

**Note:** If this method is used to perform an operation on a device that has multiple active subscriptions, the user has not set a default SMS subscription, and the operation is being performed while the application is not in the foreground, the SMS disambiguation dialog will not be shown. The result of the operation will conclude as if the user cancelled the disambiguation dialog and the operation will finish as outlined above, depending on the target SDK version of the calling application. It is safer to use getSmsManagerForSubscriptionId if the application will perform the operation while in the background because this can cause unpredictable results, such as the operation being sent over the wrong subscription or failing completely, depending on the user's default SMS subscription setting.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#!` | the SmsManager associated with the default subscription id. |

**See Also**

- getDefaultSmsSubscriptionId

### getDefaultSmsSubscriptionId

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultSmsSubscriptionId(): Int
```

Get default sms subscription id.

**Note:** This returns a value different from getDefaultSmsSubscriptionId if the user has not chosen a default. In this case it returns the active subscription id if there's only one active subscription available. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the user-defined default SMS subscription id, or the active subscription id if there's only one active subscription available, otherwise `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getSmsCapacityOnIcc

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSmsCapacityOnIcc(): Int
```

Gets the total capacity of SMS storage on the SIM card.

This is the number of 176 byte EF-SMS records which can be stored on the SIM card. See 3GPP TS 31.102 - 4.2.25 - EF-SMS for more information.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this method will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total number of SMS records which can be stored on the SIM card. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getSmsManagerForSubscriptionId

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSmsManagerForSubscriptionId(subId: Int): SmsManager!
```

**Deprecated:** *Use android.content.Context#getSystemService .createForSubscriptionId instead*

Get the instance of the SmsManager associated with a particular subscription ID.

**Note:** Constructing an SmsManager in this manner will never cause an SMS disambiguation dialog to appear, unlike getDefault.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an SMS subscription ID, typically accessed using SubscriptionManager |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#!` | the instance of the SmsManager associated with subscription |

**See Also**

- getActiveSubscriptionInfoList
- getDefaultSmsSubscriptionId

### getSmsMessagesForFinancialApp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSmsMessagesForFinancialApp(
    params: Bundle!, 
    executor: Executor, 
    callback: SmsManager.FinancialSmsCallback
): Unit
```

Get SMS messages for the calling financial app. The result will be delivered asynchronously in the passing in callback interface.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SMS_FINANCIAL_TRANSACTIONS:kotlin.String`

| Parameters ||
|---|---|
| `params` | [Bundle](../android.os/Bundle.md)!: the parameters to filter SMS messages returned. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [SmsManager.FinancialSmsCallback](../android/telephony/SmsManager.FinancialSmsCallback.md): a callback to receive CursorWindow with SMS messages. This value cannot be `null`. |
| --- | --- |

### getSmscAddress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSmscAddress(): String?
```

Gets the SMSC address from (U)SIM.

**Note:** Using this method requires that your app is the default SMS application, or READ_PRIVILEGED_PHONE_STATE permission, or has the carrier privileges.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this method will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the SMSC address string, null if failed. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getSubscriptionId

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubscriptionId(): Int
```

Get the associated subscription id. If the instance was returned by getDefault, then this method may return different values at different points in time (if the user changes the default subscription id).

**Note:** This method used to display a disambiguation dialog to the user asking them to choose a default subscription to send SMS messages over if they haven't chosen yet. Starting in API level 29, we allow the user to not have a default set as a valid option for the default SMS subscription on multi-SIM devices. We no longer show the disambiguation dialog and return `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` if the device has multiple active subscriptions and no default is set.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | associated subscription ID or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` if the default subscription id cannot be determined or the device has multiple active subscriptions and and no default is set ("ask every time") by the user. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### injectSmsPdu

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun injectSmsPdu(
    pdu: ByteArray!, 
    format: String!, 
    receivedIntent: PendingIntent!
): Unit
```

Inject an SMS PDU into the android application framework.

Requires permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or carrier privileges per hasCarrierPrivileges.

**Note:** This method is intended for internal use by carrier applications or the Telephony framework and will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the SMS being injected on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the SMS is delivered to the correct subscription.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `pdu` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: is the byte array of pdu to be injected into android application framework |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: is the format of SMS pdu (`https://developer.android.com/reference/kotlin/android/telephony/SmsMessage#FORMAT_3GPP:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telephony/SmsMessage#FORMAT_3GPP2:kotlin.String`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/SmsMessage#FORMAT_3GPP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/telephony/SmsMessage#FORMAT_3GPP2:kotlin.String` |
| `receivedIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is successfully received by the android application framework, or failed. This intent is broadcasted at the same time an SMS received from radio is acknowledged back. The result code will be `https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents.html#RESULT_SMS_HANDLED:kotlin.Int` for success, or `https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents.html#RESULT_SMS_GENERIC_ERROR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/SmsManager#RESULT_REMOTE_EXCEPTION:kotlin.Int` for error. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the format is invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendDataMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendDataMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    destinationPort: Short, 
    data: ByteArray!, 
    sentIntent: PendingIntent!, 
    deliveryIntent: PendingIntent!
): Unit
```

Send a data based SMS to a specific application port.

**Note:** Using this method requires that your app has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` permission.

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail sending the SMS message because no suitable default subscription could be found. In this case, if `sentIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_ERROR_GENERIC_FAILURE` and an extra string `"noDefault"` containing the boolean value `true`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: is the service center address or null to use the current default SMSC |
| `destinationPort` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the port to deliver the message to |
| --- | --- |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the body of the message to send |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is successfully sent, or failed. The result code will be `Activity.RESULT_OK` for success, or one of these errors: `RESULT_ERROR_GENERIC_FAILURE` `RESULT_ERROR_RADIO_OFF` `RESULT_ERROR_NULL_PDU` `RESULT_ERROR_NO_SERVICE` `RESULT_ERROR_LIMIT_EXCEEDED` `RESULT_ERROR_FDN_CHECK_FAILURE` `RESULT_ERROR_SHORT_CODE_NOT_ALLOWED` `RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED` `RESULT_RADIO_NOT_AVAILABLE` `RESULT_NETWORK_REJECT` `RESULT_INVALID_ARGUMENTS` `RESULT_INVALID_STATE` `RESULT_NO_MEMORY` `RESULT_INVALID_SMS_FORMAT` `RESULT_SYSTEM_ERROR` `RESULT_MODEM_ERROR` `RESULT_NETWORK_ERROR` `RESULT_ENCODING_ERROR` `RESULT_INVALID_SMSC_ADDRESS` `RESULT_OPERATION_NOT_ALLOWED` `RESULT_INTERNAL_ERROR` `RESULT_NO_RESOURCES` `RESULT_CANCELLED` `RESULT_REQUEST_NOT_SUPPORTED` `RESULT_NO_BLUETOOTH_SERVICE` `RESULT_INVALID_BLUETOOTH_ADDRESS` `RESULT_BLUETOOTH_DISCONNECTED` `RESULT_UNEXPECTED_EVENT_STOP_SENDING` `RESULT_SMS_BLOCKED_DURING_EMERGENCY` `RESULT_SMS_SEND_RETRY_FAILED` `RESULT_REMOTE_EXCEPTION` `RESULT_NO_DEFAULT_SMS_APP` `RESULT_RIL_RADIO_NOT_AVAILABLE` `RESULT_RIL_SMS_SEND_FAIL_RETRY` `RESULT_RIL_NETWORK_REJECT` `RESULT_RIL_INVALID_STATE` `RESULT_RIL_INVALID_ARGUMENTS` `RESULT_RIL_NO_MEMORY` `RESULT_RIL_REQUEST_RATE_LIMITED` `RESULT_RIL_INVALID_SMS_FORMAT` `RESULT_RIL_SYSTEM_ERR` `RESULT_RIL_ENCODING_ERR` `RESULT_RIL_INVALID_SMSC_ADDRESS` `RESULT_RIL_MODEM_ERR` `RESULT_RIL_NETWORK_ERR` `RESULT_RIL_INTERNAL_ERR` `RESULT_RIL_REQUEST_NOT_SUPPORTED` `RESULT_RIL_INVALID_MODEM_STATE` `RESULT_RIL_NETWORK_NOT_READY` `RESULT_RIL_OPERATION_NOT_ALLOWED` `RESULT_RIL_NO_RESOURCES` `RESULT_RIL_CANCELLED` `RESULT_RIL_SIM_ABSENT` `RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED` `RESULT_RIL_ACCESS_BARRED` `RESULT_RIL_BLOCKED_DUE_TO_CALL` For `RESULT_ERROR_GENERIC_FAILURE` or any of the RESULT_RIL errors, the sentIntent may include the extra "errorCode" containing a radio technology specific value, generally only useful for troubleshooting. |
| `deliveryIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if destinationAddress or data are empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendMultimediaMessage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMultimediaMessage(
    context: Context!, 
    contentUri: Uri!, 
    locationUrl: String!, 
    configOverrides: Bundle!, 
    sentIntent: PendingIntent!
): Unit
```

Send an MMS message

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail sending the MMS message because no suitable default subscription could be found. In this case, if `sentIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_NO_DEFAULT_SMS_APP`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: application context |
| `contentUri` | [Uri](../android.net/Uri.md)!: the content Uri from which the message pdu will be read |
| `locationUrl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the optional location url where message should be sent to |
| --- | --- |
| `configOverrides` | [Bundle](../android.os/Bundle.md)!: the carrier-specific messaging configuration values to override for sending the message. |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is successfully sent, or failed The result code will be `Activity.RESULT_OK` for success or one of these errors: `MMS_ERROR_UNSPECIFIED` `MMS_ERROR_INVALID_APN` `MMS_ERROR_UNABLE_CONNECT_MMS` `MMS_ERROR_HTTP_FAILURE` `MMS_ERROR_IO_ERROR` `MMS_ERROR_RETRY` `MMS_ERROR_CONFIGURATION_ERROR` `MMS_ERROR_NO_DATA_NETWORK` `MMS_ERROR_INVALID_SUBSCRIPTION_ID` `MMS_ERROR_INACTIVE_SUBSCRIPTION` `MMS_ERROR_DATA_DISABLED` `MMS_ERROR_MMS_DISABLED_BY_CARRIER` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if contentUri is empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendMultimediaMessage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMultimediaMessage(
    context: Context, 
    contentUri: Uri, 
    locationUrl: String?, 
    configOverrides: Bundle?, 
    sentIntent: PendingIntent?, 
    messageId: Long
): Unit
```

Send an MMS message Same as sendMultimediaMessage, but adds an optional messageId.

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail sending the MMS message because no suitable default subscription could be found. In this case, if `sentIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_NO_DEFAULT_SMS_APP`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): application context. This value cannot be `null`. |
| `contentUri` | [Uri](../android.net/Uri.md): the content Uri from which the message pdu will be read. This value cannot be `null`. |
| `locationUrl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the optional location url where message should be sent to. This value may be `null`. |
| --- | --- |
| `configOverrides` | [Bundle](../android.os/Bundle.md)?: the carrier-specific messaging configuration values to override for sending the message. This value may be `null`. |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)?: if not NULL this `PendingIntent` is broadcast when the message is successfully sent, or failed The result code will be `Activity.RESULT_OK` for success or one of these errors: `MMS_ERROR_UNSPECIFIED` `MMS_ERROR_INVALID_APN` `MMS_ERROR_UNABLE_CONNECT_MMS` `MMS_ERROR_HTTP_FAILURE` `MMS_ERROR_IO_ERROR` `MMS_ERROR_RETRY` `MMS_ERROR_CONFIGURATION_ERROR` `MMS_ERROR_NO_DATA_NETWORK` `MMS_ERROR_INVALID_SUBSCRIPTION_ID` `MMS_ERROR_INACTIVE_SUBSCRIPTION` `MMS_ERROR_DATA_DISABLED` `MMS_ERROR_MMS_DISABLED_BY_CARRIER` . This value may be `null`. |
| `messageId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): an id that uniquely identifies the message requested to be sent. Used for logging and diagnostics purposes. The id may be 0. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if contentUri is empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendMultipartTextMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMultipartTextMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    parts: ArrayList<String!>!, 
    sentIntents: ArrayList<PendingIntent!>!, 
    deliveryIntents: ArrayList<PendingIntent!>!
): Unit
```

Send a multi-part text based SMS. The callee should have already divided the message into correctly sized parts by calling `divideMessage`

**Note:** Using this method requires that your app has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` permission.

**Note:** Beginning with Android 4.4 (API level 19), if *and only if* an app is not selected as the default SMS app, the system automatically writes messages sent using this method to the SMS Provider (the default SMS app is always responsible for writing its sent messages to the SMS Provider). For information about how to behave as the default SMS app, see `https://developer.android.com/reference/kotlin/android/provider/Telephony.html#`.

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail sending the SMS message because no suitable default subscription could be found. In this case, if `sentIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_ERROR_GENERIC_FAILURE` and an extra string `"noDefault"` containing the boolean value `true`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: is the service center address or null to use the current default SMSC |
| `parts` | [ArrayList](../java.util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an `ArrayList` of strings that, in order, comprise the original message |
| --- | --- |
| `sentIntents` | [ArrayList](../java.util/ArrayList.md)\< [PendingIntent](../android.app/PendingIntent.md)!\>!: if not null, an `ArrayList` of `PendingIntent`s (one for each message part) that is broadcast when the corresponding message part has been sent. The result code will be `Activity.RESULT_OK` for success, or one of these errors: `RESULT_ERROR_GENERIC_FAILURE` `RESULT_ERROR_RADIO_OFF` `RESULT_ERROR_NULL_PDU` `RESULT_ERROR_NO_SERVICE` `RESULT_ERROR_LIMIT_EXCEEDED` `RESULT_ERROR_FDN_CHECK_FAILURE` `RESULT_ERROR_SHORT_CODE_NOT_ALLOWED` `RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED` `RESULT_RADIO_NOT_AVAILABLE` `RESULT_NETWORK_REJECT` `RESULT_INVALID_ARGUMENTS` `RESULT_INVALID_STATE` `RESULT_NO_MEMORY` `RESULT_INVALID_SMS_FORMAT` `RESULT_SYSTEM_ERROR` `RESULT_MODEM_ERROR` `RESULT_NETWORK_ERROR` `RESULT_ENCODING_ERROR` `RESULT_INVALID_SMSC_ADDRESS` `RESULT_OPERATION_NOT_ALLOWED` `RESULT_INTERNAL_ERROR` `RESULT_NO_RESOURCES` `RESULT_CANCELLED` `RESULT_REQUEST_NOT_SUPPORTED` `RESULT_NO_BLUETOOTH_SERVICE` `RESULT_INVALID_BLUETOOTH_ADDRESS` `RESULT_BLUETOOTH_DISCONNECTED` `RESULT_UNEXPECTED_EVENT_STOP_SENDING` `RESULT_SMS_BLOCKED_DURING_EMERGENCY` `RESULT_SMS_SEND_RETRY_FAILED` `RESULT_REMOTE_EXCEPTION` `RESULT_NO_DEFAULT_SMS_APP` `RESULT_RIL_RADIO_NOT_AVAILABLE` `RESULT_RIL_SMS_SEND_FAIL_RETRY` `RESULT_RIL_NETWORK_REJECT` `RESULT_RIL_INVALID_STATE` `RESULT_RIL_INVALID_ARGUMENTS` `RESULT_RIL_NO_MEMORY` `RESULT_RIL_REQUEST_RATE_LIMITED` `RESULT_RIL_INVALID_SMS_FORMAT` `RESULT_RIL_SYSTEM_ERR` `RESULT_RIL_ENCODING_ERR` `RESULT_RIL_INVALID_SMSC_ADDRESS` `RESULT_RIL_MODEM_ERR` `RESULT_RIL_NETWORK_ERR` `RESULT_RIL_INTERNAL_ERR` `RESULT_RIL_REQUEST_NOT_SUPPORTED` `RESULT_RIL_INVALID_MODEM_STATE` `RESULT_RIL_NETWORK_NOT_READY` `RESULT_RIL_OPERATION_NOT_ALLOWED` `RESULT_RIL_NO_RESOURCES` `RESULT_RIL_CANCELLED` `RESULT_RIL_SIM_ABSENT` `RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED` `RESULT_RIL_ACCESS_BARRED` `RESULT_RIL_BLOCKED_DUE_TO_CALL` For `RESULT_ERROR_GENERIC_FAILURE` or any of the RESULT_RIL errors, the sentIntent may include the extra "errorCode" containing a radio technology specific value, generally only useful for troubleshooting. |
| `deliveryIntents` | [ArrayList](../java.util/ArrayList.md)\< [PendingIntent](../android.app/PendingIntent.md)!\>!: if not null, an `ArrayList` of `PendingIntent`s (one for each message part) that is broadcast when the corresponding message part has been delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if destinationAddress or data are empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendMultipartTextMessage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMultipartTextMessage(
    destinationAddress: String, 
    scAddress: String?, 
    parts: MutableList<String!>, 
    sentIntents: MutableList<PendingIntent!>?, 
    deliveryIntents: MutableList<PendingIntent!>?, 
    packageName: String, 
    attributionTag: String?
): Unit
```

Similar method as #sendMultipartTextMessage(String, String, ArrayList, ArrayList, ArrayList) With an additional argument.

**Note:** This method is intended for internal use the Telephony framework and will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the SMS being sent on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the SMS is sent on the correct subscription.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `parts` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |
| --- | --- |
| `sentIntents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PendingIntent](../android.app/PendingIntent.md)!\>?: This value may be `null`. |
| `deliveryIntents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PendingIntent](../android.app/PendingIntent.md)!\>?: This value may be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): serves as the default package name if the package name that is associated with the user id is null. |
| --- | --- |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendMultipartTextMessage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMultipartTextMessage(
    destinationAddress: String, 
    scAddress: String?, 
    parts: MutableList<String!>, 
    sentIntents: MutableList<PendingIntent!>?, 
    deliveryIntents: MutableList<PendingIntent!>?, 
    messageId: Long
): Unit
```

Send a multi-part text based SMS. Same as #sendMultipartTextMessage(String, String, ArrayList, ArrayList, ArrayList), but adds an optional messageId. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `parts` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |
| --- | --- |
| `sentIntents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PendingIntent](../android.app/PendingIntent.md)!\>?: This value may be `null`. |
| `deliveryIntents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PendingIntent](../android.app/PendingIntent.md)!\>?: This value may be `null`. |
| `messageId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): An id that uniquely identifies the message requested to be sent. Used for logging and diagnostics purposes. The id may be 0. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if destinationAddress or data are empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendTextMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendTextMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    text: String!, 
    sentIntent: PendingIntent!, 
    deliveryIntent: PendingIntent!
): Unit
```

Send a text based SMS.

**Note:** Using this method requires that your app has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` permission.

**Note:** Beginning with Android 4.4 (API level 19), if *and only if* an app is not selected as the default SMS app, the system automatically writes messages sent using this method to the SMS Provider (the default SMS app is always responsible for writing its sent messages to the SMS Provider). For information about how to behave as the default SMS app, see `https://developer.android.com/reference/kotlin/android/provider/Telephony.html#`.

**Note:** If getDefault is used to instantiate this manager on a multi-SIM device, this operation may fail sending the SMS message because no suitable default subscription could be found. In this case, if `sentIntent` is non-null, then the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` will be sent with an error code `RESULT_ERROR_GENERIC_FAILURE` and an extra string `"noDefault"` containing the boolean value `true`. See getDefault for more information on the conditions where this operation may fail.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: is the service center address or null to use the current default SMSC |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the body of the message to send |
| --- | --- |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is successfully sent, or failed. The result code will be `Activity.RESULT_OK` for success, or one of these errors: `RESULT_ERROR_GENERIC_FAILURE` `RESULT_ERROR_RADIO_OFF` `RESULT_ERROR_NULL_PDU` `RESULT_ERROR_NO_SERVICE` `RESULT_ERROR_LIMIT_EXCEEDED` `RESULT_ERROR_FDN_CHECK_FAILURE` `RESULT_ERROR_SHORT_CODE_NOT_ALLOWED` `RESULT_ERROR_SHORT_CODE_NEVER_ALLOWED` `RESULT_RADIO_NOT_AVAILABLE` `RESULT_NETWORK_REJECT` `RESULT_INVALID_ARGUMENTS` `RESULT_INVALID_STATE` `RESULT_NO_MEMORY` `RESULT_INVALID_SMS_FORMAT` `RESULT_SYSTEM_ERROR` `RESULT_MODEM_ERROR` `RESULT_NETWORK_ERROR` `RESULT_ENCODING_ERROR` `RESULT_INVALID_SMSC_ADDRESS` `RESULT_OPERATION_NOT_ALLOWED` `RESULT_INTERNAL_ERROR` `RESULT_NO_RESOURCES` `RESULT_CANCELLED` `RESULT_REQUEST_NOT_SUPPORTED` `RESULT_NO_BLUETOOTH_SERVICE` `RESULT_INVALID_BLUETOOTH_ADDRESS` `RESULT_BLUETOOTH_DISCONNECTED` `RESULT_UNEXPECTED_EVENT_STOP_SENDING` `RESULT_SMS_BLOCKED_DURING_EMERGENCY` `RESULT_SMS_SEND_RETRY_FAILED` `RESULT_REMOTE_EXCEPTION` `RESULT_NO_DEFAULT_SMS_APP` `RESULT_RIL_RADIO_NOT_AVAILABLE` `RESULT_RIL_SMS_SEND_FAIL_RETRY` `RESULT_RIL_NETWORK_REJECT` `RESULT_RIL_INVALID_STATE` `RESULT_RIL_INVALID_ARGUMENTS` `RESULT_RIL_NO_MEMORY` `RESULT_RIL_REQUEST_RATE_LIMITED` `RESULT_RIL_INVALID_SMS_FORMAT` `RESULT_RIL_SYSTEM_ERR` `RESULT_RIL_ENCODING_ERR` `RESULT_RIL_INVALID_SMSC_ADDRESS` `RESULT_RIL_MODEM_ERR` `RESULT_RIL_NETWORK_ERR` `RESULT_RIL_INTERNAL_ERR` `RESULT_RIL_REQUEST_NOT_SUPPORTED` `RESULT_RIL_INVALID_MODEM_STATE` `RESULT_RIL_NETWORK_NOT_READY` `RESULT_RIL_OPERATION_NOT_ALLOWED` `RESULT_RIL_NO_RESOURCES` `RESULT_RIL_CANCELLED` `RESULT_RIL_SIM_ABSENT` `RESULT_RIL_SIMULTANEOUS_SMS_AND_CALL_NOT_ALLOWED` `RESULT_RIL_ACCESS_BARRED` `RESULT_RIL_BLOCKED_DUE_TO_CALL` For `RESULT_ERROR_GENERIC_FAILURE` or any of the RESULT_RIL errors, the sentIntent may include the extra "errorCode" containing a radio technology specific value, generally only useful for troubleshooting. |
| `deliveryIntent` | [PendingIntent](../android.app/PendingIntent.md)!: if not NULL this `PendingIntent` is broadcast when the message is delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if destinationAddress or text are empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendTextMessage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendTextMessage(
    destinationAddress: String, 
    scAddress: String?, 
    text: String, 
    sentIntent: PendingIntent?, 
    deliveryIntent: PendingIntent?, 
    messageId: Long
): Unit
```

Send a text based SMS. Same as sendTextMessage, but adds an optional messageId. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| --- | --- |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)?: This value may be `null`. |
| `deliveryIntent` | [PendingIntent](../android.app/PendingIntent.md)?: This value may be `null`. |
| `messageId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): An id that uniquely identifies the message requested to be sent. Used for logging and diagnostics purposes. The id may be 0. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if destinationAddress or text are empty |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### sendTextMessageWithoutPersisting

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendTextMessageWithoutPersisting(
    destinationAddress: String!, 
    scAddress: String!, 
    text: String!, 
    sentIntent: PendingIntent!, 
    deliveryIntent: PendingIntent!
): Unit
```

Send a text based SMS without writing it into the SMS Provider.

The message will be sent directly over the network and will not be visible in SMS applications. Intended for internal carrier use only.

Requires Permission: Both `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`, or that the calling app has carrier privileges (see hasCarrierPrivileges), or that the calling app is the default IMS app (see `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CONFIG_IMS_PACKAGE_OVERRIDE_STRING:kotlin.String`).

**Note:** This method is intended for internal use by carrier applications or the Telephony framework and will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this message will be INVALID, which will result in the SMS being sent on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the SMS is sent on the correct subscription.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

**See Also**

- sendTextMessage

### setSmscAddress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSmscAddress(smsc: String): Boolean
```

Sets the SMSC address on (U)SIM.

**Note:** Using this method requires that your app is the default SMS application, or has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` permission, or has the carrier privileges.

**Note:** This method will never trigger an SMS disambiguation dialog. If this method is called on a device that has multiple active subscriptions, this SmsManager instance has been created with getDefault, and no user-defined default subscription is defined, the subscription ID associated with this method will be INVALID, which will result in the operation being completed on the subscription associated with logical slot 0. Use getSmsManagerForSubscriptionId to ensure the operation is performed on the correct subscription.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `smsc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the SMSC address string. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true for success, false otherwise. Failure can be due modem returning an error. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |
