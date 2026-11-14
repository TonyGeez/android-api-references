# android.content.pm

## Interfaces

| [OnChecksumsReadyListener](../android/content/pm/PackageManager.OnChecksumsReadyListener.md) | Listener that gets notified when checksums are available. |
| --- | --- |

## Classes

| [ActivityInfo](ActivityInfo.md) | Information you can retrieve about a particular application activity or receiver. |
| --- | --- |
| [ApkChecksum](ApkChecksum.md) | A typed checksum of an APK. |
| [ApplicationInfo](ApplicationInfo.md) | Information you can retrieve about a particular application. |
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | Contains fields required to show archived package in Launcher. |
| --- | --- |
| [ArchivedPackageInfo](ArchivedPackageInfo.md) | Contains fields required for archived package installation, i. |
| [Attribution](Attribution.md) | Information about an attribution declared by a package. |
| [Capability](Capability.md) | Represents a capability that can be performed by an app, also known as App Action. |
| --- | --- |
| [CapabilityParams](CapabilityParams.md) | Represents the parameters and its matching names which can be associated with a `https://developer.android.com/reference/kotlin/android/content/pm/Capability`. |
| [ChangedPackages](ChangedPackages.md) | Packages that have been changed since the last time they were requested. |
| [Checksum](Checksum.md) | A typed checksum. |
| --- | --- |
| [ComponentInfo](ComponentInfo.md) | Base class containing information common to all application components (`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo`). |
| [ConfigurationInfo](ConfigurationInfo.md) | Information you can retrieve about hardware configuration preferences declared by an application. |
| [CrossProfileApps](CrossProfileApps.md) | Class for handling cross profile operations. |
| --- | --- |
| [FeatureGroupInfo](FeatureGroupInfo.md) | A set of features that can be requested by an application. |
| [FeatureInfo](FeatureInfo.md) | Definition of a single optional hardware or software feature of an Android device. |
| [InstallSourceInfo](InstallSourceInfo.md) | Information about how an app was installed. |
| --- | --- |
| [InstrumentationInfo](InstrumentationInfo.md) | Information you can retrieve about a particular piece of test instrumentation. |
| [LabeledIntent](LabeledIntent.md) | A special subclass of Intent that can have a custom label/icon associated with it. |
| [LauncherActivityInfo](LauncherActivityInfo.md) | A representation of an activity that can belong to this user or a managed profile associated with this user. |
| --- | --- |
| [LauncherApps](LauncherApps.md) | Class for retrieving a list of launchable activities for the current user and any associated managed profiles that are visible to the current user, which can be retrieved with `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()`. |
| [LauncherUserInfo](LauncherUserInfo.md) | The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges). |
| [MemoryBudgetInfo](MemoryBudgetInfo.md) | Memory budget information for an application. |
| --- | --- |
| [ModuleInfo](ModuleInfo.md) | Information you can retrieve about a particular system module. |
| [PackageInfo](PackageInfo.md) | Overall information about the contents of a package. |
| [PackageInstaller](PackageInstaller.md) | Offers the ability to install, upgrade, and remove applications on the device. |
| --- | --- |
| [PackageItemInfo](PackageItemInfo.md) | Base class containing information common to all package items held by the package manager. |
| [PackageManager](PackageManager.md) | Class for retrieving various kinds of information related to the application packages that are currently installed on the device. |
| [PackageStats](PackageStats.md) | implementation of PackageStats associated with a application package. |
| --- | --- |
| [PathPermission](PathPermission.md) | Description of permissions needed to access a particular path in a `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo`. |
| [PermissionGroupInfo](PermissionGroupInfo.md) | Information you can retrieve about a particular security permission group known to the system. |
| [PermissionInfo](PermissionInfo.md) | Information you can retrieve about a particular security permission known to the system. |
| --- | --- |
| [ProviderInfo](ProviderInfo.md) | Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`. |
| [ResolveInfo](ResolveInfo.md) | Information that is returned from resolving an intent against an IntentFilter. |
| [ServiceInfo](ServiceInfo.md) | Information you can retrieve about a particular application service. |
| --- | --- |
| [SharedLibraryInfo](SharedLibraryInfo.md) | This class provides information for a shared library. |
| [ShortcutInfo](ShortcutInfo.md) | Represents a shortcut that can be published via `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`. |
| [ShortcutManager](ShortcutManager.md) | `ShortcutManager` executes operations on an app's set of *shortcuts*, which represent specific tasks and actions that users can perform within your app. |
| --- | --- |
| [Signature](Signature.md) | Opaque, immutable representation of a signing certificate associated with an application package. |
| [SigningInfo](SigningInfo.md) | Information pertaining to the signing certificates used to sign a package. |
| [VersionedPackage](VersionedPackage.md) | Encapsulates a package and its version code. |
| --- | --- |

## Exceptions

| [SigningInfoException](SigningInfoException.md) | Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information. |
| --- | --- |
