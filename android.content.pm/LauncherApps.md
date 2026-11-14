Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LauncherApps

```
open class LauncherApps
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.LauncherApps](../android/content/pm/LauncherApps.md) |

Class for retrieving a list of launchable activities for the current user and any associated managed profiles that are visible to the current user, which can be retrieved with `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()`. This is mainly for use by launchers. Apps can be queried for each user profile. Since the PackageManager will not deliver package broadcasts for other profiles, you can register for package changes here.

To watch for managed profiles being added or removed, register for the following broadcasts: `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_ADDED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_REMOVED:kotlin.String`.

Note as of Android O, apps on a managed profile are no longer allowed to access apps on the main profile. Apps can only access profiles returned by `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ArchiveCompatibilityParams` Used to enable Archiving compatibility options with `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#setArchiveCompatibility(android.content.pm.LauncherApps.ArchiveCompatibilityParams)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback` Callbacks for package changes to this and related managed profiles. |
| | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` Represents a "pin shortcut" or a "pin appwidget" request made by an app, which is sent with an `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String` intent respectively to the default launcher app. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ShortcutQuery` Represents a query passed to `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcuts(android.content.pm.LauncherApps.ShortcutQuery,%20android.os.UserHandle)`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String` Activity Action: For the default launcher to show the confirmation dialog to create a pinned app widget. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String` Activity Action: For the default launcher to show the confirmation dialog to create a pinned shortcut. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#EXTRA_PIN_ITEM_REQUEST:kotlin.String` An extra for `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String` \& `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String` containing a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` of appropriate type asked to pin. |
| --- | --- |

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LauncherActivityInfo](../android/content/pm/LauncherActivityInfo.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getActivityList(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Retrieves a list of activities that specify `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`, across all apps, for a specified user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getAllPackageInstallerSessions()()` Return list of all known install sessions in this user and managed profiles, regardless of the installer. |
| open [IntentSender](../android/content/IntentSender.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getAppMarketActivityIntent(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns an intent sender which can be used to start the App Market activity (Installer Activity). |
| --- | --- |
| open [ApplicationInfo](../android/content/pm/ApplicationInfo.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getApplicationInfo(kotlin.String,%20kotlin.Int,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` about an application installed for a specific user profile. |
| [LauncherUserInfo](../android/content/pm/LauncherUserInfo.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getLauncherUserInfo(android.os.UserHandle)(userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns information related to a user which is useful for displaying UI elements to distinguish it from other users (eg, badges). |
| open [LauncherApps.PinItemRequest](../android/content/pm/LauncherApps.PinItemRequest.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPinItemRequest(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` A helper method to extract a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` set to the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#EXTRA_PIN_ITEM_REQUEST:kotlin.String` extra. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPreInstalledSystemPackages(android.os.UserHandle)(userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns the list of the system packages that are installed at user creation. |
| open [IntentSender](../android/content/IntentSender.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPrivateSpaceSettingsIntent()()` Returns `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` which can be used to start the Private Space Settings Activity. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UserHandle](../android/os/UserHandle.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getProfiles()()` Return a list of profiles that the caller can access via the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#` APIs. |
| --- | --- |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutBadgedIconDrawable(android.content.pm.ShortcutInfo,%20kotlin.Int)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!, density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the shortcut icon with badging appropriate for the profile. |
| open [IntentSender](../android/content/IntentSender.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutConfigActivityIntent(android.content.pm.LauncherActivityInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo)` Returns an intent sender which can be used to start the configure activity for creating custom shortcuts. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LauncherActivityInfo](../android/content/pm/LauncherActivityInfo.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutConfigActivityList(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Retrieves a list of config activities for creating `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`. |
| --- | --- |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutIconDrawable(android.content.pm.ShortcutInfo,%20kotlin.Int)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo, density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the icon for this shortcut, without any badging for the profile. |
| open [PendingIntent](../android/app/PendingIntent.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutIntent(kotlin.String,%20kotlin.String,%20android.os.Bundle,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, shortcutId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns PendingIntent associated with specified shortcut. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](../android/content/pm/ShortcutInfo.md)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcuts(android.content.pm.LauncherApps.ShortcutQuery,%20android.os.UserHandle)(query: https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ShortcutQuery, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match `query`. |
| --- | --- |
| open [Bundle](../android/os/Bundle.md)? | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getSuspendedPackageLauncherExtras(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Gets the launcher extras supplied to the system when the given package was suspended via `PackageManager#setPackagesSuspended(String[], boolean, PersistableBundle, PersistableBundle, String)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()()` Returns whether the caller can access the shortcut information. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#isActivityEnabled(android.content.ComponentName,%20android.os.UserHandle)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Checks if the activity exists and it enabled for a profile. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#isPackageEnabled(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Checks if the package is installed and enabled for a profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#pinShortcuts(kotlin.String,%20kotlin.collections.MutableList,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Pin shortcuts on a package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#registerCallback(android.content.pm.LauncherApps.Callback)(callback: https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback!)` Registers a callback for changes to packages in this user and managed profiles. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#registerCallback(android.content.pm.LauncherApps.Callback,%20android.os.Handler)(callback: https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Registers a callback for changes to packages in this user and managed profiles. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#registerPackageInstallerSessionCallback(java.util.concurrent.Executor,%20android.content.pm.PackageInstaller.SessionCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback)` Register a callback to watch for session lifecycle events in this user and managed profiles. |
| open [LauncherActivityInfo](../android/content/pm/LauncherActivityInfo.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#resolveActivity(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Returns the activity info for a given intent and user handle, if it resolves. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#setArchiveCompatibility(android.content.pm.LauncherApps.ArchiveCompatibilityParams)(params: https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ArchiveCompatibilityParams)` Disable different archive compatibility options of the launcher for the caller of this method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#shouldHideFromSuggestions(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Returns whether a package should be hidden from suggestions to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startAppDetailsActivity(android.content.ComponentName,%20android.os.UserHandle,%20android.graphics.Rect,%20android.os.Bundle)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, sourceBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Starts the settings activity to show the application details for a package in the specified profile. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle,%20android.graphics.Rect,%20android.os.Bundle)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, sourceBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Starts a Main activity in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startPackageInstallerSessionDetailsActivity(android.content.pm.PackageInstaller.SessionInfo,%20android.graphics.Rect,%20android.os.Bundle)(sessionInfo: https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo, sourceBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Starts an activity to show the details of the specified session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startShortcut(android.content.pm.ShortcutInfo,%20android.graphics.Rect,%20android.os.Bundle)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo, sourceBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?, startActivityOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Launches a shortcut. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startShortcut(kotlin.String,%20kotlin.String,%20android.graphics.Rect,%20android.os.Bundle,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, shortcutId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, sourceBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?, startActivityOptions: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Starts a shortcut. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#unregisterCallback(android.content.pm.LauncherApps.Callback)(callback: https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback!)` Unregisters a callback that was previously registered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#unregisterPackageInstallerSessionCallback(android.content.pm.PackageInstaller.SessionCallback)(callback: https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionCallback)` Unregisters a callback that was previously registered. |
| --- | --- |

## Constants

### ACTION_CONFIRM_PIN_APPWIDGET

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONFIRM_PIN_APPWIDGET: String
```

Activity Action: For the default launcher to show the confirmation dialog to create a pinned app widget.

See the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)` javadoc for details.

Use `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPinItemRequest(android.content.Intent)` to get a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` object, and call `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest#accept(android.os.Bundle)` if the user accepts. If the user doesn't accept, no further action is required.

 Value: "android.content.pm.action.CONFIRM_PIN_APPWIDGET"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#EXTRA_PIN_ITEM_REQUEST:kotlin.String`

### ACTION_CONFIRM_PIN_SHORTCUT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONFIRM_PIN_SHORTCUT: String
```

Activity Action: For the default launcher to show the confirmation dialog to create a pinned shortcut.

See the `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager` javadoc for details.

Use `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPinItemRequest(android.content.Intent)` to get a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` object, and call `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest#accept(android.os.Bundle)` if the user accepts. If the user doesn't accept, no further action is required.

 Value: "android.content.pm.action.CONFIRM_PIN_SHORTCUT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#EXTRA_PIN_ITEM_REQUEST:kotlin.String`

### EXTRA_PIN_ITEM_REQUEST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PIN_ITEM_REQUEST: String
```

An extra for `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String` \& `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String` containing a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` of appropriate type asked to pin.

A helper function `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPinItemRequest(android.content.Intent)` can be used instead of using this constant directly.

 Value: "android.content.pm.extra.PIN_ITEM_REQUEST"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String`

## Public methods

### getActivityList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityList(
    packageName: String!, 
    user: UserHandle!
): MutableList<LauncherActivityInfo!>!
```

Retrieves a list of activities that specify `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`, across all apps, for a specified user. If an app doesn't have any activities that specify `ACTION_MAIN` or `CATEGORY_LAUNCHER`, the system adds a synthesized activity to the list. This synthesized activity represents the app's details page within system settings.

**Note:**It's possible for system apps, such as app stores, to prevent the system from adding synthesized activities to the returned list.

As of [Android Q](../reference/android/os/Build.VERSION_CODES.md), at least one of the app's activities or synthesized activities appears in the returned list unless the app satisfies at least one of the following conditions:

- The app is a system app.
- The app doesn't request any [permissions](../guide/topics/permissions/overview.md).
- The app doesn't have a *launcher activity* that is enabled by default. A launcher activity has an intent containing the `ACTION_MAIN` action and the `CATEGORY_LAUNCHER` category.

Additionally, the system hides synthesized activities for some or all apps in the following enterprise-related cases:

- If the device is a [fully managed device](https://developers.google.com/android/work/overview#company-owned-devices-for-knowledge-workers), no synthesized activities for any app appear in the returned list.
- If the current user has a [work profile](https://developers.google.com/android/work/overview#employee-owned-devices-byod), no synthesized activities for the user's work apps appear in the returned list.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

For the returned `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo` objects, the App Lock fields (`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean`) within the underlying `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` (retrieved via `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getApplicationInfo()`) are present if the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)` for more information about App Lock.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The specific package to query. If null, it checks all installed packages in the profile. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The UserHandle of the profile. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo!>!` | List of launchable activities. Can be an empty list but will not be null. |

### getAllPackageInstallerSessions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllPackageInstallerSessions(): MutableList<PackageInstaller.SessionInfo!>
```

Return list of all known install sessions in this user and managed profiles, regardless of the installer. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to retrieve these details.

To receive callbacks for hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.SessionInfo!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#getAllSessions()`

### getAppMarketActivityIntent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppMarketActivityIntent(
    packageName: String?, 
    user: UserHandle
): IntentSender?
```

Returns an intent sender which can be used to start the App Market activity (Installer Activity). This method is primarily used to get an intent sender which starts App Market activity for another profile, if the caller is not otherwise allowed to start activity in that profile.

When packageName is set, intent sender to start the App Market Activity which installed the package in calling user will be returned, but for the profile passed.

When packageName is not set, intent sender to launch the default App Market Activity for the profile will be returned. In case there are multiple App Market Activities available for the profile, IntentPicker will be started, allowing user to choose the preferred activity.

The method will fall back to the behaviour of not having the packageName set, in case:

- No activity for the packageName is found in calling user-space.
- The App Market Activity which installed the package in calling user-space is not present.
- The App Market Activity which installed the package in calling user-space is not present in the profile passed.

<br />

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the package for which intent sender to launch App Market Activity is required. This value may be `null`. |
| `user` | [UserHandle](../android/os/UserHandle.md): the profile for which intent sender to launch App Market Activity is required. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` object which launches the App Market Activity, null in case there is no such activity. |

### getApplicationInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationInfo(
    packageName: String, 
    flags: Int, 
    user: UserHandle
): ApplicationInfo!
```

Returns `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` about an application installed for a specific user profile.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

App Lock fields in the returned `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` object (`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean`) are present if the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)` for more information about App Lock.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the application. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags android.content.pm.PackageManager#getApplicationInfo Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SHARED_LIBRARY_FILES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_UNINSTALLED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_SYSTEM_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_COMPONENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_UNINSTALLED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_APEX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_ARCHIVED_PACKAGES:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_APP_LOCK_INFO:kotlin.Long` |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!` | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` containing information about the package. Returns `null` if the package isn't installed for the given profile, or the profile isn't enabled. |

### getLauncherUserInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLauncherUserInfo(userHandle: UserHandle): LauncherUserInfo?
```

Returns information related to a user which is useful for displaying UI elements to distinguish it from other users (eg, badges).

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `userHandle` | [UserHandle](../android/os/UserHandle.md): user handle of the user for which LauncherUserInfo is requested. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo?` | the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo` object related to the user specified, null in case the user is inaccessible. |

### getPinItemRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPinItemRequest(intent: Intent!): LauncherApps.PinItemRequest!
```

A helper method to extract a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` set to the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#EXTRA_PIN_ITEM_REQUEST:kotlin.String` extra.

### getPreInstalledSystemPackages

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreInstalledSystemPackages(userHandle: UserHandle): MutableList<String!>
```

Returns the list of the system packages that are installed at user creation.

An empty list denotes that all system packages should be treated as pre-installed for that user at creation.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `userHandle` | [UserHandle](../android/os/UserHandle.md): the user for which installed system packages are required. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/java/lang/String.html#`, representing the package name of the installed package. Can be empty but not null. |

### getPrivateSpaceSettingsIntent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrivateSpaceSettingsIntent(): IntentSender?
```

Returns `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` which can be used to start the Private Space Settings Activity.

Caller should have `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` and either of the permissions required.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` object which launches the Private Space Settings Activity, if successful, null otherwise. |

### getProfiles

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProfiles(): MutableList<UserHandle!>!
```

Return a list of profiles that the caller can access via the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#` APIs.

If the caller is running on a managed profile, it'll return only the current profile. Otherwise it'll return the same list as `https://developer.android.com/reference/kotlin/android/os/UserManager.html#getUserProfiles()` would.

To get hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

### getShortcutBadgedIconDrawable

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutBadgedIconDrawable(
    shortcut: ShortcutInfo!, 
    density: Int
): Drawable!
```

Returns the shortcut icon with badging appropriate for the profile.

The calling launcher application must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional density for the icon, or 0 to use the default density. Use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | A badged icon for the shortcut. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`
- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutIconDrawable(android.content.pm.ShortcutInfo,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`

### getShortcutConfigActivityIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutConfigActivityIntent(info: LauncherActivityInfo): IntentSender?
```

Returns an intent sender which can be used to start the configure activity for creating custom shortcuts. Use this method if the provider is in another profile as you are not allowed to start an activity in another profile.

The caller should receive `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.PinItemRequest` in onActivityResult on `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`.

Callers must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

| Parameters ||
|---|---|
| `info` | [LauncherActivityInfo](../android/content/pm/LauncherActivityInfo.md): a configuration activity returned by `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutConfigActivityList(kotlin.String,%20android.os.UserHandle)` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked or not running. |
| `java.lang.SecurityException` | if `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()` is false. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getPinItemRequest(android.content.Intent)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_SHORTCUT:kotlin.String`

### getShortcutConfigActivityList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutConfigActivityList(
    packageName: String?, 
    user: UserHandle
): MutableList<LauncherActivityInfo!>!
```

Retrieves a list of config activities for creating `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The specific package to query. If null, it checks all installed packages in the profile. |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo!>!` | List of config activities. Can be an empty list but will not be null. Empty list will be returned for user-profiles that have items restricted on home screen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_SHORTCUT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutConfigActivityIntent(android.content.pm.LauncherActivityInfo)`

### getShortcutIconDrawable

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutIconDrawable(
    shortcut: ShortcutInfo, 
    density: Int
): Drawable!
```

Returns the icon for this shortcut, without any badging for the profile.

The calling launcher application must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `shortcut` | [ShortcutInfo](../android/content/pm/ShortcutInfo.md): This value cannot be `null`. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The preferred density of the icon, zero for default density. Use density DPI values from `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | The drawable associated with the shortcut. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`
- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcutBadgedIconDrawable(android.content.pm.ShortcutInfo,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`

### getShortcutIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutIntent(
    packageName: String, 
    shortcutId: String, 
    opts: Bundle?, 
    user: UserHandle
): PendingIntent?
```

Returns PendingIntent associated with specified shortcut.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The packageName of the shortcut. This value cannot be `null`. |
| `shortcutId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the shortcut. This value cannot be `null`. |
| `opts` | [Bundle](../android/os/Bundle.md)?: This parameter is no longer supported. This value may be `null`. |
| --- | --- |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#?` | This value may be `null`. |

### getShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcuts(
    query: LauncherApps.ShortcutQuery, 
    user: UserHandle
): MutableList<ShortcutInfo!>?
```

Returns `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match `query`.

Callers must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

| Parameters ||
|---|---|
| `query` | [LauncherApps.ShortcutQuery](../android/content/pm/LauncherApps.ShortcutQuery.md): result includes shortcuts matching this query. This value cannot be `null`. |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>?` | the IDs of `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match the query. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`

### getSuspendedPackageLauncherExtras

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSuspendedPackageLauncherExtras(
    packageName: String!, 
    user: UserHandle!
): Bundle?
```

Gets the launcher extras supplied to the system when the given package was suspended via `PackageManager#setPackagesSuspended(String[], boolean, PersistableBundle, PersistableBundle, String)`.

The contents of this `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` are supposed to be a contract between the suspending app and the launcher.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

Note: This just returns whatever extras were provided to the system, *which might even be `null`.*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package for which to fetch the launcher extras. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | A `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of launcher extras. Or `null` if the package is not currently suspended. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback#onPackagesSuspended(kotlin.Array,%20android.os.UserHandle,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#isPackageSuspended()`

### hasShortcutHostPermission

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasShortcutHostPermission(): Boolean
```

Returns whether the caller can access the shortcut information. Access is currently available to:

- The current launcher (or default launcher if there is no set current launcher).
- The currently active voice interaction service.

<br />

Note when this method returns `false`, it may be a temporary situation because the user is trying a new launcher application. The user may decide to change the default launcher back to the calling application again, so even if a launcher application loses this permission, it does **not** have to purge pinned shortcut information. If the calling launcher application contains pinned shortcuts, they will still work, even though the caller no longer has the shortcut host permission.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`

### isActivityEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isActivityEnabled(
    component: ComponentName!, 
    user: UserHandle!
): Boolean
```

Checks if the activity exists and it enabled for a profile.

The activity may still not be exported, in which case `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle,%20android.graphics.Rect,%20android.os.Bundle)` will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` unless the caller has the same UID as the target app's.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android/content/ComponentName.md)!: The activity to check. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The UserHandle of the profile. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the activity exists and is enabled. |

### isPackageEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPackageEnabled(
    packageName: String!, 
    user: UserHandle!
): Boolean
```

Checks if the package is installed and enabled for a profile.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package to check. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The UserHandle of the profile. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the package exists and is enabled. |

### pinShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pinShortcuts(
    packageName: String, 
    shortcutIds: MutableList<String!>, 
    user: UserHandle
): Unit
```

Pin shortcuts on a package.

This API is **NOT** cumulative; this will replace all pinned shortcuts for the package. However, different launchers may have different set of pinned shortcuts.

The calling launcher application must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

For user-profiles with items restricted on home screen, caller must have the required permission.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The target package name. This value cannot be `null`. |
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: The IDs of the shortcut to be pinned. This value cannot be `null`. |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager`

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerCallback(callback: LauncherApps.Callback!): Unit
```

Registers a callback for changes to packages in this user and managed profiles.

To receive callbacks for hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

This callback will also receive changes to the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserConfig()`, allowing clients to monitor updates to the user-specific configuration.

| Parameters ||
|---|---|
| `callback` | [LauncherApps.Callback](../android/content/pm/LauncherApps.Callback.md)!: The callback to register. |

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerCallback(
    callback: LauncherApps.Callback!, 
    handler: Handler!
): Unit
```

Registers a callback for changes to packages in this user and managed profiles.

To receive callbacks for hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

This callback will also receive changes to the `https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserConfig()`, allowing clients to monitor updates to the user-specific configuration.

| Parameters ||
|---|---|
| `callback` | [LauncherApps.Callback](../android/content/pm/LauncherApps.Callback.md)!: The callback to register. |
| `handler` | [Handler](../android/os/Handler.md)!: that should be used to post callbacks on, may be null. |

### registerPackageInstallerSessionCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerPackageInstallerSessionCallback(
    executor: Executor, 
    callback: PackageInstaller.SessionCallback
): Unit
```

Register a callback to watch for session lifecycle events in this user and managed profiles. Callers need to either declare \<queries\> element with the specific package name in the app's manifest, have the android.permission.QUERY_ALL_PACKAGES, or be the session owner to watch for these events.

Session callbacks are not sent for user-profiles that have items restricted on home screen.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to handle the callbacks, cannot be null. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md): The callback to register. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#registerSessionCallback(android.content.pm.PackageInstaller.SessionCallback)`

### resolveActivity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveActivity(
    intent: Intent!, 
    user: UserHandle!
): LauncherActivityInfo!
```

Returns the activity info for a given intent and user handle, if it resolves. Otherwise it returns null.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

For the returned `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo` object, the App Lock fields (`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean`) within the underlying `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo` (retrieved via `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getApplicationInfo()`) are present if the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)` for more information about App Lock.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The intent to find a match for. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The profile to look in for a match. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo!` | An activity info object if there is a match. |

### setArchiveCompatibility

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setArchiveCompatibility(params: LauncherApps.ArchiveCompatibilityParams): Unit
```

Disable different archive compatibility options of the launcher for the caller of this method.

| Parameters ||
|---|---|
| `params` | [LauncherApps.ArchiveCompatibilityParams](../android/content/pm/LauncherApps.ArchiveCompatibilityParams.md): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ArchiveCompatibilityParams`

### shouldHideFromSuggestions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shouldHideFromSuggestions(
    packageName: String, 
    user: UserHandle
): Boolean
```

Returns whether a package should be hidden from suggestions to the user. Currently, this could be done because the package was marked as distracting to the user via `PackageManager.setDistractingPackageRestrictions(String[], int)`.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package for which to check. This value cannot be `null`. |
| `user` | [UserHandle](../android/os/UserHandle.md): the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | |

### startAppDetailsActivity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startAppDetailsActivity(
    component: ComponentName!, 
    user: UserHandle!, 
    sourceBounds: Rect!, 
    opts: Bundle!
): Unit
```

Starts the settings activity to show the application details for a package in the specified profile.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android/content/ComponentName.md)!: The ComponentName of the package to launch settings for. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The UserHandle of the profile |
| `sourceBounds` | [Rect](../android/graphics/Rect.md)!: The Rect containing the source bounds of the clicked icon |
| --- | --- |
| `opts` | [Bundle](../android/os/Bundle.md)!: Options to pass to startActivity |

### startMainActivity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startMainActivity(
    component: ComponentName!, 
    user: UserHandle!, 
    sourceBounds: Rect!, 
    opts: Bundle!
): Unit
```

Starts a Main activity in the specified profile.

If the user in question is a hidden profile `https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String`, caller should have normal `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HIDDEN_PROFILES:kotlin.String` permission and the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_HOME:kotlin.String` role.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android/content/ComponentName.md)!: The ComponentName of the activity to launch |
| `user` | [UserHandle](../android/os/UserHandle.md)!: The UserHandle of the profile |
| `sourceBounds` | [Rect](../android/graphics/Rect.md)!: The Rect containing the source bounds of the clicked icon |
| --- | --- |
| `opts` | [Bundle](../android/os/Bundle.md)!: Options to pass to startActivity |

### startPackageInstallerSessionDetailsActivity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startPackageInstallerSessionDetailsActivity(
    sessionInfo: PackageInstaller.SessionInfo, 
    sourceBounds: Rect?, 
    opts: Bundle?
): Unit
```

Starts an activity to show the details of the specified session.

| Parameters ||
|---|---|
| `sessionInfo` | [PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md): The SessionInfo of the session. This value cannot be `null`. |
| `sourceBounds` | [Rect](../android/graphics/Rect.md)?: The Rect containing the source bounds of the clicked icon. This value may be `null`. |
| `opts` | [Bundle](../android/os/Bundle.md)?: Options to pass to startActivity. This value may be `null`. |
| --- | --- |

### startShortcut

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startShortcut(
    shortcut: ShortcutInfo, 
    sourceBounds: Rect?, 
    startActivityOptions: Bundle?
): Unit
```

Launches a shortcut.

The calling launcher application must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

| Parameters ||
|---|---|
| `shortcut` | [ShortcutInfo](../android/content/pm/ShortcutInfo.md): The target shortcut. This value cannot be `null`. |
| `sourceBounds` | [Rect](../android/graphics/Rect.md)?: The Rect containing the source bounds of the clicked icon. This value may be `null`. |
| `startActivityOptions` | [Bundle](../android/os/Bundle.md)?: Options to pass to startActivity. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | failed to start shortcut. (e.g. the shortcut no longer exists, is disabled, the intent receiver activity doesn't exist, etc) |
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

### startShortcut

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startShortcut(
    packageName: String, 
    shortcutId: String, 
    sourceBounds: Rect?, 
    startActivityOptions: Bundle?, 
    user: UserHandle
): Unit
```

Starts a shortcut.

The calling launcher application must be allowed to access the shortcut information, as defined in `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#hasShortcutHostPermission()`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The target shortcut package name. This value cannot be `null`. |
| `shortcutId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The target shortcut ID. This value cannot be `null`. |
| `sourceBounds` | [Rect](../android/graphics/Rect.md)?: The Rect containing the source bounds of the clicked icon. This value may be `null`. |
| --- | --- |
| `startActivityOptions` | [Bundle](../android/os/Bundle.md)?: Options to pass to startActivity. This value may be `null`. |
| `user` | [UserHandle](../android/os/UserHandle.md): The UserHandle of the profile. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | failed to start shortcut. (e.g. the shortcut no longer exists, is disabled, the intent receiver activity doesn't exist, etc) |
| `java.lang.IllegalStateException` | when the user is locked, or when the `user` user is locked or not running. |

### unregisterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterCallback(callback: LauncherApps.Callback!): Unit
```

Unregisters a callback that was previously registered.

| Parameters ||
|---|---|
| `callback` | [LauncherApps.Callback](../android/content/pm/LauncherApps.Callback.md)!: The callback to unregister. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#registerCallback(android.content.pm.LauncherApps.Callback)`

### unregisterPackageInstallerSessionCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterPackageInstallerSessionCallback(callback: PackageInstaller.SessionCallback): Unit
```

Unregisters a callback that was previously registered.

| Parameters ||
|---|---|
| `callback` | [PackageInstaller.SessionCallback](../android/content/pm/PackageInstaller.SessionCallback.md): The callback to unregister. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#registerPackageInstallerSessionCallback(java.util.concurrent.Executor,%20android.content.pm.PackageInstaller.SessionCallback)`
