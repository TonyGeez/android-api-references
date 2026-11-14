Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiManager

```
open class WifiManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiManager](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#) |

This class provides the primary API for managing all aspects of Wi-Fi connectivity.

On releases before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, this object should only be obtained from an [application context](https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()), and not from any other derived context to avoid memory leaks within the calling process.

It deals with several categories of items:

- The list of configured networks. The list can be viewed and updated, and attributes of individual entries can be modified.
- The currently active Wi-Fi network, if any. Connectivity can be established or torn down, and dynamic information about the state of the network can be queried.
- Results of access point scans, containing enough information to make decisions about what access point to connect to.
- It defines the names of various Intent actions that are broadcast upon any sort of change in Wi-Fi state.

This is the API to use when performing Wi-Fi specific operations. To perform operations that pertain to network connectivity at an abstract level, use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`.
. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.AddNetworkResult` Provides the results of a call to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkPrivileged(android.net.wifi.WifiConfiguration)` |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.InterfaceCreationImpact` Class describing an impact of interface creation - returned by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#reportCreateInterfaceImpact(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.BiConsumer)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener` Interface for local-only connection failure listener. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback` Callback class for applications to receive updates about the LocalOnlyHotspot status. |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotReservation` LocalOnlyHotspotReservation that contains the `https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration` for the active LocalOnlyHotspot request. |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.MulticastLock` Allows an application to receive Wifi Multicast packets. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback` Abstract class for scan results callback. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` Abstract callback class for applications to receive updates about the Wi-Fi subsystem restarting. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener` Interface for suggestion connection status listener. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener` Interface for network suggestion user approval status change listener. |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock` Allows an application to keep the Wi-Fi radio awake. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener` Listener interface for applications to be notified when the Wi-Fi enabled state changes. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback` Interface for callback invocation on a start WPS action |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_PICK_WIFI_NETWORK:kotlin.String` Activity Action: Pick a Wi-Fi network to connect to. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int` If one of the removed suggestions is currently connected, trigger an immediate disconnect after suggestions removal |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_LINGER:kotlin.Int` If one of the removed suggestions is currently connected, that network will be disconnected after a short delay as opposed to immediately (which will be done by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int`). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REQUEST_SCAN_ALWAYS_AVAILABLE:kotlin.String` Activity Action: Show a system activity that allows the user to enable scans to be available even with Wi-Fi turned off. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION:kotlin.String` Directed broadcast intent action indicating that the device has connected to one of the network suggestions provided by the app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_SCAN_AVAILABILITY_CHANGED:kotlin.String` Broadcast intent action indicating whether Wi-Fi scanning is currently available. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_FREQUENCY_MHZ:kotlin.String` The bundle key string for the channel frequency in MHz. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_NUM_AP:kotlin.String` The bundle key for the number of APs found on the corresponding channel specified by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_FREQUENCY_MHZ:kotlin.String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ERROR_AUTHENTICATING:kotlin.Int` The error code if there was a problem authenticating. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_BSSID:kotlin.String` The lookup key for a String giving the BSSID of the access point to which we are connected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NETWORK_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` object associated with the Wi-Fi network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NETWORK_SUGGESTION:kotlin.String` Sent as as a part of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION:kotlin.String` that holds an instance of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` corresponding to the connected network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NEW_RSSI:kotlin.String` The lookup key for an `int` giving the new RSSI in dBm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NEW_STATE:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState` describing the new state Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_PREVIOUS_WIFI_STATE:kotlin.String` The previous Wi-Fi state. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_RESULTS_UPDATED:kotlin.String` Lookup key for a `boolean` extra in intent `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#SCAN_RESULTS_AVAILABLE_ACTION:kotlin.String` representing if the scan was successful or not. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SCAN_AVAILABLE:kotlin.String` A boolean extra indicating whether scanning is currently available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SUPPLICANT_CONNECTED:kotlin.String` The lookup key for a boolean that indicates whether a connection to the supplicant daemon has been gained or lost. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SUPPLICANT_ERROR:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState` describing the supplicant error code if any Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_WIFI_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo` object giving the information about the access point to which we are connected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_WIFI_STATE:kotlin.String` The lookup key for an int that indicates whether Wi-Fi is enabled, disabled, enabling, disabling, or unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_OPEN:kotlin.Int` Do not send the DHCP hostname to open networks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_SECURE:kotlin.Int` Do not send the DHCP hostname to secure network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#NETWORK_IDS_CHANGED_ACTION:kotlin.String` The network IDs of the configured networks could have changed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#NETWORK_STATE_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that the state of Wi-Fi connectivity has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_AGGRESSIVE:kotlin.Int` Allows the device to roam more quickly than the normal roaming mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_NONE:kotlin.Int` Roaming is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_NORMAL:kotlin.Int` Chipset has roaming trigger capability based on the score calculated using multiple parameters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#RSSI_CHANGED_ACTION:kotlin.String` The RSSI (signal strength) has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#SCAN_RESULTS_AVAILABLE_ACTION:kotlin.String` An access point scan has completed, and results are available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION:kotlin.Int` Reason code if local-only network connection attempt failed with association failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION:kotlin.Int` Reason code if local-only network connection attempt failed with an authentication failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING:kotlin.Int` Reason code if local-only network connection attempt failed with an IP provisioning failure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND:kotlin.Int` Reason code if local-only network connection attempt failed with AP not in range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE:kotlin.Int` Reason code if local-only network connection attempt failed with AP not responding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN:kotlin.Int` Reason code if local-only network connection attempt failed with an unknown failure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT:kotlin.Int` Reason code if local-only network request rejected by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE:kotlin.Int` Reason code if one or more of the network suggestions added already exists in platform's database. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP:kotlin.Int` Reason code if the number of network suggestions provided by the app crosses the max threshold set per app. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID:kotlin.Int` Reason code if one or more of the network suggestions added is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED:kotlin.Int` Reason code if one or more of the network suggestions added is not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED:kotlin.Int` Reason code if the user has disallowed "android:change_wifi_state" app-ops from the app. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL:kotlin.Int` Reason code if there was an internal error in the platform while processing the addition or removal of suggestions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID:kotlin.Int` Reason code if one or more of the network suggestions removed does not exist in platform's database. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN:kotlin.Int` Reason code if `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_WIFI_CONFIG:kotlin.String` user restriction is set and calling app is restricted by device admin. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_SUCCESS:kotlin.Int` Reason code if all of the network suggestions were successfully added or removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE:kotlin.Int` Status code if the calling app was approved by virtue of being a carrier privileged app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER:kotlin.Int` Status code if the calling app got the user approval for suggestions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_PENDING:kotlin.Int` Status code if the calling app is still pending user approval for suggestions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER:kotlin.Int` Status code if the calling app suggestions were rejected by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_UNKNOWN:kotlin.Int` Status code if suggestion approval status is unknown, an App which hasn't made any suggestions will get this code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION:kotlin.Int` Reason code if suggested network connection attempt failed with association failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION:kotlin.Int` Reason code if suggested network connection attempt failed with an authentication failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING:kotlin.Int` Reason code if suggested network connection attempt failed with an IP provision failure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN:kotlin.Int` Reason code if suggested network connection attempt failed with an unknown failure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#SUPPLICANT_CONNECTION_CHANGE_ACTION:kotlin.String` Broadcast intent action indicating that a connection to the supplicant has been established (and it is now possible to perform Wi-Fi operations) or the connection to the supplicant has been lost. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#SUPPLICANT_STATE_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that the state of establishing a connection to an access point has changed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#UNKNOWN_SSID:kotlin.String` Indicates an invalid SSID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AP:kotlin.Int` Wi-Fi interface of type AP (access point Wi-Fi infrastructure device). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AWARE:kotlin.Int` Wi-Fi interface of type Wi-Fi Aware (aka NAN). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_DIRECT:kotlin.Int` Wi-Fi interface of type Wi-Fi Direct (aka P2P). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_STA:kotlin.Int` Wi-Fi interface of type STA (station/client Wi-Fi infrastructure device). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL:kotlin.Int` In this Wi-Fi lock mode, Wi-Fi will be kept active, and will behave normally, i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` In this Wi-Fi lock mode, Wi-Fi will not go to power save. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` In this Wi-Fi lock mode, Wi-Fi will operate with a priority to achieve low latency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_SCAN_ONLY:kotlin.Int` In this Wi-Fi lock mode, Wi-Fi will be kept active, but the only operation that will be supported is initiation of scans, and the subsequent reporting of scan results. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DBS_AP:kotlin.Int` Wi-Fi simultaneous connection to multiple internet-providing Wi-FI networks (APs) is enabled and restricted to a single network on different bands (e.g. a DBS AP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DISABLED:kotlin.Int` Wi-Fi simultaneous connection to multiple internet-providing Wi-Fi networks (APs) is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_MULTI_AP:kotlin.Int` Wi-Fi simultaneous connection to multiple internet-providing Wi-Fi networks (APs) is enabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that Wi-Fi has been enabled, disabled, enabling, disabling, or unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLED:kotlin.Int` Wi-Fi is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLING:kotlin.Int` Wi-Fi is currently being disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLED:kotlin.Int` Wi-Fi is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLING:kotlin.Int` Wi-Fi is currently being enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_UNKNOWN:kotlin.Int` Wi-Fi is in an unknown state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WPS_AUTH_FAILURE:kotlin.Int` Authentication failure on WPS |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WPS_OVERLAP_ERROR:kotlin.Int` WPS overlap detected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WPS_TIMED_OUT:kotlin.Int` WPS timed out |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WPS_TKIP_ONLY_PROHIBITED:kotlin.Int` TKIP only prohibited |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WPS_WEP_PROHIBITED:kotlin.Int` WEP on WPS is prohibited |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addLocalOnlyConnectionFailureListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener)` Add a listener for local-only networks. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)(config: https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration!)` Add a new network description to the set of configured networks. |
| open [WifiManager.AddNetworkResult](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.AddNetworkResult) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkPrivileged(android.net.wifi.WifiConfiguration)(config: https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration)` This is a new version of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)` which returns more detailed failure codes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)(networkSuggestions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion!>)` Provide a list of network suggestions to the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addOrUpdatePasspointConfiguration(android.net.wifi.hotspot2.PasspointConfiguration)(config: https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration!)` Add or update a Passpoint configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionConnectionStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionConnectionStatusListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener)` Add a listener for suggestion networks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener)` Add a listener for Wi-Fi network suggestion user approval status. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addWifiStateChangedListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.WifiStateChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener)` Register a callback for Wi-Fi state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#allowAutojoinGlobal(kotlin.Boolean)(allowAutojoin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Control whether the device will automatically search for and connect to Wi-Fi networks - auto-join Wi-Fi networks. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#calculateSignalLevel(kotlin.Int)(rssi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Given a raw RSSI, return the RSSI signal quality rating using the system default RSSI quality rating thresholds. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#calculateSignalLevel(kotlin.Int,%20kotlin.Int)(rssi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, numLevels: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Calculates the level of the signal. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#cancelWps(android.net.wifi.WifiManager.WpsCallback)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback!)` WPS support has been deprecated from Client mode and this method will immediately trigger `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback#onFailed(kotlin.Int)` with a generic error. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#compareSignalLevel(kotlin.Int,%20kotlin.Int)(rssiA: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rssiB: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Compares two signal strengths. |
| open [WifiManager.MulticastLock](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.MulticastLock)! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#createMulticastLock(kotlin.String)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a new MulticastLock |
| open [WifiManager.WifiLock](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock)! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#createWifiLock(kotlin.Int,%20kotlin.String)(lockType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new WifiLock. |
| --- | --- |
| open [WifiManager.WifiLock](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock)! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#createWifiLock(kotlin.String)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new WifiLock. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#disableNetwork(kotlin.Int)(netId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Disable a configured network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#disallowCurrentSuggestedNetwork(android.net.wifi.BlockingOption)(blockingOption: https://developer.android.com/reference/kotlin/android/net/wifi/BlockingOption)` When the device is connected to a network suggested by calling app `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, this API provide a way to avoid the current connection without `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#disconnect()()` Disassociate from the currently active access point. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#enableNetwork(kotlin.Int,%20kotlin.Boolean)(netId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, attemptConnect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Allow a previously configured network to be associated with. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#flushPasspointAnqpCache()()` Flush Passpoint ANQP cache, and clear pending ANQP requests. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiAvailableChannel](https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getAllowedChannels(kotlin.Int,%20kotlin.Int)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` for the specified band and operational mode(s), that is allowed for the current regulatory domain. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getCallerConfiguredNetworks()()` Return a list of all the networks previously configured by the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getChannelData(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>!>)` Get channel data such as the number of APs found on each channel from the most recent scan. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration)!\>! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getConfiguredNetworks()()` Return a list of all the networks configured for the current foreground user. |
| open [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo)! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getConnectionInfo()()` Return dynamic information about the current Wi-Fi connection, if any is active. |
| open [DhcpInfo](https://developer.android.com/reference/kotlin/android/net/DhcpInfo.html#)! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getDhcpInfo()()` Return the DHCP-assigned addresses from the last successful DHCP request, if any. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxNumberOfChannelsPerNetworkSpecifierRequest()()` Returns the max number of channels that is allowed to be set on a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxNumberOfNetworkSuggestionsPerApp()()` Returns the max number of network suggestions that are allowed per app on the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxSignalLevel()()` Get the system default maximum signal level. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxSupportedConcurrentTdlsSessions(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Return the maximum number of concurrent TDLS sessions supported by the device. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getNetworkSuggestions()()` Get all network suggestions provided by the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getNumberOfEnabledTdlsSessions(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Return the number of currently enabled TDLS sessions. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PasspointConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration)!\>! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getPasspointConfigurations()()` Return the list of installed Passpoint configurations added by the caller. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getPerSsidRoamingModes(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>)` This API allows a privileged application to get roaming mode policies configured using the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult)!\>! | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getScanResults()()` Return the results of the latest access point scan. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getStaConcurrencyForMultiInternetMode()()` The device may support concurrent connections to multiple internet-providing Wi-Fi networks (APs) - that is indicated by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForMultiInternetSupported()`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiAvailableChannel](https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getUsableChannels(kotlin.Int,%20kotlin.Int)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` for the specified band and operational mode(s) per the current regulatory domain and device-specific constraints such as concurrency state and interference due to other radios. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()()` Gets the Wi-Fi enabled state. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#is24GHzBandSupported()()` Check if the chipset supports 2. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#is5GHzBandSupported()()` Check if the chipset supports 5GHz band. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#is60GHzBandSupported()()` Check if the chipset supports the 60GHz frequency band. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#is6GHzBandSupported()()` Check if the chipset supports 6GHz band. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isAggressiveRoamingModeSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isAutoWakeupEnabled()()` Get the persisted Wi-Fi auto wakeup feature state. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isBridgedApConcurrencySupported()()` Query whether or not the device supports multiple Access point (AP) which are bridged together. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isCarrierNetworkOffloadEnabled(kotlin.Int,%20kotlin.Boolean)(subscriptionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, merged: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Get the carrier network offload state for merged or unmerged networks for specified subscription. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isD2dSupportedWhenInfraStaDisabled()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isDecoratedIdentitySupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isDeviceToApRttSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isDualBandSimultaneousSupported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEasyConnectDppAkmSupported()()` Wi-Fi Easy Connect DPP AKM enables provisioning and configuration of Wi-Fi devices without the need of using the device PSK passphrase. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEasyConnectEnrolleeResponderModeSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEasyConnectSupported()()` Wi-Fi Easy Connect (DPP) introduces standardized mechanisms to simplify the provisioning and configuration of Wi-Fi devices. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEnhancedOpenSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEnhancedPowerReportingSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isMakeBeforeBreakWifiSwitchingSupported()()` Query whether or not the device supports concurrent station (STA) connections for make-before-break wifi to wifi switching. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isP2pSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isPasspointTermsAndConditionsSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isPreferredNetworkOffloadSupported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isScanAlwaysAvailable()()` Check if scanning is always available. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isScanThrottleEnabled()()` Get the persisted Wi-Fi scan throttle state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaApConcurrencySupported()()` Query whether or not the device supports Station (STA) + Access point (AP) concurrency. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaBridgedApConcurrencySupported()()` Query whether or not the device supports concurrency of Station (STA) + multiple access points (AP) (where the APs bridged together). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForLocalOnlyConnectionsSupported()()` Query whether or not the device supports concurrent station (STA) connections for local-only connections using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForMultiInternetSupported()()` Query whether or not the device supports concurrent station (STA) connections for multi internet connections. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTdlsOperationCurrentlyAvailable(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Check if a TDLS session can be established at this time via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` Internally framework checks the STA connected state, device support for TDLS and the number of TDLS sessions available in driver/firmware. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTdlsSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTidToLinkMappingNegotiationSupported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTlsMinimumVersionSupported()()` Indicate that whether or not settings required TLS minimum version is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTlsV13Supported()()` Indicate that whether or not TLS v1. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTrustOnFirstUseSupported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWapiSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWepSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiDisplayR2Supported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiEnabled()()` Return whether Wi-Fi is enabled or disabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiPasspointEnabled()()` If the device supports Wi-Fi Passpoint, the user can explicitly enable or disable it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiStandardSupported(kotlin.Int)(standard: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check if the chipset supports a certain Wi-Fi standard. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWpa3SaeH2eSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWpa3SaePublicKeySupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWpa3SaeSupported()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWpa3SuiteBSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWpaPersonalSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#pingSupplicant()()` Check that the supplicant daemon is responding to requests. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#queryAutojoinGlobal(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Query whether or not auto-join global is enabled/disabled |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#querySendDhcpHostnameRestriction(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)` Query the global restriction on which networks to send the device hostname to during DHCP. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#reassociate()()` Reconnect to the currently active access point, even if we are already connected. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#reconnect()()` Reconnect to the currently active access point, if we are currently disconnected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#registerScanResultsCallback(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.ScanResultsCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback)` Register a callback for Scan Results. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#registerSubsystemRestartTrackingCallback(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SubsystemRestartTrackingCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback)` Registers a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` to listen to Wi-Fi subsystem restarts. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeLocalOnlyConnectionFailureListener(android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener)` Allow callers to remove a previously registered listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetwork(kotlin.Int)(netId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove the specified network from the list of configured networks. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)(networkSuggestions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion!>)` Remove some or all of the network suggestions that were previously provided by the app. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList,%20kotlin.Int)(networkSuggestions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion!>, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove some or all of the network suggestions that were previously provided by the app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNonCallerConfiguredNetworks()()` Remove all configured networks that were not created by the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removePasspointConfiguration(kotlin.String)(fqdn: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Remove the Passpoint configuration identified by its FQDN (Fully Qualified Domain Name) added by the caller. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removePerSsidRoamingMode(android.net.wifi.WifiSsid)(ssid: https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid)` This API allows a privileged application to remove roaming mode policy configured using the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeSuggestionConnectionStatusListener(android.net.wifi.WifiManager.SuggestionConnectionStatusListener)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener)` Allow callers to remove a previously registered listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeSuggestionUserApprovalStatusListener(android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener)` Allow callers to remove a previously registered listener using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeWifiStateChangedListener(android.net.wifi.WifiManager.WifiStateChangedListener)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener)` Unregisters a WifiStateChangedListener from listening on the current Wi-Fi state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#reportCreateInterfaceImpact(kotlin.Int,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.BiConsumer)(interfaceType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, requireNewInterface: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultCallback: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.InterfaceCreationImpact!>!>)` Queries the framework to determine whether the specified interface can be created, and if so - what other interfaces would be torn down by the framework to allow this creation if it were requested. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#saveConfiguration()()` Tell the device to persist the current list of configured networks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)(ssid: https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid, roamingMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This API allows a privileged application to set roaming mode per SSID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setSendDhcpHostnameRestriction(kotlin.Int)(restriction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the global restrictions on which networks to send the device hostname to during DHCP. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)(remoteIPAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable/Disable TDLS on a specific local route. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(remoteIPAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Enable/Disable TDLS on a specific local route. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean)(remoteMacAddress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Similar to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)`, except this version allows you to specify remote endpoint with a MAC address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(remoteMacAddress: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>)` Enable/Disable TDLS with a specific peer Mac Address. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setWifiEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable Wi-Fi. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startLocalOnlyHotspot(android.net.wifi.WifiManager.LocalOnlyHotspotCallback,%20android.os.Handler)(callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Request a local only hotspot that an application can use to communicate between co-located devices connected to the created WiFi hotspot. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startLocalOnlyHotspotWithConfiguration(android.net.wifi.SoftApConfiguration,%20java.util.concurrent.Executor,%20android.net.wifi.WifiManager.LocalOnlyHotspotCallback)(config: https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback)` Starts a local-only hotspot with a specific configuration applied. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startScan()()` Request a scan for access points. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startWps(android.net.wifi.WpsInfo,%20android.net.wifi.WifiManager.WpsCallback)(config: https://developer.android.com/reference/kotlin/android/net/wifi/WpsInfo!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback!)` WPS suport has been deprecated from Client mode and this method will immediately trigger `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback#onFailed(kotlin.Int)` with a generic error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#unregisterScanResultsCallback(android.net.wifi.WifiManager.ScanResultsCallback)(callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback)` Allow callers to unregister a previously registered callback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#unregisterSubsystemRestartTrackingCallback(android.net.wifi.WifiManager.SubsystemRestartTrackingCallback)(callback: https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback)` Unregisters a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` registered with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#registerSubsystemRestartTrackingCallback(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SubsystemRestartTrackingCallback)` Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#updateNetwork(android.net.wifi.WifiConfiguration)(config: https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration!)` Update the network description of an existing configured network. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#validateSoftApConfiguration(android.net.wifi.SoftApConfiguration)(config: https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration)` Check if input configuration is valid. |
| --- | --- |

## Constants

### ACTION_PICK_WIFI_NETWORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PICK_WIFI_NETWORK: String
```

Activity Action: Pick a Wi-Fi network to connect to.

Input: Nothing.

Output: Nothing.

 Value: "android.net.wifi.PICK_WIFI_NETWORK"

### ACTION_REMOVE_SUGGESTION_DISCONNECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REMOVE_SUGGESTION_DISCONNECT: Int
```

If one of the removed suggestions is currently connected, trigger an immediate disconnect after suggestions removal

 Value: 2

### ACTION_REMOVE_SUGGESTION_LINGER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REMOVE_SUGGESTION_LINGER: Int
```

If one of the removed suggestions is currently connected, that network will be disconnected after a short delay as opposed to immediately (which will be done by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int`). The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` may call the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onLosing(android.net.Network,%20kotlin.Int)` on such networks.

 Value: 1

### ACTION_REQUEST_SCAN_ALWAYS_AVAILABLE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_SCAN_ALWAYS_AVAILABLE: String
```

Activity Action: Show a system activity that allows the user to enable scans to be available even with Wi-Fi turned off.

Notification of the result of this activity is posted using the android.app.Activity#onActivityResult callback. The `resultCode` will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if scan always mode has been turned on or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if the user has rejected the request or an error has occurred.

 Value: "android.net.wifi.action.REQUEST_SCAN_ALWAYS_AVAILABLE"

### ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION: String
```

Directed broadcast intent action indicating that the device has connected to one of the network suggestions provided by the app. This will be sent post connection to a network which was created with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsAppInteractionRequired(kotlin.Boolean)` flag set.

Note: The broadcast is sent to the app only if it holds `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission.

 Value: "android.net.wifi.action.WIFI_NETWORK_SUGGESTION_POST_CONNECTION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NETWORK_SUGGESTION:kotlin.String`

### ACTION_WIFI_SCAN_AVAILABILITY_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_SCAN_AVAILABILITY_CHANGED: String
```

Broadcast intent action indicating whether Wi-Fi scanning is currently available. Available extras: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SCAN_AVAILABLE:kotlin.String`

 Value: "android.net.wifi.action.WIFI_SCAN_AVAILABILITY_CHANGED"

### CHANNEL_DATA_KEY_FREQUENCY_MHZ

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_DATA_KEY_FREQUENCY_MHZ: String
```

The bundle key string for the channel frequency in MHz. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getChannelData(java.util.concurrent.Executor,%20java.util.function.Consumer)`

 Value: "CHANNEL_DATA_KEY_FREQUENCY_MHZ"

### CHANNEL_DATA_KEY_NUM_AP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_DATA_KEY_NUM_AP: String
```

The bundle key for the number of APs found on the corresponding channel specified by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_FREQUENCY_MHZ:kotlin.String`. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getChannelData(java.util.concurrent.Executor,%20java.util.function.Consumer)`

 Value: "CHANNEL_DATA_KEY_NUM_AP"

### ERROR_AUTHENTICATING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_AUTHENTICATING: Int
```

**Deprecated:** *This is no longer supported.*

The error code if there was a problem authenticating.

 Value: 1

### EXTRA_BSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BSSID: String
```

**Deprecated:** *Deprecated in Java.*

The lookup key for a String giving the BSSID of the access point to which we are connected. No longer used.

 Value: "bssid"

### EXTRA_NETWORK_INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_INFO: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` object associated with the Wi-Fi network. Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "networkInfo"

### EXTRA_NETWORK_SUGGESTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_SUGGESTION: String
```

Sent as as a part of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION:kotlin.String` that holds an instance of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` corresponding to the connected network.

 Value: "android.net.wifi.extra.NETWORK_SUGGESTION"

### EXTRA_NEW_RSSI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NEW_RSSI: String
```

The lookup key for an `int` giving the new RSSI in dBm.

 Value: "newRssi"

### EXTRA_NEW_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NEW_STATE: String
```

**Deprecated:** *This is no longer supported.*

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState` describing the new state Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "newState"

### EXTRA_PREVIOUS_WIFI_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREVIOUS_WIFI_STATE: String
```

The previous Wi-Fi state.

 Value: "previous_wifi_state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_WIFI_STATE:kotlin.String`

### EXTRA_RESULTS_UPDATED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RESULTS_UPDATED: String
```

Lookup key for a `boolean` extra in intent `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#SCAN_RESULTS_AVAILABLE_ACTION:kotlin.String` representing if the scan was successful or not. Scans may fail for multiple reasons, these may include:

1. An app requested too many scans in a certain period of time. This may lead to additional scan request rejections via "scan throttling" for both foreground and background apps. Note: Apps holding android.Manifest.permission.NETWORK_SETTINGS permission are exempted from scan throttling.
2. The device is idle and scanning is disabled.
3. Wifi hardware reported a scan failure.

<br />

 Value: "resultsUpdated"

### EXTRA_SCAN_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SCAN_AVAILABLE: String
```

A boolean extra indicating whether scanning is currently available. Sent in the broadcast `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_SCAN_AVAILABILITY_CHANGED:kotlin.String`. Its value is true if scanning is currently available, false otherwise.

 Value: "android.net.wifi.extra.SCAN_AVAILABLE"

### EXTRA_SUPPLICANT_CONNECTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUPPLICANT_CONNECTED: String
```

**Deprecated:** *This is no longer supported.*

The lookup key for a boolean that indicates whether a connection to the supplicant daemon has been gained or lost. `true` means a connection now exists. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanExtra(kotlin.String,%20kotlin.Boolean)`.

 Value: "connected"

### EXTRA_SUPPLICANT_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUPPLICANT_ERROR: String
```

**Deprecated:** *This is no longer supported.*

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState` describing the supplicant error code if any Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`.

 Value: "supplicantError"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ERROR_AUTHENTICATING:kotlin.Int`

### EXTRA_WIFI_INFO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_INFO: String
```

**Deprecated:** *Deprecated in Java.*

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo` object giving the information about the access point to which we are connected. No longer used.

 Value: "wifiInfo"

### EXTRA_WIFI_STATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_STATE: String
```

The lookup key for an int that indicates whether Wi-Fi is enabled, disabled, enabling, disabling, or unknown. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`.

 Value: "wifi_state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_UNKNOWN:kotlin.Int`

### FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_OPEN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_OPEN: Int
```

Do not send the DHCP hostname to open networks.

 Value: 1

### FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_SECURE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_SECURE: Int
```

Do not send the DHCP hostname to secure network.

 Value: 2

### NETWORK_IDS_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_IDS_CHANGED_ACTION: String
```

The network IDs of the configured networks could have changed.

 Value: "android.net.wifi.NETWORK_IDS_CHANGED"

### NETWORK_STATE_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_STATE_CHANGED_ACTION: String
```

Broadcast intent action indicating that the state of Wi-Fi connectivity has changed. An extra provides the new state in the form of a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` object. No network-related permissions are required to subscribe to this broadcast.

This broadcast is not delivered to manifest receivers in applications that target API version 26 or later.

 Value: "android.net.wifi.STATE_CHANGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NETWORK_INFO:kotlin.String`

### ROAMING_MODE_AGGRESSIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROAMING_MODE_AGGRESSIVE: Int
```

Allows the device to roam more quickly than the normal roaming mode. Used in cases such as where APs are installed in a high density.

 Value: 2

### ROAMING_MODE_NONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROAMING_MODE_NONE: Int
```

Roaming is disabled.

 Value: 0

### ROAMING_MODE_NORMAL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROAMING_MODE_NORMAL: Int
```

Chipset has roaming trigger capability based on the score calculated using multiple parameters. If device is configured to this mode then it will be using chipset's normal (default) roaming.

 Value: 1

### RSSI_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RSSI_CHANGED_ACTION: String
```

The RSSI (signal strength) has changed. Receiver Required Permission: android.Manifest.permission.ACCESS_WIFI_STATE

 Value: "android.net.wifi.RSSI_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NEW_RSSI:kotlin.String`

### SCAN_RESULTS_AVAILABLE_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCAN_RESULTS_AVAILABLE_ACTION: String
```

An access point scan has completed, and results are available. Call `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getScanResults()` to obtain the results. The broadcast intent may contain an extra field with the key `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_RESULTS_UPDATED:kotlin.String` and a `boolean` value indicating if the scan was successful.

 Value: "android.net.wifi.SCAN_RESULTS"

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION: Int
```

Reason code if local-only network connection attempt failed with association failure.

 Value: 1

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION: Int
```

Reason code if local-only network connection attempt failed with an authentication failure.

 Value: 2

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING: Int
```

Reason code if local-only network connection attempt failed with an IP provisioning failure.

 Value: 3

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND: Int
```

Reason code if local-only network connection attempt failed with AP not in range.

 Value: 4

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE: Int
```

Reason code if local-only network connection attempt failed with AP not responding.

 Value: 5

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN: Int
```

Reason code if local-only network connection attempt failed with an unknown failure.

 Value: 0

### STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT: Int
```

Reason code if local-only network request rejected by the user.

 Value: 6

### STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE: Int
```

Reason code if one or more of the network suggestions added already exists in platform's database. Note: this code will not be returned with Android 11 as in-place modification is allowed, please check `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any)`

### STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP: Int
```

Reason code if the number of network suggestions provided by the app crosses the max threshold set per app. The framework will reject all suggestions provided by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)` if the total size exceeds the limit.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxNumberOfNetworkSuggestionsPerApp()`

### STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID: Int
```

Reason code if one or more of the network suggestions added is invalid. Framework will reject all the suggestions in the list. The framework will reject all suggestions provided by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)` if one or more of them is invalid. Please use `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder` to create network suggestions.

 Value: 7

### STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED: Int
```

Reason code if one or more of the network suggestions added is not allowed. The framework will reject all suggestions provided by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)` if one or more of them is not allowed. This error may be caused by suggestion is using SIM-based encryption method, but calling app is not carrier privileged.

 Value: 6

### STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED: Int
```

Reason code if the user has disallowed "android:change_wifi_state" app-ops from the app.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#unsafeCheckOp(kotlin.String,%20kotlin.Int,%20kotlin.String)`

### STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL: Int
```

Reason code if there was an internal error in the platform while processing the addition or removal of suggestions.

 Value: 1

### STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID: Int
```

Reason code if one or more of the network suggestions removed does not exist in platform's database. The framework won't remove any suggestions if one or more of suggestions provided by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` does not exist in database.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any)`

### STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN: Int
```

Reason code if `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_ADD_WIFI_CONFIG:kotlin.String` user restriction is set and calling app is restricted by device admin.

 Value: 8

### STATUS_NETWORK_SUGGESTIONS_SUCCESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NETWORK_SUGGESTIONS_SUCCESS: Int
```

Reason code if all of the network suggestions were successfully added or removed.

 Value: 0

### STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE: Int
```

Status code if the calling app was approved by virtue of being a carrier privileged app.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`

### STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER: Int
```

Status code if the calling app got the user approval for suggestions.

 Value: 2

### STATUS_SUGGESTION_APPROVAL_PENDING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_APPROVAL_PENDING: Int
```

Status code if the calling app is still pending user approval for suggestions.

 Value: 1

### STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER: Int
```

Status code if the calling app suggestions were rejected by the user.

 Value: 3

### STATUS_SUGGESTION_APPROVAL_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_APPROVAL_UNKNOWN: Int
```

Status code if suggestion approval status is unknown, an App which hasn't made any suggestions will get this code.

 Value: 0

### STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION: Int
```

Reason code if suggested network connection attempt failed with association failure.

 Value: 1

### STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION: Int
```

Reason code if suggested network connection attempt failed with an authentication failure.

 Value: 2

### STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING: Int
```

Reason code if suggested network connection attempt failed with an IP provision failure.

 Value: 3

### STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN: Int
```

Reason code if suggested network connection attempt failed with an unknown failure.

 Value: 0

### SUPPLICANT_CONNECTION_CHANGE_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPLICANT_CONNECTION_CHANGE_ACTION: String
```

**Deprecated:** *This is no longer supported.*

Broadcast intent action indicating that a connection to the supplicant has been established (and it is now possible to perform Wi-Fi operations) or the connection to the supplicant has been lost. One extra provides the connection state as a boolean, where `true` means CONNECTED.

 Value: "android.net.wifi.supplicant.CONNECTION_CHANGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SUPPLICANT_CONNECTED:kotlin.String`

### SUPPLICANT_STATE_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPLICANT_STATE_CHANGED_ACTION: String
```

**Deprecated:** *This is no longer supported.*

Broadcast intent action indicating that the state of establishing a connection to an access point has changed.One extra provides the new `https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState`. Note that the supplicant state is Wi-Fi specific, and is not generally the most useful thing to look at if you are just interested in the overall state of connectivity.

 Value: "android.net.wifi.supplicant.STATE_CHANGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_NEW_STATE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_SUPPLICANT_ERROR:kotlin.String`

### UNKNOWN_SSID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_SSID: String
```

Indicates an invalid SSID.

 Value: "<unknown ssid>"

### WIFI_INTERFACE_TYPE_AP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_INTERFACE_TYPE_AP: Int
```

Wi-Fi interface of type AP (access point Wi-Fi infrastructure device).

 Value: 1

### WIFI_INTERFACE_TYPE_AWARE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_INTERFACE_TYPE_AWARE: Int
```

Wi-Fi interface of type Wi-Fi Aware (aka NAN).

 Value: 2

### WIFI_INTERFACE_TYPE_DIRECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_INTERFACE_TYPE_DIRECT: Int
```

Wi-Fi interface of type Wi-Fi Direct (aka P2P).

 Value: 3

### WIFI_INTERFACE_TYPE_STA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_INTERFACE_TYPE_STA: Int
```

Wi-Fi interface of type STA (station/client Wi-Fi infrastructure device).

 Value: 0

### WIFI_MODE_FULL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MODE_FULL: Int
```

**Deprecated:** *This API is non-functional and will have no impact.*

In this Wi-Fi lock mode, Wi-Fi will be kept active, and will behave normally, i.e., it will attempt to automatically establish a connection to a remembered access point that is within range, and will do periodic scans if there are remembered access points but none are in range.

 Value: 1

### WIFI_MODE_FULL_HIGH_PERF

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MODE_FULL_HIGH_PERF: Int
```

**Deprecated:** *The `WIFI_MODE_FULL_HIGH_PERF` is deprecated and is automatically replaced with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` with all the restrictions documented on that lock. I.e. any request to the `WIFI_MODE_FULL_HIGH_PERF` will now obtain a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` lock instead. Deprecation is due to the impact of `WIFI_MODE_FULL_HIGH_PERF` on power dissipation. The `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` provides much of the same desired functionality with less impact on power dissipation.*

In this Wi-Fi lock mode, Wi-Fi will not go to power save. This results in operating with low packet latency. The lock is only active when the device is connected to an access point. The lock is active even when the device screen is off or the acquiring application is running in the background. This mode will consume more power and hence should be used only when there is a need for this tradeoff.

An example use case is when a voice connection needs to be kept active even after the device screen goes off. Holding a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` lock for the duration of the voice call may improve the call quality.

When there is no support from the hardware, the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` lock will have no impact.

 Value: 3

### WIFI_MODE_FULL_LOW_LATENCY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MODE_FULL_LOW_LATENCY: Int
```

In this Wi-Fi lock mode, Wi-Fi will operate with a priority to achieve low latency. `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` lock has the following limitations:

1. The lock is only active when the device is connected to an access point.
2. The lock is only active when the screen is on.
3. The lock is only active when the acquiring app is running in the foreground.

Low latency mode optimizes for reduced packet latency, and as a result other performance measures may suffer when there are trade-offs to make:

<!-- -->

1. Battery life may be reduced.
2. Throughput may be reduced.
3. Frequency of Wi-Fi scanning may be reduced. This may result in:
 - The device may not roam or switch to the AP with highest signal quality.
 - Location accuracy may be reduced.

<br />

Example use cases are real time gaming or virtual reality applications where low latency is a key factor for user experience.

Note: For an app which acquires both `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` locks, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` lock will be effective when app is running in foreground and screen is on, while the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` lock will take effect otherwise.

 Value: 4

### WIFI_MODE_SCAN_ONLY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MODE_SCAN_ONLY: Int
```

**Deprecated:** *This API is non-functional and will have no impact.*

In this Wi-Fi lock mode, Wi-Fi will be kept active, but the only operation that will be supported is initiation of scans, and the subsequent reporting of scan results. No attempts will be made to automatically connect to remembered access points, nor will periodic scans be automatically performed looking for remembered access points. Scans must be explicitly requested by an application in this mode.

 Value: 2

### WIFI_MULTI_INTERNET_MODE_DBS_AP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MULTI_INTERNET_MODE_DBS_AP: Int
```

Wi-Fi simultaneous connection to multiple internet-providing Wi-FI networks (APs) is enabled and restricted to a single network on different bands (e.g. a DBS AP).

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getStaConcurrencyForMultiInternetMode()`

### WIFI_MULTI_INTERNET_MODE_DISABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MULTI_INTERNET_MODE_DISABLED: Int
```

Wi-Fi simultaneous connection to multiple internet-providing Wi-Fi networks (APs) is disabled.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getStaConcurrencyForMultiInternetMode()`

### WIFI_MULTI_INTERNET_MODE_MULTI_AP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_MULTI_INTERNET_MODE_MULTI_AP: Int
```

Wi-Fi simultaneous connection to multiple internet-providing Wi-Fi networks (APs) is enabled. The device can connect to any networks/APs - it is just restricted to using different bands for individual connections.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getStaConcurrencyForMultiInternetMode()`

### WIFI_STATE_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_CHANGED_ACTION: String
```

Broadcast intent action indicating that Wi-Fi has been enabled, disabled, enabling, disabling, or unknown. One extra provides this state as an int. Another extra provides the previous state, if available. No network-related permissions are required to subscribe to this broadcast.

This broadcast is not delivered to manifest receivers in applications that target API version 26 or later.

 Value: "android.net.wifi.WIFI_STATE_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_WIFI_STATE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#EXTRA_PREVIOUS_WIFI_STATE:kotlin.String`

### WIFI_STATE_DISABLED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_DISABLED: Int
```

Wi-Fi is disabled.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### WIFI_STATE_DISABLING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_DISABLING: Int
```

Wi-Fi is currently being disabled. The state will change to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLED:kotlin.Int` if it finishes successfully.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### WIFI_STATE_ENABLED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_ENABLED: Int
```

Wi-Fi is enabled.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### WIFI_STATE_ENABLING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_ENABLING: Int
```

Wi-Fi is currently being enabled. The state will change to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLED:kotlin.Int` if it finishes successfully.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### WIFI_STATE_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_STATE_UNKNOWN: Int
```

Wi-Fi is in an unknown state. This state will occur when an error happens while enabling or disabling.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### WPS_AUTH_FAILURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WPS_AUTH_FAILURE: Int
```

**Deprecated:** *This is deprecated*

Authentication failure on WPS

 Value: 6

### WPS_OVERLAP_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WPS_OVERLAP_ERROR: Int
```

**Deprecated:** *This is deprecated*

WPS overlap detected

 Value: 3

### WPS_TIMED_OUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WPS_TIMED_OUT: Int
```

**Deprecated:** *This is deprecated*

WPS timed out

 Value: 7

### WPS_TKIP_ONLY_PROHIBITED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WPS_TKIP_ONLY_PROHIBITED: Int
```

**Deprecated:** *This is deprecated*

TKIP only prohibited

 Value: 5

### WPS_WEP_PROHIBITED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WPS_WEP_PROHIBITED: Int
```

**Deprecated:** *This is deprecated*

WEP on WPS is prohibited

 Value: 4

## Public methods

### addLocalOnlyConnectionFailureListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLocalOnlyConnectionFailureListener(
    executor: Executor, 
    listener: WifiManager.LocalOnlyConnectionFailureListener
): Unit
```

Add a listener for local-only networks. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier`. Specify the caller will only get connection failures for networks they requested. Caller can remove a previously registered listener using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeLocalOnlyConnectionFailureListener(android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener)` Same caller can add multiple listeners to monitor the event.

Applications should have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` permissions. Callers without the permission will trigger a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to execute the listener of the `listener` object. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [WifiManager.LocalOnlyConnectionFailureListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener): listener for local-only network connection failure. This value cannot be `null`. |

### addNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addNetwork(config: WifiConfiguration!): Int
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `-1`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Add a new network description to the set of configured networks. The `networkId` field of the supplied configuration object is ignored.

<br />

The new network will be marked DISABLED by default. To enable it, called `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#enableNetwork(kotlin.Int,%20kotlin.Boolean)`.

| Parameters ||
|---|---|
| `config` | [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration)!: the set of variables that describe the configuration, contained in a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` object. If the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` has an Http Proxy set the calling app must be System, or be provisioned as the Profile or Device Owner. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ID of the newly created network description. This is used in other operations to specified the network to be acted upon. Returns `-1` on failure. |

### addNetworkPrivileged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addNetworkPrivileged(config: WifiConfiguration): WifiManager.AddNetworkResult
```

This is a new version of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)` which returns more detailed failure codes. The usage of this API is limited to Device Owner (DO), Profile Owner (PO), system app, and privileged apps.

Add a new network description to the set of configured networks. The `networkId` field of the supplied configuration object is ignored. The new network will be marked DISABLED by default. To enable it, call `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#enableNetwork(kotlin.Int,%20kotlin.Boolean)`.

<br />

| Parameters ||
|---|---|
| `config` | [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration): the set of variables that describe the configuration, contained in a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` object. If the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` has an Http Proxy set the calling app must be System, or be provisioned as the Profile or Device Owner. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.AddNetworkResult` | A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.AddNetworkResult` Object. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input configuration is null or if the security type in input configuration is not supported. |
| `java.lang.SecurityException` | if the calling app is not a Device Owner (DO), Profile Owner (PO), system app, or a privileged app that has one of the permissions required by this API. |

### addNetworkSuggestions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addNetworkSuggestions(networkSuggestions: MutableList<WifiNetworkSuggestion!>): Int
```

Provide a list of network suggestions to the device. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` for a detailed explanation of the parameters. When the device decides to connect to one of the provided network suggestions, platform sends a directed broadcast `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_WIFI_NETWORK_SUGGESTION_POST_CONNECTION:kotlin.String` to the app if the network was created with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsAppInteractionRequired(kotlin.Boolean)` flag set and the app holds `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission.

NOTE:

- These networks are just a suggestion to the platform. The platform will ultimately decide on which network the device connects to.
- When an app is uninstalled or disabled, all its suggested networks are discarded. If the device is currently connected to a suggested network which is being removed then the device will disconnect from that network.
- If user reset network settings, all added suggestions will be discarded. Apps can use `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getNetworkSuggestions()` to check if their suggestions are in the device.
- In-place modification of existing suggestions are allowed.
 - If the provided suggestions include any previously provided suggestions by the app, previous suggestions will be updated.
 - If one of the provided suggestions marks a previously unmetered suggestion as metered and the device is currently connected to that suggested network, then the device will disconnect from that network. The system will immediately re-evaluate all the network candidates and possibly reconnect back to the same suggestion. This disconnect is to make sure that any traffic flowing over unmetered networks isn't accidentally continued over a metered network.
 - On `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or above If one of the provided suggestions marks a previously trusted suggestion as untrusted and the device is currently connected to that suggested network, then the device will disconnect from that network. The system will immediately re-evaluate all the network candidates. This disconnect is to make sure device will not remain connected to an untrusted network without a related `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#`.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkSuggestions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion)!\>: List of network suggestions provided by the app. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Status code for the operation. One of the STATUS_NETWORK_SUGGESTIONS_ values. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is missing required permissions. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any)`

### addOrUpdatePasspointConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOrUpdatePasspointConfiguration(config: PasspointConfiguration!): Unit
```

Add or update a Passpoint configuration. The configuration provides a credential for connecting to Passpoint networks that are operated by the Passpoint service provider specified in the configuration. Each configuration is uniquely identified by a unique key which depends on the contents of the configuration. This allows the caller to install multiple profiles with the same FQDN (Fully qualified domain name). Therefore, in order to update an existing profile, it is first required to remove it using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removePasspointConfiguration(kotlin.String)`. Otherwise, a new profile will be added with both configuration. Deprecated for general app usage - except DO/PO apps. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setPasspointConfig(android.net.wifi.hotspot2.PasspointConfiguration)` to create a passpoint suggestion. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or above, this API will always fail and throw `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

Deprecation Exemptions:

- Device Owner (DO), Profile Owner (PO) and system apps.

| Parameters ||
|---|---|
| `config` | [PasspointConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration)!: The Passpoint configuration to be added |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if configuration is invalid or Passpoint is not enabled on the device. |

### addSuggestionConnectionStatusListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addSuggestionConnectionStatusListener(
    executor: Executor, 
    listener: WifiManager.SuggestionConnectionStatusListener
): Unit
```

Add a listener for suggestion networks. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener`. Caller will receive the event when suggested network have connection failure. Caller can remove a previously registered listener using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeSuggestionConnectionStatusListener(android.net.wifi.WifiManager.SuggestionConnectionStatusListener)` Same caller can add multiple listeners to monitor the event.

Applications should have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` permissions. Callers without the permission will trigger a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to execute the listener of the `listener` object. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [WifiManager.SuggestionConnectionStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener): listener for suggestion network connection failure. This value cannot be `null`. |

### addSuggestionUserApprovalStatusListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addSuggestionUserApprovalStatusListener(
    executor: Executor, 
    listener: WifiManager.SuggestionUserApprovalStatusListener
): Unit
```

Add a listener for Wi-Fi network suggestion user approval status. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener`. Caller will receive a callback immediately after adding a listener and when the user approval status of the caller has changed. Caller can remove a previously registered listener using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeSuggestionUserApprovalStatusListener(android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)` A caller can add multiple listeners to monitor the event. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to execute the listener of the `listener` object. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [WifiManager.SuggestionUserApprovalStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener): listener for suggestion user approval status changes. This value cannot be `null`. |

### addWifiStateChangedListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addWifiStateChangedListener(
    executor: Executor, 
    listener: WifiManager.WifiStateChangedListener
): Unit
```

Register a callback for Wi-Fi state. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener`. Caller will receive the event when the Wi-Fi state changes. Caller can remove a previously registered callback using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeWifiStateChangedListener(android.net.wifi.WifiManager.WifiStateChangedListener)` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor to execute listener callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [WifiManager.WifiStateChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener): Listener to register. This value cannot be `null`. |

### allowAutojoinGlobal

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allowAutojoinGlobal(allowAutojoin: Boolean): Unit
```

Control whether the device will automatically search for and connect to Wi-Fi networks - auto-join Wi-Fi networks. Disabling this option will not impact manual connections - i.e. the user will still be able to manually select and connect to a Wi-Fi network. Disabling this option significantly impacts the device connectivity and is a restricted operation (see below for permissions). Note that disabling this operation will also disable connectivity initiated scanning operations.

Disabling the auto-join configuration is a temporary operation (with the exception of a DO/PO caller): it will be reset (to enabled) when the device reboots or the user toggles Wi-Fi off/on. When the caller is a DO/PO then toggling Wi-Fi will not reset the configuration. Additionally, if a DO/PO disables auto-join then it cannot be (re)enabled by a non-DO/PO caller.

| Parameters ||
|---|---|
| `allowAutojoin` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to allow auto-join, false to disallow auto-join Available for DO/PO apps. Other apps require `android.Manifest.permission#NETWORK_SETTINGS` or `android.Manifest.permission#MANAGE_WIFI_NETWORK_SELECTION` permission. |

### calculateSignalLevel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun calculateSignalLevel(rssi: Int): Int
```

Given a raw RSSI, return the RSSI signal quality rating using the system default RSSI quality rating thresholds.

| Parameters ||
|---|---|
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a raw RSSI value, in dBm, usually between -55 and -90 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the RSSI signal quality rating, in the range \[0, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxSignalLevel()`\], where 0 is the lowest (worst signal) RSSI rating and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getMaxSignalLevel()` is the highest (best signal) RSSI rating. Value is 0 or greater |

### calculateSignalLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun calculateSignalLevel(
    rssi: Int, 
    numLevels: Int
): Int
```

**Deprecated:** *Callers should use `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#calculateSignalLevel(kotlin.Int)` instead to get the signal level using the system default RSSI thresholds, or otherwise compute the RSSI level themselves using their own formula.*

Calculates the level of the signal. This should be used any time a signal is being shown.

| Parameters ||
|---|---|
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The power of the signal measured in RSSI. |
| `numLevels` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of levels to consider in the calculated level. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A level of the signal, given in the range of 0 to numLevels-1 (both inclusive). |

### cancelWps

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelWps(listener: WifiManager.WpsCallback!): Unit
```

**Deprecated:** *This API is deprecated*

WPS support has been deprecated from Client mode and this method will immediately trigger `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback#onFailed(kotlin.Int)` with a generic error.

| Parameters ||
|---|---|
| `listener` | [WifiManager.WpsCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback)!: for callbacks on success or failure. Can be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the WifiManager instance needs to be initialized again |

### compareSignalLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun compareSignalLevel(
    rssiA: Int, 
    rssiB: Int
): Int
```

Compares two signal strengths.

| Parameters ||
|---|---|
| `rssiA` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The power of the first signal measured in RSSI. |
| `rssiB` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The power of the second signal measured in RSSI. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns \<0 if the first signal is weaker than the second signal, 0 if the two signals have the same strength, and \>0 if the first signal is stronger than the second signal. |

### createMulticastLock

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createMulticastLock(tag: String!): WifiManager.MulticastLock!
```

Create a new MulticastLock

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a tag for the MulticastLock to identify it in debugging messages. This string is never shown to the user under normal conditions, but should be descriptive enough to identify your application and the specific MulticastLock within it, if it holds multiple MulticastLocks. The maximum string length is 255. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.MulticastLock!` | a new, unacquired MulticastLock with the given tag. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.MulticastLock`

### createWifiLock

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createWifiLock(
    lockType: Int, 
    tag: String!
): WifiManager.WifiLock!
```

Creates a new WifiLock.

| Parameters ||
|---|---|
| `lockType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of lock to create. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_HIGH_PERF:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MODE_FULL_LOW_LATENCY:kotlin.Int` for descriptions of the types of Wi-Fi locks. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a tag for the WifiLock to identify it in debugging messages. This string is never shown to the user under normal conditions, but should be descriptive enough to identify your application and the specific WifiLock within it, if it holds multiple WifiLocks. The maximum string length is 255. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock!` | a new, unacquired WifiLock with the given tag. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock`

### createWifiLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createWifiLock(tag: String!): WifiManager.WifiLock!
```

**Deprecated:** *This API is non-functional.*

Creates a new WifiLock.

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a tag for the WifiLock to identify it in debugging messages. This string is never shown to the user under normal conditions, but should be descriptive enough to identify your application and the specific WifiLock within it, if it holds multiple WifiLocks. The maximum string length is 255. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock!` | a new, unacquired WifiLock with the given tag. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiLock`

### disableNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disableNetwork(netId: Int): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Disable a configured network. The specified network will not be a candidate for associating. This may result in the asynchronous delivery of state change events. Applications are not allowed to disable networks created by other applications.

| Parameters ||
|---|---|
| `netId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the network as returned by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getConfiguredNetworks()`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### disallowCurrentSuggestedNetwork

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disallowCurrentSuggestedNetwork(blockingOption: BlockingOption): Unit
```

When the device is connected to a network suggested by calling app `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, this API provide a way to avoid the current connection without `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)`. The disallowed network will be disconnected or roam to other networks. App can only use this API to control the current connected network which was suggested by this app. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `blockingOption` | [BlockingOption](https://developer.android.com/reference/kotlin/android/net/wifi/BlockingOption): Option to change for the network blocking `https://developer.android.com/reference/kotlin/android/net/wifi/BlockingOption` This value cannot be `null`. |

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disconnect(): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Disassociate from the currently active access point. This may result in the asynchronous delivery of state change events.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### enableNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enableNetwork(
    netId: Int, 
    attemptConnect: Boolean
): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Allow a previously configured network to be associated with. If `attemptConnect` is true, an attempt to connect to the selected network is initiated. This may result in the asynchronous delivery of state change events.

**Note:** Network communication may not use Wi-Fi even if Wi-Fi is connected; traffic may instead be sent through another network, such as cellular data, Bluetooth tethering, or Ethernet. For example, traffic will never use a Wi-Fi network that does not provide Internet access (e.g. a wireless printer), if another network that does offer Internet access (e.g. cellular data) is available. Applications that need to ensure that their network traffic uses Wi-Fi should use APIs such as `https://developer.android.com/reference/kotlin/android/net/Network.html#bindSocket(java.net.Socket)`, `https://developer.android.com/reference/kotlin/android/net/Network.html#openConnection(java.net.URL)`, or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#bindProcessToNetwork(android.net.Network)` to do so. Applications are not allowed to enable networks created by other applications.

| Parameters ||
|---|---|
| `netId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the network as returned by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getConfiguredNetworks()`. |
| `attemptConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The way to select a particular network to connect to is specify `true` for this parameter. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### flushPasspointAnqpCache

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flushPasspointAnqpCache(): Unit
```

Flush Passpoint ANQP cache, and clear pending ANQP requests. Allows the caller to reset the Passpoint ANQP state, if required. Notes: 1. Flushing the ANQP cache may cause delays in discovering and connecting to Passpoint networks. 2. Intended to be used by Device Owner (DO), Profile Owner (PO), Settings and provisioning apps.

### getAllowedChannels

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedChannels(
    band: Int, 
    mode: Int
): MutableList<WifiAvailableChannel!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` for the specified band and operational mode(s), that is allowed for the current regulatory domain. An empty list implies that there are no available channels for use. Note: the `band` parameter which is specified as a `WifiScanner#WIFI_BAND_*` constant is limited to one of the band values specified below. Specifically, if the 5GHz band is included then it must include the DFS channels - an exception will be thrown otherwise. The caller should not make any assumptions about whether DFS channels are allowed. This API will indicate whether DFS channels are allowed for the specified operation mode(s) per device policy. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

| Parameters ||
|---|---|
| `band` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the following band constants defined in `WifiScanner#WIFI_BAND_*` constants. 1. `WifiScanner#WIFI_BAND_UNSPECIFIED`=0 - no band specified; Looks for the channels in all the available bands - 2.4 GHz, 5 GHz, 6 GHz and 60 GHz 2. `WifiScanner#WIFI_BAND_24_GHZ`=1 3. `WifiScanner#WIFI_BAND_5_GHZ_WITH_DFS`=6 4. `WifiScanner#WIFI_BAND_BOTH_WITH_DFS`=7 5. `WifiScanner#WIFI_BAND_6_GHZ`=8 6. `WifiScanner#WIFI_BAND_24_5_WITH_DFS_6_GHZ`=15 7. `WifiScanner#WIFI_BAND_60_GHZ`=16 8. `WifiScanner#WIFI_BAND_24_5_WITH_DFS_6_60_GHZ`=31 |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bitwise OR of `WifiAvailableChannel#OP_MODE_*` constants e.g. `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_AWARE:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_STA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_SAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_DIRECT_CLI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_DIRECT_GO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_AWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_TDLS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel!>` | a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | - if this API is not supported on this device or IllegalArgumentException - if the band specified is not one among the list of bands mentioned above. |

### getCallerConfiguredNetworks

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallerConfiguredNetworks(): MutableList<WifiConfiguration!>
```

Return a list of all the networks previously configured by the calling app. Can be called by Device Owner (DO), Profile Owner (PO), Callers with Carrier privilege and system apps. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration!>` | a list of network configurations in the form of a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` objects. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not allowed to call this API |

### getChannelData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelData(
    executor: Executor, 
    resultsCallback: Consumer<MutableList<Bundle!>!>
): Unit
```

Get channel data such as the number of APs found on each channel from the most recent scan. App requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\>!\>: A callback that will return `List<Bundle>` containing channel data such as the number of APs found on each channel. `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_FREQUENCY_MHZ:kotlin.String` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#CHANNEL_DATA_KEY_NUM_AP:kotlin.String` are used to get the frequency (Mhz) and number of APs. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |
| `java.lang.SecurityException` | if the caller does not have permission. |
| `java.lang.UnsupportedOperationException` | if the API is not supported on this SDK version. |
| --- | --- |

### getConfiguredNetworks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfiguredNetworks(): MutableList<WifiConfiguration!>!
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return an empty list.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps will have access to the full list.
- Callers with Carrier privilege will receive a restricted list only containing configurations which they created.*

<br />

Return a list of all the networks configured for the current foreground user. Not all fields of WifiConfiguration are returned. Only the following fields are filled in:

- networkId
- SSID
- BSSID
- priority
- allowedProtocols
- allowedKeyManagement
- allowedAuthAlgorithms
- allowedPairwiseCiphers
- allowedGroupCiphers
- status

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration!>!` | a list of network configurations in the form of a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` objects. |

### getConnectionInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConnectionInfo(): WifiInfo!
```

**Deprecated:** *Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, WifiInfo retrieval is moved to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` API surface. WifiInfo is attached in `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#getTransportInfo()` which is available via callback in `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onCapabilitiesChanged(android.net.Network,%20android.net.NetworkCapabilities)` or on-demand from `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#getNetworkCapabilities(android.net.Network)`.*

<br />

*Usage example:
```kotlin
final NetworkRequest request =
new NetworkRequest.Builder()
.addTransportType(NetworkCapabilities.TRANSPORT_WIFI)
.build();
final ConnectivityManager connectivityManager =
context.getSystemService(ConnectivityManager.class);
final NetworkCallback networkCallback = new NetworkCallback() {
...
@Override
void onAvailable(Network network) {}

@Override
void onCapabilitiesChanged(Network network, NetworkCapabilities networkCapabilities) {
WifiInfo wifiInfo = (WifiInfo) networkCapabilities.getTransportInfo();
}
// etc.
};
connectivityManager.requestNetwork(request, networkCallback); // For request
connectivityManager.registerNetworkCallback(request, networkCallback); // For listen

```
**Compatibility Notes:**
- Apps can continue using this API, however newer features such as ability to mask out location sensitive data in WifiInfo will not be supported via this API.
- On devices supporting concurrent connections (indicated via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForLocalOnlyConnectionsSupported()`, etc) this API will return the details of the internet providing connection (if any) to all apps, except for the apps that triggered the creation of the concurrent connection. For such apps, this API will return the details of the connection they created. e.g. apps using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier` will trigger a concurrent connection on supported devices and hence this API will provide details of their peer to peer connection (not the internet providing connection). This is to maintain backwards compatibility with behavior on single STA devices.*

<br />

Return dynamic information about the current Wi-Fi connection, if any is active.

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo!` | the Wi-Fi information, contained in `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo`. |

### getDhcpInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDhcpInfo(): DhcpInfo!
```

**Deprecated:** *Use the methods on `https://developer.android.com/reference/kotlin/android/net/LinkProperties.html#` which can be obtained either via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onLinkPropertiesChanged(android.net.Network,%20android.net.LinkProperties)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#getLinkProperties(android.net.Network)`.*

***Compatibility Notes:***
*- On devices supporting concurrent connections (indicated via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForLocalOnlyConnectionsSupported()`, etc), this API will return the details of the internet providing connection (if any) to all apps, except for the apps that triggered the creation of the concurrent connection. For such apps, this API will return the details of the connection they created. e.g. apps using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier` will trigger a concurrent connection on supported devices and hence this API will provide details of their peer to peer connection (not the internet providing connection). This is to maintain backwards compatibility with behavior on single STA devices.*

<br />

Return the DHCP-assigned addresses from the last successful DHCP request, if any.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/DhcpInfo.html#!` | the DHCP information |

### getMaxNumberOfChannelsPerNetworkSpecifierRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxNumberOfChannelsPerNetworkSpecifierRequest(): Int
```

Returns the max number of channels that is allowed to be set on a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The max number of channels can be set on a request. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#setPreferredChannelsFrequenciesMhz(kotlin.IntArray)`

### getMaxNumberOfNetworkSuggestionsPerApp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxNumberOfNetworkSuggestionsPerApp(): Int
```

Returns the max number of network suggestions that are allowed per app on the device.
**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)`

### getMaxSignalLevel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxSignalLevel(): Int
```

Get the system default maximum signal level. This is the maximum RSSI level returned by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#calculateSignalLevel(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 0 or greater |

### getMaxSupportedConcurrentTdlsSessions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxSupportedConcurrentTdlsSessions(
    executor: Executor, 
    resultsCallback: Consumer<Int!>
): Unit
```

Return the maximum number of concurrent TDLS sessions supported by the device.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: An asynchronous callback that will return the maximum number of concurrent TDLS sessions supported by the device. Returns `-1` if information is not available, e.g. if the driver/firmware doesn't provide this information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |
| `java.lang.UnsupportedOperationException` | if the feature is not available. |

### getNetworkSuggestions

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkSuggestions(): MutableList<WifiNetworkSuggestion!>
```

Get all network suggestions provided by the calling app. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)` See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion!>` | a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` This value cannot be `null`. |

### getNumberOfEnabledTdlsSessions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberOfEnabledTdlsSessions(
    executor: Executor, 
    resultsCallback: Consumer<Int!>
): Unit
```

Return the number of currently enabled TDLS sessions. Tracks the number of peers enabled for TDLS session via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: An asynchronous callback that will return the number of Peer Mac addresses configured in the driver for TDLS session. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |

### getPasspointConfigurations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPasspointConfigurations(): MutableList<PasspointConfiguration!>!
```

**Deprecated:** *This will be non-functional in a future release.
Requires `android.Manifest.permission.NETWORK_SETTINGS` or `android.Manifest.permission.NETWORK_SETUP_WIZARD`.*

Return the list of installed Passpoint configurations added by the caller. An empty list will be returned when no configurations are installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration!>!` | A list of `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration` added by the caller |

### getPerSsidRoamingModes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPerSsidRoamingModes(
    executor: Executor, 
    resultsCallback: Consumer<MutableMap<String!, Int!>!>
): Unit
```

This API allows a privileged application to get roaming mode policies configured using the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)`. Available for Device Owner (DO) and profile owner of an organization owned device. Other apps require `android.Manifest.permission#NETWORK_SETTINGS` or `android.Manifest.permission#MANAGE_WIFI_NETWORK_SELECTION` permission.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>: An asynchronous callback that will return the corresponding roaming policies for the API caller. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if caller does not have the required permission. |
| `java.lang.UnsupportedOperationException` | if the API is not supported on this SDK version. |

### getScanResults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScanResults(): MutableList<ScanResult!>!
```

Return the results of the latest access point scan. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult!>!` | the list of access points found in the most recent scan. An app must hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` permission in order to get valid results. When an Access Point's beacon or probe response includes a Multi-BSSID Element, the returned scan results should include separate scan result for each BSSID within the Multi-BSSID Information Element. This includes both transmitted and non-transmitted BSSIDs. Original Multi-BSSID Element will be included in the Information Elements attached to each of the scan results. Note: This is the expected behavior for devices supporting 11ax (WiFi-6) and above, and an optional requirement for devices running with older WiFi generations. |

### getStaConcurrencyForMultiInternetMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStaConcurrencyForMultiInternetMode(): Int
```

The device may support concurrent connections to multiple internet-providing Wi-Fi networks (APs) - that is indicated by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForMultiInternetSupported()`. This method indicates whether or not the feature is currently enabled. A value of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DISABLED:kotlin.Int` indicates that the feature is disabled, a value of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DBS_AP:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_MULTI_AP:kotlin.Int` indicates that the feature is enabled. The app can register to receive the corresponding Wi-Fi networks using the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` API with a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier` configured using the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#setBand(kotlin.Int)` method. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_DBS_AP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_MULTI_INTERNET_MODE_MULTI_AP:kotlin.Int` |

### getUsableChannels

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUsableChannels(
    band: Int, 
    mode: Int
): MutableList<WifiAvailableChannel!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` for the specified band and operational mode(s) per the current regulatory domain and device-specific constraints such as concurrency state and interference due to other radios. An empty list implies that there are no available channels for use. Note: the `band` parameter which is specified as a `WifiScanner#WIFI_BAND_*` constant is limited to one of the band values specified below. Specifically, if the 5GHz band is included then it must include the DFS channels - an exception will be thrown otherwise. The caller should not make any assumptions about whether DFS channels are allowed. This API will indicate whether DFS channels are allowed for the specified operation mode(s) per device policy. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

| Parameters ||
|---|---|
| `band` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the following band constants defined in `WifiScanner#WIFI_BAND_*` constants. 1. `WifiScanner#WIFI_BAND_UNSPECIFIED`=0 - no band specified; Looks for the channels in all the available bands - 2.4 GHz, 5 GHz, 6 GHz and 60 GHz 2. `WifiScanner#WIFI_BAND_24_GHZ`=1 3. `WifiScanner#WIFI_BAND_5_GHZ_WITH_DFS`=6 4. `WifiScanner#WIFI_BAND_BOTH_WITH_DFS`=7 5. `WifiScanner#WIFI_BAND_6_GHZ`=8 6. `WifiScanner#WIFI_BAND_24_5_WITH_DFS_6_GHZ`=15 7. `WifiScanner#WIFI_BAND_60_GHZ`=16 8. `WifiScanner#WIFI_BAND_24_5_WITH_DFS_6_60_GHZ`=31 |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bitwise OR of `WifiAvailableChannel#OP_MODE_*` constants e.g. `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_AWARE:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_STA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_SAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_DIRECT_CLI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_DIRECT_GO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_WIFI_AWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel#OP_MODE_TDLS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel!>` | a list of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiAvailableChannel` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | - if this API is not supported on this device or IllegalArgumentException - if the band specified is not one among the list of bands mentioned above. |

### getWifiState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWifiState(): Int
```

Gets the Wi-Fi enabled state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_DISABLING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_ENABLING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_STATE_UNKNOWN:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiEnabled()`

### is24GHzBandSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun is24GHzBandSupported(): Boolean
```

Check if the chipset supports 2.4GHz band.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### is5GHzBandSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun is5GHzBandSupported(): Boolean
```

Check if the chipset supports 5GHz band.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### is60GHzBandSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun is60GHzBandSupported(): Boolean
```

Check if the chipset supports the 60GHz frequency band.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### is6GHzBandSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun is6GHzBandSupported(): Boolean
```

Check if the chipset supports 6GHz band.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isAggressiveRoamingModeSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAggressiveRoamingModeSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Aggressive roaming mode `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)` |

### isAutoWakeupEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoWakeupEnabled(): Boolean
```

Get the persisted Wi-Fi auto wakeup feature state. Defaults to false, unless changed by the user via Settings.

The feature is described in [https://source.android.com/devices/tech/connect/wifi-infrastructure #turn_on_wi-fi_automatically](https://developer.android.com/reference/kotlin/android/net/wifi/Wi-Fi Turn on automatically). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true to indicate that wakeup feature is enabled, false to indicate that wakeup feature is disabled. |

### isBridgedApConcurrencySupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBridgedApConcurrencySupported(): Boolean
```

Query whether or not the device supports multiple Access point (AP) which are bridged together.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports concurrency of multiple AP which bridged together, false otherwise. |

### isCarrierNetworkOffloadEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCarrierNetworkOffloadEnabled(
    subscriptionId: Int, 
    merged: Boolean
): Boolean
```

Get the carrier network offload state for merged or unmerged networks for specified subscription. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): subscription ID see `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo.html#getSubscriptionId()` |
| `merged` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True for carrier merged network, false otherwise. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setCarrierMerged(kotlin.Boolean)` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True to indicate that carrier network offload is enabled, false otherwise. |

### isD2dSupportedWhenInfraStaDisabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isD2dSupportedWhenInfraStaDisabled(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this devices supports device-to-device (D2d) Wi-Fi use-cases such as Wi-Fi Direct when infra station (STA) is disabled. |

### isDecoratedIdentitySupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDecoratedIdentitySupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports RFC 7542 decorated identity. |

### isDeviceToApRttSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceToApRttSupported(): Boolean
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI_RTT:kotlin.String`.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this adapter supports Device-to-AP RTT |

### isDualBandSimultaneousSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDualBandSimultaneousSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Dual Band Simultaneous (DBS) operation. |

### isEasyConnectDppAkmSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEasyConnectDppAkmSupported(): Boolean
```

Wi-Fi Easy Connect DPP AKM enables provisioning and configuration of Wi-Fi devices without the need of using the device PSK passphrase. For more details, visit <https://www.wi-fi.org/> and search for "Easy Connect" or "Device Provisioning Protocol specification".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Easy-connect DPP (Device Provisioning Protocol) AKM, false otherwise. |

### isEasyConnectEnrolleeResponderModeSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEasyConnectEnrolleeResponderModeSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Easy Connect (DPP) Enrollee Responder mode. |

### isEasyConnectSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEasyConnectSupported(): Boolean
```

Wi-Fi Easy Connect (DPP) introduces standardized mechanisms to simplify the provisioning and configuration of Wi-Fi devices. For more details, visit <https://www.wi-fi.org/> and search for "Easy Connect" or "Device Provisioning Protocol specification".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Easy-connect (Device Provisioning Protocol) |

### isEnhancedOpenSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnhancedOpenSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Enhanced Open (OWE) |

### isEnhancedPowerReportingSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnhancedPowerReportingSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this adapter supports advanced power/performance counters |

### isMakeBeforeBreakWifiSwitchingSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMakeBeforeBreakWifiSwitchingSupported(): Boolean
```

Query whether or not the device supports concurrent station (STA) connections for make-before-break wifi to wifi switching. Note: This is an internal feature which is not available to apps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports multiple STA concurrency for this use-case, false otherwise. |

### isP2pSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isP2pSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this adapter supports WifiP2pManager (Wi-Fi Direct) |

### isPasspointTermsAndConditionsSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPasspointTermsAndConditionsSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Passpoint Terms and Conditions feature. |

### isPreferredNetworkOffloadSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPreferredNetworkOffloadSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this adapter supports offloaded connectivity scan |

### isScanAlwaysAvailable

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScanAlwaysAvailable(): Boolean
```

**Deprecated:** *The ability for apps to trigger scan requests will be removed in a future release.*

Check if scanning is always available. If this return `true`, apps can issue `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startScan()` and fetch scan results even when Wi-Fi is turned off. To change this setting, see `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REQUEST_SCAN_ALWAYS_AVAILABLE:kotlin.String`.

### isScanThrottleEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScanThrottleEnabled(): Boolean
```

Get the persisted Wi-Fi scan throttle state. Defaults to true, unless changed by the user via Developer options.

The throttling limits for apps are described in [https://developer.android.com/guide/topics/connectivity/wifi-scan#wifi-scan-throttling](https://developer.android.com/reference/kotlin/android/net/wifi/Wi-Fi Scan Throttling)
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true to indicate that scan throttling is enabled, false to indicate that scan throttling is disabled. |

### isStaApConcurrencySupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStaApConcurrencySupported(): Boolean
```

Query whether or not the device supports Station (STA) + Access point (AP) concurrency.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports STA + AP concurrency, false otherwise. |

### isStaBridgedApConcurrencySupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStaBridgedApConcurrencySupported(): Boolean
```

Query whether or not the device supports concurrency of Station (STA) + multiple access points (AP) (where the APs bridged together).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports concurrency of STA + multiple APs which are bridged together, false otherwise. |

### isStaConcurrencyForLocalOnlyConnectionsSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStaConcurrencyForLocalOnlyConnectionsSupported(): Boolean
```

Query whether or not the device supports concurrent station (STA) connections for local-only connections using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports multiple STA concurrency for this use-case, false otherwise. |

### isStaConcurrencyForMultiInternetSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStaConcurrencyForMultiInternetSupported(): Boolean
```

Query whether or not the device supports concurrent station (STA) connections for multi internet connections.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports multiple STA concurrency for this use-case, false otherwise. |

### isTdlsOperationCurrentlyAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTdlsOperationCurrentlyAvailable(
    executor: Executor, 
    resultsCallback: Consumer<Boolean!>
): Unit
```

Check if a TDLS session can be established at this time via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` Internally framework checks the STA connected state, device support for TDLS and the number of TDLS sessions available in driver/firmware.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: An asynchronous callback that will return `Boolean` indicating whether a TDLS session can be established at this time. `true` for available, `false` for not available. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |

### isTdlsSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTdlsSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this adapter supports Tunnel Directed Link Setup |

### isTidToLinkMappingNegotiationSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTidToLinkMappingNegotiationSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports TID-To-Link Mapping Negotiation. |

### isTlsMinimumVersionSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTlsMinimumVersionSupported(): Boolean
```

Indicate that whether or not settings required TLS minimum version is supported. If the device doesn't support this capability, the minimum accepted TLS version is 1.0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports setting TLS minimum version. |

### isTlsV13Supported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTlsV13Supported(): Boolean
```

Indicate that whether or not TLS v1.3 is supported. If requested minimum is not supported, it will default to the maximum supported version.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports TLS v1.3. |

### isTrustOnFirstUseSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTrustOnFirstUseSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Trust On First Use (TOFU). |

### isWapiSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWapiSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports WAPI. |

### isWepSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWepSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports connections to Wi-Fi WEP networks. |

### isWifiDisplayR2Supported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWifiDisplayR2Supported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Display R2. |

### isWifiEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWifiEnabled(): Boolean
```

Return whether Wi-Fi is enabled or disabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if Wi-Fi is enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()`

### isWifiPasspointEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWifiPasspointEnabled(): Boolean
```

If the device supports Wi-Fi Passpoint, the user can explicitly enable or disable it. That status can be queried using this method. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if Wi-Fi Passpoint is enabled |

### isWifiStandardSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWifiStandardSupported(standard: Int): Boolean
```

Check if the chipset supports a certain Wi-Fi standard.

| Parameters ||
|---|---|
| `standard` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the IEEE 802.11 standard to check on. valid values from `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult`'s `WIFI_STANDARD_` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_LEGACY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11N:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isWpa3SaeH2eSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWpa3SaeH2eSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports WPA3 SAE Hash-to-Element. |

### isWpa3SaePublicKeySupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWpa3SaePublicKeySupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports WPA3 SAE Public Key. |

### isWpa3SaeSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWpa3SaeSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports WPA3-Personal SAE |

### isWpa3SuiteBSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWpa3SuiteBSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports WPA3-Enterprise Suite-B-192 |

### isWpaPersonalSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWpaPersonalSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports connections to Wi-Fi WPA-Personal networks. Note that this is the older and less secure WPA-Personal protocol, not WPA2-Personal or later protocols. |

### pingSupplicant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pingSupplicant(): Boolean
```

**Deprecated:** *Will return the output of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isWifiEnabled()` instead.*

Check that the supplicant daemon is responding to requests.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if we were able to communicate with the supplicant and it returned the expected response to the PING message. |

### queryAutojoinGlobal

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryAutojoinGlobal(
    executor: Executor, 
    resultsCallback: Consumer<Boolean!>
): Unit
```

Query whether or not auto-join global is enabled/disabled

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: An asynchronous callback that will return `Boolean` indicating whether auto-join global is enabled/disabled. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |
| `java.lang.SecurityException` | if the caller does not have permission. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#allowAutojoinGlobal(kotlin.Boolean)`

### querySendDhcpHostnameRestriction

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun querySendDhcpHostnameRestriction(
    executor: Executor, 
    resultsCallback: IntConsumer
): Unit
```

Query the global restriction on which networks to send the device hostname to during DHCP. 
Requires android.Manifest.permission#NETWORK_SETTINGS or android.Manifest.permission#NETWORK_SETUP_WIZARD

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#): An asynchronous callback that will return a bitmask of android.net.wifi.WifiManager.SendDhcpHostnameRestriction. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the calling app is not a Device Owner (DO), or a privileged app that has one of the permissions required by this API. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setSendDhcpHostnameRestriction(kotlin.Int)`

### reassociate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reassociate(): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always return false.*

Reconnect to the currently active access point, even if we are already connected. This may result in the asynchronous delivery of state change events.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### reconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reconnect(): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Reconnect to the currently active access point, if we are currently disconnected. This may result in the asynchronous delivery of state change events.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### registerScanResultsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerScanResultsCallback(
    executor: Executor, 
    callback: WifiManager.ScanResultsCallback
): Unit
```

Register a callback for Scan Results. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback`. Caller will receive the event when scan results are available. Caller should use `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getScanResults()` requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` to get the scan results. Caller can remove a previously registered callback using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#unregisterScanResultsCallback(android.net.wifi.WifiManager.ScanResultsCallback)` Same caller can add multiple listeners.

Applications should have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` permission. Callers without the permission will trigger a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to execute the callback of the `callback` object. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [WifiManager.ScanResultsCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback): callback for Scan Results events. This value cannot be `null`. |

### registerSubsystemRestartTrackingCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSubsystemRestartTrackingCallback(
    executor: Executor, 
    callback: WifiManager.SubsystemRestartTrackingCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` to listen to Wi-Fi subsystem restarts. The subsystem may restart due to internal recovery mechanisms or via user action. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor to execute callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [WifiManager.SubsystemRestartTrackingCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback): `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` to register. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#unregisterSubsystemRestartTrackingCallback(android.net.wifi.WifiManager.SubsystemRestartTrackingCallback)`

### removeLocalOnlyConnectionFailureListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLocalOnlyConnectionFailureListener(listener: WifiManager.LocalOnlyConnectionFailureListener): Unit
```

Allow callers to remove a previously registered listener. After calling this method, applications will no longer receive local-only connection events through that listener. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [WifiManager.LocalOnlyConnectionFailureListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener): listener to remove. This value cannot be `null`. |

### removeNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeNetwork(netId: Int): Boolean
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Remove the specified network from the list of configured networks. This may result in the asynchronous delivery of state change events. Applications are not allowed to remove networks created by other applications.

| Parameters ||
|---|---|
| `netId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the network as returned by `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getConfiguredNetworks()`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded |

### removeNetworkSuggestions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeNetworkSuggestions(networkSuggestions: MutableList<WifiNetworkSuggestion!>): Int
```

Remove some or all of the network suggestions that were previously provided by the app. If one of the suggestions being removed was used to establish connection to the current network, then the device will immediately disconnect from that network. This method is same as `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int` See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` for a detailed explanation of the parameters. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any)` for the equivalence evaluation used.

[removeNetworkSuggestions(List,int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList,%20kotlin.Int)). An `action` of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int` is equivalent to the current behavior. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkSuggestions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion)!\>: List of network suggestions to be removed. Pass an empty list to remove all the previous suggestions provided by the app. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Status code for the operation. One of the `STATUS_NETWORK_SUGGESTIONS_*` values. Any matching suggestions are removed from the device and will not be considered for any further connection attempts. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN:kotlin.Int` |

### removeNetworkSuggestions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeNetworkSuggestions(
    networkSuggestions: MutableList<WifiNetworkSuggestion!>, 
    action: Int
): Int
```

Remove some or all of the network suggestions that were previously provided by the app. If one of the suggestions being removed was used to establish connection to the current network, then the specified action will be executed. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion` for a detailed explanation of the parameters. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any)` for the equivalence evaluation used. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkSuggestions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion)!\>: List of network suggestions to be removed. Pass an empty list to remove all the previous suggestions provided by the app. This value cannot be `null`. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired action to execute after removing the suggestion. One of `ACTION_REMOVE_SUGGESTION_*` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_LINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ACTION_REMOVE_SUGGESTION_DISCONNECT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Status code for the operation. One of the `STATUS_NETWORK_SUGGESTIONS_*` values. Any matching suggestions are removed from the device and will not be considered for further connection attempts. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_INTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_APP_DISALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_DUPLICATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_EXCEEDS_MAX_PER_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_REMOVE_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_ADD_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_NETWORK_SUGGESTIONS_ERROR_RESTRICTED_BY_ADMIN:kotlin.Int` |

### removeNonCallerConfiguredNetworks

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeNonCallerConfiguredNetworks(): Boolean
```

Remove all configured networks that were not created by the calling app. Can only be called by a Device Owner (DO) app. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if at least one network is removed, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not a Device Owner app |

### removePasspointConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removePasspointConfiguration(fqdn: String!): Unit
```

**Deprecated:** *This will be non-functional in a future release.
Requires `android.Manifest.permission.NETWORK_SETTINGS` or `android.Manifest.permission.NETWORK_CARRIER_PROVISIONING`.*

Remove the Passpoint configuration identified by its FQDN (Fully Qualified Domain Name) added by the caller.

| Parameters ||
|---|---|
| `fqdn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The FQDN of the Passpoint configuration added by the caller to be removed |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if no configuration is associated with the given FQDN or Passpoint is not enabled on the device. |

### removePerSsidRoamingMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removePerSsidRoamingMode(ssid: WifiSsid): Unit
```

This API allows a privileged application to remove roaming mode policy configured using the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setPerSsidRoamingMode(android.net.wifi.WifiSsid,%20kotlin.Int)`. Available for Device Owner (DO) and profile owner of an organization owned device. Other apps require `android.Manifest.permission#NETWORK_SETTINGS` or `android.Manifest.permission#MANAGE_WIFI_NETWORK_SELECTION` permission.

| Parameters ||
|---|---|
| `ssid` | [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid): SSID to be removed from the roaming mode policy. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided a null input. |
| `java.lang.SecurityException` | if caller does not have the required permission. |
| `java.lang.UnsupportedOperationException` | if the API is not supported on this SDK version. |
| --- | --- |

### removeSuggestionConnectionStatusListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeSuggestionConnectionStatusListener(listener: WifiManager.SuggestionConnectionStatusListener): Unit
```

Allow callers to remove a previously registered listener. After calling this method, applications will no longer receive suggestion connection events through that listener. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [WifiManager.SuggestionConnectionStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener): listener to remove. This value cannot be `null`. |

### removeSuggestionUserApprovalStatusListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeSuggestionUserApprovalStatusListener(listener: WifiManager.SuggestionUserApprovalStatusListener): Unit
```

Allow callers to remove a previously registered listener using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)`. After calling this method, applications will no longer receive network suggestion user approval status change through that listener. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [WifiManager.SuggestionUserApprovalStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener): This value cannot be `null`. |

### removeWifiStateChangedListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeWifiStateChangedListener(listener: WifiManager.WifiStateChangedListener): Unit
```

Unregisters a WifiStateChangedListener from listening on the current Wi-Fi state. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [WifiManager.WifiStateChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener): WifiStateChangedListener to unregister. This value cannot be `null`. |

### reportCreateInterfaceImpact

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportCreateInterfaceImpact(
    interfaceType: Int, 
    requireNewInterface: Boolean, 
    executor: Executor, 
    resultCallback: BiConsumer<Boolean!, MutableSet<WifiManager.InterfaceCreationImpact!>!>
): Unit
```

Queries the framework to determine whether the specified interface can be created, and if so - what other interfaces would be torn down by the framework to allow this creation if it were requested. The result is returned via the specified `https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#` callback which returns two arguments:
- First argument: a `boolean` - indicating whether or not the interface can be created.
- Second argument: a `Set<InterfaceCreationImpact>` - if the interface can be created (first argument is `true` then this is the set of interface types which will be removed and the packages which requested them. Possibly an empty set. If the first argument is `false`, then an empty set will be returned here.
- Interfaces, input and output, are specified using the `WIFI_INTERFACE_*` constants: `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_STA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AWARE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_DIRECT:kotlin.Int`.
- This method does not actually create the interface. That operation is handled by the framework when a particular service method is called. E.g. a Wi-Fi Direct interface may be created when various methods of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager` are called, similarly for Wi-Fi Aware and `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager`.
- Note: the information returned via this method is the current snapshot of the system. It may change due to actions of the framework or other apps. 
 Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_WIFI_INTERFACES:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `interfaceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The interface type whose possible creation is being queried. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_STA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_AWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#WIFI_INTERFACE_TYPE_DIRECT:kotlin.Int` |
| `requireNewInterface` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Indicates that the query is for a new interface of the specified type - an existing interface won't meet the query. Some operations (such as Wi-Fi Direct and Wi-Fi Aware are a shared resource and so may not need a new interface). |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): An `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to return the result. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `resultCallback` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [WifiManager.InterfaceCreationImpact](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.InterfaceCreationImpact)!\>!\>: The asynchronous callback which will return two argument: a `boolean` (whether the interface can be created), and a `Set<InterfaceCreationImpact>` (a set of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.InterfaceCreationImpact`: interfaces which will be destroyed when the interface is created and the packages which requested them and thus may be impacted). This value cannot be `null`. |

### saveConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun saveConfiguration(): Boolean
```

**Deprecated:** *There is no need to call this method - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#updateNetwork(android.net.wifi.WifiConfiguration)` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetwork(kotlin.Int)` already persist the configurations automatically.*

Tell the device to persist the current list of configured networks.

Note: It is possible for this method to change the network IDs of existing networks. You should assume the network IDs can be different after calling this method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false`. |

### setPerSsidRoamingMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPerSsidRoamingMode(
    ssid: WifiSsid, 
    roamingMode: Int
): Unit
```

This API allows a privileged application to set roaming mode per SSID. Available for Device Owner (DO) and profile owner of an organization owned device. Other apps require `android.Manifest.permission#NETWORK_SETTINGS` or `android.Manifest.permission#MANAGE_WIFI_NETWORK_SELECTION` permission.

| Parameters ||
|---|---|
| `ssid` | [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid): SSID to be mapped to apply roaming policy. This value cannot be `null`. |
| `roamingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of the `ROAMING_MODE_` values. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#ROAMING_MODE_AGGRESSIVE:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is invalid. |
| `java.lang.NullPointerException` | if the caller provided a null input. |
| `java.lang.SecurityException` | if caller does not have the required permission. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the API is not supported on this SDK version or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isAggressiveRoamingModeSupported()` returns false, but input roaming mode is `ROAMING_MODE_AGGRESSIVE`. |

### setSendDhcpHostnameRestriction

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSendDhcpHostnameRestriction(restriction: Int): Unit
```

Sets the global restrictions on which networks to send the device hostname to during DHCP. 
Requires android.Manifest.permission#NETWORK_SETTINGS or android.Manifest.permission#NETWORK_SETUP_WIZARD

| Parameters ||
|---|---|
| `restriction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bitmask of android.net.wifi.WifiManager.SendDhcpHostnameRestriction, or none to indicate no restriction. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_OPEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#FLAG_SEND_DHCP_HOSTNAME_RESTRICTION_SECURE:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is invalid |
| `java.lang.SecurityException` | if the calling app is not a Device Owner (DO), or a privileged app that has one of the permissions required by this API. |

### setTdlsEnabled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTdlsEnabled(
    remoteIPAddress: InetAddress!, 
    enable: Boolean
): Unit
```

Enable/Disable TDLS on a specific local route.

TDLS enables two wireless endpoints to talk to each other directly without going through the access point that is managing the local network. It saves bandwidth and improves quality of the link.

This API enables/disables the option of using TDLS. If enabled, the underlying hardware is free to use TDLS or a hop through the access point. If disabled, existing TDLS session is torn down and hardware is restricted to use access point for transferring wireless packets. Default value for all routes is 'disabled', meaning restricted to use access point for transferring packets.

| Parameters ||
|---|---|
| `remoteIPAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!: IP address of the endpoint to setup TDLS with |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true = setup and false = tear down TDLS |

### setTdlsEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTdlsEnabled(
    remoteIPAddress: InetAddress, 
    enable: Boolean, 
    executor: Executor, 
    resultsCallback: Consumer<Boolean!>
): Unit
```

Enable/Disable TDLS on a specific local route. Similar to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)`, except this version sends the result of the Enable/Disable request.

| Parameters ||
|---|---|
| `remoteIPAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#): IP address of the endpoint to setup TDLS with. This value cannot be `null`. |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true = setup and false = tear down TDLS |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: An asynchronous callback that will return `Boolean` indicating whether TDLS was successfully enabled or disabled. `true` for success, `false` for failure. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |

### setTdlsEnabledWithMacAddress

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTdlsEnabledWithMacAddress(
    remoteMacAddress: String!, 
    enable: Boolean
): Unit
```

Similar to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabled(java.net.InetAddress,%20kotlin.Boolean)`, except this version allows you to specify remote endpoint with a MAC address.

| Parameters ||
|---|---|
| `remoteMacAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: MAC address of the remote endpoint such as 00:00:0c:9f:f2:ab |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true = setup and false = tear down TDLS |

### setTdlsEnabledWithMacAddress

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTdlsEnabledWithMacAddress(
    remoteMacAddress: String, 
    enable: Boolean, 
    executor: Executor, 
    resultsCallback: Consumer<Boolean!>
): Unit
```

Enable/Disable TDLS with a specific peer Mac Address. Similar to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#setTdlsEnabledWithMacAddress(kotlin.String,%20kotlin.Boolean)`, except this version sends the result of the Enable/Disable request.

| Parameters ||
|---|---|
| `remoteMacAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Mac address of the endpoint to setup TDLS with. This value cannot be `null`. |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true = setup and false = tear down TDLS |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>: An asynchronous callback that will return `Boolean` indicating whether TDLS was successfully enabled or disabled. `true` for success, `false` for failure. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the caller provided invalid inputs. |

### setWifiEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWifiEnabled(enabled: Boolean): Boolean
```

**Deprecated:** *Starting with Build.VERSION_CODES#Q, applications are not allowed to enable/disable Wi-Fi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `false`. If apps are targeting an older SDK (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` or below), they can continue to use this API.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.
Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, DO and a profile owner of an organization owned device may set a user restriction (DISALLOW_CHANGE_WIFI_STATE) to only allow DO/PO to use this API.*

<br />

Enable or disable Wi-Fi.

Applications must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` permission to toggle wifi.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to enable, `false` to disable. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if the request cannot be satisfied; `true` indicates that wifi is either already in the requested state, or in progress toward the requested state. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is missing required permissions. |

### startLocalOnlyHotspot

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startLocalOnlyHotspot(
    callback: WifiManager.LocalOnlyHotspotCallback!, 
    handler: Handler?
): Unit
```

Request a local only hotspot that an application can use to communicate between co-located devices connected to the created WiFi hotspot. The network created by this method will not have Internet access. Each application can make a single request for the hotspot, but multiple applications could be requesting the hotspot at the same time. When multiple applications have successfully registered concurrently, they will be sharing the underlying hotspot. `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onStarted(android.net.wifi.WifiManager.LocalOnlyHotspotReservation)` is called when the hotspot is ready for use by the application.

Each application can make a single active call to this method. The `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onStarted(android.net.wifi.WifiManager.LocalOnlyHotspotReservation)` callback supplies the requestor with a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotReservation` that contains a `https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration` with the SSID, security type and credentials needed to connect to the hotspot. Communicating this information is up to the application.

If the LocalOnlyHotspot cannot be created, the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onFailed(kotlin.Int)` method will be called. Example failures include errors bringing up the network or if there is an incompatible operating mode. For example, if the user is currently using Wifi Tethering to provide an upstream to another device, LocalOnlyHotspot may not start due to an incompatible mode. The possible error codes include: `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#ERROR_NO_CHANNEL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#ERROR_GENERIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#ERROR_INCOMPATIBLE_MODE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#ERROR_TETHERING_DISALLOWED:kotlin.Int`.

Internally, requests will be tracked to prevent the hotspot from being torn down while apps are still using it. The `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotReservation` object passed in the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onStarted(android.net.wifi.WifiManager.LocalOnlyHotspotReservation)` call should be closed when the LocalOnlyHotspot is no longer needed using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotReservation#close()`. Since the hotspot may be shared among multiple applications, removing the final registered application request will trigger the hotspot teardown. This means that applications should not listen to broadcasts containing wifi state to determine if the hotspot was stopped after they are done using it. Additionally, once `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotReservation#close()` is called, applications will not receive callbacks of any kind.

Applications should be aware that the user may also stop the LocalOnlyHotspot through the Settings UI; it is not guaranteed to stay up as long as there is a requesting application. The requestors will be notified of this case via `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onStopped()`. Other cases may arise where the hotspot is torn down (Emergency mode, etc). Application developers should be aware that it can stop unexpectedly, but they will receive a notification if they have properly registered.

Applications should also be aware that this network will be shared with other applications. Applications are responsible for protecting their data on this network (e.g. TLS).

Applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later need to have the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`. Applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or prior SDK levels need to have the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` Callers without the permissions will trigger a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

| Parameters ||
|---|---|
| `callback` | [WifiManager.LocalOnlyHotspotCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback)!: LocalOnlyHotspotCallback for the application to receive updates about operating status. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: Handler to be used for callbacks. If the caller passes a null Handler, the main thread will be used. |

### startLocalOnlyHotspotWithConfiguration

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startLocalOnlyHotspotWithConfiguration(
    config: SoftApConfiguration, 
    executor: Executor, 
    callback: WifiManager.LocalOnlyHotspotCallback
): Unit
```

Starts a local-only hotspot with a specific configuration applied. See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startLocalOnlyHotspot(android.net.wifi.WifiManager.LocalOnlyHotspotCallback,%20android.os.Handler)`. Since custom configuration settings may be incompatible with each other, the hotspot started through this method cannot coexist with another hotspot created through `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#startLocalOnlyHotspot(android.net.wifi.WifiManager.LocalOnlyHotspotCallback,%20android.os.Handler)`. If this is attempted, the first hotspot request wins and others receive `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#ERROR_GENERIC:kotlin.Int` through `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback#onFailed(kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

| Parameters ||
|---|---|
| `config` | [SoftApConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration): Custom configuration for the hotspot. See `https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration`. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor to run callback methods on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [WifiManager.LocalOnlyHotspotCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyHotspotCallback): LocalOnlyHotspotCallback for the application to receive updates about operating status. This value cannot be `null`. |
| --- | --- |

### startScan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startScan(): Boolean
```

**Deprecated:** *The ability for apps to trigger scan requests will be removed in a future release.*

Request a scan for access points. Returns immediately. The availability of the results is made known later by means of an asynchronous event sent on completion of the scan.

To initiate a Wi-Fi scan, declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` permission in the manifest, and perform these steps:

1. Invoke the following method: `((WifiManager) getSystemService(WIFI_SERVICE)).startScan()`
2. Register a BroadcastReceiver to listen to `SCAN_RESULTS_AVAILABLE_ACTION`.
3. When a broadcast is received, call: `((WifiManager) getSystemService(WIFI_SERVICE)).getScanResults()`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the operation succeeded, i.e., the scan was initiated. |

### startWps

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startWps(
    config: WpsInfo!, 
    listener: WifiManager.WpsCallback!
): Unit
```

**Deprecated:** *This API is deprecated*

WPS suport has been deprecated from Client mode and this method will immediately trigger `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback#onFailed(kotlin.Int)` with a generic error.

| Parameters ||
|---|---|
| `config` | [WpsInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WpsInfo)!: WPS configuration (does not support `https://developer.android.com/reference/kotlin/android/net/wifi/WpsInfo#LABEL:kotlin.Int`) |
| `listener` | [WifiManager.WpsCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WpsCallback)!: for callbacks on success or failure. Can be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the WifiManager instance needs to be initialized again |

### unregisterScanResultsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterScanResultsCallback(callback: WifiManager.ScanResultsCallback): Unit
```

Allow callers to unregister a previously registered callback. After calling this method, applications will no longer receive Scan Results events. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [WifiManager.ScanResultsCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.ScanResultsCallback): callback to unregister for Scan Results events. This value cannot be `null`. |

### unregisterSubsystemRestartTrackingCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterSubsystemRestartTrackingCallback(callback: WifiManager.SubsystemRestartTrackingCallback): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` registered with `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#registerSubsystemRestartTrackingCallback(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SubsystemRestartTrackingCallback)` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [WifiManager.SubsystemRestartTrackingCallback](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback): `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SubsystemRestartTrackingCallback` to unregister. This value cannot be `null`. |

### updateNetwork

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateNetwork(config: WifiConfiguration!): Int
```

**Deprecated:** *a) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build()` for new mechanism to trigger connection to a Wi-Fi network. b) See `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#removeNetworkSuggestions(kotlin.collections.MutableList)` for new API to add Wi-Fi networks for consideration when auto-connecting to wifi. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or above, this API will always fail and return `-1`.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Update the network description of an existing configured network.

| Parameters ||
|---|---|
| `config` | [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration)!: the set of variables that describe the configuration, contained in a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` object. It may be sparse, so that only the items that are being changed are non-`null`. The `networkId` field must be set to the ID of the existing network being updated. If the `https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration` has an Http Proxy set the calling app must be System, or be provisioned as the Profile or Device Owner. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the `networkId` of the supplied `WifiConfiguration` on success. Returns `-1` on failure, including when the `networkId` field of the `WifiConfiguration` does not refer to an existing network. |

### validateSoftApConfiguration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun validateSoftApConfiguration(config: SoftApConfiguration): Boolean
```

Check if input configuration is valid.

This will return `false` if a non-null BSSID is set but the caller does not have any of

- android.Manifest.permission#NETWORK_SETTINGS
- android.Manifest.permission#NETWORK_STACK
- `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#`

| Parameters ||
|---|---|
| `config` | [SoftApConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/SoftApConfiguration): a configuration would like to be checked. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if config is valid, otherwise false. |
