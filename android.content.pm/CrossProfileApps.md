# CrossProfileApps

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossProfileApps

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/CrossProfileApps "View this page in Java") 

```
open class CrossProfileApps
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.CrossProfileApps](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#) |

Class for handling cross profile operations. Apps can use this class to interact with its instance in any profile that is in [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()). For example, app can use this class to start its main activity in managed profile. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED:kotlin.String) Broadcast signalling that the receiving app's permission to interact across profiles has changed. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canInteractAcrossProfiles](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canInteractAcrossProfiles())`()` Returns whether the calling package can interact across profiles. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canRequestInteractAcrossProfiles](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles())`()` Returns whether the calling package can request to navigate the user to the relevant settings page to request user consent to interact across profiles. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | [createRequestInteractAcrossProfilesIntent](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#createRequestInteractAcrossProfilesIntent())`()` Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to open the settings page that allows the user to decide whether the calling app can interact across profiles. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | [getProfileSwitchingIconDrawable](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getProfileSwitchingIconDrawable(android.os.UserHandle))`(`userHandle:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`)` Return a drawable that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getProfileSwitchingLabel](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getProfileSwitchingLabel(android.os.UserHandle))`(`userHandle:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`)` Return a label that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)!\> | [getTargetUserProfiles](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles())`()` Return a list of user profiles that that the caller can use when calling other APIs in this class. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isManagedProfile](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#isManagedProfile(android.os.UserHandle))`(`userHandle:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`)` Checks if the specified user is a managed profile. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProfile](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#isProfile(android.os.UserHandle))`(`userHandle:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`)` Checks if the specified user is a profile, i. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startActivity(android.content.Intent,%20android.os.UserHandle,%20android.app.Activity))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`, `targetUser:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`, `callingActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?`)` Starts the specified activity of the caller package in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startActivity(android.content.Intent,%20android.os.UserHandle,%20android.app.Activity,%20android.os.Bundle))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`, `targetUser:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`, `callingActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Starts the specified activity of the caller package in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMainActivity](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle))`(`component:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`, `targetUser:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`)` Starts the specified main activity of the caller package in the specified profile. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMainActivity](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle,%20android.app.Activity,%20android.os.Bundle))`(`component:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`, `targetUser:` ` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)`, `callingActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Starts the specified main activity of the caller package in the specified profile, launching in the specified activity. |

## Constants

### ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED: String
```

Broadcast signalling that the receiving app's permission to interact across profiles has changed. This includes the user, admin, or OEM changing their consent such that the permission for the app to interact across profiles has changed.

This broadcast is not sent when other circumstances result in a change to being able to interact across profiles in practice, such as the profile being turned off or removed, apps being uninstalled, etc. The methods [canInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canInteractAcrossProfiles())and [canRequestInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles())can be used by apps prior to attempting to interact across profiles or attempting to request user consent to interact across profiles.

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

- [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles())returns a non-empty list for the calling user.
- The user has previously consented to cross-profile communication for the calling package.
- The calling package has either been allowlisted by default by the OEM or has been explicitly allowlisted by the admin via [android.app.admin.DevicePolicyManager#setCrossProfilePackages(ComponentName, Set)](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setCrossProfilePackages(android.content.ComponentName,%20kotlin.collections.MutableSet)).

If`false`, the package's current ability to request user consent to interact across profiles can be checked with [canRequestInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles()). If`true`, user consent can be obtained via [createRequestInteractAcrossProfilesIntent()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#createRequestInteractAcrossProfilesIntent()). The package can then listen to [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED:kotlin.String) broadcasts.

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

If`true`, the navigation intent can be obtained via [createRequestInteractAcrossProfilesIntent()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#createRequestInteractAcrossProfilesIntent()). The package can then listen to [ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#ACTION_CAN_INTERACT_ACROSS_PROFILES_CHANGED:kotlin.String) broadcasts.

Specifically, returns whether the following are all true:

- `UserManager#getProfileIdsExcludingHidden(int)`returns at least one other profile for the calling user.
- The calling app has requested`android.Manifest.permission.INTERACT_ACROSS_PROFILES`in its manifest.
- The calling app is not a profile owner within the profile group of the calling user.

Note that in order for the user to be able to grant the consent, the requesting package must be allowlisted by the admin or the OEM and installed in the other profile. If this is not the case the user will be shown a message explaining why they can't grant the consent.

Note that user consent could already be granted if given a return value of`true`. The package's current ability to interact across profiles can be checked with [canInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canInteractAcrossProfiles()).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the calling package can request to interact across profiles. |

### createRequestInteractAcrossProfilesIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createRequestInteractAcrossProfilesIntent(): Intent
```

Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to open the settings page that allows the user to decide whether the calling app can interact across profiles.

The method [canRequestInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles())must be returning`true`.

Note that the user may already have given consent and the app may already be able to interact across profiles, even if [canRequestInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles())is`true`. The current ability to interact across profiles is given by [canInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canInteractAcrossProfiles()).

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to open the settings page that allows the user to decide whether the app can interact across profiles This value cannot be`null`. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if`mContext.getPackageName()`does not belong to the calling UID, or [canRequestInteractAcrossProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#canRequestInteractAcrossProfiles())is`false`. |

### getProfileSwitchingIconDrawable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProfileSwitchingIconDrawable(userHandle: UserHandle): Drawable
```

Return a drawable that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. For example, it may return a briefcase icon if the given user handle is the managed profile one.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | an icon that calling app can show user for the semantic of launching its own activity in specified user profile. This value cannot be`null`. |

**See Also**

- [#startMainActivity(ComponentName, UserHandle)](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle)) 

### getProfileSwitchingLabel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProfileSwitchingLabel(userHandle: UserHandle): CharSequence
```

Return a label that calling app can show to user for the semantic of profile switching -- launching its own activity in specified user profile. For example, it may return "Switch to work" if the given user handle is the managed profile one.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | a label that calling app can show user for the semantic of launching its own activity in the specified user profile. This value cannot be`null`. |

**See Also**

- [#startMainActivity(ComponentName, UserHandle)](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#startMainActivity(android.content.ComponentName,%20android.os.UserHandle)) 

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
- It is not hidden (ex. profile type [UserManager.USER_TYPE_PROFILE_PRIVATE](https://developer.android.com/reference/kotlin/android/os/UserManager.html#USER_TYPE_PROFILE_PRIVATE:kotlin.String))

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)!> | This value cannot be`null`. |

**See Also**

- [android.os.UserManager#getUserProfiles()](https://developer.android.com/reference/kotlin/android/os/UserManager.html#getUserProfiles()) 

### isManagedProfile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isManagedProfile(userHandle: UserHandle): Boolean
```

Checks if the specified user is a managed profile.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |

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
| `userHandle` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the target profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |

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

The caller must have the [android.Manifest.permission#INTERACT_ACROSS_PROFILES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERACT_ACROSS_PROFILES:kotlin.String),`android.Manifest.permission#INTERACT_ACROSS_USERS`, or`android.Manifest.permission#INTERACT_ACROSS_USERS_FULL`permission. Both the caller and target user profiles must be in the same profile group. The target user must be a valid user returned from [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()). 
Requires [android.Manifest.permission#INTERACT_ACROSS_PROFILES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERACT_ACROSS_PROFILES:kotlin.String) or android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):The intent to launch. A component in the caller package must be specified. This value cannot be`null`. |
| `targetUser` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) of the profile; must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles())if different to the calling user, otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?:The activity to start the new activity from for the purposes of passing back any result and deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task and no result will be returned. |

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

The caller must have the [android.Manifest.permission#INTERACT_ACROSS_PROFILES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERACT_ACROSS_PROFILES:kotlin.String),`android.Manifest.permission#INTERACT_ACROSS_USERS`, or`android.Manifest.permission#INTERACT_ACROSS_USERS_FULL`permission. Both the caller and target user profiles must be in the same profile group. The target user must be a valid user returned from [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()). 
Requires [android.Manifest.permission#INTERACT_ACROSS_PROFILES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERACT_ACROSS_PROFILES:kotlin.String) or android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):The intent to launch. A component in the caller package must be specified. This value cannot be`null`. |
| `targetUser` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) of the profile; must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles())if different to the calling user, otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?:The activity to start the new activity from for the purposes of passing back any result and deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task and no result will be returned. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:The activity options or`null`. See [android.app.ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#). |

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
| `component` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#):The ComponentName of the activity to launch, it must be exported and has action [android.content.Intent#ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String), category [android.content.Intent#CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String). Otherwise, SecurityException will be thrown. This value cannot be`null`. |
| `targetUser` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |

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
| `component` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#):The ComponentName of the activity to launch, it must be exported and has action [android.content.Intent#ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String), category [android.content.Intent#CATEGORY_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String). Otherwise, SecurityException will be thrown. This value cannot be`null`. |
| `targetUser` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#):The UserHandle of the profile, must be one of the users returned by [getTargetUserProfiles()](https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps#getTargetUserProfiles()), otherwise a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) will be thrown. This value cannot be`null`. |
| `callingActivity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?:The activity to start the new activity from for the purposes of deciding which task the new activity should belong to. If`null`, the activity will always be started in a new task. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:The activity options or`null`. See [android.app.ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#). |
