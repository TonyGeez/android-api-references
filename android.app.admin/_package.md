# android.app.admin

## Interfaces

| [OnClearApplicationUserDataListener](../android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener.md) | Callback used in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#clearApplicationUserData(android.content.ComponentName,%20kotlin.String,%20java.util.concurrent.Executor,%20android.app.admin.DevicePolicyManager.OnClearApplicationUserDataListener)` to indicate that the clearing of an application's user data is done. |
| --- | --- |

## Classes

| [ConnectEvent](../android/app/admin/ConnectEvent.md) | A class that represents a TCP connect event initiated through the standard network stack. |
| --- | --- |
| [DelegatedAdminReceiver](../android/app/admin/DelegatedAdminReceiver.md) | Base class for delegated apps to handle callbacks related to their delegated capabilities. |
| [DeviceAdminInfo](../android/app/admin/DeviceAdminInfo.md) | This class is used to specify meta information of a device administrator component. |
| [DeviceAdminReceiver](../android/app/admin/DeviceAdminReceiver.md) | Base class for implementing a device administration component. |
| --- | --- |
| [DeviceAdminService](../android/app/admin/DeviceAdminService.md) | Base class for a service that device owner/profile owners can optionally have. |
| [DevicePolicyIdentifiers](../android/app/admin/DevicePolicyIdentifiers.md) | Class containing identifiers for policy APIs in `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`, for example they will be passed in `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicySetResult(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` and `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicyChanged(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` to communicate updates of a certain policy back to the admin. |
| [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md) | Manages device policy and restrictions applied to the user of the device or apps running on the device. |
| --- | --- |
| [DevicePolicyResources](../android/app/admin/DevicePolicyResources.md) | Class containing the required identifiers to update device management resources. |
| [DevicePolicyResourcesManager](../android/app/admin/DevicePolicyResourcesManager.md) | Class containing required APIs to set, reset, and get device policy related resources. |
| [DnsEvent](../android/app/admin/DnsEvent.md) | A class that represents a DNS lookup event initiated through the standard network stack. |
| --- | --- |
| [FactoryResetProtectionPolicy](../android/app/admin/FactoryResetProtectionPolicy.md) | The factory reset protection policy determines which accounts can unlock a device that has gone through untrusted factory reset. |
| [FreezePeriod](../android/app/admin/FreezePeriod.md) | A class that represents one freeze period which repeats *annually*. |
| [ManagedSubscriptionsPolicy](../android/app/admin/ManagedSubscriptionsPolicy.md) | A policy class that describes how managed SIM subscriptions should behave on the device. |
| --- | --- |
| [NetworkEvent](../android/app/admin/NetworkEvent.md) | An abstract class that represents a network event. |
| [PackageIdentifier](../android/app/admin/PackageIdentifier.md) | Identifies a package on the current device. |
| [PackagePolicy](../android/app/admin/PackagePolicy.md) | A generic class that defines which APK packages are in scope for some device policy. |
| --- | --- |
| [PolicyIdentifier](../android/app/admin/PolicyIdentifier.md) | Represents a type safe identifier for a policy. |
| [PolicyUpdateReceiver](../android/app/admin/PolicyUpdateReceiver.md) | Base class for implementing a policy update receiver. |
| [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md) | Class containing the reason for the policy (set from `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`) update (e.g. success, failure reasons, etc.). |
| --- | --- |
| [PreferentialNetworkServiceConfig](../android/app/admin/PreferentialNetworkServiceConfig.md) | Network configuration to be set for the user profile. |
| [SecurityLog](../android/app/admin/SecurityLog.md) | Definitions for working with security logs. |
| [SystemUpdateInfo](../android/app/admin/SystemUpdateInfo.md) | A class containing information about a pending system update. |
| --- | --- |
| [SystemUpdatePolicy](../android/app/admin/SystemUpdatePolicy.md) | Determines when over-the-air system updates are installed on a device. |
| [TargetUser](../android/app/admin/TargetUser.md) | Class representing the target user of a policy set by an admin (set from `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager`), this is passed in to `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicySetResult(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)` and `https://developer.android.com/reference/kotlin/android/app/admin/PolicyUpdateReceiver#onPolicyChanged(android.content.Context,%20kotlin.String,%20android.os.Bundle,%20android.app.admin.TargetUser,%20android.app.admin.PolicyUpdateResult)`. |
| [WifiSsidPolicy](../android/app/admin/WifiSsidPolicy.md) | Used to indicate the Wi-Fi SSID restriction policy the network must satisfy in order to be eligible for a connection. |
| --- | --- |

## Exceptions

| [UnsafeStateException](../android/app/admin/UnsafeStateException.md) | Exception thrown when a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager` operation failed because it was not safe to be executed at that moment. |
| --- | --- |
