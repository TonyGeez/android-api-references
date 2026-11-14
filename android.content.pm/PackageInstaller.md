# PackageInstaller

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageInstaller

Kotlin| [Java](PackageInstaller.md) 
| --- | --- |

```
open class PackageInstaller
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.PackageInstaller](PackageInstaller.md) |

Offers the ability to install, upgrade, and remove applications on the device. This includes support for apps packaged either as a single "monolithic" APK, or apps packaged as multiple "split" APKs.

An app is delivered for installation through a [PackageInstaller.Session](../android/content/pm/PackageInstaller.Session.md), which any app can create. Once the session is created, the installer can stream one or more APKs into place until it decides to either commit or destroy the session. Committing may require user intervention to complete the installation, unless the caller falls into one of the following categories, in which case the installation will complete automatically.

- the device owner
- the affiliated profile owner

Sessions can install brand new apps, upgrade existing apps, or add new splits into an existing app.

Apps packaged as multiple split APKs always consist of a single "base" APK (with a`null`split name) and zero or more "split" APKs (with unique split names). Any subset of these APKs can be installed together, as long as the following constraints are met:

- All APKs must have the exact same package name, version code, and signing certificates.
- All APKs must have unique split names.
- All installations must contain a single base APK.

The ApiDemos project contains examples of using this API:`ApiDemos/src/com/example/android/apis/content/InstallApk*.java`.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md) A class to encapsulate constraints for installation. |
| | [InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md) The callback result of [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](PackageInstaller.md)). |
| | [PreapprovalDetails](../android/content/pm/PackageInstaller.PreapprovalDetails.md) Details for requesting the pre-commit install approval. |
| --- | --- |
| open | [Session](../android/content/pm/PackageInstaller.Session.md) An installation that is being actively staged. |
| abstract | [SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md) Events for observing session lifecycle. |
| open | [SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md) Details for an active install session. |
| --- | --- |
| open | [SessionParams](../android/content/pm/PackageInstaller.SessionParams.md) Parameters for creating a new [PackageInstaller.Session](../android/content/pm/PackageInstaller.Session.md). |
| | [UnarchivalState](../android/content/pm/PackageInstaller.UnarchivalState.md) Used to communicate the unarchival state in [reportUnarchivalState](PackageInstaller.md)). |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_COMMITTED](PackageInstaller.md) Broadcast Action: Explicit broadcast sent to the last known default launcher when a session for a new install is committed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_DETAILS](PackageInstaller.md) Activity Action: Show details about a particular install session. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_UPDATED](PackageInstaller.md) Broadcast Action: Send information about a staged install session when its state is updated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED](PackageInstaller.md) Developer verification failed because the developer cannot be verified, as reported by the verifier via [DeveloperVerificationSession.reportVerificationComplete(DeveloperVerificationStatus)](PackageInstaller.md) or [DeveloperVerificationSession.reportVerificationComplete(](PackageInstaller.md) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](PackageInstaller.md) Developer verification failed because the network is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN](PackageInstaller.md) Developer verification failed because of unknown reasons, such as when the verifier times out or cannot be connected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE](PackageInstaller.md) An extra containing the response provided by the developer verifier to any extension params provided by the installer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON](PackageInstaller.md) When an installation fails because the developer verification was incomplete or blocked, this extra provides a code that explains the reason, such as [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](PackageInstaller.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED](PackageInstaller.md) An extra containing a boolean indicating whether the lite version of the developer verification was performed on the app to be installed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INSTALL_CONSTRAINTS](PackageInstaller.md) The [InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md) object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INSTALL_CONSTRAINTS_RESULT](PackageInstaller.md) The [InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md) object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_OTHER_PACKAGE_NAME](PackageInstaller.md) Another package name relevant to a status. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](PackageInstaller.md) Package name that an operation is working with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PRE_APPROVAL](PackageInstaller.md) Indicate if the status is for a pre-approval request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SESSION](PackageInstaller.md) [SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md) that an operation is working with. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SESSION_ID](PackageInstaller.md) An integer session ID that an operation is working with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS](PackageInstaller.md) Current status of an operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS_MESSAGE](PackageInstaller.md) Detailed string representation of the status, including raw details that are useful for debugging. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STORAGE_PATH](PackageInstaller.md) Storage path relevant to a status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_ALL_USERS](PackageInstaller.md) If true, the requestor of the unarchival has specified that the app should be unarchived for all users. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_ID](PackageInstaller.md) Extra field for the unarchive ID. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_PACKAGE_NAME](PackageInstaller.md) Extra field for the package name of a package that is requested to be unarchived. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_STATUS](PackageInstaller.md) Current status of an unarchive operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_DOWNLOADED_FILE](PackageInstaller.md) Code indicating that the package being installed comes from a file that was downloaded to the device by the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_LOCAL_FILE](PackageInstaller.md) Code indicating that the package being installed comes from a local file on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_OTHER](PackageInstaller.md) Code indicating that the package being installed is from a source not reflected by any other package source constant. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_STORE](PackageInstaller.md) Code indicating that the package being installed is from a store. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_UNSPECIFIED](PackageInstaller.md) The installer did not call [PackageInstaller.SessionParams.setPackageSource(int)](../android/content/pm/PackageInstaller.SessionParams.md))to specify the package source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE](PackageInstaller.md) The operation failed in a generic way. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_ABORTED](PackageInstaller.md) The operation failed because it was actively aborted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_BLOCKED](PackageInstaller.md) The operation failed because it was blocked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_CONFLICT](PackageInstaller.md) The operation failed because it conflicts (or is inconsistent with) with another package already installed on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_INCOMPATIBLE](PackageInstaller.md) The operation failed because it is fundamentally incompatible with this device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_INVALID](PackageInstaller.md) The operation failed because one or more of the APKs was invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_STORAGE](PackageInstaller.md) The operation failed because of storage issues. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_TIMEOUT](PackageInstaller.md) The operation failed because it didn't complete within the specified timeout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PENDING_USER_ACTION](PackageInstaller.md) User action is currently required to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESS](PackageInstaller.md) The operation succeeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSTALLER_DISABLED](PackageInstaller.md) The installer responsible for the unarchival is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](PackageInstaller.md) The installer responsible for the unarchival has been uninstalled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](PackageInstaller.md) Not enough storage to unarchive the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_NO_CONNECTIVITY](PackageInstaller.md) The device is not connected to the internet |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_USER_ACTION_NEEDED](PackageInstaller.md) The user needs to interact with the installer to enable the installation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_GENERIC_ERROR](PackageInstaller.md) Generic error: The app cannot be unarchived. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_OK](PackageInstaller.md) The unarchival is possible and will commence. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandonSession](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Completely abandon the given session, destroying all staged data and rendering it invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkInstallConstraints](PackageInstaller.md))`(`packageNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `constraints:` ` [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [Consumer](../java.util.function/Consumer.md)< [PackageInstaller.InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md)!>`)` Check if install constraints are satisfied for the given packages. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitSessionAfterInstallConstraintsAreMet](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`, `constraints:` ` [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md)`, `timeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Commit the session when all constraints are satisfied. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [createSession](PackageInstaller.md))`(`params:` ` [PackageInstaller.SessionParams](../android/content/pm/PackageInstaller.SessionParams.md)`)` Create a new session using the given parameters, returning a unique ID that represents the session. |
| open [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)? | [getActiveStagedSession](PackageInstaller.md))`()` Returns first active staged session, or`null`if there is none. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!\> | [getActiveStagedSessions](PackageInstaller.md))`()` Returns list of active staged sessions. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!\> | [getAllSessions](PackageInstaller.md))`()` Return list of all known install sessions, regardless of the installer. |
| [ComponentName](../android.content/ComponentName.md)? | [getDeveloperVerificationServiceProvider](PackageInstaller.md))`()` Return the component name of the developer verification service provider, for the purpose of interacting with the specific verifier in relation to extension parameters and response structure. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!\> | [getMySessions](PackageInstaller.md))`()` Return list of all known install sessions owned by the calling app. |
| --- | --- |
| open [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)? | [getSessionInfo](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return details for a specific session. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!\> | [getStagedSessions](PackageInstaller.md))`()` Return list of all staged install sessions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [installExistingPackage](PackageInstaller.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `installReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)?`)` Install the given package, which already exists on the device, for the user for which this installer was created. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [installPackageArchived](PackageInstaller.md))`(`archivedPackageInfo:` ` [ArchivedPackageInfo](ArchivedPackageInfo.md)`, `sessionParams:` ` [PackageInstaller.SessionParams](../android/content/pm/PackageInstaller.SessionParams.md)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Install package in an archived state. |
| open [PackageInstaller.Session](../android/content/pm/PackageInstaller.Session.md) | [openSession](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Open an existing session to actively perform work. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerSessionCallback](PackageInstaller.md))`(`callback:` ` [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md)`)` Register to watch for session lifecycle events. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerSessionCallback](PackageInstaller.md))`(`callback:` ` [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)`)` Register to watch for session lifecycle events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportUnarchivalState](PackageInstaller.md))`(`unarchivalState:` ` [PackageInstaller.UnarchivalState](../android/content/pm/PackageInstaller.UnarchivalState.md)`)` Reports the state of an unarchival to the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportUnarchivalStatus](PackageInstaller.md))`(`unarchiveId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requiredStorageBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `userActionIntent:` ` [PendingIntent](../android.app/PendingIntent.md)?`)` Reports the status of an unarchival to the system. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestArchive](PackageInstaller.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Requests to archive a package which is currently installed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestUnarchive](PackageInstaller.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Requests to unarchive a currently archived package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](PackageInstaller.md))`(`versionedPackage:` ` [VersionedPackage](VersionedPackage.md)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Uninstall the given package with a specific version code, removing it completely from the device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](PackageInstaller.md))`(`versionedPackage:` ` [VersionedPackage](VersionedPackage.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Uninstall the given package with a specific version code, removing it completely from the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](PackageInstaller.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)`)` Uninstall the given package, removing it completely from the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstallExistingPackage](PackageInstaller.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](../android.content/IntentSender.md)?`)` Uninstall the given package for the user for which this installer was created if the package will still exist for other users on the device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterSessionCallback](PackageInstaller.md))`(`callback:` ` [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md)`)` Unregister a previously registered callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSessionAppIcon](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appIcon:` ` [Bitmap](../android.graphics/Bitmap.md)?`)` Update the icon representing the app being installed in a specific session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSessionAppLabel](PackageInstaller.md))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appLabel:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Update the label representing the app being installed in a specific session. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForInstallConstraints](PackageInstaller.md))`(`packageNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `constraints:` ` [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md)`, `callback:` ` [IntentSender](../android.content/IntentSender.md)`, `timeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Similar to [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](PackageInstaller.md)), but the callback is invoked only when the constraints are satisfied or after timeout. |

## Constants

### ACTION_SESSION_COMMITTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_COMMITTED: String
```

Broadcast Action: Explicit broadcast sent to the last known default launcher when a session for a new install is committed. For managed profile, this is sent to the default launcher of the primary profile. For user-profiles that have items restricted on home screen, this broadcast is sent to the default launcher of the primary profile, only if it has either Manifest.permission.ACCESS_HIDDEN_PROFILES_FULL or Manifest.permission.ACCESS_HIDDEN_PROFILES permission.

The associated session is defined in [EXTRA_SESSION](PackageInstaller.md) and the user for which this session was created in [Intent.EXTRA_USER](../android.content/Intent.md). 

 Value: "android.content.pm.action.SESSION_COMMITTED"

### ACTION_SESSION_DETAILS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_DETAILS: String
```

Activity Action: Show details about a particular install session. This may surface actions such as pause, resume, or cancel.

This should always be scoped to the installer package that owns the session. Clients should use [SessionInfo.createDetailsIntent()](../android/content/pm/PackageInstaller.SessionInfo.md))to build this intent correctly.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

The session to show details for is defined in [EXTRA_SESSION_ID](PackageInstaller.md). 

 Value: "android.content.pm.action.SESSION_DETAILS"

### ACTION_SESSION_UPDATED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_UPDATED: String
```

Broadcast Action: Send information about a staged install session when its state is updated.

The associated session information is defined in [EXTRA_SESSION](PackageInstaller.md). 

 Value: "android.content.pm.action.SESSION_UPDATED"

### DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED: Int
```

Developer verification failed because the developer cannot be verified, as reported by the verifier via [DeveloperVerificationSession.reportVerificationComplete(DeveloperVerificationStatus)](PackageInstaller.md) or [DeveloperVerificationSession.reportVerificationComplete(](PackageInstaller.md) 

 Value: 2

### DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE: Int
```

Developer verification failed because the network is unavailable. This corresponds to the status of [DeveloperVerificationSession.DEVELOPER_VERIFICATION_INCOMPLETE_NETWORK_UNAVAILABLE](PackageInstaller.md) reported by the verifier via [DeveloperVerificationSession.reportVerificationIncomplete(int)](PackageInstaller.md). 

 Value: 1

### DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN: Int
```

Developer verification failed because of unknown reasons, such as when the verifier times out or cannot be connected. It can also corresponds to the status of [DeveloperVerificationSession.DEVELOPER_VERIFICATION_INCOMPLETE_UNKNOWN](PackageInstaller.md) reported by the verifier via [DeveloperVerificationSession.reportVerificationIncomplete(int)](PackageInstaller.md). 

 Value: 0

### EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE: String
```

An extra containing the response provided by the developer verifier to any extension params provided by the installer. It will be of type [PersistableBundle](../android.os/PersistableBundle.md). 

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_EXTENSION_RESPONSE"

### EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON: String
```

When an installation fails because the developer verification was incomplete or blocked, this extra provides a code that explains the reason, such as [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](PackageInstaller.md). It is included in the installation result returned via the [IntentSender](../android.content/IntentSender.md) in [Session.commit(IntentSender)](../android/content/pm/PackageInstaller.Session.md)). However, along with this reason code, installers can receive different status codes from [EXTRA_STATUS](PackageInstaller.md) depending on their target SDK and permission status:

- Installers without the [INSTALL_PACKAGES](../android/Manifest.permission.md) permission but with the [REQUEST_INSTALL_PACKAGES](../android/Manifest.permission.md) permission and targeting [API 36](../android/os/Build.VERSION_CODES.md) or less will first receive the [STATUS_PENDING_USER_ACTION](PackageInstaller.md) status code without this reason code. They will be forced through the user action flow to allow the OS to inform the user of such verification context before continuing to fail the install. If the user has the option to bypass the verification result and chooses to do so, the installation will proceed. Otherwise, the installer will receive the [STATUS_FAILURE_ABORTED](PackageInstaller.md) status code along with this reason code that explains why the verification had failed.
- Installers with the [INSTALL_PACKAGES](../android/Manifest.permission.md) permission and targeting [API 36](../android/os/Build.VERSION_CODES.md) or less will directly receive the [STATUS_FAILURE_ABORTED](PackageInstaller.md) status code. This is because they are not expected to have the capability of handling the [STATUS_PENDING_USER_ACTION](PackageInstaller.md) flow, so the installation will directly fail. This reason code will be supplied to them for providing additional information.
- For all installers targeting higher than [API 36](../android/os/Build.VERSION_CODES.md)
 - For situations that require user input, such as when the developer verification policy allows the user to bypass a verification failure caused by network issues, the installer will receive a [STATUS_PENDING_USER_ACTION](PackageInstaller.md) status code without this reason code. The installer will be forced through the user action flow to allow the OS to inform the user of such verification context before continuing to fail the installation. If the user has the option to bypass the verification result and chooses to do so, the installation will proceed. Otherwise, the install will receive the [STATUS_FAILURE_ABORTED](PackageInstaller.md) status code along with this reason code that explains why the verification had failed.
 - For all other situations, the installer will receive a [STATUS_FAILURE_ABORTED](PackageInstaller.md) status code along with this reason code, so the installers can explain the failure to the user accordingly. An [Intent.EXTRA_INTENT](../android.content/Intent.md) will also be populated with an intent that can provide additional context where appropriate, should the installer prefer to defer to the OS to explain the failure to the user.

<br />

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_FAILURE_REASON"

### EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED: String
```

An extra containing a boolean indicating whether the lite version of the developer verification was performed on the app to be installed. It is included in the installation result returned via the [IntentSender](../android.content/IntentSender.md) in [Session.commit(IntentSender)](../android/content/pm/PackageInstaller.Session.md))when the installation failed. 

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_LITE_PERFORMED"

### EXTRA_INSTALL_CONSTRAINTS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INSTALL_CONSTRAINTS: String
```

The [InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md) object. 

 Value: "android.content.pm.extra.INSTALL_CONSTRAINTS"

**See Also**

- [android.content.Intent#getParcelableExtra(String, Class)](../android.content/Intent.md))
- [#waitForInstallConstraints(List, InstallConstraints, IntentSender, long)](PackageInstaller.md)) 

### EXTRA_INSTALL_CONSTRAINTS_RESULT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INSTALL_CONSTRAINTS_RESULT: String
```

The [InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md) object. 

 Value: "android.content.pm.extra.INSTALL_CONSTRAINTS_RESULT"

**See Also**

- [android.content.Intent#getParcelableExtra(String, Class)](../android.content/Intent.md))
- [#waitForInstallConstraints(List, InstallConstraints, IntentSender, long)](PackageInstaller.md)) 

### EXTRA_OTHER_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_OTHER_PACKAGE_NAME: String
```

Another package name relevant to a status. This is typically the package responsible for causing an operation failure. 

 Value: "android.content.pm.extra.OTHER_PACKAGE_NAME"

**See Also**

- [android.content.Intent#getStringExtra(String)](../android.content/Intent.md)) 

### EXTRA_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PACKAGE_NAME: String
```

Package name that an operation is working with. 

 Value: "android.content.pm.extra.PACKAGE_NAME"

**See Also**

- [android.content.Intent#getStringExtra(String)](../android.content/Intent.md)) 

### EXTRA_PRE_APPROVAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PRE_APPROVAL: String
```

Indicate if the status is for a pre-approval request. If callers use the same [IntentSender](../android.content/IntentSender.md) for both [Session.requestUserPreapproval(PreapprovalDetails, IntentSender)](../android/content/pm/PackageInstaller.Session.md))and [Session.commit(IntentSender)](../android/content/pm/PackageInstaller.Session.md)), they can use this to differentiate between them. 

 Value: "android.content.pm.extra.PRE_APPROVAL"

**See Also**

- [android.content.Intent#getBooleanExtra(String, boolean)](../android.content/Intent.md)) 

### EXTRA_SESSION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SESSION: String
```

[SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md) that an operation is working with. 

 Value: "android.content.pm.extra.SESSION"

**See Also**

- [android.content.Intent#getParcelableExtra(String)](../android.content/Intent.md)) 

### EXTRA_SESSION_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SESSION_ID: String
```

An integer session ID that an operation is working with. 

 Value: "android.content.pm.extra.SESSION_ID"

**See Also**

- [android.content.Intent#getIntExtra(String, int)](../android.content/Intent.md)) 

### EXTRA_STATUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS: String
```

Current status of an operation. Will be one of [STATUS_PENDING_USER_ACTION](PackageInstaller.md), [STATUS_SUCCESS](PackageInstaller.md), [STATUS_FAILURE](PackageInstaller.md), [STATUS_FAILURE_ABORTED](PackageInstaller.md), [STATUS_FAILURE_BLOCKED](PackageInstaller.md), [STATUS_FAILURE_CONFLICT](PackageInstaller.md), [STATUS_FAILURE_INCOMPATIBLE](PackageInstaller.md), [STATUS_FAILURE_INVALID](PackageInstaller.md), [STATUS_FAILURE_STORAGE](PackageInstaller.md), or [STATUS_FAILURE_TIMEOUT](PackageInstaller.md).

More information about a status may be available through additional extras; see the individual status documentation for details. 

 Value: "android.content.pm.extra.STATUS"

**See Also**

- [android.content.Intent#getIntExtra(String, int)](../android.content/Intent.md)) 

### EXTRA_STATUS_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS_MESSAGE: String
```

Detailed string representation of the status, including raw details that are useful for debugging. 

 Value: "android.content.pm.extra.STATUS_MESSAGE"

**See Also**

- [android.content.Intent#getStringExtra(String)](../android.content/Intent.md)) 

### EXTRA_STORAGE_PATH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STORAGE_PATH: String
```

Storage path relevant to a status. 

 Value: "android.content.pm.extra.STORAGE_PATH"

**See Also**

- [android.content.Intent#getStringExtra(String)](../android.content/Intent.md)) 

### EXTRA_UNARCHIVE_ALL_USERS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_ALL_USERS: String
```

If true, the requestor of the unarchival has specified that the app should be unarchived for all users. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](../android.content/Intent.md) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_ALL_USERS"

### EXTRA_UNARCHIVE_ID

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_ID: String
```

Extra field for the unarchive ID. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](../android.content/Intent.md) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_ID"

**See Also**

- [android.content.pm.PackageInstaller.SessionParams#setUnarchiveId](../android/content/pm/PackageInstaller.SessionParams.md)) 

### EXTRA_UNARCHIVE_PACKAGE_NAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_PACKAGE_NAME: String
```

Extra field for the package name of a package that is requested to be unarchived. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](../android.content/Intent.md) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_PACKAGE_NAME"

### EXTRA_UNARCHIVE_STATUS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_STATUS: String
```

Current status of an unarchive operation. Will be one of [UNARCHIVAL_OK](PackageInstaller.md), [UNARCHIVAL_ERROR_USER_ACTION_NEEDED](PackageInstaller.md), [UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](PackageInstaller.md), [UNARCHIVAL_ERROR_NO_CONNECTIVITY](PackageInstaller.md), [UNARCHIVAL_GENERIC_ERROR](PackageInstaller.md), [UNARCHIVAL_ERROR_INSTALLER_DISABLED](PackageInstaller.md) or [UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](PackageInstaller.md).

If the status is not [UNARCHIVAL_OK](PackageInstaller.md), then [Intent.EXTRA_INTENT](../android.content/Intent.md) will be set with an intent for a corresponding follow-up action (e.g. storage clearing dialog) or a failure dialog.

Used as part of [requestUnarchive](PackageInstaller.md))to return the status of the unarchival through the [IntentSender](../android.content/IntentSender.md). 

 Value: "android.content.pm.extra.UNARCHIVE_STATUS"

**See Also**

- [#requestUnarchive](PackageInstaller.md)) 

### PACKAGE_SOURCE_DOWNLOADED_FILE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_DOWNLOADED_FILE: Int
```

Code indicating that the package being installed comes from a file that was downloaded to the device by the user. For use in place of [PACKAGE_SOURCE_LOCAL_FILE](PackageInstaller.md) when the installer knows the package was downloaded. 

 Value: 4

### PACKAGE_SOURCE_LOCAL_FILE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_LOCAL_FILE: Int
```

Code indicating that the package being installed comes from a local file on the device. A file manager that is facilitating the installation of an APK file would use this. 

 Value: 3

### PACKAGE_SOURCE_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_OTHER: Int
```

Code indicating that the package being installed is from a source not reflected by any other package source constant. 

 Value: 1

### PACKAGE_SOURCE_STORE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_STORE: Int
```

Code indicating that the package being installed is from a store. An app store that installs an app for the user would use this. 

 Value: 2

### PACKAGE_SOURCE_UNSPECIFIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_UNSPECIFIED: Int
```

The installer did not call [PackageInstaller.SessionParams.setPackageSource(int)](../android/content/pm/PackageInstaller.SessionParams.md))to specify the package source. 

 Value: 0

### STATUS_FAILURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE: Int
```

The operation failed in a generic way. The system will always try to provide a more specific failure reason, but in some rare cases this may be delivered. 

 Value: 1

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md) 

### STATUS_FAILURE_ABORTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_ABORTED: Int
```

The operation failed because it was actively aborted. For example, the user actively declined requested permissions, or the session was abandoned. 

 Value: 3

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md) 

### STATUS_FAILURE_BLOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_BLOCKED: Int
```

The operation failed because it was blocked. For example, a device policy may be blocking the operation, a package verifier may have blocked the operation, or the app may be required for core system operation.

The result may also contain [EXTRA_OTHER_PACKAGE_NAME](PackageInstaller.md) with the specific package blocking the install. 

 Value: 2

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md)
- [#EXTRA_OTHER_PACKAGE_NAME](PackageInstaller.md) 

### STATUS_FAILURE_CONFLICT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_CONFLICT: Int
```

The operation failed because it conflicts (or is inconsistent with) with another package already installed on the device. For example, an existing permission, incompatible certificates, etc. The user may be able to uninstall another app to fix the issue.

The result may also contain [EXTRA_OTHER_PACKAGE_NAME](PackageInstaller.md) with the specific package identified as the cause of the conflict. 

 Value: 5

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md)
- [#EXTRA_OTHER_PACKAGE_NAME](PackageInstaller.md) 

### STATUS_FAILURE_INCOMPATIBLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_INCOMPATIBLE: Int
```

The operation failed because it is fundamentally incompatible with this device. For example, the app may require a hardware feature that doesn't exist, it may be missing native code for the ABIs supported by the device, or it requires a newer SDK version, etc. Starting in [Build.VERSION_CODES.UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), an app with only 32-bit native code can still be installed on a device that supports both 64-bit and 32-bit ABIs. However, a warning dialog will be displayed when the app is launched. 

 Value: 7

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md) 

### STATUS_FAILURE_INVALID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_INVALID: Int
```

The operation failed because one or more of the APKs was invalid. For example, they might be malformed, corrupt, incorrectly signed, mismatched, etc. 

 Value: 4

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md) 

### STATUS_FAILURE_STORAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_STORAGE: Int
```

The operation failed because of storage issues. For example, the device may be running low on space, or external media may be unavailable. The user may be able to help free space or insert different external media.

The result may also contain [EXTRA_STORAGE_PATH](PackageInstaller.md) with the path to the storage device that caused the failure. 

 Value: 6

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md)
- [#EXTRA_STORAGE_PATH](PackageInstaller.md) 

### STATUS_FAILURE_TIMEOUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_TIMEOUT: Int
```

The operation failed because it didn't complete within the specified timeout. 

 Value: 8

**See Also**

- [#EXTRA_STATUS_MESSAGE](PackageInstaller.md) 

### STATUS_PENDING_USER_ACTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PENDING_USER_ACTION: Int
```

User action is currently required to proceed. You can launch the intent activity described by [Intent.EXTRA_INTENT](../android.content/Intent.md) to involve the user and continue.

You may choose to immediately launch the intent if the user is actively using your app. Otherwise, you should use a notification to guide the user back into your app before launching. 

 Value: -1

**See Also**

- [android.content.Intent#getParcelableExtra(String)](../android.content/Intent.md)) 

### STATUS_SUCCESS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_SUCCESS: Int
```

The operation succeeded. 

 Value: 0

### UNARCHIVAL_ERROR_INSTALLER_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_ERROR_INSTALLER_DISABLED: Int
```

The installer responsible for the unarchival is disabled.

The system will return this status if appropriate. Installers do not need to verify for this error. 

 Value: 4

### UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED: Int
```

The installer responsible for the unarchival has been uninstalled

The system will return this status if appropriate. Installers do not need to verify for this error. 

 Value: 5

### UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE: Int
```

Not enough storage to unarchive the application.

The installer can optionally provide a`userActionIntent`for a space-clearing dialog. If no action is provided, then a generic intent [android.os.storage.StorageManager#ACTION_MANAGE_STORAGE](../android.os.storage/StorageManager.md) is started instead. 

 Value: 2

### UNARCHIVAL_ERROR_NO_CONNECTIVITY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_ERROR_NO_CONNECTIVITY: Int
```

The device is not connected to the internet 

 Value: 3

### UNARCHIVAL_ERROR_USER_ACTION_NEEDED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_ERROR_USER_ACTION_NEEDED: Int
```

The user needs to interact with the installer to enable the installation.

An example use case for this could be that the user needs to login to allow the download for a paid app. 

 Value: 1

### UNARCHIVAL_GENERIC_ERROR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_GENERIC_ERROR: Int
```

Generic error: The app cannot be unarchived. 

 Value: 100

### UNARCHIVAL_OK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNARCHIVAL_OK: Int
```

The unarchival is possible and will commence.

Note that this does not mean that the unarchival has completed. This status should be sent before any longer asynchronous action (e.g. app download) is started. 

 Value: 0

## Public methods

### abandonSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abandonSession(sessionId: Int): Unit
```

Completely abandon the given session, destroying all staged data and rendering it invalid. Abandoned sessions will be reported to [SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md) listeners as failures. This is equivalent to opening the session and calling [Session.abandon()](../android/content/pm/PackageInstaller.Session.md)).

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------|
| `java.lang.SecurityException` | when the caller does not own the session, or the session is invalid. |

### checkInstallConstraints

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkInstallConstraints(
    packageNames: MutableList<String!>, 
    constraints: PackageInstaller.InstallConstraints, 
    executor: Executor, 
    callback: Consumer<PackageInstaller.InstallConstraintsResult!>
): Unit
```

Check if install constraints are satisfied for the given packages. Note this query result is just a hint and subject to race because system states could change anytime in-between this query and committing the session. The result is returned by a callback because some constraints might take a long time to evaluate.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:a list of package names to check the constraints for installation This value cannot be`null`. |
| `constraints` | [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md):the constraints for installation. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [PackageInstaller.InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md)!\>:called when the [InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md) is ready This value cannot be`null`. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the given packages' installer of record doesn't match the caller's own package name or the installerPackageName set by the caller doesn't match the caller's own package name. |

### commitSessionAfterInstallConstraintsAreMet

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun commitSessionAfterInstallConstraintsAreMet(
    sessionId: Int, 
    statusReceiver: IntentSender, 
    constraints: PackageInstaller.InstallConstraints, 
    timeoutMillis: Long
): Unit
```

Commit the session when all constraints are satisfied. This is a convenient method to combine [waitForInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,android.content.IntentSender,long)](PackageInstaller.md))and [Session.commit(IntentSender)](../android/content/pm/PackageInstaller.Session.md)).

Once this method is called, the session is sealed and no additional mutations may be performed on the session. In the case of timeout, you may commit the session again using this method or [Session.commit(IntentSender)](../android/content/pm/PackageInstaller.Session.md))for retries.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the session ID to commit when all constraints are satisfied. |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Called when the state of the session changes. Intents sent to this receiver contain [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value cannot be`null`. |
| `constraints` | [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md):The requirements to satisfy before committing the session. This value cannot be`null`. |
| --- | --- |
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum time to wait, in milliseconds until the constraints are satisfied. The caller will be notified via`statusReceiver`if timeout happens before commit. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`statusReceiver`from an immutable [android.app.PendingIntent](../android.app/PendingIntent.md) when caller has a target SDK of API 35 or above. |

### createSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSession(params: PackageInstaller.SessionParams): Int
```

Create a new session using the given parameters, returning a unique ID that represents the session. Once created, the session can be opened multiple times across multiple device boots.

The system may automatically destroy sessions that have not been finalized (either committed or abandoned) within a reasonable period of time, typically on the order of a day.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [PackageInstaller.SessionParams](../android/content/pm/PackageInstaller.SessionParams.md):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | positive, non-zero unique ID that represents the created session. This ID remains consistent across device reboots until the session is finalized. IDs are not reused during a given boot. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if parameters were unsatisfiable, such as lack of disk space or unavailable media. |
| `java.lang.SecurityException` | when installation services are unavailable, such as when called from a restricted user. |
| `java.lang.IllegalArgumentException` | when [SessionParams](../android/content/pm/PackageInstaller.SessionParams.md) is invalid. |
| --- | --- |

### getActiveStagedSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveStagedSession(): PackageInstaller.SessionInfo?
```

**Deprecated:** *Use [getActiveStagedSessions](PackageInstaller.md))as there can be more than one active staged session*

Returns first active staged session, or`null`if there is none.

For more information on what sessions are considered active see [SessionInfo.isStagedSessionActive()](../android/content/pm/PackageInstaller.SessionInfo.md)). 

### getActiveStagedSessions

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveStagedSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Returns list of active staged sessions. Returns empty list if there is none.

For more information on what sessions are considered active see \* [SessionInfo.isStagedSessionActive()](../android/content/pm/PackageInstaller.SessionInfo.md)).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!> | This value cannot be`null`. |

### getAllSessions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all known install sessions, regardless of the installer. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!> | This value cannot be`null`. |

### getDeveloperVerificationServiceProvider

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeveloperVerificationServiceProvider(): ComponentName?
```

Return the component name of the developer verification service provider, for the purpose of interacting with the specific verifier in relation to extension parameters and response structure. Return null if the system verifier service provider is not available to the caller, or if there is no such provider specified by the system. 

### getMySessions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMySessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all known install sessions owned by the calling app.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!> | This value cannot be`null`. |

### getSessionInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionInfo(sessionId: Int): PackageInstaller.SessionInfo?
```

Return details for a specific session. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)? | details for the requested session, or`null`if the session does not exist. |

### getStagedSessions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStagedSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all staged install sessions. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!> | This value cannot be`null`. |

### installExistingPackage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun installExistingPackage(
    packageName: String, 
    installReason: Int, 
    statusReceiver: IntentSender?
): Unit
```

Install the given package, which already exists on the device, for the user for which this installer was created.

This will [all restricted permissions](../android/content/pm/PackageInstaller.SessionParams.md)). 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md) and android.Manifest.permission.INSTALL_EXISTING_PACKAGES

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to install. This value cannot be`null`. |
| `installReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Reason for install. Value is [android.content.pm.PackageManager#INSTALL_REASON_UNKNOWN](PackageManager.md), [android.content.pm.PackageManager#INSTALL_REASON_POLICY](PackageManager.md), [android.content.pm.PackageManager#INSTALL_REASON_DEVICE_RESTORE](PackageManager.md), [android.content.pm.PackageManager#INSTALL_REASON_DEVICE_SETUP](PackageManager.md), [android.content.pm.PackageManager#INSTALL_REASON_USER](PackageManager.md), or android.content.pm.PackageManager.INSTALL_REASON_ROLLBACK |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md)?:Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value may be`null`. |
| --- | --- |

### installPackageArchived

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun installPackageArchived(
    archivedPackageInfo: ArchivedPackageInfo, 
    sessionParams: PackageInstaller.SessionParams, 
    statusReceiver: IntentSender
): Unit
```

Install package in an archived state. 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `archivedPackageInfo` | [ArchivedPackageInfo](ArchivedPackageInfo.md):archived package data such as package name, signature etc. This value cannot be`null`. |
| `sessionParams` | [PackageInstaller.SessionParams](../android/content/pm/PackageInstaller.SessionParams.md):used to create an underlying installation session This value cannot be`null`. |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Called when the state of the session changes. Intents sent to this receiver contain [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value cannot be`null`. |
| --- | --- |

**See Also**

- [#createSession](PackageInstaller.md))
- [android.content.pm.PackageInstaller.Session#commit](../android/content/pm/PackageInstaller.Session.md)) 

### openSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openSession(sessionId: Int): PackageInstaller.Session
```

Open an existing session to actively perform work. To succeed, the caller must be the owner of the install session.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [PackageInstaller.Session](../android/content/pm/PackageInstaller.Session.md) | This value cannot be`null`. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------|
| `java.io.IOException` | if parameters were unsatisfiable, such as lack of disk space or unavailable media. |
| `java.lang.SecurityException` | when the caller does not own the session, or the session is invalid. |

### registerSessionCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerSessionCallback(callback: PackageInstaller.SessionCallback): Unit
```

Register to watch for session lifecycle events. The callers need to be the session owner or have the android.permission.QUERY_ALL_PACKAGES to watch for these events.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md):This value cannot be`null`. |

### registerSessionCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerSessionCallback(
    callback: PackageInstaller.SessionCallback, 
    handler: Handler
): Unit
```

Register to watch for session lifecycle events. No special permissions are required to watch for these events.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [Handler](../android.os/Handler.md):to dispatch callback events through, otherwise uses calling thread. This value cannot be`null`. |
| `callback` | [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md):This value cannot be`null`. |

### reportUnarchivalState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reportUnarchivalState(unarchivalState: PackageInstaller.UnarchivalState): Unit
```

Reports the state of an unarchival to the system. 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unarchivalState` | [PackageInstaller.UnarchivalState](../android/content/pm/PackageInstaller.UnarchivalState.md):This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | if no unarchival with`unarchiveId`exists |

**See Also**

- [android.content.pm.PackageInstaller.UnarchivalState](../android/content/pm/PackageInstaller.UnarchivalState.md) 

### reportUnarchivalStatus

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reportUnarchivalStatus(
    unarchiveId: Int, 
    status: Int, 
    requiredStorageBytes: Long, 
    userActionIntent: PendingIntent?
): Unit
```

Reports the status of an unarchival to the system. 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unarchiveId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID provided by the system as part of the intent.action.UNARCHIVE broadcast with EXTRA_UNARCHIVE_ID. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is used for the system to provide the user with necessary follow-up steps or errors. Value is android.content.pm.PackageInstaller.UNARCHIVAL_STATUS_UNSET, [android.content.pm.PackageInstaller#UNARCHIVAL_OK](PackageInstaller.md), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_USER_ACTION_NEEDED](PackageInstaller.md), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](PackageInstaller.md), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_NO_CONNECTIVITY](PackageInstaller.md), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_DISABLED](PackageInstaller.md), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](PackageInstaller.md), or [android.content.pm.PackageInstaller#UNARCHIVAL_GENERIC_ERROR](PackageInstaller.md) |
| `requiredStorageBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):If the error is UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE this field should be set to specify how many additional bytes of storage are required to unarchive the app. |
| --- | --- |
| `userActionIntent` | [PendingIntent](../android.app/PendingIntent.md)?:Optional intent to start a follow up action required to facilitate the unarchival flow (e.g. user needs to log in). This value may be`null`. |

| Exceptions ||
|-----------------------------------------------------------|------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | if no unarchival with`unarchiveId`exists |

### requestArchive

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestArchive(
    packageName: String, 
    statusReceiver: IntentSender
): Unit
```

Requests to archive a package which is currently installed.

During the archival process, the apps APKs and cache are removed from the device while the user data is kept. Through the [requestUnarchive](PackageInstaller.md))call, apps can be restored again through their responsible installer.

Archived apps are returned as displayable apps through the [LauncherApps](LauncherApps.md) APIs and will be displayed to users with UI treatment to highlight that said apps are archived. If a user taps on an archived app, the app will be unarchived and the restoration process is communicated. 
Requires [android.Manifest.permission#DELETE_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Callback used to notify when the operation is completed. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|------------------------------------------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | If`packageName`isn't found or not available to the caller or isn't archived. |

### requestUnarchive

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestUnarchive(
    packageName: String, 
    statusReceiver: IntentSender
): Unit
```

Requests to unarchive a currently archived package.

Sends a request to unarchive an app to the responsible installer. The installer is determined by [InstallSourceInfo.getUpdateOwnerPackageName()](InstallSourceInfo.md)), or [InstallSourceInfo.getInstallingPackageName()](InstallSourceInfo.md))if the former value is null.

The installation will happen asynchronously and can be observed through [android.content.Intent#ACTION_PACKAGE_ADDED](../android.content/Intent.md). 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Callback used to notify whether the installer has accepted the unarchival request or an error has occurred. The status update will be sent though [EXTRA_UNARCHIVE_STATUS](PackageInstaller.md). Only one status will be sent. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | If`packageName`isn't found or not visible to the caller or if the package has no installer on the device anymore to unarchive it. |
| `java.io.IOException` | If parameters were unsatisfiable, such as lack of disk space. |

### uninstall

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstall(
    versionedPackage: VersionedPackage, 
    statusReceiver: IntentSender
): Unit
```

Uninstall the given package with a specific version code, removing it completely from the device. If the version code of the package does not match the one passed in the versioned package argument this method is a no-op. Use [PackageManager.VERSION_CODE_HIGHEST](PackageManager.md) to uninstall the latest version of the package.

This method is available to:

- the current "installer of record" for the package
- the device owner
- the affiliated profile owner

<br />

Requires [android.Manifest.permission#DELETE_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `versionedPackage` | [VersionedPackage](VersionedPackage.md):The versioned package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

**See Also**

- [android.app.admin.DevicePolicyManager](../android.app.admin/DevicePolicyManager.md) 

### uninstall

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstall(
    versionedPackage: VersionedPackage, 
    flags: Int, 
    statusReceiver: IntentSender
): Unit
```

Uninstall the given package with a specific version code, removing it completely from the device. This method is only available to the current "installer of record" for the package. If the version code of the package does not match the one passed in the versioned package argument this method is a no-op. Use [PackageManager.VERSION_CODE_HIGHEST](PackageManager.md) to uninstall the latest version of the package. 
Requires [android.Manifest.permission#DELETE_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `versionedPackage` | [VersionedPackage](VersionedPackage.md):The versioned package to uninstall. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags for uninstall. Value is either`0`or a combination of android.content.pm.PackageManager.DELETE_KEEP_DATA, android.content.pm.PackageManager.DELETE_ALL_USERS, android.content.pm.PackageManager.DELETE_SYSTEM_APP, android.content.pm.PackageManager.DELETE_DONT_KILL_APP, and android.content.pm.PackageManager.DELETE_CHATTY |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value cannot be`null`. |
| --- | --- |

### uninstall

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstall(
    packageName: String, 
    statusReceiver: IntentSender
): Unit
```

Uninstall the given package, removing it completely from the device. This method is available to:

- the current "installer of record" for the package
- the device owner
- the affiliated profile owner

<br />

Requires [android.Manifest.permission#DELETE_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](../android/Manifest.permission.md)

<br />

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

**See Also**

- [android.app.admin.DevicePolicyManager](../android.app.admin/DevicePolicyManager.md) 

### uninstallExistingPackage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstallExistingPackage(
    packageName: String, 
    statusReceiver: IntentSender?
): Unit
```

Uninstall the given package for the user for which this installer was created if the package will still exist for other users on the device. 
Requires [android.Manifest.permission#DELETE_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](../android.content/IntentSender.md)?:Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](PackageInstaller.md). Refer to the individual status codes on how to handle them. This value may be`null`. |

### unregisterSessionCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterSessionCallback(callback: PackageInstaller.SessionCallback): Unit
```

Unregister a previously registered callback.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md):This value cannot be`null`. |

### updateSessionAppIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateSessionAppIcon(
    sessionId: Int, 
    appIcon: Bitmap?
): Unit
```

Update the icon representing the app being installed in a specific session. This should be roughly [ActivityManager.getLauncherLargeIconSize()](../android.app/ActivityManager.md))in both dimensions.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `appIcon` | [Bitmap](../android.graphics/Bitmap.md)?:This value may be`null`. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------|
| `java.lang.SecurityException` | when the caller does not own the session, or the session is invalid. |

### updateSessionAppLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateSessionAppLabel(
    sessionId: Int, 
    appLabel: CharSequence?
): Unit
```

Update the label representing the app being installed in a specific session.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `appLabel` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:This value may be`null`. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------|
| `java.lang.SecurityException` | when the caller does not own the session, or the session is invalid. |

### waitForInstallConstraints

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun waitForInstallConstraints(
    packageNames: MutableList<String!>, 
    constraints: PackageInstaller.InstallConstraints, 
    callback: IntentSender, 
    timeoutMillis: Long
): Unit
```

Similar to [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](PackageInstaller.md)), but the callback is invoked only when the constraints are satisfied or after timeout.

Note: the device idle constraint might take a long time to evaluate. The system will ensure the constraint is evaluated completely before handling timeout.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:a list of package names to check the constraints for installation This value cannot be`null`. |
| `constraints` | [PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md):the constraints for installation. This value cannot be`null`. |
| `callback` | [IntentSender](../android.content/IntentSender.md):Called when the constraints are satisfied or after timeout. Intents sent to this callback contain: [Intent.EXTRA_PACKAGES](../android.content/Intent.md) for the input package names, [EXTRA_INSTALL_CONSTRAINTS](PackageInstaller.md) for the input constraints, [EXTRA_INSTALL_CONSTRAINTS_RESULT](PackageInstaller.md) for the result. This value cannot be`null`. |
| --- | --- |
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum time to wait, in milliseconds until the constraints are satisfied. Valid range is from 0 to one week.`0`means the callback will be invoked immediately no matter constraints are satisfied or not. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the given packages' installer of record doesn't match the caller's own package name or the installerPackageName set by the caller doesn't match the caller's own package name. |
