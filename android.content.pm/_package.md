# android.content.pm

## Interfaces

| [OnChecksumsReadyListener](../android/content/pm/PackageManager.OnChecksumsReadyListener.md) | Listener that gets notified when checksums are available. |
| --- | --- |

## Classes

| [ActivityInfo](../android/content/pm/ActivityInfo.md) | Information you can retrieve about a particular application activity or receiver. |
| --- | --- |
| [ApkChecksum](../android/content/pm/ApkChecksum.md) | A typed checksum of an APK. |
| [ApplicationInfo](../android/content/pm/ApplicationInfo.md) | Information you can retrieve about a particular application. |
| [ArchivedActivityInfo](../android/content/pm/ArchivedActivityInfo.md) | Contains fields required to show archived package in Launcher. |
| --- | --- |
| [ArchivedPackageInfo](../android/content/pm/ArchivedPackageInfo.md) | Contains fields required for archived package installation, i. |
| [Attribution](../android/content/pm/Attribution.md) | Information about an attribution declared by a package. |
| [Capability](../android/content/pm/Capability.md) | Represents a capability that can be performed by an app, also known as App Action. |
| --- | --- |
| [CapabilityParams](../android/content/pm/CapabilityParams.md) | Represents the parameters and its matching names which can be associated with a `https://developer.android.com/reference/kotlin/android/content/pm/Capability`. |
| [ChangedPackages](../android/content/pm/ChangedPackages.md) | Packages that have been changed since the last time they were requested. |
| [Checksum](../android/content/pm/Checksum.md) | A typed checksum. |
| --- | --- |
| [ComponentInfo](../android/content/pm/ComponentInfo.md) | Base class containing information common to all application components (`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo`). |
| [ConfigurationInfo](../android/content/pm/ConfigurationInfo.md) | Information you can retrieve about hardware configuration preferences declared by an application. |
| [CrossProfileApps](../android/content/pm/CrossProfileApps.md) | Class for handling cross profile operations. |
| --- | --- |
| [FeatureGroupInfo](../android/content/pm/FeatureGroupInfo.md) | A set of features that can be requested by an application. |
| [FeatureInfo](../android/content/pm/FeatureInfo.md) | Definition of a single optional hardware or software feature of an Android device. |
| [InstallSourceInfo](../android/content/pm/InstallSourceInfo.md) | Information about how an app was installed. |
| --- | --- |
| [InstrumentationInfo](../android/content/pm/InstrumentationInfo.md) | Information you can retrieve about a particular piece of test instrumentation. |
| [LabeledIntent](../android/content/pm/LabeledIntent.md) | A special subclass of Intent that can have a custom label/icon associated with it. |
| [LauncherActivityInfo](../android/content/pm/LauncherActivityInfo.md) | A representation of an activity that can belong to this user or a managed profile associated with this user. |
| --- | --- |
| [LauncherApps](../android/content/pm/LauncherApps.md) | Class for retrieving a list of launchable activities for the current user and any associated managed profiles that are visible to the current user, which can be retrieved with `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()`. |
| [LauncherUserInfo](../android/content/pm/LauncherUserInfo.md) | The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges). |
| [MemoryBudgetInfo](../android/content/pm/MemoryBudgetInfo.md) | Memory budget information for an application. |
| --- | --- |
| [ModuleInfo](../android/content/pm/ModuleInfo.md) | Information you can retrieve about a particular system module. |
| [PackageInfo](../android/content/pm/PackageInfo.md) | Overall information about the contents of a package. |
| [PackageInstaller](../android/content/pm/PackageInstaller.md) | Offers the ability to install, upgrade, and remove applications on the device. |
| --- | --- |
| [PackageItemInfo](../android/content/pm/PackageItemInfo.md) | Base class containing information common to all package items held by the package manager. |
| [PackageManager](../android/content/pm/PackageManager.md) | Class for retrieving various kinds of information related to the application packages that are currently installed on the device. |
| [PackageStats](../android/content/pm/PackageStats.md) | implementation of PackageStats associated with a application package. |
| --- | --- |
| [PathPermission](../android/content/pm/PathPermission.md) | Description of permissions needed to access a particular path in a `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo`. |
| [PermissionGroupInfo](../android/content/pm/PermissionGroupInfo.md) | Information you can retrieve about a particular security permission group known to the system. |
| [PermissionInfo](../android/content/pm/PermissionInfo.md) | Information you can retrieve about a particular security permission known to the system. |
| --- | --- |
| [ProviderInfo](../android/content/pm/ProviderInfo.md) | Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`. |
| [ResolveInfo](../android/content/pm/ResolveInfo.md) | Information that is returned from resolving an intent against an IntentFilter. |
| [ServiceInfo](../android/content/pm/ServiceInfo.md) | Information you can retrieve about a particular application service. |
| --- | --- |
| [SharedLibraryInfo](../android/content/pm/SharedLibraryInfo.md) | This class provides information for a shared library. |
| [ShortcutInfo](../android/content/pm/ShortcutInfo.md) | Represents a shortcut that can be published via `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`. |
| [ShortcutManager](../android/content/pm/ShortcutManager.md) | `ShortcutManager` executes operations on an app's set of *shortcuts*, which represent specific tasks and actions that users can perform within your app. |
| --- | --- |
| [Signature](../android/content/pm/Signature.md) | Opaque, immutable representation of a signing certificate associated with an application package. |
| [SigningInfo](../android/content/pm/SigningInfo.md) | Information pertaining to the signing certificates used to sign a package. |
| [VersionedPackage](../android/content/pm/VersionedPackage.md) | Encapsulates a package and its version code. |
| --- | --- |

## Exceptions

| [SigningInfoException](../android/content/pm/SigningInfoException.md) | Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information. |
| --- | --- |
