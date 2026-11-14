# android.app.admin

## Interfaces

| [OnClearApplicationUserDataListener](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener) | Callback used in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#clearApplicationUserData(android.content.ComponentName,%20kotlin.String,%20java.util.concurrent.Executor,%20android.app.admin.DevicePolicyManager.OnClearApplicationUserDataListener)` to indicate that the clearing of an application's user data is done. |

## Classes

| [ConnectEvent](https://developer.android.com/reference/kotlin/android/app/admin/ConnectEvent) | A class that represents a TCP connect event initiated through the standard network stack. |
| [DelegatedAdminReceiver](https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver) | Base class for delegated apps to handle callbacks related to their delegated capabilities. |
| [DeviceAdminInfo](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminInfo) | This class is used to specify meta information of a device administrator component. |
| [DeviceAdminReceiver](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver) | Base class for implementing a device administration component. |
| [DeviceAdminService](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminService) | Base class for a service that device owner/profile owners can optionally have. |
| [DevicePolicyIdentifiers](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyIdentifiers) | Class containing identifiers for policy APIs in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`, for example they will be passed in `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicySetResult(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` and `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicyChanged(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` to communicate updates of a certain policy back to the admin. |
| [DevicePolicyManager](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager) | Manages device policy and restrictions applied to the user of the device or apps running on the device. |
| [DevicePolicyResources](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResources) | Class containing the required identifiers to update device management resources. |
| [DevicePolicyResourcesManager](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager) | Class containing required APIs to set, reset, and get device policy related resources. |
| [DnsEvent](https://developer.android.com/reference/kotlin/android/app/admin/DnsEvent) | A class that represents a DNS lookup event initiated through the standard network stack. |
| [FactoryResetProtectionPolicy](https://developer.android.com/reference/kotlin/android/app/admin/FactoryResetProtectionPolicy) | The factory reset protection policy determines which accounts can unlock a device that has gone through untrusted factory reset. |
| [FreezePeriod](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod) | A class that represents one freeze period which repeats *annually*. |
| [ManagedSubscriptionsPolicy](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy) | A policy class that describes how managed SIM subscriptions should behave on the device. |
| [NetworkEvent](https://developer.android.com/reference/kotlin/android/app/admin/NetworkEvent) | An abstract class that represents a network event. |
| [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/admin/PackageIdentifier) | Identifies a package on the current device. |
| [PackagePolicy](https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy) | A generic class that defines which APK packages are in scope for some device policy. |
| [PolicyIdentifier](https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier) | Represents a type safe identifier for a policy. |
| [PolicyUpdateReceiver](https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver) | Base class for implementing a policy update receiver. |
| [PolicyUpdateResult](https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateResult) | Class containing the reason for the policy (set from `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`) update (e.g. success, failure reasons, etc.). |
| [PreferentialNetworkServiceConfig](https://developer.android.com/reference/kotlin/android/app/admin/PreferentialNetworkServiceConfig) | Network configuration to be set for the user profile. |
| [SecurityLog](https://developer.android.com/reference/kotlin/android/app/admin/SecurityLog) | Definitions for working with security logs. |
| [SystemUpdateInfo](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdateInfo) | A class containing information about a pending system update. |
| [SystemUpdatePolicy](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy) | Determines when over-the-air system updates are installed on a device. |
| [TargetUser](https://developer.android.com/reference/kotlin/android/app/admin/TargetUser) | Class representing the target user of a policy set by an admin (set from `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`), this is passed in to `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicySetResult(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` and `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicyChanged(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)`. |
| [WifiSsidPolicy](https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy) | Used to indicate the Wi-Fi SSID restriction policy the network must satisfy in order to be eligible for a connection. |

## Exceptions

| [UnsafeStateException](https://developer.android.com/reference/kotlin/android/app/admin/UnsafeStateException) | Exception thrown when a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager` operation failed because it was not safe to be executed at that moment. |
