# android.content.pm

## Interfaces

| [OnChecksumsReadyListener](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.OnChecksumsReadyListener) | Listener that gets notified when checksums are available. |
| --- | --- |

## Classes

| [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo) | Information you can retrieve about a particular application activity or receiver. |
| --- | --- |
| [ApkChecksum](https://developer.android.com/reference/kotlin/android/content/pm/ApkChecksum) | A typed checksum of an APK. |
| [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo) | Information you can retrieve about a particular application. |
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo) | Contains fields required to show archived package in Launcher. |
| --- | --- |
| [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo) | Contains fields required for archived package installation, i. |
| [Attribution](https://developer.android.com/reference/kotlin/android/content/pm/Attribution) | Information about an attribution declared by a package. |
| [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability) | Represents a capability that can be performed by an app, also known as App Action. |
| --- | --- |
| [CapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/CapabilityParams) | Represents the parameters and its matching names which can be associated with a `https://developer.android.com/reference/kotlin/android/content/pm/Capability`. |
| [ChangedPackages](https://developer.android.com/reference/kotlin/android/content/pm/ChangedPackages) | Packages that have been changed since the last time they were requested. |
| [Checksum](https://developer.android.com/reference/kotlin/android/content/pm/Checksum) | A typed checksum. |
| --- | --- |
| [ComponentInfo](https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo) | Base class containing information common to all application components (`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo`, `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo`). |
| [ConfigurationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo) | Information you can retrieve about hardware configuration preferences declared by an application. |
| [CrossProfileApps](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps) | Class for handling cross profile operations. |
| --- | --- |
| [FeatureGroupInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureGroupInfo) | A set of features that can be requested by an application. |
| [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo) | Definition of a single optional hardware or software feature of an Android device. |
| [InstallSourceInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo) | Information about how an app was installed. |
| --- | --- |
| [InstrumentationInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo) | Information you can retrieve about a particular piece of test instrumentation. |
| [LabeledIntent](https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent) | A special subclass of Intent that can have a custom label/icon associated with it. |
| [LauncherActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo) | A representation of an activity that can belong to this user or a managed profile associated with this user. |
| --- | --- |
| [LauncherApps](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps) | Class for retrieving a list of launchable activities for the current user and any associated managed profiles that are visible to the current user, which can be retrieved with `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()`. |
| [LauncherUserInfo](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo) | The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges). |
| [MemoryBudgetInfo](https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo) | Memory budget information for an application. |
| --- | --- |
| [ModuleInfo](https://developer.android.com/reference/kotlin/android/content/pm/ModuleInfo) | Information you can retrieve about a particular system module. |
| [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo) | Overall information about the contents of a package. |
| [PackageInstaller](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller) | Offers the ability to install, upgrade, and remove applications on the device. |
| --- | --- |
| [PackageItemInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo) | Base class containing information common to all package items held by the package manager. |
| [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager) | Class for retrieving various kinds of information related to the application packages that are currently installed on the device. |
| [PackageStats](https://developer.android.com/reference/kotlin/android/content/pm/PackageStats) | implementation of PackageStats associated with a application package. |
| --- | --- |
| [PathPermission](https://developer.android.com/reference/kotlin/android/content/pm/PathPermission) | Description of permissions needed to access a particular path in a `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo`. |
| [PermissionGroupInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo) | Information you can retrieve about a particular security permission group known to the system. |
| [PermissionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo) | Information you can retrieve about a particular security permission known to the system. |
| --- | --- |
| [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo) | Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`. |
| [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo) | Information that is returned from resolving an intent against an IntentFilter. |
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo) | Information you can retrieve about a particular application service. |
| --- | --- |
| [SharedLibraryInfo](https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo) | This class provides information for a shared library. |
| [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo) | Represents a shortcut that can be published via `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`. |
| [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager) | `ShortcutManager` executes operations on an app's set of *shortcuts*, which represent specific tasks and actions that users can perform within your app. |
| --- | --- |
| [Signature](https://developer.android.com/reference/kotlin/android/content/pm/Signature) | Opaque, immutable representation of a signing certificate associated with an application package. |
| [SigningInfo](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo) | Information pertaining to the signing certificates used to sign a package. |
| [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage) | Encapsulates a package and its version code. |
| --- | --- |

## Exceptions

| [SigningInfoException](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfoException) | Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information. |
| --- | --- |
