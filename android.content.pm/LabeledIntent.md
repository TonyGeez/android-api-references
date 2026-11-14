Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LabeledIntent

```
open class LabeledIntent : Intent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) ||
| | ↳ | [android.content.pm.LabeledIntent](https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#) |

A special subclass of Intent that can have a custom label/icon associated with it. Primarily for use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_AIRPLANE_MODE_CHANGED:kotlin.String`

Broadcast Action: The user has switched the phone into or out of Airplane Mode. One or more radios have been turned off or on. The intent will have the following extra value:

- *state* - A boolean value indicating whether Airplane Mode is on. If true, then cell radio and possibly other radios such as bluetooth or WiFi may have also been turned off

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ALL_APPS:kotlin.String`

Activity Action: List all available applications.

Input: Nothing.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ANSWER:kotlin.String`

Activity Action: Handle an incoming phone call.

Input: nothing.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APPLICATION_LOCALE_CHANGED:kotlin.String`

Broadcast Action: Locale of a particular app has changed.

This broadcast is explicitly sent to the `https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo#getInstallingPackageName()` installer of the app whose locale has changed.

The broadcast could also be received by manifest-declared receivers with `android.permission.READ_APP_SPECIFIC_LOCALES`

This is a protected intent that can only be sent by the system.

Includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` is the name of the package for which locale changed.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCALE_LIST:kotlin.String` contains locales that are currently set for specified app

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APPLICATION_PREFERENCES:kotlin.String`

An activity that provides a user interface for adjusting application preferences. Optional but recommended settings for all applications which have settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APPLICATION_RESTRICTIONS_CHANGED:kotlin.String`

Broadcast Action: Sent after application restrictions are changed.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APP_ERROR:kotlin.String`

Activity Action: The user pressed the "Report" button in the crash/ANR dialog. This intent is delivered to the package which installed the application, usually Google Play.

Input: No data is specified. The bug report is passed in using an `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_BUG_REPORT:kotlin.String` field.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String`

Activity Action: Perform assist action.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_PACKAGE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_CONTEXT:kotlin.String`, can provide additional optional contextual information about where the user was when they requested the assist; `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER:kotlin.String` may be set with additional referrer information. Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ATTACH_DATA:kotlin.String`

Used to indicate that some piece of data should be attached to some other place. For example, image data could be attached to a contact. It is up to the recipient to decide where the data should be attached; the intent does not specify the ultimate destination.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of data to be attached.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_AUTO_REVOKE_PERMISSIONS:kotlin.String`

Activity action: Launch UI to manage auto-revoke state. This is equivalent to Intent#ACTION_APPLICATION_DETAILS_SETTINGS

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)` should be a `package`-scheme `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with a package name, whose auto-revoke state will be reviewed (mandatory). E.g. `Uri.fromParts("package", packageName, null) `

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String`

Broadcast Action: This is a *sticky broadcast* containing the charging state, level, and other information about the battery. See `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for documentation on the contents of the Intent.

You *cannot* receive this through components declared in manifests, only by explicitly registering for it with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_LOW:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_OKAY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_POWER_CONNECTED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_POWER_DISCONNECTED:kotlin.String` for distinct battery-related broadcasts that are sent and can be received through manifest receivers.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_LOW:kotlin.String`

Broadcast Action: Indicates low battery condition on the device. This broadcast corresponds to the "Low battery warning" system dialog.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_OKAY:kotlin.String`

Broadcast Action: Indicates the battery is now okay after being low. This will be sent after `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_LOW:kotlin.String` once the battery has gone back up to an okay state.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BOOT_COMPLETED:kotlin.String`

Broadcast Action: This is broadcast once, after the user has finished booting. It can be used to perform application-specific initialization, such as installing alarms. You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECEIVE_BOOT_COMPLETED:kotlin.String` permission in order to receive this broadcast.

This broadcast is sent at boot by all devices (both with and without direct boot support). Upon receipt of this broadcast, the user is unlocked and both device-protected and credential-protected storage can accessed safely.

If you need to run while the user is still locked (before they've entered their lock pattern or PIN for the first time), you can listen for the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LOCKED_BOOT_COMPLETED:kotlin.String` broadcast.

Starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this broadcast is not only sent after the device boots but also delivered to an app when it is removed from the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int` state and the user is unlocked, such as the first launch after force-stopping the app. This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BUG_REPORT:kotlin.String`

Activity Action: Show activity for reporting a bug.

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String`

Activity Action: Perform a call to someone specified by the data.

Input: If nothing, an empty dialer is started; else `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of a phone number to be dialed or a tel: URI of an explicit phone number.

Output: nothing.

Note: there will be restrictions on which applications can initiate a call; most applications should use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String`.

Note: this Intent **cannot** be used to call emergency numbers. Applications can **dial** emergency numbers using `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String`, however.

Note: This Intent can only be used to dial call forwarding MMI codes if the application using this intent is set as the default or system dialer. The system will treat any other application using this Intent for the purpose of dialing call forwarding MMI codes as if the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String` Intent was used instead.

Note: An app filling the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_DIALER:kotlin.String` role should use `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#placeCall(android.net.Uri,%20android.os.Bundle)` to place calls rather than relying on this intent.

Note: If your app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` or higher and declares as using the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String` permission which is not granted, then attempting to use this action will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL_BUTTON:kotlin.String`

Activity Action: The user pressed the "call" button to go to the dialer or other appropriate UI for placing a call.

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CAMERA_BUTTON:kotlin.String`

Broadcast Action: The "Camera Button" was pressed. Includes a single extra field, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_KEY_EVENT:kotlin.String`, containing the key event that caused the broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CARRIER_SETUP:kotlin.String`

Activity Action: Main entry point for carrier setup apps.

Carrier apps that provide an implementation for this action may be invoked to configure carrier service and typically require `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()` to fulfill their duties.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`

Activity Action: Display an activity chooser, allowing the user to pick what they want to before proceeding. This can be used as an alternative to the standard activity picker that is displayed by the system when you try to start an activity with multiple possible matches, with these differences in behavior:

- You can specify the title that will appear in the activity chooser.
- The user does not have the option to make one of the matching activities a preferred activity, and all possible activities will always be shown even if one of them is currently marked as the preferred activity.

<br />

This action should be used when the user will naturally expect to select an activity in order to proceed. An example if when not to use it is when the user clicks on a "mailto:" link. They would naturally expect to go directly to their mail app, so startActivity() should be called directly: it will either launch the current preferred app, or put up a dialog allowing the user to pick an app to use and optionally marking that as preferred.

In contrast, if the user is selecting a menu item to send a picture they are viewing to someone else, there are many different things they may want to do at this point: send it through e-mail, upload it to a web service, etc. In this case the CHOOSER action should be used, to always present to the user a list of the things they can do, with a nice title given by the caller such as "Send this photo with:".

If you need to grant URI permissions through a chooser, you must specify the permissions to be granted on the ACTION_CHOOSER Intent *in addition* to the EXTRA_INTENT inside. This means using `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)` to specify the URIs to be granted as well as `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` as appropriate.

As a convenience, an Intent of this form can be created with the #createChooser function.

Input: No data should be specified. get\*Extra must have a `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` field containing the Intent being executed, and can optionally have a `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TITLE:kotlin.String` field containing the title text to display in the chooser.

Output: Depends on the protocol of `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CLOSE_SYSTEM_DIALOGS:kotlin.String`

Broadcast Action: This is broadcast when a user action should request a temporary system dialog to dismiss. Some examples of temporary system dialogs are the notification window-shade and the recent tasks dialog. 
Requires android.Manifest.permission.BROADCAST_CLOSE_SYSTEM_DIALOGS

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CONFIGURATION_CHANGED:kotlin.String`

Broadcast Action: The current device `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` (orientation, locale, etc) has changed. When such a change happens, the UIs (view hierarchy) will need to be rebuilt based on this new information; for the most part, applications don't need to worry about this, because the system will take care of stopping and restarting the application to make sure it sees the new changes. Some system code that can not be restarted will need to watch for this action and handle it appropriately.

You *cannot* receive this through components declared in manifests, only by explicitly registering for it with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_DOCUMENT:kotlin.String`

Activity Action: Allow the user to create a new document. When invoked, the system will display the various `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#` instances installed on the device, letting the user navigate through them. The returned document may be a newly created document with no content, or it may be an existing document with the requested MIME type.

Each document is represented as a `content://` URI backed by a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#`, which can be opened as a stream with `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`, or queried for `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document.html#` metadata.

Callers must indicate the concrete MIME type of the document being created by setting `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`. This MIME type cannot be changed after the document is created.

Callers can provide an initial display name through `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TITLE:kotlin.String`, but the user may change this value before creating the file.

Callers must include `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_OPENABLE:kotlin.String` in the Intent to obtain URIs that can be opened with `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`.

Callers can set a document URI through `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#EXTRA_INITIAL_URI:kotlin.String` to indicate the initial location of documents navigator. System will do its best to launch the navigator in the specified document if it's a folder, or the folder that contains the specified document if not.

Output: The URI of the item that was created. This must be a `content://` URI so that any receiver can access it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_NOTE:kotlin.String`

Activity Action: Starts a note-taking activity that can be used to create a note. This action can be used to start an activity on the lock screen. Activity should ensure to appropriately handle privacy sensitive data and features when launched on the lock screen. See `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for lock screen checks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_REMINDER:kotlin.String`

Activity Action: Creates a reminder.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TITLE:kotlin.String` The title of the reminder that will be shown to the user. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` The reminder text that will be shown to the user. The intent should at least specify a title or a text. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIME:kotlin.String` The time when the reminder will be shown to the user. The time is specified in milliseconds since the Epoch (optional).

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_SHORTCUT:kotlin.String`

Activity Action: Creates a shortcut.

Input: Nothing.

Output: An Intent representing the `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo` result.

For compatibility with older versions of android the intent may also contain three extras: SHORTCUT_INTENT (value: Intent), SHORTCUT_NAME (value: String), and SHORTCUT_ICON (value: Bitmap) or SHORTCUT_ICON_RESOURCE (value: ShortcutIconResource).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DATE_CHANGED:kotlin.String`

Broadcast Action: The date has changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DEFAULT:kotlin.String`

A synonym for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`, the "standard" action that is performed on a piece of data.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DEFINE:kotlin.String`

Activity Action: Define the meaning of the selected word(s).

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` is the text to define.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DELETE:kotlin.String`

Activity Action: Delete the given data from its container.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of data to be deleted.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DEVICE_STORAGE_LOW:kotlin.String`

Broadcast Action: A sticky broadcast that indicates low storage space condition on the device

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DEVICE_STORAGE_OK:kotlin.String`

Broadcast Action: Indicates low storage space condition on the device no longer exists

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DIAL:kotlin.String`

Activity Action: Dial a number as specified by the data. This shows a UI with the number being dialed, allowing the user to explicitly initiate the call.

Input: If nothing, an empty dialer is started; else `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of a phone number to be dialed or a tel: URI of an explicit phone number.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DOCK_EVENT:kotlin.String`

Broadcast Action: A sticky broadcast for changes in the physical docking state of the device.

The intent will have the following extra values:

- *`https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String`* - the current dock state, indicating which dock the device is physically in.

This is intended for monitoring the current physical dock state. See `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for the normal API dealing with dock mode changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DREAMING_STARTED:kotlin.String`

Broadcast Action: Sent after the system starts dreaming.

This is a protected intent that can only be sent by the system. It is only sent to registered receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DREAMING_STOPPED:kotlin.String`

Broadcast Action: Sent after the system stops dreaming.

This is a protected intent that can only be sent by the system. It is only sent to registered receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EDIT:kotlin.String`

Activity Action: Provide explicit editable access to the given data.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of data to be edited.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_AVAILABLE:kotlin.String`

Broadcast Action: Resources for a set of packages (which were previously unavailable) are currently available since the media on which they exist is available. The extra data `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` contains a list of packages whose availability changed. The extra data `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` contains a list of uids of packages whose availability changed. Note that the packages in this list do *not* receive this broadcast. The specified set of packages are now available on the system.

Includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` is the set of packages whose resources(were previously unavailable) are currently available. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` is the set of uids of the packages whose resources(were previously unavailable) are currently available.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_UNAVAILABLE:kotlin.String`

Broadcast Action: Resources for a set of packages are currently unavailable since the media on which they exist is unavailable. The extra data `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` contains a list of packages whose availability changed. The extra data `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` contains a list of uids of packages whose availability changed. The specified set of packages can no longer be launched and are practically unavailable on the system.

Inclues the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` is the set of packages whose resources are no longer available. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` is the set of packages whose resources are no longer available.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_FACTORY_TEST:kotlin.String`

Activity Action: Main entry point for factory tests. Only used when the device is booting in factory test node. The implementing package must be installed in the system image.

Input: nothing

Output: nothing

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_CONTENT:kotlin.String`

Activity Action: Allow the user to select a particular kind of data and return it. This is different than `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK:kotlin.String` in that here we just say what kind of data is desired, not a URI of existing data from which the user can pick. An ACTION_GET_CONTENT could allow the user to create the data as it runs (for example taking a picture or recording a sound), let them browse over the web and download the desired data, etc.

There are two main ways to use this action: if you want a specific kind of data, such as a person contact, you set the MIME type to the kind of data you want and launch it with `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`. The system will then launch the best application to select that kind of data for you.

You may also be interested in any of a set of types of content the user can pick. For example, an e-mail application that wants to allow the user to add an attachment to an e-mail message can use this action to bring up a list of all of the types of content the user can attach.

In this case, you should wrap the GET_CONTENT intent with a chooser (through #createChooser), which will give the proper interface for the user to pick how to send your data and allow you to specify a prompt indicating what they are doing. You will usually specify a broad MIME type (such as image/\* or \*/\*), resulting in a broad range of content types the user can select from.

When using such a broad GET_CONTENT action, it is often desirable to only pick from data that can be represented as a stream. This is accomplished by requiring the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_OPENABLE:kotlin.String` in the Intent.

Callers can optionally specify `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCAL_ONLY:kotlin.String` to request that the launched content chooser only returns results representing data that is locally available on the device. For example, if this extra is set to true then an image picker should not show any pictures that are available from a remote server but not already on the local device (thus requiring they be downloaded when opened).

If the caller can handle multiple returned items (the user performing multiple selection), then it can specify `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_MULTIPLE:kotlin.String` to indicate this.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getType()` is the desired MIME type to retrieve. Note that no URI is supplied in the intent, as there are no constraints on where the returned data originally comes from. You may also include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_OPENABLE:kotlin.String` if you can only accept data that can be opened as a stream. You may use `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCAL_ONLY:kotlin.String` to limit content selection to local data. You may use `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_MULTIPLE:kotlin.String` to allow the user to select multiple items.

Output: The URI of the item that was picked. This must be a content: URI so that any receiver can access it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_RESTRICTION_ENTRIES:kotlin.String`

Broadcast to a specific application to query any supported restrictions to impose on restricted users. The broadcast intent contains an extra with the currently persisted restrictions as a Bundle of key/value pairs. The value types can be Boolean, String or String\[\] depending on the restriction type.

<br />

The response should contain an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_LIST:kotlin.String`, which is of type `ArrayList<RestrictionEntry>`. It can also contain an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_INTENT:kotlin.String`, which is of type `Intent`. The activity specified by that intent will be launched for a result which must contain one of the extras `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_LIST:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_BUNDLE:kotlin.String`. The keys and values of the returned restrictions will be persisted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GTALK_SERVICE_CONNECTED:kotlin.String`

Broadcast Action: A GTalk connection has been established.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GTALK_SERVICE_DISCONNECTED:kotlin.String`

Broadcast Action: A GTalk connection has been disconnected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_HEADSET_PLUG:kotlin.String`

Broadcast Action: Wired Headset plugged in or unplugged. Same as `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#ACTION_HEADSET_PLUG:kotlin.String`, to be consulted for value and documentation.

If the minimum SDK version of your application is `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, it is recommended to refer to the `AudioManager` constant in your receiver registration code instead.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_HOME_TIME_ZONE_CHANGED:kotlin.String`

Broadcast Action: The user's home timezone has changed. The intent will have the following extra values:

<br />

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_HOME_TIME_ZONE_ID:kotlin.String` - The time zone ID string value of the new time zone.

This is a protected intent that can only be sent by the system.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_HOME_TIME_ZONE:kotlin.String` permission. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_HOME_TIME_ZONE:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INPUT_METHOD_CHANGED:kotlin.String`

Broadcast Action: An input method has been changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSERT:kotlin.String`

Activity Action: Insert an empty item into the given container.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of the directory (vnd.android.cursor.dir/\*) in which to place the data.

Output: URI of the new data that was created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSERT_OR_EDIT:kotlin.String`

Activity Action: Pick an existing item, or insert a new item, and then edit it.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getType()` is the desired MIME type of the item to create or edit. The extras can contain type specific data to pass through to the editing/creating activity.

Output: The URI of the item that was picked. This must be a content: URI so that any receiver can access it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_FAILURE:kotlin.String`

Activity Action: Activity to handle split installation failures.

Splits may be installed dynamically. This happens when an Activity is launched, but the split that contains the application isn't installed. When a split is installed in this manner, the containing package usually doesn't know this is happening. However, if an error occurs during installation, the containing package can define a single activity handling this action to deal with such failures.

The activity handling this action must be in the base package.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` the original intent that started split installation. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SPLIT_NAME:kotlin.String` the name of the split that failed to be installed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String`

Activity Action: Launch application installer.

Input: The data must be a content: URI at which the application can be retrieved. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int`, you can also use "package:" to install an application for the current user that is already installed for another user. You can optionally supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INSTALLER_PACKAGE_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_NOT_UNKNOWN_SOURCE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_REPLACE:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RETURN_RESULT:kotlin.String`.

Output: If `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RETURN_RESULT:kotlin.String`, returns whether the install succeeded.

**Note:** If your app is targeting API level higher than 25 you need to hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String` in order to launch the application installer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`

Activity Action: Use with startActivityForResult to start a system activity that captures content on the screen to take a screenshot and present it to the user for editing. The edited screenshot is saved on device and returned to the calling activity as a through `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`. User interaction is required to return the edited screenshot to the calling activity.

The response `https://developer.android.com/reference/kotlin/android/content/Intent.html#` may include additional data to "backlink" directly back to the application for which the screenshot was captured. If present, the application "backlink" can be retrieved via `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()`. The data is present only if the user accepted to include the link information with the screenshot. The data can contain one of the following:

- A deeplinking `https://developer.android.com/reference/kotlin/android/net/Uri.html#` or an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` if the captured app integrates with `https://developer.android.com/reference/kotlin/android/app/assist/AssistContent.html#`.
- Otherwise, a main launcher intent that launches the screenshotted application to its home screen.

The "backlink" to the screenshotted application will be set within `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`, either as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` or an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` if present.

This intent action requires the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`.

Callers should query `https://developer.android.com/reference/kotlin/android/app/StatusBarManager.html#canLaunchCaptureContentActivityForNote(android.app.Activity)` before showing a UI element that allows users to trigger this flow.

Callers should query for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` in the response `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to check if the request was a success. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LOCALE_CHANGED:kotlin.String`

Broadcast Action: The receiver's effective locale has changed. This happens when the device locale, the receiving app's locale (set via `https://developer.android.com/reference/kotlin/android/app/LocaleManager.html#setApplicationLocales(android.os.LocaleList)`) or language tags of Regional preferences changed. Can be received by manifest-declared receivers.

If only the app locale changed, includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` is the name of the package for which locale changed.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCALE_LIST:kotlin.String` contains locales that are currently set for specified app

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LOCKED_BOOT_COMPLETED:kotlin.String`

Broadcast Action: This is broadcast once, after the user has finished booting, but while still in the "locked" state. It can be used to perform application-specific initialization, such as installing alarms. You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECEIVE_BOOT_COMPLETED:kotlin.String` permission in order to receive this broadcast.

This broadcast is sent immediately at boot by all devices (regardless of direct boot support) running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` or higher. Upon receipt of this broadcast, the user is still locked and only device-protected storage can be accessed safely. If you want to access credential-protected storage, you need to wait for the user to be unlocked (typically by entering their lock pattern or PIN for the first time), after which the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_UNLOCKED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BOOT_COMPLETED:kotlin.String` broadcasts are sent.

To receive this broadcast, your receiver component must be marked as being `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo#directBootAware:kotlin.Boolean`.

Starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this broadcast is not only sent after the device boots but also delivered to an app when it is removed from the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int` state, such as the first launch after force-stopping the app. This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LOOK_UP_TEXT:kotlin.String`

Activity Action: Launch an activity to look up the user's selected text.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` contains the selected text to look up.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String`

Activity Action: Start as a main entry point, does not expect to receive data.

Input: nothing

Output: nothing

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_ADDED:kotlin.String`

Broadcast sent to the primary user when an associated managed profile is added (the profile was created and is ready to be used). Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile that was added. Only applications (for example Launchers) that need to display merged content across both primary and managed profiles need to worry about this broadcast. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_AVAILABLE:kotlin.String`

Broadcast sent to the primary user when an associated managed profile has become available. Currently this includes when the user disables quiet mode for the profile. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. When quiet mode is changed, this broadcast will carry a boolean extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUIET_MODE:kotlin.String` indicating the new state of quiet mode. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_REMOVED:kotlin.String`

Broadcast sent to the primary user when an associated managed profile is removed. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile that was removed. Only applications (for example Launchers) that need to display merged content across both primary and managed profiles need to worry about this broadcast. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_UNAVAILABLE:kotlin.String`

Broadcast sent to the primary user when an associated managed profile has become unavailable. Currently this includes when the user enables quiet mode for the profile. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. When quiet mode is changed, this broadcast will carry a boolean extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUIET_MODE:kotlin.String` indicating the new state of quiet mode. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_UNLOCKED:kotlin.String`

Broadcast sent to the primary user when the credential-encrypted private storage for an associated managed profile is unlocked. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile that was unlocked. Only applications (for example Launchers) that need to display merged content across both primary and managed profiles need to worry about this broadcast. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGE_NETWORK_USAGE:kotlin.String`

Activity Action: Show settings for managing network data usage of a specific application. Applications should define an activity that offers options to control data usage.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGE_PACKAGE_STORAGE:kotlin.String`

Broadcast Action: Indicates low memory condition notification acknowledged by user and package management should be started. This is triggered by the user from the ACTION_DEVICE_STORAGE_LOW notification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGE_UNUSED_APPS:kotlin.String`

Activity action: Launch UI to manage unused apps (hibernated apps).

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BAD_REMOVAL:kotlin.String`

Broadcast Action: External media was removed from SD card slot, but mount point was not unmounted. The path to the mount point for the removed media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String`

Broadcast Action: The "Media Button" was pressed. Includes a single extra field, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_KEY_EVENT:kotlin.String`, containing the key event that caused the broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_CHECKING:kotlin.String`

Broadcast Action: External media is present, and being disk-checked The path to the mount point for the checking media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_EJECT:kotlin.String`

Broadcast Action: User has expressed the desire to remove the external storage media. Applications should close all files they have open within the mount point when they receive this intent. The path to the mount point for the media to be ejected is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_MOUNTED:kotlin.String`

Broadcast Action: External media is present and mounted at its mount point. The path to the mount point for the mounted media is contained in the Intent.mData field. The Intent contains an extra with name "read-only" and Boolean value to indicate if the media was mounted read only.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_NOFS:kotlin.String`

Broadcast Action: External media is present, but is using an incompatible fs (or is blank) The path to the mount point for the checking media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_REMOVED:kotlin.String`

Broadcast Action: External media has been removed. The path to the mount point for the removed media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SCANNER_FINISHED:kotlin.String`

Broadcast Action: The media scanner has finished scanning a directory. The path to the scanned directory is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SCANNER_SCAN_FILE:kotlin.String`

Broadcast Action: Request the media scanner to scan a file and add it to the media database.

The path to the file is contained in `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SCANNER_STARTED:kotlin.String`

Broadcast Action: The media scanner has started scanning a directory. The path to the directory being scanned is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_SHARED:kotlin.String`

Broadcast Action: External media is unmounted because it is being shared via USB mass storage. The path to the mount point for the shared media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTABLE:kotlin.String`

Broadcast Action: External media is present but cannot be mounted. The path to the mount point for the unmountable media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_UNMOUNTED:kotlin.String`

Broadcast Action: External media is present, but not mounted at its mount point. The path to the mount point for the unmounted media is contained in the Intent.mData field.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_REPLACED:kotlin.String`

Broadcast Action: A new version of your application has been installed over an existing one. This is only sent to the application that was replaced. It does not contain any additional data; to receive it, just use an intent filter for this action.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`

Broadcast Action: Sent to a package that has been suspended by the system. This is sent whenever a package is put into a suspended state or any of its app extras change while in the suspended state.

Optionally includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUSPENDED_PACKAGE_EXTRAS:kotlin.String` which is a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` which will contain useful information for the app being suspended.

This is a protected intent that can only be sent by the system. *This will be delivered to `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` components declared in the manifest.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_UNSUSPENDED:kotlin.String`

Broadcast Action: Sent to a package that has been unsuspended.

This is a protected intent that can only be sent by the system. *This will be delivered to `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` components declared in the manifest.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_NEW_OUTGOING_CALL:kotlin.String`

Broadcast Action: An outgoing call is about to be placed.

The Intent will have the following extra value:

- *`https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PHONE_NUMBER:kotlin.String`* - the phone number dialed.

Starting in Android 15, this broadcast is no longer sent as an ordered broadcast. The `resultData` no longer has any effect and will not determine the actual routing of the call. Further, receivers of this broadcast do not get foreground priority and cannot launch background activities.

Once the broadcast is finished, the resultData is used as the actual number to call. If `null`, no call will be placed.

It is perfectly acceptable for multiple receivers to process the outgoing call in turn: for example, a parental control application might verify that the user is authorized to place the call at that time, then a number-rewriting application might add an area code if one was not specified.

For consistency, any receiver whose purpose is to prohibit phone calls should have a priority of 0, to ensure it will see the final phone number to be dialed. Any receiver whose purpose is to rewrite phone numbers to be called should have a positive priority. Negative priorities are reserved for the system for this broadcast; using them may cause problems.

Any BroadcastReceiver receiving this Intent *must not* abort the broadcast.

Emergency calls cannot be intercepted using this mechanism, and other calls cannot be modified to call emergency numbers using this mechanism.

Some apps (such as VoIP apps) may want to redirect the outgoing call to use their own service instead. Those apps should first prevent the call from being placed by setting resultData to `null` and then start their own app to make the call.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PROCESS_OUTGOING_CALLS:kotlin.String` permission to receive this Intent.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this broadcast is no longer sent as an ordered broadcast, and does not allow activity launches. This means that receivers may no longer change the phone number for the outgoing call, or cancel the outgoing call. This functionality is only possible using the `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#` API. Although background receivers are woken up to handle this intent, no guarantee is made as to the timeliness of the broadcast.

This is a protected intent that can only be sent by the system.

If the user has chosen a `https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#` to handle redirection of outgoing calls, this intent will NOT be sent as an ordered broadcast. This means that attempts to re-write the outgoing call by other apps using this intent will be ignored.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String`

Activity Action: Allow the user to select and return one or more existing documents. When invoked, the system will display the various `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#` instances installed on the device, letting the user interactively navigate through them. These documents include local media, such as photos and video, and documents provided by installed cloud storage providers.

Each document is represented as a `content://` URI backed by a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#`, which can be opened as a stream with `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`, or queried for `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document.html#` metadata.

All selected documents are returned to the calling application with persistable read and write permission grants. If you want to maintain access to the documents across device reboots, you need to explicitly take the persistable permissions using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#takePersistableUriPermission(android.net.Uri,%20kotlin.Int)`.

Callers must indicate the acceptable document MIME types through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`. For example, to select photos, use `image/*`. If multiple disjoint MIME types are acceptable, define them in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)` to \*/\*.

If the caller can handle multiple returned items (the user performing multiple selection), then you can specify `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_MULTIPLE:kotlin.String` to indicate this.

Callers must include `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_OPENABLE:kotlin.String` in the Intent to obtain URIs that can be opened with `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`.

Callers can set a document URI through `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#EXTRA_INITIAL_URI:kotlin.String` to indicate the initial location of documents navigator. System will do its best to launch the navigator in the specified document if it's a folder, or the folder that contains the specified document if not.

Output: The URI of the item that was picked, returned in `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`. This must be a `content://` URI so that any receiver can access it. If multiple documents were selected, they are returned in `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT_TREE:kotlin.String`

Activity Action: Allow the user to pick a directory subtree. When invoked, the system will display the various `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#` instances installed on the device, letting the user navigate through them. Apps can fully manage documents within the returned directory.

To gain access to descendant (child, grandchild, etc) documents, use `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#buildDocumentUriUsingTree(android.net.Uri,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#buildChildDocumentsUriUsingTree(android.net.Uri,%20kotlin.String)` with the returned URI.

Callers can set a document URI through `https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#EXTRA_INITIAL_URI:kotlin.String` to indicate the initial location of documents navigator. System will do its best to launch the navigator in the specified document if it's a folder, or the folder that contains the specified document if not.

Output: The URI representing the selected directory tree.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_EYE_DROPPER:kotlin.String`

Activity Action: Launch an eye dropper. It allows the user to pick a pixel on the display. The color of the selected pixel is returned to the requesting activity as an activity result. Pixels from secure windows and protected buffers are blacked out.

Output: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_COLOR:kotlin.String` is the color of the selected pixel in ARGB format (0xFFRRGGBB).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGES_SUSPENDED:kotlin.String`

Broadcast Action: Packages have been suspended.

Includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` is the set of packages which have been suspended
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` is the set of uids which have been suspended

This is a protected intent that can only be sent by the system. It is only sent to registered receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGES_UNSUSPENDED:kotlin.String`

Broadcast Action: Packages have been unsuspended.

Includes the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String` is the set of packages which have been unsuspended
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String` is the set of uids which have been unsuspended

This is a protected intent that can only be sent by the system. It is only sent to registered receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_ADDED:kotlin.String`

Broadcast Action: A new application package has been installed on the device. The data contains the name of the package. Note that the newly installed package does *not* receive this broadcast.

May include the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the new package.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACING:kotlin.String` is set to true if this is following an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` broadcast for the same package.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_CHANGED:kotlin.String`

Broadcast Action: An existing application package has been changed (for example, a component has been enabled or disabled). The data contains the name of the package.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the package.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_COMPONENT_NAME_LIST:kotlin.String` containing the class name of the changed components (or the package name itself).
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DONT_KILL_APP:kotlin.String` containing boolean field to override the default action of restarting the application.

<br />

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_DATA_CLEARED:kotlin.String`

Broadcast Action: The user has cleared the data of a package. This should be preceded by `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_RESTARTED:kotlin.String`, after which all of its persistent data is erased and this broadcast sent. Note that the cleared package does *not* receive this broadcast. The data contains the name of the package.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the package. If the package whose data was cleared is an uninstalled instant app, then the UID will be -1. The platform keeps some meta-data associated with instant apps after they are uninstalled.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` containing the package name only if the cleared data was for an instant app.

<br />

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_FIRST_LAUNCH:kotlin.String`

Broadcast Action: Sent to the installer package of an application when that application is first launched (that is the first time it is moved out of the stopped state). The data contains the name of the package.

When the application is first launched, the application itself doesn't receive this broadcast.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_FULLY_REMOVED:kotlin.String`

Broadcast Action: An existing application package has been completely removed from the device. The data contains the name of the package. This is like `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String`, but only set when `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DATA_REMOVED:kotlin.String` is true and `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACING:kotlin.String` is false of that broadcast.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid previously assigned to the package.

<br />

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_INSTALL:kotlin.String`

Broadcast Action: Trigger the download and eventual installation of a package.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is the URI of the package file to download.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String`

Broadcast Action: Sent to the system package verifier when a package needs to be verified. The data contains the package URI.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String`

Broadcast Action: An existing application package has been removed from the device. The data contains the name of the package. The package that is being removed does *not* receive this Intent.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid previously assigned to the package.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DATA_REMOVED:kotlin.String` is set to true if the entire application -- data and code -- is being removed.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACING:kotlin.String` is set to true if this will be followed by an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_ADDED:kotlin.String` broadcast for the same package.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER_INITIATED:kotlin.String` containing boolean field to signal that the application was removed with the user-initiated action.

<br />

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REPLACED:kotlin.String`

Broadcast Action: A new version of an application package has been installed, replacing an existing version that was previously installed. The data contains the name of the package.

May include the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the new package.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_RESTARTED:kotlin.String`

Broadcast Action: The user has restarted a package, and all of its processes have been killed. All runtime state associated with it (processes, alarms, notifications, etc) should be removed. Note that the restarted package does *not* receive this broadcast. The data contains the name of the package.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the package.

<br />

This is a protected intent that can only be sent by the system.

Starting in Android V, an extra timestamp `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIME:kotlin.String` is included with this broadcast to indicate the exact time the package was restarted, in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_UNSTOPPED:kotlin.String`

Broadcast Action: An application package that was previously in the stopped state has been started and is no longer considered stopped.

When a package is force-stopped, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_RESTARTED:kotlin.String` broadcast is sent and the package in the stopped state cannot self-start for any reason unless there's an explicit request to start a component in the package. The `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_UNSTOPPED:kotlin.String` broadcast is sent when such an explicit process start occurs and the package is taken out of the stopped state. The data contains the name of the package.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String` containing the integer uid assigned to the package.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIME:kotlin.String` containing the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` of when the package was unstopped.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_VERIFIED:kotlin.String`

Broadcast Action: Sent to the system package verifier when a package is verified. The data contains the package URI.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PASTE:kotlin.String`

Activity Action: Create a new item in the given container, initializing it from the current contents of the clipboard.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of the directory (vnd.android.cursor.dir/\*) in which to place the data.

Output: URI of the new data that was created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK:kotlin.String`

Activity Action: Pick an item from the data, returning what was selected.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI containing a directory of data (vnd.android.cursor.dir/\*) from which to pick an item.

Output: The URI of the item that was picked.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK_ACTIVITY:kotlin.String`

Activity Action: Pick an activity given an intent, returning the class selected.

Input: get\*Extra field `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` is an Intent used with android.content.pm.PackageManager#queryIntentActivities to determine the set of activities from which to pick.

Output: Class name of the activity that was selected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_POWER_CONNECTED:kotlin.String`

Broadcast Action: External power has been connected to the device. This is intended for applications that wish to register specifically to this notification. Unlike ACTION_BATTERY_CHANGED, applications will be woken for this and so do not have to stay active to receive this notification. This action can be used to implement actions that wait until power is available to trigger.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_POWER_DISCONNECTED:kotlin.String`

Broadcast Action: External power has been removed from the device. This is intended for applications that wish to register specifically to this notification. Unlike ACTION_BATTERY_CHANGED, applications will be woken for this and so do not have to stay active to receive this notification. This action can be used to implement actions that wait until power is available to trigger.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_POWER_USAGE_SUMMARY:kotlin.String`

Activity Action: Show power usage information to the user.

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String`

Activity Action: Process a piece of text.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PROCESS_TEXT:kotlin.String` contains the text to be processed. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PROCESS_TEXT_READONLY:kotlin.String` states if the resulting text will be read-only.

Output: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PROCESS_TEXT:kotlin.String` contains the processed text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_ACCESSIBLE:kotlin.String`

Broadcast sent to the parent user when an associated profile has been started and unlocked. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_ADDED:kotlin.String`

Broadcast sent to the parent user when an associated profile is added (the profile was created and is ready to be used). Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile that was added.

This broadcast is similar to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_ADDED:kotlin.String` but functions as a generic broadcast for all profile users. It is sent in addition to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_ADDED:kotlin.String` broadcast when a managed user is added.

Only applications (for example Launchers) that need to display merged content across both the parent user and its associated profiles need to worry about this broadcast. This is only sent to registered receivers created with android.content.Context#registerReceiver. It is not sent to manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_AVAILABLE:kotlin.String`

Broadcast sent to the primary user when an associated profile has become available. This is sent when a user disables quiet mode for the profile. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. When quiet mode is changed, this broadcast will carry a boolean extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUIET_MODE:kotlin.String` indicating the new state of quiet mode. This is only sent to registered receivers, not manifest receivers.

This broadcast is similar to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_AVAILABLE:kotlin.String` but functions as a generic broadcast for all users of type `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isProfile()`}. In case of a managed profile, both `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_AVAILABLE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_AVAILABLE:kotlin.String` broadcasts are sent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_INACCESSIBLE:kotlin.String`

Broadcast sent to the parent user when an associated profile has stopped. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. This is only sent to registered receivers, not manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_REMOVED:kotlin.String`

Broadcast sent to the parent user when an associated profile is removed. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile that was removed.

This broadcast is similar to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_REMOVED:kotlin.String` but functions as a generic broadcast for all profile users. It is sent in addition to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_REMOVED:kotlin.String` broadcast when a managed user is removed.

Only applications (for example Launchers) that need to display merged content across both the parent user and its associated profiles need to worry about this broadcast. This is only sent to registered receivers created with android.content.Context#registerReceiver. It is not sent to manifest receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_UNAVAILABLE:kotlin.String`

Broadcast sent to the primary user when an associated profile has become unavailable. This is sent when a user enables quiet mode for the profile. Carries an extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String` that specifies the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` of the profile. When quiet mode is changed, this broadcast will carry a boolean extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUIET_MODE:kotlin.String` indicating the new state of quiet mode. This is only sent to registered receivers, not manifest receivers.

This broadcast is similar to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_UNAVAILABLE:kotlin.String` but functions as a generic broadcast for all users of type `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isProfile()`}. In case of a managed profile, both `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MANAGED_PROFILE_UNAVAILABLE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROFILE_UNAVAILABLE:kotlin.String` broadcasts are sent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROVIDER_CHANGED:kotlin.String`

Broadcast Action: Some content providers have parts of their namespace where they publish new events or items that the user may be especially interested in. For these things, they may broadcast this action when the set of interesting items change. For example, GmailProvider sends this notification when the set of unread mail in the inbox changes.

The data of the intent identifies which part of which provider changed. When queried through the content resolver, the data URI will return the data set in question.

The intent will have the following extra values:

- *count* - The number of items in the data set. This is the same as the number of items in the cursor returned by querying the data URI.

This intent will be sent at boot (if the count is non-zero) and when the data set changes. It is possible for the data set to change without the count changing (for example, if a new unread message arrives in the same sync operation in which a message is archived). The phone should still ring/vibrate/etc as normal in this case.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_QUICK_CLOCK:kotlin.String`

Sent when the user taps on the clock widget in the system's "quick settings" area.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_QUICK_VIEW:kotlin.String`

Activity Action: Quick view the data. Launches a quick viewer for a URI or a list of URIs.

Activities handling this intent action should handle the vast majority of MIME types rather than only specific ones.

Quick viewers must render the quick view image locally, and must not send file content outside current device.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is a mandatory content URI of the item to preview. `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` contains an optional list of content URIs if there is more than one item to preview. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INDEX:kotlin.String` is an optional index of the URI in the clip data to show first. `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUICK_VIEW_FEATURES:kotlin.String` is an optional extra indicating the features that can be shown in the quick view UI.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_REBOOT:kotlin.String`

Broadcast Action: Have the device reboot. This is only for use by system code.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_RUN:kotlin.String`

Activity Action: Run the data, whatever that means.

Input: ? (Note: this is currently specific to the test harness.)

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SAFETY_CENTER:kotlin.String`

Activity action: Launch UI to open the Safety Center, which highlights the user's security and privacy status.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_OFF:kotlin.String`

Broadcast Action: Sent when the device goes to sleep and becomes non-interactive.

For historical reasons, the name of this broadcast action refers to the power state of the screen but it is actually sent in response to changes in the overall interactive state of the device.

This broadcast is sent when the device becomes non-interactive which may have nothing to do with the screen turning off. To determine the actual state of the screen, use `https://developer.android.com/reference/kotlin/android/view/Display.html#getState()`.

See `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#isInteractive()` for details.
You *cannot* receive this through components declared in manifests, only by explicitly registering for it with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SCREEN_ON:kotlin.String`

Broadcast Action: Sent when the device wakes up and becomes interactive.

For historical reasons, the name of this broadcast action refers to the power state of the screen but it is actually sent in response to changes in the overall interactive state of the device.

This broadcast is sent when the device becomes interactive which may have nothing to do with the screen turning on. To determine the actual state of the screen, use `https://developer.android.com/reference/kotlin/android/view/Display.html#getState()`.

See `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#isInteractive()` for details.
You *cannot* receive this through components declared in manifests, only by explicitly registering for it with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEARCH:kotlin.String`

Activity Action: Perform a search.

Input: `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` is the text to search for. If empty, simply enter your search results Activity with the search UI activated.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEARCH_LONG_PRESS:kotlin.String`

Activity Action: Start action associated with long pressing on the search key.

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String`

Activity Action: Deliver some data to someone else. Who the data is being delivered to is not specified; it is up to the receiver of this action to ask the user where the data should be sent.

When launching a SEND intent, you should usually wrap it in a chooser (through #createChooser), which will give the proper interface for the user to pick how to send your data and allow you to specify a prompt indicating what they are doing.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getType()` is the MIME type of the data being sent. get\*Extra can have either a `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` field, containing the data to be sent. If using EXTRA_TEXT, the MIME type should be "text/plain"; otherwise it should be the MIME type of the data in EXTRA_STREAM. Use \*/\* if the MIME type is unknown (this will only allow senders that can handle generic data streams). If using `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String`, you can also optionally supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_HTML_TEXT:kotlin.String` for clients to retrieve your text with HTML formatting.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int`, the data being sent can be supplied through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. This allows you to use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` when sharing content: URIs and other advanced features of `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`. If using this approach, you still must supply the same data through the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` fields described below for compatibility with old applications. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, if `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_TYPED_OPENABLE:kotlin.String` is passed, then the Uris passed in either `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` or via `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)` may be openable only as asset typed files using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle)`.

Optional standard extras, which may be interpreted by some recipients as appropriate, are: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EMAIL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_BCC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUBJECT:kotlin.String`.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SENDTO:kotlin.String`

Activity Action: Send a message to someone specified by the data.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI describing the target.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND_MULTIPLE:kotlin.String`

Activity Action: Deliver multiple data to someone else.

Like `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String`, except the data is multiple.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getType()` is the MIME type of the data being sent. get\*ArrayListExtra can have either a `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` field, containing the data to be sent. If using `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String`, you can also optionally supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_HTML_TEXT:kotlin.String` for clients to retrieve your text with HTML formatting.

Multiple types are supported, and receivers should handle mixed types whenever possible. The right way for the receiver to check them is to use the content resolver on each URI. The intent sender should try to put the most concrete mime type in the intent type, but it can fall back to \<type\>/\* or \*/\* as needed.

e.g. if you are sending image/jpg and image/jpg, the intent's type can be image/jpg, but if you are sending image/jpg and image/png, then the intent's type should be image/\*.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int`, the data being sent can be supplied through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. This allows you to use `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` when sharing content: URIs and other advanced features of `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`. If using this approach, you still must supply the same data through the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` fields described below for compatibility with old applications. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, if `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_TYPED_OPENABLE:kotlin.String` is passed, then the Uris passed in either `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` or via `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)` may be openable only as asset typed files using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle)`.

Optional standard extras, which may be interpreted by some recipients as appropriate, are: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EMAIL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_BCC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUBJECT:kotlin.String`.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SET_WALLPAPER:kotlin.String`

Activity Action: Show settings for choosing wallpaper.

Input: Nothing.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SHOW_APP_INFO:kotlin.String`

Activity Action: Launch an activity showing the app information. For applications which install other applications (such as app stores), it is recommended to handle this action for providing the app information to the user.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` specifies the package whose information needs to be displayed.

Output: Nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SHOW_WORK_APPS:kotlin.String`

Activity Action: Action to show the list of all work apps in the launcher. For example, shows the work apps folder or tab.

Input: Nothing.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SHUTDOWN:kotlin.String`

Broadcast Action: This is broadcast when the user is being shut down. Once the broadcast is complete, the final shutdown will proceed and all unsaved data lost. Apps will not normally need to handle this, since the foreground activity will be paused as well.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` this broadcast is only sent to receivers registered through `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`.

This is a protected intent that can only be sent by the system.

May include the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHUTDOWN_USERSPACE_ONLY:kotlin.String` a boolean that is set to true if this shutdown is only for userspace processes. If not set, assumed to be false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_STOP_VOICE_COMMAND:kotlin.String`

Broadcast Action: Stop Voice Command.

The intent will have the following extra values.

- *`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String`* indicates the BluetoothDevice which initiated this request.
- *`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String`* indicates the profile (e.g., `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#HEADSET:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#LE_AUDIO:kotlin.Int`) which triggered this request.

Additionally, if the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#HEADSET:kotlin.Int`, the app should call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset.html#stopVoiceRecognition(android.bluetooth.BluetoothDevice)` to stop voice assistant session. If the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#LE_AUDIO:kotlin.Int`, the app should call `https://developer.android.com/reference/kotlin/android/media/AudioRecord.html#stop()` to stop voice assistant session.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SYNC:kotlin.String`

Activity Action: Perform a data synchronization.

Input: ?

Output: ?

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SYSTEM_TUTORIAL:kotlin.String`

Activity Action: Start the platform-defined tutorial

Input: `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` is the text to search for. If empty, simply enter your search results Activity with the search UI activated.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_CHANGED:kotlin.String`

Broadcast Action: The timezone has changed. The intent will have the following extra values:

<br />

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIMEZONE:kotlin.String` - The java.util.TimeZone.getID() value identifying the new time zone.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_OFFSET_CHANGED:kotlin.String`

Broadcast Action: Indicates that the system's time zone offset has changed without the time zone having changed. This happens for example during seasonal clock changes, or when a region changes offset.

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_OLD_TIMEZONE_OFFSET:kotlin.String` - The old time zone offset in seconds.
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_NEW_TIMEZONE_OFFSET:kotlin.String` - The new time zone offset in seconds.

<br />

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIME_CHANGED:kotlin.String`

Broadcast Action: The time was set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIME_TICK:kotlin.String`

Broadcast Action: The current time has changed. Sent every minute. You *cannot* receive this through components declared in manifests, only by explicitly registering for it with `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TRANSLATE:kotlin.String`

Activity Action: Perform text translation.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` is the text to translate.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UID_REMOVED:kotlin.String`

Broadcast Action: A uid has been removed from the system. The uid number is stored in the extra data under `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String`. In certain instances, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACING:kotlin.String` is set to true if the UID is not being fully removed.

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UMS_CONNECTED:kotlin.String`

Broadcast Action: The device has entered USB Mass Storage mode. This is used mainly for the USB Settings panel. Apps should listen for ACTION_MEDIA_MOUNTED and ACTION_MEDIA_UNMOUNTED broadcasts to be notified when the SD card file system is mounted or unmounted

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UMS_DISCONNECTED:kotlin.String`

Broadcast Action: The device has exited USB Mass Storage mode. This is used mainly for the USB Settings panel. Apps should listen for ACTION_MEDIA_MOUNTED and ACTION_MEDIA_UNMOUNTED broadcasts to be notified when the SD card file system is mounted or unmounted

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNARCHIVE_PACKAGE:kotlin.String`

Broadcast Action: Sent to the responsible installer of an archived package when unarchival is requested.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNINSTALL_PACKAGE:kotlin.String`

Activity Action: Launch application uninstaller.

Input: The data must be a package: URI whose scheme specific part is the package name of the current installed package to be uninstalled. You can optionally supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RETURN_RESULT:kotlin.String`.

Output: If `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RETURN_RESULT:kotlin.String`, returns whether the uninstall succeeded.

Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_DELETE_PACKAGES:kotlin.String` since `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_BACKGROUND:kotlin.String`

Sent after a user switch is complete, if the switch caused the process's user to be sent to the background. This is only sent to receivers registered through `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. It is sent to the user that is going to the background. This is sent as a foreground broadcast, since it is part of a visible user interaction; be as quick as possible when handling it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_FOREGROUND:kotlin.String`

Sent after a user switch is complete, if the switch caused the process's user to be brought to the foreground. This is only sent to receivers registered through `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. It is sent to the user that is going to the foreground. This is sent as a foreground broadcast, since it is part of a visible user interaction; be as quick as possible when handling it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_INITIALIZE:kotlin.String`

Sent the first time a user is starting, to allow system apps to perform one time initialization. (This will not be seen by third party applications because a newly initialized user does not have any third party applications installed for it.) This is sent early in starting the user, around the time the home app is started, before `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BOOT_COMPLETED:kotlin.String` is sent. This is sent as a foreground broadcast, since it is part of a visible user interaction; be as quick as possible when handling it.

**Note:** This broadcast is not sent to the system user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_PRESENT:kotlin.String`

Broadcast Action: Sent when the user is present after device wakes up (e.g when the keyguard is gone).

This is a protected intent that can only be sent by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_USER_UNLOCKED:kotlin.String`

Broadcast Action: Sent when the credential-encrypted private storage has become unlocked for the target user. This is only sent to registered receivers, not manifest receivers.

**Note:** The user's actual state might have changed by the time the broadcast is received. For example, the user could have been removed, started or stopped already, regardless of which broadcast you receive. Because of that, receivers should always check the current state of the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`

Activity Action: Display the data to the user. This is the most common action performed on data -- it is the generic action you can use on a piece of data to get the most reasonable thing to occur. For example, when used on a contacts entry it will view the entry; when used on a mailto: URI it will bring up a compose window filled with the information supplied by the URI; when used with a tel: URI it will invoke the dialer.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI from which to retrieve data.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_LOCUS:kotlin.String`

Activity Action: Display an activity state associated with an unique `https://developer.android.com/reference/kotlin/android/content/LocusId.html#`.

For example, a chat app could use the context to resume a conversation between 2 users.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCUS_ID:kotlin.String` specifies the unique identifier of the locus in the app domain. Should be stable across reboots and backup / restore.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE:kotlin.String`

Activity action: Launch UI to show information about the usage of a given permission group. This action would be handled by apps that want to show details about how and why given permission group is being used.

**Important:** You must protect the activity that handles this action with the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#START_VIEW_PERMISSION_USAGE:kotlin.String` permission to ensure that only the system can launch this activity. The system will not launch activities that are not properly protected.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PERMISSION_GROUP_NAME:kotlin.String` specifies the permission group for which the launched UI would be targeted.

Output: Nothing.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#START_VIEW_PERMISSION_USAGE:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE_FOR_PERIOD:kotlin.String`

Activity action: Launch UI to show information about the usage of a given permission group in a given period. This action would be handled by apps that want to show details about how and why given permission group is being used.

**Important:** You must protect the activity that handles this action with the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#START_VIEW_PERMISSION_USAGE:kotlin.String` permission to ensure that only the system can launch this activity. The system will not launch activities that are not properly protected.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PERMISSION_GROUP_NAME:kotlin.String` specifies the permission group for which the launched UI would be targeted.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ATTRIBUTION_TAGS:kotlin.String` specifies the attribution tags for the usage entry.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_START_TIME:kotlin.String` specifies the start time of the period (epoch time in millis). Both start time and end time are needed and start time must be \<= end time.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_END_TIME:kotlin.String` specifies the end time of the period (epoch time in millis). Both start time and end time are needed and start time must be \<= end time.

Output: Nothing.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#START_VIEW_PERMISSION_USAGE:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VOICE_COMMAND:kotlin.String`

Activity Action: Start Voice Command.

For apps targeting or running on devices with SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` or lower, the extras `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` are not included as part of the intent. For apps targeting versions higher than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, the extras `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` are included as part of the intent.

Information about the extras is below.

- *`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String`* indicates the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` which initiated this request.
- *`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String`* indicates the profile (e.g., `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#HEADSET:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#LE_AUDIO:kotlin.Int`) which triggered this request.

Additionally, if the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#HEADSET:kotlin.Int`, the app should call the following APIs to start voice assistant session.

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset.html#startVoiceRecognition(android.bluetooth.BluetoothDevice)`
- android.media.AudioRecord#setPreferredDevice() for the `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo.html#TYPE_BLUETOOTH_SCO:kotlin.Int` device whose MAC address matches the address received in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioRecord.html#startRecording()`

If the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#EXTRA_PROFILE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.html#LE_AUDIO:kotlin.Int`, the app should call the following APIs to start voice assistant session.

- android.media.AudioRecord#setPreferredDevice() for the `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo.html#TYPE_BLE_HEADSET:kotlin.Int` device whose MAC address matches the address received in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#EXTRA_DEVICE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioRecord.html#startRecording()`

Output: Nothing.

In some cases, a matching Activity may not exist, so ensure you safeguard against this.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String`

Broadcast Action: The current system wallpaper has changed. See `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#` for retrieving the new wallpaper. This should *only* be used to determine when the wallpaper has changed to show the new wallpaper to the user. You should certainly never, in response to this, change the wallpaper or other attributes of it such as the suggested size. That would be unexpected, right? You'd cause all kinds of loops, especially if other apps are doing similar things, right? Of course. So please don't do this.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String`

Activity Action: Perform a web search.

Input: `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` is the text to search for. If it is a url starts with http or https, the site will be opened. If it is plain text, Google search will be applied.

Output: nothing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_BLOCKED_BY_ADMIN:kotlin.Int`

A response code used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` to indicate that screenshot is blocked by IT admin.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_FAILED:kotlin.Int`

A response code used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` to indicate that something went wrong.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_SUCCESS:kotlin.Int`

A response code used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` to indicate that the request was a success.

This code will only be returned after the user has interacted with the system screenshot activity to consent to sharing the data with the note.

The captured screenshot is returned as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` through `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_USER_CANCELED:kotlin.Int`

A response code used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` to indicate that user canceled the content capture flow.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_WINDOW_MODE_UNSUPPORTED:kotlin.Int`

A response code used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String` to indicate that the intent action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String` was started by an activity that is running in a non-supported window mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_ACCESSIBILITY_SHORTCUT_TARGET:kotlin.String`

The accessibility shortcut is a global gesture for users with disabilities to trigger an important for them accessibility feature to help developers determine whether they want to make their activity a shortcut target.

An activity of interest to users with accessibility needs may request to be the target of the accessibility shortcut. It handles intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` with this category, which will be dispatched by the system when the user activates the shortcut when it is configured to point at this target.

An activity declared itself to be a target of the shortcut in AndroidManifest.xml. It must also do two things:

Specify that it handles the `android.intent.action.MAIN` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` with category `android.intent.category.ACCESSIBILITY_SHORTCUT_TARGET`.
<!-- -->

Provide a meta-data entry `android.accessibilityshortcut.target` in the manifest when declaring the activity.

If either of these items is missing, the system will ignore the accessibility shortcut target. Following is an example declaration:

<br />

```kotlin
<activity android:name=".MainActivity"
  . . .
    <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.ACCESSIBILITY_SHORTCUT_TARGET" />
    </intent-filter>
    <meta-data android:name="android.accessibilityshortcut.target"
                    android:resource="@xml/accessibilityshortcut" />
  </activity>
  
```

This is a sample XML file configuring a accessibility shortcut target:

```kotlin
<accessibility-shortcut-target
      android:description="@string/shortcut_target_description"
      android:summary="@string/shortcut_target_summary"
      android:animatedImageDrawable="@drawable/shortcut_target_animated_image"
      android:htmlDescription="@string/shortcut_target_html_description"
      android:settingsActivity="com.example.android.shortcut.target.SettingsActivity" />
  
```

Both description and summary are necessary. The system will ignore the accessibility shortcut target if they are missing. The animated image and html description are supported to help users understand how to use the shortcut target. The settings activity is a component name that allows the user to modify the settings for this accessibility shortcut target.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_ALTERNATIVE:kotlin.String`

Set if the activity should be considered as an alternative action to the data the user is currently viewing. See also `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SELECTED_ALTERNATIVE:kotlin.String` for an alternative action that applies to the selection in a list of items.

Supporting this category means that you would like your activity to be displayed in the set of alternative things the user can do, usually as part of the current activity's options menu. You will usually want to include a specific label in the \<intent-filter\> of this action describing to the user what it does.

The action of IntentFilter with this category is important in that it describes the specific action the target will perform. This generally should not be a generic action (such as `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`, but rather a specific name such as "com.android.camera.action.CROP. Only one alternative of any particular action will be shown to the user, so using a specific action like this makes sure that your alternative will be displayed while also allowing other applications to provide their own overrides of that particular action.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_BROWSER:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the browser application. The activity should be able to browse the Internet.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_CALCULATOR:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the calculator application. The activity should be able to perform standard arithmetic operations.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_CALENDAR:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the calendar application. The activity should be able to view and manipulate calendar entries.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_CONTACTS:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the contacts application. The activity should be able to view and manipulate address book entries.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_EMAIL:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the email application. The activity should be able to send and receive email.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_FILES:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the files application. The activity should be able to browse and manage files stored on the device.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_FITNESS:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the fitness application. The activity should be able to give the user fitness information and manage workouts

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_GALLERY:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the gallery application. The activity should be able to view and manipulate image and video files stored on the device.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MAPS:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the maps application. The activity should be able to show the user's current location and surroundings.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MARKET:kotlin.String`

This activity allows the user to browse and download new applications.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MESSAGING:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the messaging application. The activity should be able to send and receive text messages.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MUSIC:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the music application. The activity should be able to play, browse, or manipulate music files stored on the device.

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_WEATHER:kotlin.String`

Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch the weather application. The activity should be able to give the user information about the weather

NOTE: This should not be used as the primary key of an Intent, since it will not result in the app launching with the correct action and category. Instead, use this with `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)` to generate a main Intent with this category in the selector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_BROWSABLE:kotlin.String`

Activities that can be safely invoked from a browser must support this category. For example, if the user is viewing a web page or an e-mail and clicks on a link in the text, the Intent generated to execute that link will require the BROWSABLE category, so that only activities supporting this category will be considered as possible actions. By supporting this category, you are promising that there is nothing damaging (without user intervention) that can happen by invoking any matching Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_CAR_DOCK:kotlin.String`

An activity to run when device is inserted into a car dock. Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch an activity. For more information, see `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_CAR_MODE:kotlin.String`

Used to indicate that the activity can be used in a car environment.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`

Set if the activity should be an option for the default action (center press) to perform on a piece of data. Setting this will hide from the user any activities without it set when performing an action on some data. Note that this is normally -not- set in the Intent when initiating an action -- it is for use in intent filters specified in packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DESK_DOCK:kotlin.String`

An activity to run when device is inserted into a desk dock. Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch an activity. For more information, see `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEVELOPMENT_PREFERENCE:kotlin.String`

This activity is a development preference panel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_EMBED:kotlin.String`

Capable of running inside a parent activity container.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_FRAMEWORK_INSTRUMENTATION_TEST:kotlin.String`

To be used as code under test for framework instrumentation tests.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HE_DESK_DOCK:kotlin.String`

An activity to run when device is inserted into a digital (high end) dock. Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch an activity. For more information, see `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`

This is the home activity, that is the first activity that is displayed when the device boots.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_INFO:kotlin.String`

Provides information about the package it is in; typically used if a package does not contain a `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String` to provide a front-door to the user without having to be shown in the all apps list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`

Should be displayed in the top-level launcher.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LEANBACK_LAUNCHER:kotlin.String`

Indicates an activity optimized for Leanback mode, and that should be displayed in the Leanback launcher.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LE_DESK_DOCK:kotlin.String`

An activity to run when device is inserted into a analog (low end) dock. Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch an activity. For more information, see `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_MONKEY:kotlin.String`

This activity may be exercised by the monkey or other automated test tools.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_OPENABLE:kotlin.String`

Used to indicate that an intent only wants URIs that can be opened with `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`. Openable URIs must support at least the columns defined in `https://developer.android.com/reference/kotlin/android/provider/OpenableColumns.html#` when queried.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_PREFERENCE:kotlin.String`

This activity is a preference panel.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SAMPLE_CODE:kotlin.String`

To be used as a sample code example (not part of the normal user experience).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SECONDARY_HOME:kotlin.String`

The home activity shown on secondary displays that support showing home activities.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SELECTED_ALTERNATIVE:kotlin.String`

Set if the activity should be considered as an alternative selection action to the data the user has currently selected. This is like `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_ALTERNATIVE:kotlin.String`, but is used in activities showing a list of items from which the user can select, giving them alternatives to the default action that will be performed on it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_TAB:kotlin.String`

Intended to be used as a tab inside of a containing TabActivity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_TEST:kotlin.String`

To be used as a test (not part of the normal user experience).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_TYPED_OPENABLE:kotlin.String`

Used to indicate that an intent filter can accept files which are not necessarily openable by `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`, but at least streamable via `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle)` using one of the stream types exposed via `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#getStreamTypes(android.net.Uri,%20kotlin.String)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_UNIT_TEST:kotlin.String`

To be used as a unit test (run through the Test Harness).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_VOICE:kotlin.String`

Categories for activities that can participate in voice interaction. An activity that supports this category must be prepared to run with no UI shown at all (though in some case it may have a UI shown), and rely on `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#` to interact with the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_VR_HOME:kotlin.String`

An activity to use for the launcher when the device is placed in a VR Headset viewer. Used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` to launch an activity. For more information, see `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CHOOSER_CONTENT_TYPE_ALBUM:kotlin.Int`

Indicates that the content being shared with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` represents an album (e.g. containing photos).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String`

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` pending intents to tell the application being invoked how many pending alarms are being delivered with the intent. For one-shot alarms this will always be 1. For recurring alarms, this might be greater than 1 if the device was asleep or powered off at the time an earlier alarm would have been delivered.

Note: You must supply a **mutable** `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to `AlarmManager` while setting your alarms to be able to read this value on receiving them. *Mutability of pending intents must be explicitly specified by apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher*.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_MULTIPLE:kotlin.String`

Extra used to indicate that an intent can allow the user to select and return multiple items. This is a boolean extra; the default is false. If true, an implementation is allowed to present the user with a UI where they can pick multiple items that are all returned to the caller. When this happens, they should be returned as the `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` part of the result Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALLOW_REPLACE:kotlin.String`

Used as a boolean extra field with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String` to install a package. Tells the installer UI to skip the confirmation with the user if the .apk is replacing an existing one.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String`

An Intent\[\] describing additional, alternate choices you would like shown with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

An app may be capable of providing several different payload types to complete a user's intended action. For example, an app invoking `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` to share photos with another app may use EXTRA_ALTERNATE_INTENTS to have the chooser transparently offer several different supported sending mechanisms for sharing, such as the actual "image/\*" photo data or a hosted link where the photos can be viewed.

The intent present in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` will be treated as the first/primary/preferred intent in the set. Additional intents specified in this extra are ordered; by default intents that appear earlier in the array will be preferred over intents that appear later in the array as matches for the same target component. To alter this preference, a calling app may also supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ARCHIVAL:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_ADDED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` intents to indicate that the package is being archived. Either by removing the existing APK, or by installing a package without an APK.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_CONTEXT:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` and containing additional contextual information supplied by the current foreground app at the time of the assist request. This is a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of additional data.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_DISPLAY_ID:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` containing the display id that should be used to invoke the assist. If not set, invoke the assist on the default display is suggested.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_INPUT_DEVICE_ID:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` containing the InputDevice id that was used to invoke the assist.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_INPUT_HINT_KEYBOARD:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` suggesting that the user will likely use a keyboard as the primary input device for assistance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_PACKAGE:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` containing the name of the current foreground application package at the time the assist was invoked.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_UID:kotlin.String`

An optional field on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String` containing the uid of the current foreground application package at the time the assist was invoked.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ATTRIBUTION_TAGS:kotlin.String`

A String\[\] holding attribution tags when used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE_FOR_PERIOD:kotlin.String` and ACTION_MANAGE_PERMISSION_USAGE E.g. an attribution tag could be location_provider, com.google.android.gms.\*, etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_AUTO_LAUNCH_SINGLE_CHOICE:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` intents to specify whether to show the chooser or not when there is only one application available to choose from.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_BCC:kotlin.String`

A String\[\] holding e-mail addresses that should be blind carbon copied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_BUG_REPORT:kotlin.String`

Used as a parcelable extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APP_ERROR:kotlin.String`, containing the bug report.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CAPTURE_CONTENT_FOR_NOTE_STATUS_CODE:kotlin.String`

An int extra used by activity started with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LAUNCH_CAPTURE_CONTENT_ACTIVITY_FOR_NOTE:kotlin.String` to indicate status of the response. This extra is used along with result code set to `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`.

The value for this extra can be one of the following:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_SUCCESS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_FAILED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_USER_CANCELED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_WINDOW_MODE_UNSUPPORTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CAPTURE_CONTENT_FOR_NOTE_BLOCKED_BY_ADMIN:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CC:kotlin.String`

A String\[\] holding e-mail addresses that should be carbon copied.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_COMPONENT_NAME:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_COMPONENT_NAME_LIST:kotlin.String`

This field is part of `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_CHANGED:kotlin.String`, and contains a string array of all of the components that have changed. If the state of the overall package has changed, then it will contain an entry with the package name itself.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_PACKAGE_LIST:kotlin.String`

This field is part of `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_AVAILABLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_UNAVAILABLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGES_SUSPENDED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGES_UNSUSPENDED:kotlin.String` and contains a string array of all of the components that have changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHANGED_UID_LIST:kotlin.String`

This field is part of `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_AVAILABLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_EXTERNAL_APPLICATIONS_UNAVAILABLE:kotlin.String` and contains an integer array of uids of all of the components that have changed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI:kotlin.String`

Optional argument used to provide a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#``https://developer.android.com/reference/kotlin/android/net/Uri.html#` to an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent which allows additional toggleable items to be included in the sharing UI.

For example, this could be used to show photos being shared in the context of the user's entire photo roll, with the option to change the set of photos being shared.

When this is provided in an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND_MULTIPLE:kotlin.String` target Intent, the sharesheet will query (see `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`) this URI to retrieve a set of additional items available for selection. The set of items returned by the content provider is expected to contain all the items from the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` argument, in their relative order, which will be marked as selected. The URI's authority must be different from any shared items URI provided in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` or returned by the provider.

The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` argument of the `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)` method will contains the original intent Chooser has been launched with under the `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` key as a context for the current sharing session. The returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` should contain:

- `https://developer.android.com/reference/kotlin/android/service/chooser/AdditionalContentContract.Columns.html#URI:kotlin.String` column for the item URI.
- Optional columns `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns.html#HEIGHT:kotlin.String` for the dimensions of the preview image. These columns can also be returned for each `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` item metadata `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)` call.
- Optional `https://developer.android.com/reference/kotlin/android/service/chooser/AdditionalContentContract.CursorExtraKeys.html#POSITION:kotlin.String` extra that specifies the cursor starting position; the item at this position is expected to match the item specified by `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_FOCUSED_ITEM_POSITION:kotlin.String`.

<br />

When the user makes a selection change, `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#call(kotlin.String,%20kotlin.String,%20android.os.Bundle)` method will be invoked with the "method" argument set to `https://developer.android.com/reference/kotlin/android/service/chooser/AdditionalContentContract.MethodNames.html#ON_SELECTION_CHANGED:kotlin.String`, the "arg" argument set to this argument's value, and the "extras" `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` argument containing `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` key containing the original intent Chooser has been launched with but with the modified target intent --Chooser will modify the target intent according to the selection changes made by the user. Applications may implement this method to change any of the following Chooser arguments by returning new values in the result bundle: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_TARGETS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_CUSTOM_ACTIONS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_MODIFY_SHARE_ACTION:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_METADATA_TEXT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT_INTENT_SENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EXCLUDE_COMPONENTS:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_CONTENT_TYPE_HINT:kotlin.String`

Optional integer extra to be used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` to describe conteng being shared.

If provided, sharesheets may customize their UI presentation to include a more precise description of the content being shared.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_CUSTOM_ACTIONS:kotlin.String`

A Parcelable\[\] of `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserAction.html#` objects to provide the Android Sharesheet with app-specific actions to be presented to the user when invoking `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`. You can provide as many as five custom actions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_FOCUSED_ITEM_POSITION:kotlin.String`

Optional argument to be used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI:kotlin.String`, used in combination with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI:kotlin.String`. An integer, zero-based index into `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String` argument indicating the item that should be focused by the Chooser in preview.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_MODIFY_SHARE_ACTION:kotlin.String`

Optional argument to be used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`. A `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserAction.html#` to allow the user to modify what is being shared in some way. This may be integrated into the content preview on sharesheets that have a preview UI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String`

An `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` for an Activity that will be invoked when the user makes a selection from the chooser activity presented by `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

An app preparing an action for another app to complete may wish to allow the user to disambiguate between several options for completing the action based on the chosen target or otherwise refine the action before it is invoked.

When sent, this IntentSender may be filled in with the following extras:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` The first intent that matched the user's chosen target
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String` Any additional intents that also matched the user's chosen target beyond the first
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESULT_RECEIVER:kotlin.String` A `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` that the refinement activity should fill in and send once the disambiguation is complete

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT:kotlin.String`

A `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserResult.html#` which describes how the sharing session completed.

An instance is supplied to the optional IntentSender provided to `https://developer.android.com/reference/kotlin/android/content/Intent.html#createChooser(android.content.Intent,%20kotlin.CharSequence,%20android.content.IntentSender)` when the session completes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT_INTENT_SENDER:kotlin.String`

An `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that will be notified when a user successfully chooses a target component or initiates an action such as copy or edit within an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` activity. The IntentSender will have the extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT:kotlin.String` describing the result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_TARGETS:kotlin.String`

A `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget.html#` for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` describing additional high-priority deep-link targets for the chooser to present to the user.

Targets provided in this way will be presented inline with all other targets provided by services from other apps. They will be prioritized before other service targets, but after those targets provided by sources that the user has manually pinned to the front. You can provide up to two targets on this extra (the limit of two targets starts in Android 10).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOSEN_COMPONENT:kotlin.String`

The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` chosen by the user to complete an action.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOSEN_COMPONENT_INTENT_SENDER:kotlin.String`

An `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that will be notified if a user successfully chooses a target component to handle an action in an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` activity. The IntentSender will have the extra `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOSEN_COMPONENT:kotlin.String` appended to it containing the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the chosen component.

In some situations this callback may never come, for example if the user abandons the chooser, switches to another task or any number of other reasons. Apps should not be written assuming that this callback will always occur.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_COLOR:kotlin.String`

An int extra to hold a color in ARGB format (0xAARRGGBB).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_COMPONENT_NAME:kotlin.String`

Intent extra: A `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` value.

Type: String

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CONTENT_ANNOTATIONS:kotlin.String`

An `ArrayList` of `String` annotations describing content for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CONTENT_ANNOTATIONS:kotlin.String` is present in an intent used to start a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` activity, the first three annotations will be used to rank apps.

Annotations should describe the major components or topics of the content. It is up to apps initiating `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` to learn and add annotations. Annotations should be learned in advance, e.g., when creating or saving content, to avoid increasing latency to start `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`. Names of customized annotations should not contain the colon character. Performance on customized annotations can suffer, if they are rarely used for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` in the past 14 days. Therefore, it is recommended to use the following annotations when applicable.

- "product" represents that the topic of the content is mainly about products, e.g., health \& beauty, and office supplies.
- "emotion" represents that the topic of the content is mainly about emotions, e.g., happy, and sad.
- "person" represents that the topic of the content is mainly about persons, e.g., face, finger, standing, and walking.
- "child" represents that the topic of the content is mainly about children, e.g., child, and baby.
- "selfie" represents that the topic of the content is mainly about selfies.
- "crowd" represents that the topic of the content is mainly about crowds.
- "party" represents that the topic of the content is mainly about parties.
- "animal" represent that the topic of the content is mainly about animals.
- "plant" represents that the topic of the content is mainly about plants, e.g., flowers.
- "vacation" represents that the topic of the content is mainly about vacations.
- "fashion" represents that the topic of the content is mainly about fashion, e.g. sunglasses, jewelry, handbags and clothing.
- "material" represents that the topic of the content is mainly about materials, e.g., paper, and silk.
- "vehicle" represents that the topic of the content is mainly about vehicles, like cars, and boats.
- "document" represents that the topic of the content is mainly about documents, e.g. posters.
- "design" represents that the topic of the content is mainly about design, e.g. arts and designs of houses.
- "holiday" represents that the topic of the content is mainly about holidays, e.g., Christmas and Thanksgiving.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CONTENT_QUERY:kotlin.String`

Optional CharSequence extra to provide a search query. The format of this query is dependent on the receiving application.

Applicable to `https://developer.android.com/reference/kotlin/android/content/Intent.html#` with actions:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_CONTENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DATA_REMOVED:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` intents to indicate whether this represents a full uninstall (removing both the code and its data) or a partial uninstall (leaving its data, implying that this is an update).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String`

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_DOCK_EVENT:kotlin.String` intents to request the dock state. Possible values are `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_UNDOCKED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_DESK:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_CAR:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_LE_DESK:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_HE_DESK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_CAR:kotlin.Int`

Used as an int value for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String` to represent that the phone is in a car dock.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_DESK:kotlin.Int`

Used as an int value for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String` to represent that the phone is in a desk dock.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_HE_DESK:kotlin.Int`

Used as an int value for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String` to represent that the phone is in a digital (high end) dock.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_LE_DESK:kotlin.Int`

Used as an int value for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String` to represent that the phone is in a analog (low end) dock.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE_UNDOCKED:kotlin.Int`

Used as an int value for `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DOCK_STATE:kotlin.String` to represent that the phone is not in any dock.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DONT_KILL_APP:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_CHANGED:kotlin.String` intents to override the default action of restarting the application.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_DURATION_MILLIS:kotlin.String`

Intent extra: The number of milliseconds.

Type: long

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EMAIL:kotlin.String`

A String\[\] holding e-mail addresses that should be delivered to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_END_TIME:kotlin.String`

A long representing the end timestamp (epoch time in millis) of the permission usage when used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE_FOR_PERIOD:kotlin.String` and ACTION_MANAGE_PERMISSION_USAGE

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EXCLUDE_COMPONENTS:kotlin.String`

A `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` describing components that should be filtered out and omitted from a list of components presented to the user.

When used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`, the chooser will omit any of the components in this array if it otherwise would have shown them. Useful for omitting specific targets from your own package or other apps from your organization if the idea of sending to those targets would be redundant with other app functionality. Filtered components will not be able to present targets from an associated `ChooserTargetService`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_FROM_STORAGE:kotlin.String`

Extra that can be included on activity intents coming from the storage UI when it launches sub-activities to manage various types of storage. For example, it may use `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String` with a "image/\*" MIME type to have an app show the images on the device, and in that case also include this extra to tell the app it is coming from the storage UI so should help the user manage storage of this type.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_HOME_TIME_ZONE_ID:kotlin.String`

Extra sent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_HOME_TIME_ZONE_CHANGED:kotlin.String` specifying the new home time zone of the device.

Type: String, the same as returned by `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getID()` to identify time zones. This extra will be `null` if the user disables the home time zone feature.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_HTML_TEXT:kotlin.String`

A constant String that is associated with the Intent, used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` to supply an alternative to `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` as HTML formatted text. Note that you *must* also supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INDEX:kotlin.String`

Optional index with semantics depending on the intent action.

The value must be an integer greater or equal to 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INITIAL_INTENTS:kotlin.String`

A Parcelable\[\] of `https://developer.android.com/reference/kotlin/android/content/Intent.html#` or `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#` objects as set with `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Array)` to place at the front of the list of choices, when shown to the user with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`. You can choose up to two additional activities to show before the app suggestions (the limit of two additional activities starts in Android 10).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INSTALLER_PACKAGE_NAME:kotlin.String`

Used as a string extra field with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String` to install a package. Specifies the installer package name; this package will receive the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_APP_ERROR:kotlin.String` intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String`

An Intent describing the choices you would like shown with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK_ACTIVITY:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_KEY_EVENT:kotlin.String`

A `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` object containing the event that triggered the creation of the Intent it is in.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCALE_LIST:kotlin.String`

Intent extra: A `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#`

Type: LocaleList

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCAL_ONLY:kotlin.String`

Extra used to indicate that an intent should only return data that is on the local device. This is a boolean extra; the default is false. If true, an implementation should only allow the user to select data that is already on the device, not requiring it be downloaded from a remote service when opened.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCUS_ID:kotlin.String`

Intent extra: ID of the context used on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_LOCUS:kotlin.String`.

Type: `https://developer.android.com/reference/kotlin/android/content/LocusId.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_METADATA_TEXT:kotlin.String`

A CharSequence of additional text describing the content being shared. This text will be displayed to the user as a part of the sharesheet when included in an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#`.

e.g. When sharing a photo, metadata could inform the user that location data is included in the photo they are sharing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_MIME_TYPES:kotlin.String`

Extra used to communicate a set of acceptable MIME types. The type of the extra is `String[]`. Values may be a combination of concrete MIME types (such as "image/png") and/or partial MIME types (such as "audio/\*").

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_NEW_TIMEZONE_OFFSET:kotlin.String`

Extra sent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_OFFSET_CHANGED:kotlin.String` specifying the time zone offset of the device after the time zone offset change.

Type: int, the offset in seconds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_NOT_UNKNOWN_SOURCE:kotlin.String`

Used as a boolean extra field with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String` to install a package. Specifies that the application being installed should not be treated as coming from an unknown source, but as coming from the app invoking the Intent. For this to work you must start the installer with startActivityForResult().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_OLD_TIMEZONE_OFFSET:kotlin.String`

Extra sent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_OFFSET_CHANGED:kotlin.String` specifying the time zone offset of the device before the time zone offset change.

Type: int, the offset in seconds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ORIGINATING_URI:kotlin.String`

Used as a URI extra field with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String` to indicate the URI from which the local APK in the Intent data field originated from.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGES:kotlin.String`

String array of package names.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String`

Intent extra: An app package name.

Type: String

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PERMISSION_GROUP_NAME:kotlin.String`

Intent extra: The name of a permission group.

Type: String

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PHONE_NUMBER:kotlin.String`

A String holding the phone number originally entered in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_NEW_OUTGOING_CALL:kotlin.String`, or the actual number to call in a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CALL:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PROCESS_TEXT:kotlin.String`

The name of the extra used to define the text to be processed, as a CharSequence. Note that this may be a styled CharSequence, so you must use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getCharSequence(kotlin.String)` to retrieve it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PROCESS_TEXT_READONLY:kotlin.String`

The name of the boolean extra used to define if the processed text will be used as read-only.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUICK_VIEW_FEATURES:kotlin.String`

An optional extra of `String[]` indicating which quick view features should be made available to the user in the quick view UI while handing a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_QUICK_VIEW:kotlin.String` intent.
- Enumeration of features here is not meant to restrict capabilities of the quick viewer. Quick viewer can implement features not listed below.
- Features included at this time are: `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_VIEW:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_EDIT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_DELETE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_DOWNLOAD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_SEND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/QuickViewConstants.html#FEATURE_PRINT:kotlin.String`.

 Requirements:
- Quick viewer shouldn't show a feature if the feature is absent in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUICK_VIEW_FEATURES:kotlin.String`.
- When `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUICK_VIEW_FEATURES:kotlin.String` is not present, quick viewer should follow internal policies.
- Presence of an feature in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUICK_VIEW_FEATURES:kotlin.String`, does not constitute a requirement that the feature be shown. Quick viewer may, according to its own policies, disable or hide features.

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_QUIET_MODE:kotlin.String`

Optional boolean extra indicating whether quiet mode has been switched on or off. When a profile goes into quiet mode, all apps in the profile are killed and the profile user is stopped. Widgets originating from the profile are masked, and app launcher icons are grayed out.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER:kotlin.String`

This extra can be used with any Intent used to launch an activity, supplying information about who is launching that activity. This field contains a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` object, typically an http: or https: URI of the web site that the referral came from; it can also use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_ANDROID_APP_SCHEME:kotlin.Int` scheme to identify a native application that it came from.

To retrieve this value in a client, use `https://developer.android.com/reference/kotlin/android/app/Activity.html#getReferrer()` instead of directly retrieving the extra. It is also valid for applications to instead supply `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER_NAME:kotlin.String` for cases where they can only create a string, not a Uri; the field here, if supplied, will always take precedence, however.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER_NAME:kotlin.String`

Alternate version of `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REFERRER:kotlin.String` that supplies the URI as a String rather than a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` object. Only for use in cases where Uri objects can not be created, in particular when Intent extras are supplied through the `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_INTENT_SCHEME:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_ANDROID_APP_SCHEME:kotlin.Int` schemes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REMOTE_INTENT_TOKEN:kotlin.String`

Used in the extra field in the remote intent. It's a string token passed with the remote intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACEMENT_EXTRAS:kotlin.String`

A Bundle forming a mapping of potential target package names to different extras Bundles to add to the default intent extras in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` when used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`. Each key should be a package name. The package need not be currently installed on the device.

An application may choose to provide alternate extras for the case where a user selects an activity from a predetermined set of target packages. If the activity the user selects from the chooser belongs to a package with its package name as a key in this bundle, the corresponding extras for that package will be merged with the extras already present in the intent at `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String`. If a replacement extra has the same key as an extra already present in the intent it will overwrite the extra from the intent.

*Examples:*

- An application may offer different `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String` to an application when sharing with it via `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String`, augmenting a link with additional query parameters for that target.
- An application may offer additional metadata for known targets of a given intent to pass along information only relevant to that target such as account or content identifiers already known to that application.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACING:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` intents to indicate that this is a replacement of the package, so this broadcast will immediately be followed by an add broadcast for a different version of the same package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_BUNDLE:kotlin.String`

Extra sent in the intent to the BroadcastReceiver that handles `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_RESTRICTION_ENTRIES:kotlin.String`. The type of the extra is a Bundle containing the restrictions as key/value pairs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_INTENT:kotlin.String`

Extra used in the response from a BroadcastReceiver that handles `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_RESTRICTION_ENTRIES:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESTRICTIONS_LIST:kotlin.String`

Extra used in the response from a BroadcastReceiver that handles `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_RESTRICTION_ENTRIES:kotlin.String`. The type of the extra is `ArrayList<RestrictionEntry>`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RESULT_RECEIVER:kotlin.String`

A `https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#` used to return data back to the sender.

Used to complete an app-specific `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String` for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String` is present in the intent used to start a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` activity this extra will be `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to that `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` and sent when the user selects a target component from the chooser. It is up to the recipient to send a result to this ResultReceiver to signal that disambiguation is complete and that the chooser should invoke the user's choice.

The disambiguator should provide a Bundle to the ResultReceiver with an intent assigned to the key `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String`. This supplied intent will be used by the chooser to match and fill in the final Intent or ChooserTarget before starting it. The supplied intent must `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)` one of the intents from `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String` passed to `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String` to be accepted.

The result code passed to the ResultReceiver should be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if the refinement succeeded and the supplied intent's target in the chooser should be started, or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if the chooser should finish without starting a target.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_RETURN_RESULT:kotlin.String`

Used as a boolean extra field with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UNINSTALL_PACKAGE:kotlin.String`. Specifies that the installer UI should return to the application the result code of the install/uninstall. The returned result code will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` on success or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_FIRST_USER:kotlin.Int` on failure.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHORTCUT_ICON:kotlin.String`

The name of the extra used to define the icon, as a Bitmap, of a shortcut.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHORTCUT_ICON_RESOURCE:kotlin.String`

The name of the extra used to define the icon, as a ShortcutIconResource, of a shortcut.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHORTCUT_ID:kotlin.String`

Intent extra: ID of the shortcut used to send the share intent. Will be sent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHORTCUT_INTENT:kotlin.String`

The name of the extra used to define the Intent of a shortcut.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHORTCUT_NAME:kotlin.String`

The name of the extra used to define the name of a shortcut.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SHUTDOWN_USERSPACE_ONLY:kotlin.String`

Optional extra for `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SHUTDOWN:kotlin.String` that allows the sender to qualify that this shutdown is only for the user space of the system, not a complete shutdown. When this is true, hardware devices can use this information to determine that they shouldn't do a complete shutdown of their device since this is not a complete shutdown down to the kernel, but only user space restarting. The default if not supplied is false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SPLIT_NAME:kotlin.String`

Intent extra: An app split name.

Type: String

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_START_TIME:kotlin.String`

A long representing the start timestamp (epoch time in millis) of the permission usage when used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE_FOR_PERIOD:kotlin.String` and ACTION_MANAGE_PERMISSION_USAGE

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String`

A content: URI holding a stream of data associated with the Intent, used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` to supply the data being sent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUBJECT:kotlin.String`

A constant string holding the desired subject line of a message.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUSPENDED_PACKAGE_EXTRAS:kotlin.String`

Intent extra: A `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras for a package being suspended. Will be sent as an extra with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`.

The contents of this `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` are a contract between the suspended app and the suspending app, i.e. any app with the permission `android.permission.SUSPEND_APPS`. This is meant to enable the suspended app to better handle the state of being suspended.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEMPLATE:kotlin.String`

The initial data to place in a newly created record. Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSERT:kotlin.String`. The data here is a Map containing the same fields as would be given to the underlying ContentProvider.insert() call.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String`

A constant CharSequence that is associated with the Intent, used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String` to supply the literal data to be sent. Note that this may be a styled CharSequence, so you must use `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getCharSequence(kotlin.String)` to retrieve it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIME:kotlin.String`

Optional extra specifying a time in milliseconds. The timebase depends on the Intent including this extra. The value must be non-negative.

Type: long

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TIMEZONE:kotlin.String`

Extra sent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_CHANGED:kotlin.String` specifying the new time zone of the device.

Type: String, the same as returned by `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getID()` to identify time zones.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TITLE:kotlin.String`

A CharSequence dialog title to provide to the user when used with a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_UID:kotlin.String`

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_UID_REMOVED:kotlin.String` intents to supply the uid the package had been assigned. Also an optional extra in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_CHANGED:kotlin.String` for the same purpose.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER:kotlin.String`

The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` carried with intents.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USER_INITIATED:kotlin.String`

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_REMOVED:kotlin.String` intents to signal that the application was removed with the user-initiated action.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USE_STYLUS_MODE:kotlin.String`

A boolean extra used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_NOTE:kotlin.String` indicating whether the launched note-taking activity should show a UI that is suitable to use with stylus input.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_USE_SYSTEM_CONTACTS_PICKER:kotlin.String`

Optional boolean extra indicating if the system contacts picker should be invoked with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK:kotlin.String`, if data field is set as one of:

- data android:mimeType="vnd.android.cursor.dir/contact"
- data android:mimeType="vnd.android.cursor.dir/phone_v2"
- data android:mimeType="vnd.android.cursor.dir/postal-address_v2"
- data android:mimeType="vnd.android.cursor.dir/email_v2"

<br />

Has an effect only on `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK:kotlin.String` with the mentioned data filed values, starting Android 17 (API 37)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current action value to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current categories to be overwritten, even if they are already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current ClipData to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current component value to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current data or type value overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_IDENTIFIER:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current identifier value to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current package value to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current selector to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int`

Use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to allow the current bounds rectangle to be overwritten, even if it is already set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_BROUGHT_TO_FRONT:kotlin.Int`

This flag is not normally set by application code, but set for you by the system as described in the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_launchMode:kotlin.Int` documentation for the singleTask mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int`

If set in an Intent passed to android.content.Context#startActivity, this flag will cause any existing task that would be associated with the activity to be cleared before the activity is started. That is, the activity becomes the new root of an otherwise empty task, and any old activities are finished. This can only be used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int`

If set, and the activity being launched is already running in the current task, then instead of launching a new instance of that activity, all of the other activities on top of it will be closed and this Intent will be delivered to the (now on top) old activity as a new Intent.

For example, consider a task consisting of the activities: A, B, C, D. If D calls startActivity() with an Intent that resolves to the component of activity B, then C and D will be finished and B receive the given Intent, resulting in the stack now being: A, B.

The currently running instance of activity B in the above example will either receive the new intent you are starting here in its onNewIntent() method, or be itself finished and restarted with the new intent. If it has declared its launch mode to be "multiple" (the default) and you have not set `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` in the same intent, then it will be finished and re-created; for all other launch modes or if `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` is set then this Intent will be delivered to the current instance's onNewIntent().

This launch mode can also be used to good effect in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`: if used to start the root activity of a task, it will bring any currently running instance of that task to the foreground, and then clear it to its root state. This is especially useful, for example, when launching an activity from the notification manager.

See [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) for more information about tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int`

If set, the new activity is not kept in the list of recently launched activities.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int`

If set and this intent is being used to launch a new activity from an existing one, then the reply target of the existing activity will be transferred to the new activity. This way, the new activity can call android.app.Activity#setResult and have that result sent back to the reply target of the original activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_LAUNCHED_FROM_HISTORY:kotlin.Int`

This flag is not normally set by application code, but set for you by the system if this activity is being launched from history.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_LAUNCH_ADJACENT:kotlin.Int`

This flag is only used for split-screen multi-window mode. The new activity will be displayed adjacent to the one launching it if possible. This can only be used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`. Also, setting `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` is required if you want a new instance of an existing activity to be created.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MATCH_EXTERNAL:kotlin.Int`

If set in an Intent passed to android.content.Context#startActivity, this flag will attempt to launch an instant app if no full app on the device can already handle the intent.

When attempting to resolve instant apps externally, the following `https://developer.android.com/reference/kotlin/android/content/Intent.html#` properties are supported:

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#setAction(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#addCategory(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#addFlags(kotlin.Int)`

In the case that no instant app can be found, the installer will be launched to notify the user that the intent could not be resolved. On devices that do not support instant apps, the flag will be ignored.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int`

This flag is used to create a new task and launch an activity into it. This flag is always paired with either `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`. In both cases these flags alone would search through existing tasks for ones matching this Intent. Only if no such task is found would a new task be created. When paired with FLAG_ACTIVITY_MULTIPLE_TASK both of these behaviors are modified to skip the search for a matching task and unconditionally start a new task. **When used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` do not use this flag unless you are implementing your own top-level application launcher.** Used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` to disable the behavior of bringing an existing task to the foreground. When set, a new task is *always* started to host the Activity for the Intent, regardless of whether there is already an existing task running the same thing.

**Because the default system does not include graphical task management, you should not use this flag unless you provide some way for a user to return back to the tasks you have launched.** See `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` for details of this flag's use for creating new document tasks.

This flag is ignored if one of `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` is not also set.

See [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) for more information about tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int`

This flag is used to open a document into a new task rooted at the activity launched by this Intent. Through the use of this flag, or its equivalent attribute, `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` multiple instances of the same activity containing different documents will appear in the recent tasks list.

The use of the activity attribute form of this, `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int`, is preferred over the Intent flag described here. The attribute form allows the Activity to specify multiple document behavior for all launchers of the Activity whereas using this flag requires each Intent that launches the Activity to specify it.

Note that the default semantics of this flag w.r.t. whether the recents entry for it is kept after the activity is finished is different than the use of `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` -- if this flag is being used to create a new recents entry, then by default that entry will be removed once the activity is finished. You can modify this behavior with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int`.

FLAG_ACTIVITY_NEW_DOCUMENT may be used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int`. When used alone it is the equivalent of the Activity manifest specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int`="intoExisting". When used with FLAG_ACTIVITY_MULTIPLE_TASK it is the equivalent of the Activity manifest specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int`="always". The flag is ignored even in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` when the Activity manifest specifies `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int`="never". Refer to `https://developer.android.com/reference/kotlin/android/R.attr.html#documentLaunchMode:kotlin.Int` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`

If set, this activity will become the start of a new task on this history stack. A task (from the activity that started it to the next task activity) defines an atomic group of activities that the user can move to. Tasks can be moved to the foreground and background; all of the activities inside of a particular task always remain in the same order. See [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) for more information about tasks.

This flag is generally used by activities that want to present a "launcher" style behavior: they give the user a list of separate things that can be done, which otherwise run completely independently of the activity launching them.

When using this flag, if a task is already running for the activity you are now starting, then a new activity will not be started; instead, the current task will simply be brought to the front of the screen with the state it was last in. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` for a flag to disable this behavior.

This flag can not be used when the caller is requesting a result from the activity being launched.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NO_ANIMATION:kotlin.Int`

If set in an Intent passed to android.content.Context#startActivity, this flag will prevent the system from applying an activity transition animation to go to the next activity state. This doesn't mean an animation will never run -- if another activity change happens that doesn't specify this flag before the activity started here is displayed, then that transition will be used. This flag can be put to good use when you are going to do a series of activity operations but the animation seen by the user shouldn't be driven by the first activity change but rather a later one.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NO_HISTORY:kotlin.Int`

If set, the new activity is not kept in the history stack. As soon as the user navigates away from it, the activity is finished. This may also be set with the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` attribute.

If set, android.app.Activity#onActivityResult is never invoked when the current activity starts a new activity which sets a result and finishes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NO_USER_ACTION:kotlin.Int`

If set, this flag will prevent the normal `https://developer.android.com/reference/kotlin/android/app/Activity.html#onUserLeaveHint()` callback from occurring on the current frontmost activity before it is paused as the newly-started activity is brought to the front.

Typically, an activity can rely on that callback to indicate that an explicit user action has caused their activity to be moved out of the foreground. The callback marks an appropriate point in the activity's lifecycle for it to dismiss any notifications that it intends to display "until the user has seen them," such as a blinking LED.

If an activity is ever started via any non-user-driven events such as phone-call receipt or an alarm handler, this flag should be passed to android.content.Context#startActivity, ensuring that the pausing activity does not think the user has acknowledged its notification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_PREVIOUS_IS_TOP:kotlin.Int`

If set and this intent is being used to launch a new activity from an existing one, the current activity will not be counted as the top activity for deciding whether the new intent should be delivered to the top instead of starting a new one. The previous activity will be used as the top, with the assumption being that the current activity will finish itself immediately.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_REORDER_TO_FRONT:kotlin.Int`

If set in an Intent passed to android.content.Context#startActivity, this flag will cause the launched activity to be brought to the front of its task's history stack if it is already running.

For example, consider a task consisting of four activities: A, B, C, D. If D calls startActivity() with an Intent that resolves to the component of activity B, then B will be brought to the front of the history stack, with this resulting order: A, C, D, B. This flag will be ignored if `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int` is also specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_REQUIRE_DEFAULT:kotlin.Int`

If set in an intent passed to android.content.Context#startActivity, this flag will only launch the intent if it resolves to a single result. If no such result exists or if the system chooser would otherwise be displayed, an `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` will be thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_REQUIRE_NON_BROWSER:kotlin.Int`

If set in an intent passed to android.content.Context#startActivity, this flag will only launch the intent if it resolves to a result that is not a browser. If no such result exists, an `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#` will be thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_RESET_TASK_IF_NEEDED:kotlin.Int`

If set, and this activity is either being started in a new task or bringing to the top an existing task, then it will be launched as the front door of the task. This will result in the application of any affinities needed to have that task in the proper state (either moving activities to or from it), or simply resetting that task to its initial state if needed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int`

By default a document created by `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` will have its entry in recent tasks removed when the user closes it (with back or however else it may finish()). If you would like to instead allow the document to be kept in recents so that it can be re-launched, you can use this flag. When set and the task's activity is finished, the recents entry will remain in the interface for the user to re-launch it, like a recents entry for a top-level application.

The receiving activity can override this request with `https://developer.android.com/reference/kotlin/android/R.attr.html#autoRemoveFromRecents:kotlin.Int` or by explcitly calling `https://developer.android.com/reference/kotlin/android/app/Activity.html#finishAndRemoveTask()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int`

If set, the activity will not be launched if it is already running at the top of the history stack. See [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html#TaskLaunchModes) for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_TASK_ON_HOME:kotlin.Int`

If set in an Intent passed to android.content.Context#startActivity, this flag will cause a newly launching task to be placed on top of the current home activity task (if there is one). That is, pressing back from the task will always return the user to home even if that was not the last activity they saw. This can only be used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_DEBUG_LOG_RESOLUTION:kotlin.Int`

A flag you can enable for debugging: when set, log messages will be printed during the resolution of this intent to show you what has been found to create the final resolved list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_DIRECT_BOOT_AUTO:kotlin.Int`

Flag used to automatically match intents based on their Direct Boot awareness and the current user state.

Since the default behavior is to automatically apply the current user state, this is effectively a sentinel value that doesn't change the output of any queries based on its presence or absence.

Instead, this value can be useful in conjunction with `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectImplicitDirectBoot()` to detect when a caller is relying on implicit automatic matching, instead of confirming the explicit behavior they want.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int`

If set, this intent will not match any components in packages that are currently [stopped](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int). If this is not set, then the default behavior is to include such applications in the result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_FROM_BACKGROUND:kotlin.Int`

Can be set by the caller to indicate that this Intent is coming from a background operation, not from direct user interaction.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int`

When combined with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`, the URI permission grant can be persisted across device reboots until explicitly revoked with `https://developer.android.com/reference/kotlin/android/content/Context.html#revokeUriPermission(android.net.Uri,%20kotlin.Int)`. This flag only offers the grant for possible persisting; the receiving application must call `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#takePersistableUriPermission(android.net.Uri,%20kotlin.Int)` to actually persist.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int`

When combined with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`, the URI permission grant applies to any URI that is a prefix match against the original granted URI. (Without this flag, the URI must match exactly for access to be granted.) Another URI is considered a prefix match only when scheme, authority, and all path segments defined by the prefix are an exact match.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int`

If set, the recipient of this Intent will be granted permission to perform read operations on the URI in the Intent's data and any URIs specified in its ClipData. When applying to an Intent's ClipData, all URIs as well as recursive traversals through data or other ClipData in Intent items will be granted; only the grant flags of the top-level Intent are used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`

If set, the recipient of this Intent will be granted permission to perform write operations on the URI in the Intent's data and any URIs specified in its ClipData. When applying to an Intent's ClipData, all URIs as well as recursive traversals through data or other ClipData in Intent items will be granted; only the grant flags of the top-level Intent are used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int`

If set, this intent will always match any components in packages that are currently [stopped](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int). This is the default behavior when `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int` is not set. If both of these flags are set, this one wins (it allows overriding of exclude for places where the framework may automatically set the exclude flag, such as broadcasts).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_FOREGROUND:kotlin.Int`

If set, when sending a broadcast the recipient is allowed to run at foreground priority, with a shorter timeout interval. During normal broadcasts the receivers are not automatically hoisted out of the background priority class.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_NO_ABORT:kotlin.Int`

If this is an ordered broadcast, don't allow receivers to abort the broadcast. They can still propagate results through to later receivers, but they can not prevent later receivers from seeing the broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_REGISTERED_ONLY:kotlin.Int`

If set, when sending a broadcast only registered receivers will be called -- no BroadcastReceiver components will be launched.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_REPLACE_PENDING:kotlin.Int`

If set, when sending a broadcast the new broadcast will replace any existing pending broadcast that matches it. Matching is defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)` returning true for the intents of the two broadcasts. When a match is found, the new broadcast (and receivers associated with it) will replace the existing one in the pending broadcast list, remaining at the same position in the list.

This flag is most typically used with sticky broadcasts, which only care about delivering the most recent values of the broadcast to their receivers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`

If set, the broadcast will be visible to receivers in Instant Apps. By default Instant Apps will not receive broadcasts. *This flag has no effect when used by an Instant App.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#METADATA_DOCK_HOME:kotlin.String`

Boolean that can be supplied as meta-data with a dock activity, to indicate that the dock should take over the home key when it is active.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_ALLOW_UNSAFE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)`: allow parsing of unsafe information. In particular, the flags `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int` flags can not be set, so that the generated Intent can not cause unexpected data access to happen.

If you do not trust the source of the URI being parsed, you should still do further processing to protect yourself from it. In particular, when using it to start an activity you should usually add in `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_BROWSABLE:kotlin.String` to limit the activities that can handle it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_ANDROID_APP_SCHEME:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)`: the URI string always has the "android-app:" scheme. This is a variation of `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_INTENT_SCHEME:kotlin.Int` whose format is simpler for the case of an http/https URI being delivered to a specific package name. The format is:

```kotlin
android-app://{package_id}[/{scheme}[/{host}[/{path}]]][#Intent;{...}]
```

<br />

In this scheme, only the `package_id` is required. If you include a host, you must also include a scheme; including a path also requires both a host and a scheme. The final #Intent; fragment can be used without a scheme, host, or path. Note that this can not be used with intents that have a `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSelector(android.content.Intent)`, since the base intent will always have an explicit package name.

Some examples of how this scheme maps to Intent objects:
URI Intent `android-app://com.example.app` Action: `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` Package: `com.example.app` `android-app://com.example.app/http/example.com` Action: `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String` Data: `http://example.com/` Package: `com.example.app` `android-app://com.example.app/http/example.com/foo?1234` Action: `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String` Data: `http://example.com/foo?1234` Package: `com.example.app` `android-app://com.example.app/
Intent;action=com.example.MY_ACTION;end` Action: `com.example.MY_ACTION` Package: `com.example.app` `android-app://com.example.app/http/example.com/foo?1234
Intent;action=com.example.MY_ACTION;end` Action: `com.example.MY_ACTION` Data: `http://example.com/foo?1234` Package: `com.example.app` `android-app://com.example.app/
Intent;action=com.example.MY_ACTION;
i.some_int=100;S.some_str=hello;end` Action: `com.example.MY_ACTION` Package: `com.example.app` Extras: `some_int=(int)100
some_str=(String)hello`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#URI_INTENT_SCHEME:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)`: the URI string always has the "intent:" scheme. This syntax can be used when you want to later disambiguate between URIs that are intended to describe an Intent vs. all others that should be treated as raw URIs. When used with `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)`, any other scheme will result in a generic VIEW action for that raw URI.

<br />

From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#LabeledIntent(android.content.Intent,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)(origIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, sourcePackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, labelRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a labeled intent from the given intent, supplying the label and icon resources for it. |
| `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#LabeledIntent(android.content.Intent,%20kotlin.String,%20kotlin.CharSequence,%20kotlin.Int)(origIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, sourcePackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, nonLocalizedLabel: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a labeled intent from the given intent, supplying a textual label and icon resource for it. |
| `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#LabeledIntent(kotlin.String,%20kotlin.Int,%20kotlin.Int)(sourcePackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, labelRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a labeled intent with no intent data but supplying the label and icon resources for it. |
| `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#LabeledIntent(kotlin.String,%20kotlin.CharSequence,%20kotlin.Int)(sourcePackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, nonLocalizedLabel: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a labeled intent with no intent data but supplying a textual label and icon resource for it. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#getIconResource()()` Return any resource identifier that has been given for the label icon. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#getLabelResource()()` Return any resource identifier that has been given for the label text. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#getNonLocalizedLabel()()` Return any concrete text that has been given for the label text. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#getSourcePackage()()` Return the name of the package holding label and icon resources. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)` Retrieve the icon associated with this object. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)` Retrieve the label associated with this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#readFromParcel(android.os.Parcel)(in: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#addCategory(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Add a new category to the intent. Categories provide additional detail about the action the intent performs. When resolving an intent, only activities that provide *all* of the requested categories will be used.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#addFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Add additional flags to the intent (or with existing flags value).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#clone()()`

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#cloneFilter()()`

Make a clone of only the parts of the Intent that are relevant for filter matching: the action, data, type, component, and categories.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#createChooser(android.content.Intent,%20kotlin.CharSequence)(target: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)`

Convenience function for creating a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent.

Builds a new `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent that wraps the given target intent, also optionally supplying a title. If the target intent has specified `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`, then these flags will also be set in the returned chooser intent, with its ClipData set appropriately: either a direct reflection of `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` if that is non-null, or a new ClipData built from `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#createChooser(android.content.Intent,%20kotlin.CharSequence,%20android.content.IntentSender)(target: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, sender: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!)`

Convenience function for creating a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent.

Builds a new `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` Intent that wraps the given target intent, also optionally supplying a title. If the target intent has specified `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`, then these flags will also be set in the returned chooser intent, with its ClipData set appropriately: either a direct reflection of `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` if that is non-null, or a new ClipData built from `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`.

The caller may optionally supply an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` to receive a callback when the user makes a choice. This can be useful if the calling application wants to remember the last chosen target and surface it as a more prominent or one-touch affordance elsewhere in the UI for next time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#describeContents()()`

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)(other: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Copy the contents of other in to this object, but only where fields are not defined by this object. For purposes of a field being defined, the following pieces of data in the Intent are considered to be separate fields:

- action, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setAction(kotlin.String)`.
- data Uri and MIME type, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`, or `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndType(android.net.Uri,%20kotlin.String)`.
- identifier, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setIdentifier(kotlin.String)`.
- categories, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#addCategory(kotlin.String)`.
- package, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)`.
- component, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` or related methods.
- source bounds, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSourceBounds(android.graphics.Rect)`.
- selector, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSelector(android.content.Intent)`.
- clip data, as set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`.
- each top-level name in the associated extras.

<br />

In addition, you can use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_IDENTIFIER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` to override the restriction where the corresponding field will not be replaced if it is already set.

Note: The component field will only be copied if `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` is explicitly specified. The selector will only be copied if `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` is explicitly specified.

For example, consider Intent A with {data="foo", categories="bar"} and Intent B with {action="gotit", data-type="some/thing", categories="one","two"}.

Calling A.fillIn(B, Intent.FILL_IN_DATA) will result in A now containing: {action="gotit", data-type="some/thing", categories="bar"}.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)(other: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Determine if two intents are the same for the purposes of intent resolution (filtering). That is, if their action, data, type, identity, class, and categories are the same. This does *not* compare any extra data included in the intents. Note that technically when actually matching against an `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#` the identifier is ignored, while here it is directly compared for equality like the other fields.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterHashCode()()`

Generate hash code that matches semantics of filterEquals().

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()()`

Retrieve the general action to be performed, such as `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String`. The action describes the general way the rest of the information in the intent should be interpreted -- most importantly, what to do with the data returned by `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanExtra(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBundleExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getByteArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getByteExtra(kotlin.String,%20kotlin.Byte)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCategories()()`

Return the set of all categories in the intent. If there are no categories, returns NULL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCharArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCharExtra(kotlin.String,%20kotlin.Char)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCharSequenceArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCharSequenceArrayListExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getCharSequenceExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/ClipData.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()()`

Return the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` associated with this Intent. If there is none, returns null. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getComponent()()`

Retrieve the concrete component associated with the intent. When receiving an intent, this is the component that was found to best handle it (that is, yourself) and will always be non-null; in all other cases it will be null unless explicitly set.

<br />

`https://developer.android.com/reference/kotlin/android/net/Uri.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()()`

Retrieve data this intent is operating on. This URI specifies the name of the data; often it uses the content: scheme, specifying data in a content provider. Other schemes may be handled by specific activities, such as http: by the web browser.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getDataString()()`

The same as `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()`, but returns the URI as an encoded String.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getDoubleArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getDoubleExtra(kotlin.String,%20kotlin.Double)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getExtras()()`

Retrieves a map of extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getFlags()()`

Retrieve any special flags associated with this intent. You will normally just set them with `https://developer.android.com/reference/kotlin/android/content/Intent.html#setFlags(kotlin.Int)` and let the system take the appropriate action with them.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getFloatArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getFloatExtra(kotlin.String,%20kotlin.Float)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIdentifier()()`

Retrieve the identifier for this Intent. If non-null, this is an arbitrary identity of the Intent to distinguish it from other Intents.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntegerArrayListExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntent(kotlin.String)(uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Call `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)` with 0 flags.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntentOld(kotlin.String)(uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getLongArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getLongExtra(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getPackage()()`

Retrieve the application package name this Intent is limited to. When resolving an Intent, if non-null this limits the resolution to only components in the given application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableArrayExtra(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableArrayListExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableArrayListExtra(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out T>)`

Retrieve extended data from the intent.

<br />

`T?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`T?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getScheme()()`

Return the scheme portion of the intent's data. If the data is null or does not include a scheme, null is returned. Otherwise, the scheme prefix without the final ':' is returned, i.e. "http".

This is the same as calling getData().getScheme() (and checking for null data).

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getSelector()()`

Return the specific selector associated with this Intent. If there is none, returns null. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSelector(android.content.Intent)` for more information.

<br />

`https://developer.android.com/reference/kotlin/java/io/Serializable.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getSerializableExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`T?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getSerializableExtra(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getShortArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getShortExtra(kotlin.String,%20kotlin.Short)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getSourceBounds()()`

Get the bounds of the sender of this intent, in screen coordinates. This can be used as a hint to the receiver for animations and the like. Null means that there is no source bounds.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringArrayExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringArrayListExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Retrieve extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#getType()()`

Retrieve any explicit MIME type included in the intent. This is usually null, as the type is determined by the intent data.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasCategory(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Check if a category exists in the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Returns true if an extra value is associated with the given name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#hasFileDescriptors()()`

Returns true if the Intent's extras contain a parcelled file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#isMismatchingFilter()()`

Whether the intent mismatches all intent filters declared in the receiving component.

When a component receives an intent, normally obtainable through the following methods:

- `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)`
- `https://developer.android.com/reference/kotlin/android/app/Activity.html#getIntent()`
- `https://developer.android.com/reference/kotlin/android/app/Activity.html#onNewIntent(android.content.Intent)`
- `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)`

The developer can call this method to check if this intent does not match any of its declared intent filters. A non-matching intent can be delivered when the intent sender explicitly set the component through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` or #setClassName.

This method always returns `false` if the intent originated from within the same application or the system, because these cases are always exempted from security checks.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainActivity(android.content.ComponentName)(mainActivity: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)`

Create an intent to launch the main (root) activity of a task. This is the Intent that is started when the application's is launched from Home. For anything else that wants to launch an application in the same way, it is important that they use an Intent structured the same way, and can use this function to ensure this is the case.

The returned Intent has the given Activity component as its explicit component, `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` as its action, and includes the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`. This does *not* have `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` set, though typically you will want to do that through `https://developer.android.com/reference/kotlin/android/content/Intent.html#addFlags(kotlin.Int)` on the returned Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainSelectorActivity(kotlin.String,%20kotlin.String)(selectorAction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectorCategory: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Make an Intent for the main activity of an application, without specifying a specific activity to run but giving a selector to find the activity. This results in a final Intent that is structured the same as when the application is launched from Home. For anything else that wants to launch an application in the same way, it is important that they use an Intent structured the same way, and can use this function to ensure this is the case.

The returned Intent has `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` as its action, and includes the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`. This does *not* have `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` set, though typically you will want to do that through `https://developer.android.com/reference/kotlin/android/content/Intent.html#addFlags(kotlin.Int)` on the returned Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeRestartActivityTask(android.content.ComponentName)(mainActivity: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)`

Make an Intent that can be used to re-launch an application's task in its base state. This is like `https://developer.android.com/reference/kotlin/android/content/Intent.html#makeMainActivity(android.content.ComponentName)`, but also sets the flags `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Normalize a MIME data type.

A normalized MIME type has white-space trimmed, content-type parameters removed, and is lower-case. This aligns the type with Android best practices for intent filtering.

For example, "text/plain; charset=utf-8" becomes "text/plain". "text/x-vCard" becomes "text/x-vcard".

All MIME types received from outside Android (such as user input, or external sources like Bluetooth, NFC, or the Internet) should be normalized before they are used to create an Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseIntent(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(resources: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)`

Parses the "intent" element (and its children) from XML and instantiates an Intent object. The given XML parser should be located at the tag where parsing should start (often named "intent"), from which the basic action, data, type, and package and class name will be retrieved. The function will then parse in to any child elements, looking for tags to add categories and to attach extra data to the intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#parseUri(kotlin.String,%20kotlin.Int)(uri: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Create an intent from a URI. This URI may encode the action, category, and other intent fields, if it was returned by `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)`. If the Intent was not generated by toUri(), its data will be the entire URI and its action will be ACTION_VIEW.

The URI given here must not be relative -- that is, it must include the scheme and full path.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putCharSequenceArrayListExtra(kotlin.String,%20java.util.ArrayList)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20android.os.Bundle)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20android.os.Parcelable)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/android/os/Parcelable.html#?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Array)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.BooleanArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Byte)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.ByteArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Char)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.CharArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Double)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.DoubleArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Float)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.FloatArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.IntArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20java.io.Serializable)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/java/io/Serializable.html#?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.CharSequence)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Array)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Array)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.LongArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.Short)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtra(kotlin.String,%20kotlin.ShortArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtras(android.content.Intent)(src: https://developer.android.com/reference/kotlin/android/content/Intent.html#)`

Copy all extras in 'src' in to this intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`

Add a set of extended data to the intent. The keys must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putIntegerArrayListExtra(kotlin.String,%20java.util.ArrayList)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putParcelableArrayListExtra(kotlin.String,%20java.util.ArrayList)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<out https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#putStringArrayListExtra(kotlin.String,%20java.util.ArrayList)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)`

Add extended data to the intent. The name must include a package prefix, for example the app com.android.contacts would use names like "com.android.contacts.ShowAll".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#removeCategory(kotlin.String)(category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Remove a category from an intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#removeExtra(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Remove extended data from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#removeFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Remove these flags from the intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#removeLaunchSecurityProtection()()`

When an intent comes from another app or component as an embedded extra intent, the system creates a token to identify the creator of this foreign intent. If this token is missing or invalid, the system will block the launch of this intent. If it contains a valid token, the system will perform verification against the creator to block launching target it has no permission to launch or block it from granting URI access to the tagert it cannot access. This method provides a way to opt out this feature.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#replaceExtras(android.content.Intent)(src: https://developer.android.com/reference/kotlin/android/content/Intent.html#)`

Completely replace the extras in the Intent with the extras in the given Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#replaceExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Completely replace the extras in the Intent with the given Bundle of extras.

<br />

`https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivity(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)`

Return the Activity component that should be used to handle this intent. The appropriate component is determined based on the information in the intent, evaluated as follows:

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#getComponent()` returns an explicit class, that is returned without any further consideration.

The activity must handle the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String` Intent category to be considered.

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#getAction()` is non-NULL, the activity must handle this action.

If #resolveType returns non-NULL, the activity must handle this type.

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#addCategory(kotlin.String)` has added any categories, the activity must handle ALL of the categories specified.

If `https://developer.android.com/reference/kotlin/android/content/Intent.html#getPackage()` is non-NULL, only activity components in that application package will be considered.

If there are no activities that satisfy all of these conditions, a null string is returned.

If multiple activities are found to satisfy the intent, the one with the highest priority will be used. If there are multiple activities with the same priority, the system will either pick the best activity based on user preference, or resolve to a system class that will allow the user to pick an activity and forward from there.

This method is implemented simply by calling android.content.pm.PackageManager#resolveActivity with the "defaultOnly" parameter true.

This API is called for you as part of starting an activity from an intent. You do not normally need to call it yourself.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivityInfo(android.content.pm.PackageManager,%20kotlin.Int)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Resolve the Intent into an `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo` describing the activity that should execute the intent. Resolution follows the same rules as described for `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivity(android.content.pm.PackageManager)`, but you get back the completely information about the resolved activity instead of just its class name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveType(android.content.ContentResolver)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`

Return the MIME data type of this intent. If the type field is explicitly set, that is simply returned. Otherwise, if the data is set, the type of that data is returned. If neither fields are set, a null is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveType(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)`

Return the MIME data type of this intent. If the type field is explicitly set, that is simply returned. Otherwise, if the data is set, the type of that data is returned. If neither fields are set, a null is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveTypeIfNeeded(android.content.ContentResolver)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`

Return the MIME data type of this intent, only if it will be needed for intent resolution. This is not generally useful for application code; it is used by the frameworks for communicating with back-end system services.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setAction(kotlin.String)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Set the general action to be performed.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)(packageContext: https://developer.android.com/reference/kotlin/android/content/Context.html#, cls: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` with the name returned by a `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClassName(android.content.Context,%20kotlin.String)(packageContext: https://developer.android.com/reference/kotlin/android/content/Context.html#, className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` with an explicit class name.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClassName(kotlin.String,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Convenience for calling `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` with an explicit application package name and class name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)(clip: https://developer.android.com/reference/kotlin/android/content/ClipData.html#?)`

Set a `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` associated with this Intent. This replaces any previously set ClipData.

The ClipData in an intent is not used for Intent matching or other such operations. Semantically it is like extras, used to transmit additional data with the Intent. The main feature of using this over the extras for data is that `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` will operate on any URI items included in the clip data. This is useful, in particular, if you want to transmit an Intent containing multiple `content:` URIs for which the recipient may not have global permission to access the content provider.

If the ClipData contains items that are themselves Intents, any grant flags in those Intents will be ignored. Only the top-level flags of the main Intent are respected, and will be applied to all Uri or Intent items in the clip (or sub-items of the clip).

The MIME type, label, and icon in the ClipData object are not directly used by Intent. Applications should generally rely on the MIME type of the Intent itself, not what it may find in the ClipData. A common practice is to construct a ClipData for use with an Intent with a MIME type of "\*/\*".

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?)`

(Usually optional) Explicitly set the component to handle the intent. If left with the default value of null, the system will determine the appropriate class to use based on the other fields (action, data, type, categories) in the Intent. If this class is defined, the specified class will always be used regardless of the other fields. You should only set this value when you know you absolutely want a specific class to be used; otherwise it is better to let the system find the appropriate class so that you will respect the installed applications and user preferences.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)(data: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)`

Set the data this intent is operating on. This method automatically clears any type that was previously set by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#setTypeAndNormalize(kotlin.String)`.

*Note: scheme matching in the Android framework is case-sensitive, unlike the formal RFC. As a result, you should always write your Uri with a lower case scheme, or use `https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme()` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndNormalize(android.net.Uri)` to ensure that the scheme is converted to lower case.*

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndNormalize(android.net.Uri)(data: https://developer.android.com/reference/kotlin/android/net/Uri.html#)`

Normalize and set the data this intent is operating on.

This method automatically clears any type that was previously set (for example, by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`).

The data Uri is normalized using `https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme()` before it is set, so really this is just a convenience method for

```kotlin
setData(data.normalize())
  
```

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndType(android.net.Uri,%20kotlin.String)(data: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

(Usually optional) Set the data for the intent along with an explicit MIME data type. This method should very rarely be used -- it allows you to override the MIME type that would ordinarily be inferred from the data with your own type given here.

*Note: MIME type and Uri scheme matching in the Android framework is case-sensitive, unlike the formal RFC definitions. As a result, you should always write these elements with lower case letters, or use `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme()` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndTypeAndNormalize(android.net.Uri,%20kotlin.String)` to ensure that they are converted to lower case.*

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setDataAndTypeAndNormalize(android.net.Uri,%20kotlin.String)(data: https://developer.android.com/reference/kotlin/android/net/Uri.html#, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

(Usually optional) Normalize and set both the data Uri and an explicit MIME data type. This method should very rarely be used -- it allows you to override the MIME type that would ordinarily be inferred from the data with your own type given here.

The data Uri and the MIME type are normalize using `https://developer.android.com/reference/kotlin/android/net/Uri.html#normalizeScheme()` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` before they are set, so really this is just a convenience method for

```kotlin
setDataAndType(data.normalize(), Intent.normalizeMimeType(type))
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setExtrasClassLoader(java.lang.ClassLoader)(loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#?)`

Sets the ClassLoader that will be used when unmarshalling any Parcelable values from the extras of this Intent.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set special flags controlling how this intent is handled. Most values here depend on the type of component being executed by the Intent, specifically the FLAG_ACTIVITY_\* flags are all for use with android.content.Context#startActivity and the FLAG_RECEIVER_\* flags are all for use with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`.

See the [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) documentation for important information on how some of these options impact the behavior of your application.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setIdentifier(kotlin.String)(identifier: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Set an identifier for this Intent. If set, this provides a unique identity for this Intent, allowing it to be unique from other Intents that would otherwise look the same. In particular, this will be used by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)` to determine if two Intents are the same as with other fields like `https://developer.android.com/reference/kotlin/android/content/Intent.html#setAction(kotlin.String)`. However, unlike those fields, the identifier is *never* used for matching against an `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#`; it is as if the identifier has not been set on the Intent.

This can be used, for example, to make this Intent unique from other Intents that are otherwise the same, for use in creating a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. (Be aware however that the receiver of the PendingIntent will see whatever you put in here.) The structure of this string is completely undefined by the platform, however if you are going to be exposing identifier strings across different applications you may need to define your own structure if there is no central party defining the contents of this field.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

(Usually optional) Set an explicit application package name that limits the components this Intent will resolve to. If left to the default value of null, all components in all applications will considered. If non-null, the Intent can only match the components in the given application package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSelector(android.content.Intent)(selector: https://developer.android.com/reference/kotlin/android/content/Intent.html#?)`

Set a selector for this Intent. This is a modification to the kinds of things the Intent will match. If the selector is set, it will be used when trying to find entities that can handle the Intent, instead of the main contents of the Intent. This allows you build an Intent containing a generic protocol while targeting it more specifically.

An example of where this may be used is with things like `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_BROWSER:kotlin.String`. This category allows you to build an Intent that will launch the Browser application. However, the correct main entry point of an application is actually `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName)` used to specify the actual Activity to launch. If you launch the browser with something different, undesired behavior may happen if the user has previously or later launches it the normal way, since they do not match. Instead, you can build an Intent with the MAIN action (but no ComponentName yet specified) and set a selector with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_BROWSER:kotlin.String` to point it specifically to the browser activity.

Setting a selector does not impact the behavior of `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterHashCode()`. This is part of the desired behavior of a selector -- it does not impact the base meaning of the Intent, just what kinds of things will be matched against it when determining who can handle it.

You can not use both a selector and `https://developer.android.com/reference/kotlin/android/content/Intent.html#setPackage(kotlin.String)` on the same base Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setSourceBounds(android.graphics.Rect)(r: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?)`

Set the bounds of the sender of this intent, in screen coordinates. This can be used as a hint to the receiver for animations and the like. Null means that there is no source bounds.

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Set an explicit MIME data type.

This is used to create intents that only specify a type and not data, for example to indicate the type of data to return.

This method automatically clears any data that was previously set (for example by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)`).

*Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lower case letters, or use `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#setTypeAndNormalize(kotlin.String)` to ensure that it is converted to lower case.*

<br />

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` `https://developer.android.com/reference/kotlin/android/content/Intent.html#setTypeAndNormalize(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Normalize and set an explicit MIME data type.

This is used to create intents that only specify a type and not data, for example to indicate the type of data to return.

This method automatically clears any data that was previously set (for example by `https://developer.android.com/reference/kotlin/android/content/Intent.html#setData(android.net.Uri)`).

The MIME type is normalized using `https://developer.android.com/reference/kotlin/android/content/Intent.html#normalizeMimeType(kotlin.String)` before it is set, so really this is just a convenience method for

```kotlin
setType(Intent.normalizeMimeType(type))
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Intent.html#toString()()`

Returns a string representation of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#toURI()()`

Call `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)` with 0 flags.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Convert this Intent into a String holding a URI representation of it. The returned URI string has been properly URI encoded, so it can be used with `https://developer.android.com/reference/kotlin/android/net/Uri.html#parse(kotlin.String)`. The URI contains the Intent's data as the base URI, with an additional fragment describing the action, categories, type, flags, package, component, and extras.

You can convert the returned string back to an Intent with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntent(kotlin.String)`.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [LabeledIntent](https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/LabeledIntent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### LabeledIntent

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LabeledIntent(
    origIntent: Intent!, 
    sourcePackage: String!, 
    labelRes: Int, 
    icon: Int)
```

Create a labeled intent from the given intent, supplying the label and icon resources for it.

| Parameters ||
|---|---|
| `origIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!: The original Intent to copy. |
| `sourcePackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package in which the label and icon live. |
| `labelRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the label, or 0 if none. |
| --- | --- |
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the icon, or 0 if none. |

### LabeledIntent

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LabeledIntent(
    origIntent: Intent!, 
    sourcePackage: String!, 
    nonLocalizedLabel: CharSequence!, 
    icon: Int)
```

Create a labeled intent from the given intent, supplying a textual label and icon resource for it.

| Parameters ||
|---|---|
| `origIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!: The original Intent to copy. |
| `sourcePackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package in which the label and icon live. |
| `nonLocalizedLabel` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Concrete text to use for the label. |
| --- | --- |
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the icon, or 0 if none. |

### LabeledIntent

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LabeledIntent(
    sourcePackage: String!, 
    labelRes: Int, 
    icon: Int)
```

Create a labeled intent with no intent data but supplying the label and icon resources for it.

| Parameters ||
|---|---|
| `sourcePackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package in which the label and icon live. |
| `labelRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the label, or 0 if none. |
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the icon, or 0 if none. |
| --- | --- |

### LabeledIntent

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LabeledIntent(
    sourcePackage: String!, 
    nonLocalizedLabel: CharSequence!, 
    icon: Int)
```

Create a labeled intent with no intent data but supplying a textual label and icon resource for it.

| Parameters ||
|---|---|
| `sourcePackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package in which the label and icon live. |
| `nonLocalizedLabel` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Concrete text to use for the label. |
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource containing the icon, or 0 if none. |
| --- | --- |

## Public methods

### getIconResource

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIconResource(): Int
```

Return any resource identifier that has been given for the label icon.

### getLabelResource

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabelResource(): Int
```

Return any resource identifier that has been given for the label text.

### getNonLocalizedLabel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNonLocalizedLabel(): CharSequence!
```

Return any concrete text that has been given for the label text.

### getSourcePackage

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSourcePackage(): String!
```

Return the name of the package holding label and icon resources.

### loadIcon

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadIcon(pm: PackageManager!): Drawable!
```

Retrieve the icon associated with this object. If the object does not have a icon, null will be returned, in which case you will probably want to load the icon from the underlying resolved info for the Intent.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

### loadLabel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadLabel(pm: PackageManager!): CharSequence!
```

Retrieve the label associated with this object. If the object does not have a label, null will be returned, in which case you will probably want to load the label from the underlying resolved info for the Intent.

### readFromParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFromParcel(in: Parcel!): Unit
```

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<LabeledIntent!>
```
