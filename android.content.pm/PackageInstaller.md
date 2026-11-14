# PackageInstaller

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageInstaller

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/PackageInstaller "View this page in Java") 

```
open class PackageInstaller
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.PackageInstaller](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) |

Offers the ability to install, upgrade, and remove applications on the device. This includes support for apps packaged either as a single "monolithic" APK, or apps packaged as multiple "split" APKs.

An app is delivered for installation through a [PackageInstaller.Session](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session), which any app can create. Once the session is created, the installer can stream one or more APKs into place until it decides to either commit or destroy the session. Committing may require user intervention to complete the installation, unless the caller falls into one of the following categories, in which case the installation will complete automatically.

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
| | [InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints) A class to encapsulate constraints for installation. |
| | [InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult) The callback result of [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#checkInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20java.util.concurrent.Executor,%20java.util.function.Consumer)). |
| | [PreapprovalDetails](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.PreapprovalDetails) Details for requesting the pre-commit install approval. |
| open | [Session](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session) An installation that is being actively staged. |
| abstract | [SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback) Events for observing session lifecycle. |
| open | [SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo) Details for an active install session. |
| open | [SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams) Parameters for creating a new [PackageInstaller.Session](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session). |
| | [UnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.UnarchivalState) Used to communicate the unarchival state in [reportUnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#reportUnarchivalState(android.content.pm.PackageInstaller.UnarchivalState)). |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_COMMITTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#ACTION_SESSION_COMMITTED:kotlin.String) Broadcast Action: Explicit broadcast sent to the last known default launcher when a session for a new install is committed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_DETAILS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#ACTION_SESSION_DETAILS:kotlin.String) Activity Action: Show details about a particular install session. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SESSION_UPDATED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#ACTION_SESSION_UPDATED:kotlin.String) Broadcast Action: Send information about a staged install session when its state is updated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED:kotlin.Int) Developer verification failed because the developer cannot be verified, as reported by the verifier via [DeveloperVerificationSession.reportVerificationComplete(DeveloperVerificationStatus)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) or [DeveloperVerificationSession.reportVerificationComplete(](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE:kotlin.Int) Developer verification failed because the network is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN:kotlin.Int) Developer verification failed because of unknown reasons, such as when the verifier times out or cannot be connected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE:kotlin.String) An extra containing the response provided by the developer verifier to any extension params provided by the installer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON:kotlin.String) When an installation fails because the developer verification was incomplete or blocked, this extra provides a code that explains the reason, such as [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE:kotlin.Int). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED:kotlin.String) An extra containing a boolean indicating whether the lite version of the developer verification was performed on the app to be installed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INSTALL_CONSTRAINTS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_INSTALL_CONSTRAINTS:kotlin.String) The [InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints) object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INSTALL_CONSTRAINTS_RESULT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_INSTALL_CONSTRAINTS_RESULT:kotlin.String) The [InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult) object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_OTHER_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_OTHER_PACKAGE_NAME:kotlin.String) Another package name relevant to a status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_PACKAGE_NAME:kotlin.String) Package name that an operation is working with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PRE_APPROVAL](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_PRE_APPROVAL:kotlin.String) Indicate if the status is for a pre-approval request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SESSION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_SESSION:kotlin.String) [SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo) that an operation is working with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SESSION_ID](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_SESSION_ID:kotlin.String) An integer session ID that an operation is working with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String) Current status of an operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) Detailed string representation of the status, including raw details that are useful for debugging. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STORAGE_PATH](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STORAGE_PATH:kotlin.String) Storage path relevant to a status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_ALL_USERS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_UNARCHIVE_ALL_USERS:kotlin.String) If true, the requestor of the unarchival has specified that the app should be unarchived for all users. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_ID](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_UNARCHIVE_ID:kotlin.String) Extra field for the unarchive ID. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_UNARCHIVE_PACKAGE_NAME:kotlin.String) Extra field for the package name of a package that is requested to be unarchived. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_UNARCHIVE_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_UNARCHIVE_STATUS:kotlin.String) Current status of an unarchive operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_DOWNLOADED_FILE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_DOWNLOADED_FILE:kotlin.Int) Code indicating that the package being installed comes from a file that was downloaded to the device by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_LOCAL_FILE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_LOCAL_FILE:kotlin.Int) Code indicating that the package being installed comes from a local file on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_OTHER](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_OTHER:kotlin.Int) Code indicating that the package being installed is from a source not reflected by any other package source constant. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_STORE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_STORE:kotlin.Int) Code indicating that the package being installed is from a store. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PACKAGE_SOURCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_UNSPECIFIED:kotlin.Int) The installer did not call [PackageInstaller.SessionParams.setPackageSource(int)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams#setPackageSource(kotlin.Int))to specify the package source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE:kotlin.Int) The operation failed in a generic way. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int) The operation failed because it was actively aborted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_BLOCKED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_BLOCKED:kotlin.Int) The operation failed because it was blocked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_CONFLICT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_CONFLICT:kotlin.Int) The operation failed because it conflicts (or is inconsistent with) with another package already installed on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_INCOMPATIBLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_INCOMPATIBLE:kotlin.Int) The operation failed because it is fundamentally incompatible with this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_INVALID](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_INVALID:kotlin.Int) The operation failed because one or more of the APKs was invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_STORAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_STORAGE:kotlin.Int) The operation failed because of storage issues. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILURE_TIMEOUT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_TIMEOUT:kotlin.Int) The operation failed because it didn't complete within the specified timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PENDING_USER_ACTION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_PENDING_USER_ACTION:kotlin.Int) User action is currently required to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_SUCCESS:kotlin.Int) The operation succeeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSTALLER_DISABLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_DISABLED:kotlin.Int) The installer responsible for the unarchival is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED:kotlin.Int) The installer responsible for the unarchival has been uninstalled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE:kotlin.Int) Not enough storage to unarchive the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_NO_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_NO_CONNECTIVITY:kotlin.Int) The device is not connected to the internet |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_ERROR_USER_ACTION_NEEDED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_USER_ACTION_NEEDED:kotlin.Int) The user needs to interact with the installer to enable the installation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_GENERIC_ERROR](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_GENERIC_ERROR:kotlin.Int) Generic error: The app cannot be unarchived. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNARCHIVAL_OK](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_OK:kotlin.Int) The unarchival is possible and will commence. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandonSession](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#abandonSession(kotlin.Int))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Completely abandon the given session, destroying all staged data and rendering it invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkInstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#checkInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`packageNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `constraints:` ` [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [PackageInstaller.InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult)!>`)` Check if install constraints are satisfied for the given packages. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitSessionAfterInstallConstraintsAreMet](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#commitSessionAfterInstallConstraintsAreMet(kotlin.Int,%20android.content.IntentSender,%20android.content.pm.PackageInstaller.InstallConstraints,%20kotlin.Long))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`, `constraints:` ` [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints)`, `timeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Commit the session when all constraints are satisfied. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [createSession](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#createSession(android.content.pm.PackageInstaller.SessionParams))`(`params:` ` [PackageInstaller.SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams)`)` Create a new session using the given parameters, returning a unique ID that represents the session. |
| open [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)? | [getActiveStagedSession](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getActiveStagedSession())`()` Returns first active staged session, or`null`if there is none. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!\> | [getActiveStagedSessions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getActiveStagedSessions())`()` Returns list of active staged sessions. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!\> | [getAllSessions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getAllSessions())`()` Return list of all known install sessions, regardless of the installer. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | [getDeveloperVerificationServiceProvider](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getDeveloperVerificationServiceProvider())`()` Return the component name of the developer verification service provider, for the purpose of interacting with the specific verifier in relation to extension parameters and response structure. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!\> | [getMySessions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getMySessions())`()` Return list of all known install sessions owned by the calling app. |
| open [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)? | [getSessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getSessionInfo(kotlin.Int))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return details for a specific session. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!\> | [getStagedSessions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getStagedSessions())`()` Return list of all staged install sessions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [installExistingPackage](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#installExistingPackage(kotlin.String,%20kotlin.Int,%20android.content.IntentSender))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `installReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)?`)` Install the given package, which already exists on the device, for the user for which this installer was created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [installPackageArchived](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#installPackageArchived(android.content.pm.ArchivedPackageInfo,%20android.content.pm.PackageInstaller.SessionParams,%20android.content.IntentSender))`(`archivedPackageInfo:` ` [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo)`, `sessionParams:` ` [PackageInstaller.SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Install package in an archived state. |
| open [PackageInstaller.Session](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session) | [openSession](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#openSession(kotlin.Int))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Open an existing session to actively perform work. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerSessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#registerSessionCallback(android.content.pm.PackageInstaller.SessionCallback))`(`callback:` ` [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback)`)` Register to watch for session lifecycle events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerSessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#registerSessionCallback(android.content.pm.PackageInstaller.SessionCallback,%20android.os.Handler))`(`callback:` ` [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Register to watch for session lifecycle events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportUnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#reportUnarchivalState(android.content.pm.PackageInstaller.UnarchivalState))`(`unarchivalState:` ` [PackageInstaller.UnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.UnarchivalState)`)` Reports the state of an unarchival to the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportUnarchivalStatus](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#reportUnarchivalStatus(kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20android.app.PendingIntent))`(`unarchiveId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requiredStorageBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `userActionIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)?`)` Reports the status of an unarchival to the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestArchive](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestArchive(kotlin.String,%20android.content.IntentSender))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Requests to archive a package which is currently installed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestUnarchive](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestUnarchive(kotlin.String,%20android.content.IntentSender))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Requests to unarchive a currently archived package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#uninstall(android.content.pm.VersionedPackage,%20android.content.IntentSender))`(`versionedPackage:` ` [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Uninstall the given package with a specific version code, removing it completely from the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#uninstall(android.content.pm.VersionedPackage,%20kotlin.Int,%20android.content.IntentSender))`(`versionedPackage:` ` [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Uninstall the given package with a specific version code, removing it completely from the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstall](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#uninstall(kotlin.String,%20android.content.IntentSender))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Uninstall the given package, removing it completely from the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uninstallExistingPackage](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#uninstallExistingPackage(kotlin.String,%20android.content.IntentSender))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusReceiver:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)?`)` Uninstall the given package for the user for which this installer was created if the package will still exist for other users on the device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterSessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#unregisterSessionCallback(android.content.pm.PackageInstaller.SessionCallback))`(`callback:` ` [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback)`)` Unregister a previously registered callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSessionAppIcon](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#updateSessionAppIcon(kotlin.Int,%20android.graphics.Bitmap))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appIcon:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)?`)` Update the icon representing the app being installed in a specific session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSessionAppLabel](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#updateSessionAppLabel(kotlin.Int,%20kotlin.CharSequence))`(`sessionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appLabel:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Update the label representing the app being installed in a specific session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForInstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#waitForInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20android.content.IntentSender,%20kotlin.Long))`(`packageNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `constraints:` ` [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints)`, `callback:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`, `timeoutMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Similar to [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#checkInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20java.util.concurrent.Executor,%20java.util.function.Consumer)), but the callback is invoked only when the constraints are satisfied or after timeout. |

## Constants

### ACTION_SESSION_COMMITTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_COMMITTED: String
```

Broadcast Action: Explicit broadcast sent to the last known default launcher when a session for a new install is committed. For managed profile, this is sent to the default launcher of the primary profile. For user-profiles that have items restricted on home screen, this broadcast is sent to the default launcher of the primary profile, only if it has either Manifest.permission.ACCESS_HIDDEN_PROFILES_FULL or Manifest.permission.ACCESS_HIDDEN_PROFILES permission.

The associated session is defined in [EXTRA_SESSION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_SESSION:kotlin.String) and the user for which this session was created in [Intent.EXTRA_USER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String). 

 Value: "android.content.pm.action.SESSION_COMMITTED"

### ACTION_SESSION_DETAILS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_DETAILS: String
```

Activity Action: Show details about a particular install session. This may surface actions such as pause, resume, or cancel.

This should always be scoped to the installer package that owns the session. Clients should use [SessionInfo.createDetailsIntent()](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo#createDetailsIntent())to build this intent correctly.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

The session to show details for is defined in [EXTRA_SESSION_ID](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_SESSION_ID:kotlin.String). 

 Value: "android.content.pm.action.SESSION_DETAILS"

### ACTION_SESSION_UPDATED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SESSION_UPDATED: String
```

Broadcast Action: Send information about a staged install session when its state is updated.

The associated session information is defined in [EXTRA_SESSION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_SESSION:kotlin.String). 

 Value: "android.content.pm.action.SESSION_UPDATED"

### DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_DEVELOPER_BLOCKED: Int
```

Developer verification failed because the developer cannot be verified, as reported by the verifier via [DeveloperVerificationSession.reportVerificationComplete(DeveloperVerificationStatus)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) or [DeveloperVerificationSession.reportVerificationComplete(](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) 

 Value: 2

### DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE: Int
```

Developer verification failed because the network is unavailable. This corresponds to the status of [DeveloperVerificationSession.DEVELOPER_VERIFICATION_INCOMPLETE_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) reported by the verifier via [DeveloperVerificationSession.reportVerificationIncomplete(int)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#). 

 Value: 1

### DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVELOPER_VERIFICATION_FAILED_REASON_UNKNOWN: Int
```

Developer verification failed because of unknown reasons, such as when the verifier times out or cannot be connected. It can also corresponds to the status of [DeveloperVerificationSession.DEVELOPER_VERIFICATION_INCOMPLETE_UNKNOWN](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#) reported by the verifier via [DeveloperVerificationSession.reportVerificationIncomplete(int)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#). 

 Value: 0

### EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_EXTENSION_RESPONSE: String
```

An extra containing the response provided by the developer verifier to any extension params provided by the installer. It will be of type [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#). 

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_EXTENSION_RESPONSE"

### EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_FAILURE_REASON: String
```

When an installation fails because the developer verification was incomplete or blocked, this extra provides a code that explains the reason, such as [DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#DEVELOPER_VERIFICATION_FAILED_REASON_NETWORK_UNAVAILABLE:kotlin.Int). It is included in the installation result returned via the [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) in [Session.commit(IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender)). However, along with this reason code, installers can receive different status codes from [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String) depending on their target SDK and permission status:

- Installers without the [INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) permission but with the [REQUEST_INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String) permission and targeting [API 36](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int) or less will first receive the [STATUS_PENDING_USER_ACTION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_PENDING_USER_ACTION:kotlin.Int) status code without this reason code. They will be forced through the user action flow to allow the OS to inform the user of such verification context before continuing to fail the install. If the user has the option to bypass the verification result and chooses to do so, the installation will proceed. Otherwise, the installer will receive the [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int) status code along with this reason code that explains why the verification had failed.
- Installers with the [INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) permission and targeting [API 36](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int) or less will directly receive the [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int) status code. This is because they are not expected to have the capability of handling the [STATUS_PENDING_USER_ACTION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_PENDING_USER_ACTION:kotlin.Int) flow, so the installation will directly fail. This reason code will be supplied to them for providing additional information.
- For all installers targeting higher than [API 36](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int)
 - For situations that require user input, such as when the developer verification policy allows the user to bypass a verification failure caused by network issues, the installer will receive a [STATUS_PENDING_USER_ACTION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_PENDING_USER_ACTION:kotlin.Int) status code without this reason code. The installer will be forced through the user action flow to allow the OS to inform the user of such verification context before continuing to fail the installation. If the user has the option to bypass the verification result and chooses to do so, the installation will proceed. Otherwise, the install will receive the [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int) status code along with this reason code that explains why the verification had failed.
 - For all other situations, the installer will receive a [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int) status code along with this reason code, so the installers can explain the failure to the user accordingly. An [Intent.EXTRA_INTENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String) will also be populated with an intent that can provide additional context where appropriate, should the installer prefer to defer to the OS to explain the failure to the user.

<br />

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_FAILURE_REASON"

### EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVELOPER_VERIFICATION_LITE_PERFORMED: String
```

An extra containing a boolean indicating whether the lite version of the developer verification was performed on the app to be installed. It is included in the installation result returned via the [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) in [Session.commit(IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender))when the installation failed. 

 Value: "android.content.pm.extra.DEVELOPER_VERIFICATION_LITE_PERFORMED"

### EXTRA_INSTALL_CONSTRAINTS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INSTALL_CONSTRAINTS: String
```

The [InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints) object. 

 Value: "android.content.pm.extra.INSTALL_CONSTRAINTS"

**See Also**

- [android.content.Intent#getParcelableExtra(String, Class)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String,%20java.lang.Class))
- [#waitForInstallConstraints(List, InstallConstraints, IntentSender, long)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#waitForInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20android.content.IntentSender,%20kotlin.Long)) 

### EXTRA_INSTALL_CONSTRAINTS_RESULT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INSTALL_CONSTRAINTS_RESULT: String
```

The [InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult) object. 

 Value: "android.content.pm.extra.INSTALL_CONSTRAINTS_RESULT"

**See Also**

- [android.content.Intent#getParcelableExtra(String, Class)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String,%20java.lang.Class))
- [#waitForInstallConstraints(List, InstallConstraints, IntentSender, long)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#waitForInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20android.content.IntentSender,%20kotlin.Long)) 

### EXTRA_OTHER_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_OTHER_PACKAGE_NAME: String
```

Another package name relevant to a status. This is typically the package responsible for causing an operation failure. 

 Value: "android.content.pm.extra.OTHER_PACKAGE_NAME"

**See Also**

- [android.content.Intent#getStringExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)) 

### EXTRA_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PACKAGE_NAME: String
```

Package name that an operation is working with. 

 Value: "android.content.pm.extra.PACKAGE_NAME"

**See Also**

- [android.content.Intent#getStringExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)) 

### EXTRA_PRE_APPROVAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PRE_APPROVAL: String
```

Indicate if the status is for a pre-approval request. If callers use the same [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) for both [Session.requestUserPreapproval(PreapprovalDetails, IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#requestUserPreapproval(android.content.pm.PackageInstaller.PreapprovalDetails,%20android.content.IntentSender))and [Session.commit(IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender)), they can use this to differentiate between them. 

 Value: "android.content.pm.extra.PRE_APPROVAL"

**See Also**

- [android.content.Intent#getBooleanExtra(String, boolean)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanExtra(kotlin.String,%20kotlin.Boolean)) 

### EXTRA_SESSION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SESSION: String
```

[SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo) that an operation is working with. 

 Value: "android.content.pm.extra.SESSION"

**See Also**

- [android.content.Intent#getParcelableExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)) 

### EXTRA_SESSION_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SESSION_ID: String
```

An integer session ID that an operation is working with. 

 Value: "android.content.pm.extra.SESSION_ID"

**See Also**

- [android.content.Intent#getIntExtra(String, int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)) 

### EXTRA_STATUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS: String
```

Current status of an operation. Will be one of [STATUS_PENDING_USER_ACTION](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_PENDING_USER_ACTION:kotlin.Int), [STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_SUCCESS:kotlin.Int), [STATUS_FAILURE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE:kotlin.Int), [STATUS_FAILURE_ABORTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_ABORTED:kotlin.Int), [STATUS_FAILURE_BLOCKED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_BLOCKED:kotlin.Int), [STATUS_FAILURE_CONFLICT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_CONFLICT:kotlin.Int), [STATUS_FAILURE_INCOMPATIBLE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_INCOMPATIBLE:kotlin.Int), [STATUS_FAILURE_INVALID](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_INVALID:kotlin.Int), [STATUS_FAILURE_STORAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_STORAGE:kotlin.Int), or [STATUS_FAILURE_TIMEOUT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#STATUS_FAILURE_TIMEOUT:kotlin.Int).

More information about a status may be available through additional extras; see the individual status documentation for details. 

 Value: "android.content.pm.extra.STATUS"

**See Also**

- [android.content.Intent#getIntExtra(String, int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)) 

### EXTRA_STATUS_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATUS_MESSAGE: String
```

Detailed string representation of the status, including raw details that are useful for debugging. 

 Value: "android.content.pm.extra.STATUS_MESSAGE"

**See Also**

- [android.content.Intent#getStringExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)) 

### EXTRA_STORAGE_PATH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STORAGE_PATH: String
```

Storage path relevant to a status. 

 Value: "android.content.pm.extra.STORAGE_PATH"

**See Also**

- [android.content.Intent#getStringExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)) 

### EXTRA_UNARCHIVE_ALL_USERS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_ALL_USERS: String
```

If true, the requestor of the unarchival has specified that the app should be unarchived for all users. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNARCHIVE_PACKAGE:kotlin.String) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_ALL_USERS"

### EXTRA_UNARCHIVE_ID

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_ID: String
```

Extra field for the unarchive ID. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNARCHIVE_PACKAGE:kotlin.String) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_ID"

**See Also**

- [android.content.pm.PackageInstaller.SessionParams#setUnarchiveId](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams#setUnarchiveId(kotlin.Int)) 

### EXTRA_UNARCHIVE_PACKAGE_NAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_PACKAGE_NAME: String
```

Extra field for the package name of a package that is requested to be unarchived. Sent as part of the [android.content.Intent#ACTION_UNARCHIVE_PACKAGE](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNARCHIVE_PACKAGE:kotlin.String) intent. 

 Value: "android.content.pm.extra.UNARCHIVE_PACKAGE_NAME"

### EXTRA_UNARCHIVE_STATUS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_UNARCHIVE_STATUS: String
```

Current status of an unarchive operation. Will be one of [UNARCHIVAL_OK](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_OK:kotlin.Int), [UNARCHIVAL_ERROR_USER_ACTION_NEEDED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_USER_ACTION_NEEDED:kotlin.Int), [UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE:kotlin.Int), [UNARCHIVAL_ERROR_NO_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_NO_CONNECTIVITY:kotlin.Int), [UNARCHIVAL_GENERIC_ERROR](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_GENERIC_ERROR:kotlin.Int), [UNARCHIVAL_ERROR_INSTALLER_DISABLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_DISABLED:kotlin.Int) or [UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED:kotlin.Int).

If the status is not [UNARCHIVAL_OK](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_OK:kotlin.Int), then [Intent.EXTRA_INTENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String) will be set with an intent for a corresponding follow-up action (e.g. storage clearing dialog) or a failure dialog.

Used as part of [requestUnarchive](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestUnarchive(kotlin.String,%20android.content.IntentSender))to return the status of the unarchival through the [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#). 

 Value: "android.content.pm.extra.UNARCHIVE_STATUS"

**See Also**

- [#requestUnarchive](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestUnarchive(kotlin.String,%20android.content.IntentSender)) 

### PACKAGE_SOURCE_DOWNLOADED_FILE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PACKAGE_SOURCE_DOWNLOADED_FILE: Int
```

Code indicating that the package being installed comes from a file that was downloaded to the device by the user. For use in place of [PACKAGE_SOURCE_LOCAL_FILE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#PACKAGE_SOURCE_LOCAL_FILE:kotlin.Int) when the installer knows the package was downloaded. 

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

The installer did not call [PackageInstaller.SessionParams.setPackageSource(int)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams#setPackageSource(kotlin.Int))to specify the package source. 

 Value: 0

### STATUS_FAILURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE: Int
```

The operation failed in a generic way. The system will always try to provide a more specific failure reason, but in some rare cases this may be delivered. 

 Value: 1

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) 

### STATUS_FAILURE_ABORTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_ABORTED: Int
```

The operation failed because it was actively aborted. For example, the user actively declined requested permissions, or the session was abandoned. 

 Value: 3

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) 

### STATUS_FAILURE_BLOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_BLOCKED: Int
```

The operation failed because it was blocked. For example, a device policy may be blocking the operation, a package verifier may have blocked the operation, or the app may be required for core system operation.

The result may also contain [EXTRA_OTHER_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_OTHER_PACKAGE_NAME:kotlin.String) with the specific package blocking the install. 

 Value: 2

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String)
- [#EXTRA_OTHER_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_OTHER_PACKAGE_NAME:kotlin.String) 

### STATUS_FAILURE_CONFLICT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_CONFLICT: Int
```

The operation failed because it conflicts (or is inconsistent with) with another package already installed on the device. For example, an existing permission, incompatible certificates, etc. The user may be able to uninstall another app to fix the issue.

The result may also contain [EXTRA_OTHER_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_OTHER_PACKAGE_NAME:kotlin.String) with the specific package identified as the cause of the conflict. 

 Value: 5

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String)
- [#EXTRA_OTHER_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_OTHER_PACKAGE_NAME:kotlin.String) 

### STATUS_FAILURE_INCOMPATIBLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_INCOMPATIBLE: Int
```

The operation failed because it is fundamentally incompatible with this device. For example, the app may require a hardware feature that doesn't exist, it may be missing native code for the ABIs supported by the device, or it requires a newer SDK version, etc. Starting in [Build.VERSION_CODES.UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int), an app with only 32-bit native code can still be installed on a device that supports both 64-bit and 32-bit ABIs. However, a warning dialog will be displayed when the app is launched. 

 Value: 7

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) 

### STATUS_FAILURE_INVALID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_INVALID: Int
```

The operation failed because one or more of the APKs was invalid. For example, they might be malformed, corrupt, incorrectly signed, mismatched, etc. 

 Value: 4

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) 

### STATUS_FAILURE_STORAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_STORAGE: Int
```

The operation failed because of storage issues. For example, the device may be running low on space, or external media may be unavailable. The user may be able to help free space or insert different external media.

The result may also contain [EXTRA_STORAGE_PATH](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STORAGE_PATH:kotlin.String) with the path to the storage device that caused the failure. 

 Value: 6

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String)
- [#EXTRA_STORAGE_PATH](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STORAGE_PATH:kotlin.String) 

### STATUS_FAILURE_TIMEOUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILURE_TIMEOUT: Int
```

The operation failed because it didn't complete within the specified timeout. 

 Value: 8

**See Also**

- [#EXTRA_STATUS_MESSAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS_MESSAGE:kotlin.String) 

### STATUS_PENDING_USER_ACTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PENDING_USER_ACTION: Int
```

User action is currently required to proceed. You can launch the intent activity described by [Intent.EXTRA_INTENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String) to involve the user and continue.

You may choose to immediately launch the intent if the user is actively using your app. Otherwise, you should use a notification to guide the user back into your app before launching. 

 Value: -1

**See Also**

- [android.content.Intent#getParcelableExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)) 

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

The installer can optionally provide a`userActionIntent`for a space-clearing dialog. If no action is provided, then a generic intent [android.os.storage.StorageManager#ACTION_MANAGE_STORAGE](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#ACTION_MANAGE_STORAGE:kotlin.String) is started instead. 

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

Completely abandon the given session, destroying all staged data and rendering it invalid. Abandoned sessions will be reported to [SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback) listeners as failures. This is equivalent to opening the session and calling [Session.abandon()](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#abandon()).

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
| `constraints` | [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints):the constraints for installation. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [PackageInstaller.InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult)!\>:called when the [InstallConstraintsResult](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraintsResult) is ready This value cannot be`null`. |

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

Commit the session when all constraints are satisfied. This is a convenient method to combine [waitForInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,android.content.IntentSender,long)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#waitForInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20android.content.IntentSender,%20kotlin.Long))and [Session.commit(IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender)).

Once this method is called, the session is sealed and no additional mutations may be performed on the session. In the case of timeout, you may commit the session again using this method or [Session.commit(IntentSender)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender))for retries.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the session ID to commit when all constraints are satisfied. |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Called when the state of the session changes. Intents sent to this receiver contain [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value cannot be`null`. |
| `constraints` | [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints):The requirements to satisfy before committing the session. This value cannot be`null`. |
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum time to wait, in milliseconds until the constraints are satisfied. The caller will be notified via`statusReceiver`if timeout happens before commit. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`statusReceiver`from an immutable [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) when caller has a target SDK of API 35 or above. |

### createSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSession(params: PackageInstaller.SessionParams): Int
```

Create a new session using the given parameters, returning a unique ID that represents the session. Once created, the session can be opened multiple times across multiple device boots.

The system may automatically destroy sessions that have not been finalized (either committed or abandoned) within a reasonable period of time, typically on the order of a day.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [PackageInstaller.SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | positive, non-zero unique ID that represents the created session. This ID remains consistent across device reboots until the session is finalized. IDs are not reused during a given boot. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if parameters were unsatisfiable, such as lack of disk space or unavailable media. |
| `java.lang.SecurityException` | when installation services are unavailable, such as when called from a restricted user. |
| `java.lang.IllegalArgumentException` | when [SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams) is invalid. |

### getActiveStagedSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveStagedSession(): PackageInstaller.SessionInfo?
```

**Deprecated:** *Use [getActiveStagedSessions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getActiveStagedSessions())as there can be more than one active staged session*

Returns first active staged session, or`null`if there is none.

For more information on what sessions are considered active see [SessionInfo.isStagedSessionActive()](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo#isStagedSessionActive()). 

### getActiveStagedSessions

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActiveStagedSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Returns list of active staged sessions. Returns empty list if there is none.

For more information on what sessions are considered active see \* [SessionInfo.isStagedSessionActive()](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo#isStagedSessionActive()).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!> | This value cannot be`null`. |

### getAllSessions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all known install sessions, regardless of the installer. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!> | This value cannot be`null`. |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!> | This value cannot be`null`. |

### getSessionInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionInfo(sessionId: Int): PackageInstaller.SessionInfo?
```

Return details for a specific session. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)? | details for the requested session, or`null`if the session does not exist. |

### getStagedSessions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStagedSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all staged install sessions. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PackageInstaller.SessionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo)!> | This value cannot be`null`. |

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

This will [all restricted permissions](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams#setWhitelistedRestrictedPermissions(kotlin.collections.MutableSet)). 
Requires [android.Manifest.permission#INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) and android.Manifest.permission.INSTALL_EXISTING_PACKAGES

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to install. This value cannot be`null`. |
| `installReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Reason for install. Value is [android.content.pm.PackageManager#INSTALL_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_UNKNOWN:kotlin.Int), [android.content.pm.PackageManager#INSTALL_REASON_POLICY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_POLICY:kotlin.Int), [android.content.pm.PackageManager#INSTALL_REASON_DEVICE_RESTORE](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_DEVICE_RESTORE:kotlin.Int), [android.content.pm.PackageManager#INSTALL_REASON_DEVICE_SETUP](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_DEVICE_SETUP:kotlin.Int), [android.content.pm.PackageManager#INSTALL_REASON_USER](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_USER:kotlin.Int), or android.content.pm.PackageManager.INSTALL_REASON_ROLLBACK |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)?:Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value may be`null`. |

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
Requires [android.Manifest.permission#INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String)

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `archivedPackageInfo` | [ArchivedPackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo):archived package data such as package name, signature etc. This value cannot be`null`. |
| `sessionParams` | [PackageInstaller.SessionParams](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionParams):used to create an underlying installation session This value cannot be`null`. |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Called when the state of the session changes. Intents sent to this receiver contain [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

**See Also**

- [#createSession](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#createSession(android.content.pm.PackageInstaller.SessionParams))
- [android.content.pm.PackageInstaller.Session#commit](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session#commit(android.content.IntentSender)) 

### openSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openSession(sessionId: Int): PackageInstaller.Session
```

Open an existing session to actively perform work. To succeed, the caller must be the owner of the install session.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [PackageInstaller.Session](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session) | This value cannot be`null`. |

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
| `callback` | [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback):This value cannot be`null`. |

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
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):to dispatch callback events through, otherwise uses calling thread. This value cannot be`null`. |
| `callback` | [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback):This value cannot be`null`. |

### reportUnarchivalState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reportUnarchivalState(unarchivalState: PackageInstaller.UnarchivalState): Unit
```

Reports the state of an unarchival to the system. 
Requires [android.Manifest.permission#INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unarchivalState` | [PackageInstaller.UnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.UnarchivalState):This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | if no unarchival with`unarchiveId`exists |

**See Also**

- [android.content.pm.PackageInstaller.UnarchivalState](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.UnarchivalState) 

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
Requires [android.Manifest.permission#INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String)

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unarchiveId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID provided by the system as part of the intent.action.UNARCHIVE broadcast with EXTRA_UNARCHIVE_ID. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is used for the system to provide the user with necessary follow-up steps or errors. Value is android.content.pm.PackageInstaller.UNARCHIVAL_STATUS_UNSET, [android.content.pm.PackageInstaller#UNARCHIVAL_OK](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_OK:kotlin.Int), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_USER_ACTION_NEEDED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_USER_ACTION_NEEDED:kotlin.Int), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE:kotlin.Int), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_NO_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_NO_CONNECTIVITY:kotlin.Int), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_DISABLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_DISABLED:kotlin.Int), [android.content.pm.PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_ERROR_INSTALLER_UNINSTALLED:kotlin.Int), or [android.content.pm.PackageInstaller#UNARCHIVAL_GENERIC_ERROR](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#UNARCHIVAL_GENERIC_ERROR:kotlin.Int) |
| `requiredStorageBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):If the error is UNARCHIVAL_ERROR_INSUFFICIENT_STORAGE this field should be set to specify how many additional bytes of storage are required to unarchive the app. |
| `userActionIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)?:Optional intent to start a follow up action required to facilitate the unarchival flow (e.g. user needs to log in). This value may be`null`. |

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

During the archival process, the apps APKs and cache are removed from the device while the user data is kept. Through the [requestUnarchive](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestUnarchive(kotlin.String,%20android.content.IntentSender))call, apps can be restored again through their responsible installer.

Archived apps are returned as displayable apps through the [LauncherApps](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps) APIs and will be displayed to users with UI treatment to highlight that said apps are archived. If a user taps on an archived app, the app will be unarchived and the restoration process is communicated. 
Requires [android.Manifest.permission#DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELETE_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_DELETE_PACKAGES:kotlin.String)

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Callback used to notify when the operation is completed. This value cannot be`null`. |
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

Sends a request to unarchive an app to the responsible installer. The installer is determined by [InstallSourceInfo.getUpdateOwnerPackageName()](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getUpdateOwnerPackageName()), or [InstallSourceInfo.getInstallingPackageName()](https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getInstallingPackageName())if the former value is null.

The installation will happen asynchronously and can be observed through [android.content.Intent#ACTION_PACKAGE_ADDED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_ADDED:kotlin.String). 
Requires [android.Manifest.permission#INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String)

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Callback used to notify whether the installer has accepted the unarchival request or an error has occurred. The status update will be sent though [EXTRA_UNARCHIVE_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_UNARCHIVE_STATUS:kotlin.String). Only one status will be sent. This value cannot be`null`. |
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

Uninstall the given package with a specific version code, removing it completely from the device. If the version code of the package does not match the one passed in the versioned package argument this method is a no-op. Use [PackageManager.VERSION_CODE_HIGHEST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERSION_CODE_HIGHEST:kotlin.Int) to uninstall the latest version of the package.

This method is available to:

- the current "installer of record" for the package
- the device owner
- the affiliated profile owner

<br />

Requires [android.Manifest.permission#DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELETE_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_DELETE_PACKAGES:kotlin.String)

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `versionedPackage` | [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage):The versioned package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

**See Also**

- [android.app.admin.DevicePolicyManager](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#) 

### uninstall

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstall(
    versionedPackage: VersionedPackage, 
    flags: Int, 
    statusReceiver: IntentSender
): Unit
```

Uninstall the given package with a specific version code, removing it completely from the device. This method is only available to the current "installer of record" for the package. If the version code of the package does not match the one passed in the versioned package argument this method is a no-op. Use [PackageManager.VERSION_CODE_HIGHEST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERSION_CODE_HIGHEST:kotlin.Int) to uninstall the latest version of the package. 
Requires [android.Manifest.permission#DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELETE_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_DELETE_PACKAGES:kotlin.String)

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `versionedPackage` | [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage):The versioned package to uninstall. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags for uninstall. Value is either`0`or a combination of android.content.pm.PackageManager.DELETE_KEEP_DATA, android.content.pm.PackageManager.DELETE_ALL_USERS, android.content.pm.PackageManager.DELETE_SYSTEM_APP, android.content.pm.PackageManager.DELETE_DONT_KILL_APP, and android.content.pm.PackageManager.DELETE_CHATTY |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

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

Requires [android.Manifest.permission#DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELETE_PACKAGES:kotlin.String) or [android.Manifest.permission#REQUEST_DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_DELETE_PACKAGES:kotlin.String)

<br />

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value cannot be`null`. |

**See Also**

- [android.app.admin.DevicePolicyManager](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#) 

### uninstallExistingPackage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uninstallExistingPackage(
    packageName: String, 
    statusReceiver: IntentSender?
): Unit
```

Uninstall the given package for the user for which this installer was created if the package will still exist for other users on the device. 
Requires [android.Manifest.permission#DELETE_PACKAGES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DELETE_PACKAGES:kotlin.String)

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package to uninstall. This value cannot be`null`. |
| `statusReceiver` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)?:Where to deliver the result of the operation indicated by the extra [EXTRA_STATUS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_STATUS:kotlin.String). Refer to the individual status codes on how to handle them. This value may be`null`. |

### unregisterSessionCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterSessionCallback(callback: PackageInstaller.SessionCallback): Unit
```

Unregister a previously registered callback.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [PackageInstaller.SessionCallback](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback):This value cannot be`null`. |

### updateSessionAppIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateSessionAppIcon(
    sessionId: Int, 
    appIcon: Bitmap?
): Unit
```

Update the icon representing the app being installed in a specific session. This should be roughly [ActivityManager.getLauncherLargeIconSize()](https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getLauncherLargeIconSize())in both dimensions.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `appIcon` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)?:This value may be`null`. |

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

Similar to [checkInstallConstraints(java.util.List,android.content.pm.PackageInstaller.InstallConstraints,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#checkInstallConstraints(kotlin.collections.MutableList,%20android.content.pm.PackageInstaller.InstallConstraints,%20java.util.concurrent.Executor,%20java.util.function.Consumer)), but the callback is invoked only when the constraints are satisfied or after timeout.

Note: the device idle constraint might take a long time to evaluate. The system will ensure the constraint is evaluated completely before handling timeout.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:a list of package names to check the constraints for installation This value cannot be`null`. |
| `constraints` | [PackageInstaller.InstallConstraints](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.InstallConstraints):the constraints for installation. This value cannot be`null`. |
| `callback` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):Called when the constraints are satisfied or after timeout. Intents sent to this callback contain: [Intent.EXTRA_PACKAGES](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGES:kotlin.String) for the input package names, [EXTRA_INSTALL_CONSTRAINTS](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_INSTALL_CONSTRAINTS:kotlin.String) for the input constraints, [EXTRA_INSTALL_CONSTRAINTS_RESULT](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#EXTRA_INSTALL_CONSTRAINTS_RESULT:kotlin.String) for the result. This value cannot be`null`. |
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum time to wait, in milliseconds until the constraints are satisfied. Valid range is from 0 to one week.`0`means the callback will be invoked immediately no matter constraints are satisfied or not. Value is a non-negative duration in milliseconds. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the given packages' installer of record doesn't match the caller's own package name or the installerPackageName set by the caller doesn't match the caller's own package name. |
