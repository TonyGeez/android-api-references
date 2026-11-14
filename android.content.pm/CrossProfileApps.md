# CrossProfileApps

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossProfileApps

Kotlin| [Java](CrossProfileApps.md) 
| --- | --- |

```
open class CrossProfileApps
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.CrossProfileApps](CrossProfileApps.md) |

Class for handling cross profile operations. Apps can use this class to interact with its instance in any profile that is in [getTargetUserProfiles()](CrossProfileApps.md)). For example, app can use this class to start its main activity in managed profile. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](CrossProfileApps.md) Broadcast signalling that the receiving app's permission to interact across profiles has changed. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canInteractAcrossProfiles](CrossProfileApps.md))`()` Returns whether the calling package can interact across profiles. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canRequestInteractAcrossProfiles](CrossProfileApps.md))`()` Returns whether the calling package can request to navigate the user to the relevant settings page to request user consent to interact across profiles. |
| open [Intent](../android.content/Intent.md) | [createRequestInteractAcrossProfilesIntent](CrossProfileApps.md))`()` Returns an [Intent](../android.content/Intent.md) to open the settings page that allows the user to decide whether the calling app can interact across profiles. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md) | [getProfileSwitchingIconDrawable](CrossProfileApps.md))`(`userHandle:` ` [UserHandle](../android.os/UserHandle.md)`)` Return a drawable that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getProfileSwitchingLabel](CrossProfileApps.md))`(`userHandle:` ` [UserHandle](../android.os/UserHandle.md)`)` Return a label that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UserHandle](../android.os/UserHandle.md)!\> | [getTargetUserProfiles](CrossProfileApps.md))`()` Return a list of user profiles that that the caller can use when calling other APIs in this class. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isManagedProfile](CrossProfileApps.md))`(`userHandle:` ` [UserHandle](../android.os/UserHandle.md)`)` Checks if the specified user is a managed profile. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProfile](CrossProfileApps.md))`(`userHandle:` ` [UserHandle](../android.os/UserHandle.md)`)` Checks if the specified user is a profile, i. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](CrossProfileApps.md))`(`intent:` ` [Intent](../android.content/Intent.md)`, `targetUser:` ` [UserHandle](../android.os/UserHandle.md)`, `callingActivity:` ` [Activity](../android.app/Activity.md)?`)` Starts the specified activity of the caller package in the specified profile. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](CrossProfileApps.md))`(`intent:` ` [Intent](../android.content/Intent.md)`, `targetUser:` ` [UserHandle](../android.os/UserHandle.md)`, `callingActivity:` ` [Activity](../android.app/Activity.md)?`, `options:` ` [Bundle](../android.os/Bundle.md)?`)` Starts the specified activity of the caller package in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMainActivity](CrossProfileApps.md))`(`component:` ` [ComponentName](../android.content/ComponentName.md)`, `targetUser:` ` [UserHandle](../android.os/UserHandle.md)`)` Starts the specified main activity of the caller package in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMainActivity](CrossProfileApps.md))`(`component:` ` [ComponentName](../android.content/ComponentName.md)`, `targetUser:` ` [UserHandle](../android.os/UserHandle.md)`, `callingActivity:` ` [Activity](../android.app/Activity.md)?`, `options:` ` [Bundle](../android.os/Bundle.md)?`)` Starts the specified main activity of the caller package in the specified profile, launching in the specified activity. |
| --- | --- |

## Constants

### ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED: String
```

Broadcast signalling that the receiving app's permission to interact across profiles has changed. This includes the user, admin, or OEM changing their consent such that the permission for the app to interact across profiles has changed.

This broadcast is not sent when other circumstances result in a change to being able to interact across profiles in practice, such as the profile being turned off or removed, apps being uninstalled, etc. The methods [canInteractAcrossProfiles()](CrossProfileApps.md))and [canRequestInteractAcrossProfiles()](CrossProfileApps.md))can be used by apps prior to attempting to interact across profiles or attempting to request user consent to interact across profiles.

Apps that have set the`android:crossProfile`manifest attribute to`true`can receive this broadcast in manifest broadcast receivers. Otherwise, it can only be received by dynamically-registered broadcast receivers. 

 Value: "android.content.pm.action.CAN_INTERACT_ACROSS_PROFILES_CHANGED"

## Public methods

### canInteractAcrossProfiles

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canInteractAcrossProfiles(): Boolean
```

Returns whether the calling package can interact across profiles.

Specifically, returns whether the following are all true:

- [getTargetUserProfiles()](CrossProfileApps.md))returns a non-empty list for the calling user.
- The user has previously consented to cross-profile communication for the calling package.
- The calling package has either been allowlisted by default by the OEM or has been explicitly allowlisted by the admin via [android.app.admin.DevicePolicyManager#setCrossProfilePackages(ComponentName, Set)](../android.app.admin/DevicePolicyManager.md)).

If`false`, the package's current ability to request user consent to interact across profiles can be checked with [canRequestInteractAcrossProfiles()](CrossProfileApps.md)). If`true`, user consent can be obtained via [createRequestInteractAcrossProfilesIntent()](CrossProfileApps.md)). The package can then listen to [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](CrossProfileApps.md) broadcasts.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the calling package can interact across profiles. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------|
| `java.lang.SecurityException` | if`mContext.getPackageName()`does not belong to the calling UID. |

### canRequestInteractAcrossProfiles

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canRequestInteractAcrossProfiles(): Boolean
```

Returns whether the calling package can request to navigate the user to the relevant settings page to request user consent to interact across profiles.

If`true`, the navigation intent can be obtained via [createRequestInteractAcrossProfilesIntent()](CrossProfileApps.md)). The package can then listen to [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](CrossProfileApps.md) broadcasts.

Specifically, returns whether the following are all true:

- `UserManager#getProfileIdsExcludingHidden(int)`returns at least one other profile for the calling user.
- The calling app has requested`android.Manifest.permission.INTERACT_ACROSS_PROFILES`in its manifest.
- The calling app is not a profile owner within the profile group of the calling user.

Note that in order for the user to be able to grant the consent, the requesting package must be allowlisted by the admin or the OEM and installed in the other profile. If this is not the case the user will be shown a message explaining why they can't grant the consent.

Note that user consent could already be granted if given a return value of`true`. The package's current ability to interact across profiles can be checked with [canInteractAcrossProfiles()](CrossProfileApps.md)).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the calling package can request to interact across profiles. |

### createRequestInteractAcrossProfilesIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createRequestInteractAcrossProfilesIntent(): Intent
```

Returns an [Intent](../android.content/Intent.md) to open the settings page that allows the user to decide whether the calling app can interact across profiles.

The method [canRequestInteractAcrossProfiles()](CrossProfileApps.md))must be returning`true`.

Note that the user may already have given consent and the app may already be able to interact across profiles, even if [canRequestInteractAcrossProfiles()](CrossProfileApps.md))is`true`. The current ability to interact across profiles is given by [canInteractAcrossProfiles()](CrossProfileApps.md)).

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android.content/Intent.md) | an [Intent](../android.content/Intent.md) to open the settings page that allows the user to decide whether the app can interact across profiles This value cannot be`null`. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if`mContext.getPackageName()`does not belong to the calling UID, or [canRequestInteractAcrossProfiles()](CrossProfileApps.md))is`false`. |

### getProfileSwitchingIconDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProfileSwitchingIconDrawable(userHandle: UserHandle): Drawable
```

Return a drawable that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. For example, it may return a briefcase icon if the given user handle is the managed profile one.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Drawable](../android.graphics.drawable/Drawable.md) | an icon that calling app can show user for the semantic of launching its own activity in specified user profile. This value cannot be`null`. |

**See Also**

- [#startMainActivity(ComponentName, UserHandle)](CrossProfileApps.md)) 

### getProfileSwitchingLabel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProfileSwitchingLabel(userHandle: UserHandle): CharSequence
```

Return a label that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. For example, it may return "Switch to work" if the given user handle is the managed profile one.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | a label that calling app can show user for the semantic of launching its own activity in the specified user profile. This value cannot be`null`. |

**See Also**

- [#startMainActivity(ComponentName, UserHandle)](CrossProfileApps.md)) 

### getTargetUserProfiles

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTargetUserProfiles(): MutableList<UserHandle!>
```

Return a list of user profiles that that the caller can use when calling other APIs in this class.

A user profile would be considered as a valid target user profile, provided that:

- It gets caller app installed
- It is not equal to the calling user
- It is in the same profile group of calling user profile
- It is enabled
- It is not hidden (ex. profile type [UserManager.USER_TYPE_PROFILE_PRIVATE](../android.os/UserManager.md))

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [UserHandle](../android.os/UserHandle.md)!> | This value cannot be`null`. |

**See Also**

- [android.os.UserManager#getUserProfiles()](../android.os/UserManager.md)) 

### isManagedProfile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isManagedProfile(userHandle: UserHandle): Boolean
```

Checks if the specified user is a managed profile.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the specified user is a managed profile. |

### isProfile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isProfile(userHandle: UserHandle): Boolean
```

Checks if the specified user is a profile, i.e. not the parent user.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the specified user is a profile. |

### startActivity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivity(
    intent: Intent, 
    targetUser: UserHandle, 
    callingActivity: Activity?
): Unit
```

Starts the specified activity of the caller package in the specified profile.

The caller must have the [android.Manifest.permission#INTERACT_ACROSS_PROFILES](../android/Manifest.permission.md),`android.Manifest.permission#INTERACT_ACROSS_USERS`, or`android.Manifest.permission#INTERACT_ACROSS_USERS_FULL`permission. Both the caller and target user profiles must be in the same profile group. The target user must be a valid user returned from [getTargetUserProfiles()](CrossProfileApps.md)). 
Requires [android.Manifest.permission#INTERACT_ACROSS_PROFILES](../android/Manifest.permission.md) or android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md):The intent to launch. A component in the caller package must be specified. This value cannot be`null`. |
| `targetUser` | [UserHandle](../android.os/UserHandle.md):The [UserHandle](../android.os/UserHandle.md) of the profile; must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md))if different to the calling user, otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](../android.app/Activity.md)?:The activity to start the new activity from for the purposes of passing back any result and deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task and no result will be returned. |
| --- | --- |

### startActivity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivity(
    intent: Intent, 
    targetUser: UserHandle, 
    callingActivity: Activity?, 
    options: Bundle?
): Unit
```

Starts the specified activity of the caller package in the specified profile.

The caller must have the [android.Manifest.permission#INTERACT_ACROSS_PROFILES](../android/Manifest.permission.md),`android.Manifest.permission#INTERACT_ACROSS_USERS`, or`android.Manifest.permission#INTERACT_ACROSS_USERS_FULL`permission. Both the caller and target user profiles must be in the same profile group. The target user must be a valid user returned from [getTargetUserProfiles()](CrossProfileApps.md)). 
Requires [android.Manifest.permission#INTERACT_ACROSS_PROFILES](../android/Manifest.permission.md) or android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md):The intent to launch. A component in the caller package must be specified. This value cannot be`null`. |
| `targetUser` | [UserHandle](../android.os/UserHandle.md):The [UserHandle](../android.os/UserHandle.md) of the profile; must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md))if different to the calling user, otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](../android.app/Activity.md)?:The activity to start the new activity from for the purposes of passing back any result and deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task and no result will be returned. |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)?:The activity options or`null`. See [android.app.ActivityOptions](../android.app/ActivityOptions.md). |

### startMainActivity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startMainActivity(
    component: ComponentName, 
    targetUser: UserHandle
): Unit
```

Starts the specified main activity of the caller package in the specified profile.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `component` | [ComponentName](../android.content/ComponentName.md):The ComponentName of the activity to launch, it must be exported and has action [android.content.Intent#ACTION_MAIN](../android.content/Intent.md), category [android.content.Intent#CATEGORY_LAUNCHER](../android.content/Intent.md). Otherwise, SecurityException will be thrown. This value cannot be`null`. |
| `targetUser` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |

### startMainActivity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startMainActivity(
    component: ComponentName, 
    targetUser: UserHandle, 
    callingActivity: Activity?, 
    options: Bundle?
): Unit
```

Starts the specified main activity of the caller package in the specified profile, launching in the specified activity.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `component` | [ComponentName](../android.content/ComponentName.md):The ComponentName of the activity to launch, it must be exported and has action [android.content.Intent#ACTION_MAIN](../android.content/Intent.md), category [android.content.Intent#CATEGORY_LAUNCHER](../android.content/Intent.md). Otherwise, SecurityException will be thrown. This value cannot be`null`. |
| `targetUser` | [UserHandle](../android.os/UserHandle.md):The UserHandle of the profile, must be one of the users returned by [getTargetUserProfiles()](CrossProfileApps.md)), otherwise a [SecurityException](../java.lang/SecurityException.md) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](../android.app/Activity.md)?:The activity to start the new activity from for the purposes of deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task. |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)?:The activity options or`null`. See [android.app.ActivityOptions](../android.app/ActivityOptions.md). |
