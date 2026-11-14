# ShortcutInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShortcutInfo

Kotlin| [Java](ShortcutInfo.md) 
| --- | --- |

```
class ShortcutInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ShortcutInfo](ShortcutInfo.md) |

Represents a shortcut that can be published via [ShortcutManager](ShortcutManager.md).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/content/pm/ShortcutInfo.Builder.md) Builder class for [ShortcutInfo](ShortcutInfo.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_APP_CHANGED](ShortcutInfo.md) Shortcut has been disabled due to changes to the publisher app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_BACKUP_NOT_SUPPORTED](ShortcutInfo.md) Shortcut has not been restored because the publisher app does not support backup and restore. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_BY_APP](ShortcutInfo.md) Shortcut has been disabled by the publisher app with the [ShortcutManager.disableShortcuts(List)](ShortcutManager.md))API. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_NOT_DISABLED](ShortcutInfo.md) Shortcut is not disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_OTHER_RESTORE_ISSUE](ShortcutInfo.md) Shortcut has not been restored for unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_SIGNATURE_MISMATCH](ShortcutInfo.md) Shortcut has not been restored because the publisher app's signature has changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_UNKNOWN](ShortcutInfo.md) Shortcut is disabled for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_VERSION_LOWER](ShortcutInfo.md) Shortcut has been restored from the previous device, but the publisher app on the current device is of a lower version. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SHORTCUT_CATEGORY_CONVERSATION](ShortcutInfo.md) Shortcut category for messaging related actions, such as chat. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_LAUNCHER](ShortcutInfo.md) Indicates system surfaces managed by a launcher app. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ShortcutInfo](ShortcutInfo.md) | [createFromGenericDocument](ShortcutInfo.md))`(`context:` ` [Context](../android.content/Context.md)`, `document:` ` [GenericDocument](../android.app.appsearch/GenericDocument.md)`)` Convert a [GenericDocument](../android.app.appsearch/GenericDocument.md) into a ShortcutInfo. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ShortcutInfo.md))`()` <br /> |
| [ComponentName](../android.content/ComponentName.md)? | [getActivity](ShortcutInfo.md))`()` Return the target activity. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Capability](Capability.md)!\> | [getCapabilities](ShortcutInfo.md))`()` Return a list of [Capability](Capability.md) associated with the shortcut. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CapabilityParams](CapabilityParams.md)!\> | [getCapabilityParams](ShortcutInfo.md))`(`capability:` ` [Capability](Capability.md)`)` Returns the [CapabilityParams](CapabilityParams.md) in associated with given capability. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getCategories](ShortcutInfo.md))`()` Return the shortcut's categories. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDisabledMessage](ShortcutInfo.md))`()` Return the message that should be shown when the user attempts to start a shortcut that is disabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisabledReason](ShortcutInfo.md))`()` Returns why a shortcut has been disabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExcludedFromSurfaces](ShortcutInfo.md))`()` Returns a bitmask of all surfaces this shortcut is excluded from. |
| --- | --- |
| [PersistableBundle](../android.os/PersistableBundle.md)? | [getExtras](ShortcutInfo.md))`()` Extras that the app can set for any purpose. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](ShortcutInfo.md))`()` Returns the ID of a shortcut. |
| [Intent](../android.content/Intent.md)? | [getIntent](ShortcutInfo.md))`()` Returns the intent that is executed when the user selects this shortcut. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](../android.content/Intent.md)!\>? | [getIntents](ShortcutInfo.md))`()` Return the intent set with[Builder.setIntents(Intent[])](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntents(kotlin.Array)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastChangedTimestamp](ShortcutInfo.md))`()` Last time when any of the fields was updated. |
| [LocusId](../android.content/LocusId.md)? | [getLocusId](ShortcutInfo.md))`()` Gets the [LocusId](../android.content/LocusId.md) associated with this shortcut. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getLongLabel](ShortcutInfo.md))`()` Return the long description of a shortcut. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackage](ShortcutInfo.md))`()` Return the package name of the publisher app. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRank](ShortcutInfo.md))`()` "Rank" of a shortcut, which is a non-negative, sequential value that's unique for each [getActivity](ShortcutInfo.md))for each of the two types of shortcuts (static and dynamic). |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getShortLabel](ShortcutInfo.md))`()` Return the short description of a shortcut. |
| [UserHandle](../android.os/UserHandle.md)! | [getUserHandle](ShortcutInfo.md))`()` [UserHandle](../android.os/UserHandle.md) on which the publisher created this shortcut. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKeyFieldsOnly](ShortcutInfo.md))`()` Return whether a shortcut only contains "key" information only or not. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCached](ShortcutInfo.md))`()` Return whether a shortcut is cached. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclaredInManifest](ShortcutInfo.md))`()` Return whether a shortcut is static; that is, whether a shortcut is published from AndroidManifest. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDynamic](ShortcutInfo.md))`()` Return whether a shortcut is dynamic. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](ShortcutInfo.md))`()` Returns`false`if a shortcut is disabled with android. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExcludedFromSurfaces](ShortcutInfo.md))`(`surface:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the shortcut is excluded from specified surface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImmutable](ShortcutInfo.md))`()` Return if a shortcut is immutable, in which case it cannot be modified with any of [ShortcutManager](ShortcutManager.md) APIs. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinned](ShortcutInfo.md))`()` Return whether a shortcut is pinned. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ShortcutInfo.md))`()` Return a string representation, intended for logging. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ShortcutInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ShortcutInfo](ShortcutInfo.md)!\> | [CREATOR](ShortcutInfo.md) <br /> |

## Constants

### DISABLED_REASON_APP_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_APP_CHANGED: Int
```

Shortcut has been disabled due to changes to the publisher app. (e.g. a manifest shortcut no longer exists.) 

 Value: 2

### DISABLED_REASON_BACKUP_NOT_SUPPORTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_BACKUP_NOT_SUPPORTED: Int
```

Shortcut has not been restored because the publisher app does not support backup and restore. 

 Value: 101

### DISABLED_REASON_BY_APP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_BY_APP: Int
```

Shortcut has been disabled by the publisher app with the [ShortcutManager.disableShortcuts(List)](ShortcutManager.md))API. 

 Value: 1

### DISABLED_REASON_NOT_DISABLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_NOT_DISABLED: Int
```

Shortcut is not disabled. 

 Value: 0

### DISABLED_REASON_OTHER_RESTORE_ISSUE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_OTHER_RESTORE_ISSUE: Int
```

Shortcut has not been restored for unknown reason. 

 Value: 103

### DISABLED_REASON_SIGNATURE_MISMATCH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_SIGNATURE_MISMATCH: Int
```

Shortcut has not been restored because the publisher app's signature has changed. 

 Value: 102

### DISABLED_REASON_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_UNKNOWN: Int
```

Shortcut is disabled for an unknown reason. 

 Value: 3

### DISABLED_REASON_VERSION_LOWER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLED_REASON_VERSION_LOWER: Int
```

Shortcut has been restored from the previous device, but the publisher app on the current device is of a lower version. The shortcut will not be usable until the app is upgraded to the same version or higher. 

 Value: 100

### SHORTCUT_CATEGORY_CONVERSATION

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHORTCUT_CATEGORY_CONVERSATION: String
```

Shortcut category for messaging related actions, such as chat. 

 Value: "android.shortcut.conversation"

### SURFACE_LAUNCHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SURFACE_LAUNCHER: Int
```

Indicates system surfaces managed by a launcher app. e.g. Long-Press Menu. 

 Value: 1

## Public methods

### createFromGenericDocument

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createFromGenericDocument(
    context: Context, 
    document: GenericDocument
): ShortcutInfo
```

Convert a [GenericDocument](../android.app.appsearch/GenericDocument.md) into a ShortcutInfo.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):Client context This value cannot be`null`. |
| `document` | [GenericDocument](../android.app.appsearch/GenericDocument.md):An instance of [GenericDocument](../android.app.appsearch/GenericDocument.md) that represents the shortcut. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [ShortcutInfo](ShortcutInfo.md) | This value cannot be`null`. |

### describeContents

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getActivity

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivity(): ComponentName?
```

Return the target activity.

This has nothing to do with the activity that this shortcut will launch. Launcher apps should show the launcher icon for the returned activity alongside this shortcut.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](../android.content/ComponentName.md)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setActivity](../android/content/pm/ShortcutInfo.Builder.md)) 

### getCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilities(): MutableList<Capability!>
```

Return a list of [Capability](Capability.md) associated with the shortcut.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Capability](Capability.md)!> | This value cannot be`null`. |

### getCapabilityParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilityParams(capability: Capability): MutableList<CapabilityParams!>
```

Returns the [CapabilityParams](CapabilityParams.md) in associated with given capability.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Capability](Capability.md): [Capability](Capability.md) associated with the shortcut. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CapabilityParams](CapabilityParams.md)!> | This value cannot be`null`. |

### getCategories

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCategories(): MutableSet<String!>?
```

Return the shortcut's categories.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setCategories(Set)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getDisabledMessage

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisabledMessage(): CharSequence?
```

Return the message that should be shown when the user attempts to start a shortcut that is disabled.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setDisabledMessage(CharSequence)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getDisabledReason

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisabledReason(): Int
```

Returns why a shortcut has been disabled.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.pm.ShortcutInfo#DISABLED_REASON_NOT_DISABLED](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_BY_APP](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_APP_CHANGED](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_UNKNOWN](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_VERSION_LOWER](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_BACKUP_NOT_SUPPORTED](ShortcutInfo.md), [android.content.pm.ShortcutInfo#DISABLED_REASON_SIGNATURE_MISMATCH](ShortcutInfo.md), or [android.content.pm.ShortcutInfo#DISABLED_REASON_OTHER_RESTORE_ISSUE](ShortcutInfo.md) |

### getExcludedFromSurfaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludedFromSurfaces(): Int
```

Returns a bitmask of all surfaces this shortcut is excluded from.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or [android.content.pm.ShortcutInfo#SURFACE_LAUNCHER](ShortcutInfo.md) |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setExcludedFromSurfaces(int)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): PersistableBundle?
```

Extras that the app can set for any purpose.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [PersistableBundle](../android.os/PersistableBundle.md)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setExtras(PersistableBundle)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getId

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Returns the ID of a shortcut.

Shortcut IDs are unique within each publisher app and must be stable across devices so that shortcuts will still be valid when restored on a different device. See [ShortcutManager](ShortcutManager.md) for details.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getIntent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIntent(): Intent?
```

Returns the intent that is executed when the user selects this shortcut. If setIntents() was used, then return the last intent in the array.

Launcher apps**cannot** see the intent. If a [ShortcutInfo](ShortcutInfo.md) is obtained via [LauncherApps](LauncherApps.md), then this method will always return null. Launchers can only start a shortcut intent with android.content.pm.LauncherApps#startShortcut. 
**See Also**

- [android.content.pm.ShortcutInfo.Builder#setIntent(Intent)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getIntents

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIntents(): Array<Intent!>?
```

Return the intent set with[Builder.setIntents(Intent[])](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntents(kotlin.Array)).

Launcher apps**cannot** see the intents. If a [ShortcutInfo](ShortcutInfo.md) is obtained via [LauncherApps](LauncherApps.md), then this method will always return null. Launchers can only start a shortcut intent with android.content.pm.LauncherApps#startShortcut. 
**See Also**

- [android.content.pm.ShortcutInfo.Builder#setIntents(Intent[])](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntents(kotlin.Array)) 

### getLastChangedTimestamp

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastChangedTimestamp(): Long
```

Last time when any of the fields was updated. 

### getLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocusId(): LocusId?
```

Gets the [LocusId](../android.content/LocusId.md) associated with this shortcut.

Used by the device's intelligence services to correlate objects (such as [Notification](../android.app/Notification.md) and [ContentCaptureContext](../android.view.contentcapture/ContentCaptureContext.md)) that are correlated.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [LocusId](../android.content/LocusId.md)? | This value may be`null`. |

### getLongLabel

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLongLabel(): CharSequence?
```

Return the long description of a shortcut.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setLongLabel(CharSequence)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getPackage

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackage(): String
```

Return the package name of the publisher app.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getRank

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRank(): Int
```

"Rank" of a shortcut, which is a non-negative, sequential value that's unique for each [getActivity](ShortcutInfo.md))for each of the two types of shortcuts (static and dynamic).

*Floating shortcuts* , or shortcuts that are neither static nor dynamic, will all have rank 0, because they aren't sorted. See the [ShortcutManager](ShortcutManager.md)'s class javadoc for details. 
**See Also**

- [android.content.pm.ShortcutInfo.Builder#setRank(int)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getShortLabel

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShortLabel(): CharSequence?
```

Return the short description of a shortcut.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setShortLabel(CharSequence)](../android/content/pm/ShortcutInfo.Builder.md)) 

### getUserHandle

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserHandle(): UserHandle!
```

[UserHandle](../android.os/UserHandle.md) on which the publisher created this shortcut. 

### hasKeyFieldsOnly

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasKeyFieldsOnly(): Boolean
```

Return whether a shortcut only contains "key" information only or not. If true, only the following fields are available.

- [getId()](ShortcutInfo.md))
- [getPackage()](ShortcutInfo.md))
- [getActivity()](ShortcutInfo.md))
- [getLastChangedTimestamp()](ShortcutInfo.md))
- [isDynamic()](ShortcutInfo.md))
- [isPinned()](ShortcutInfo.md))
- [isDeclaredInManifest()](ShortcutInfo.md))
- [isImmutable()](ShortcutInfo.md))
- [isEnabled()](ShortcutInfo.md))
- [getUserHandle()](ShortcutInfo.md))

<br />

For performance reasons, shortcuts passed to [LauncherApps.Callback.onShortcutsChanged(String, List, UserHandle)](../android/content/pm/LauncherApps.Callback.md))as well as those returned from [LauncherApps.getShortcuts(ShortcutQuery, UserHandle)](LauncherApps.md))while using the [ShortcutQuery.FLAG_GET_KEY_FIELDS_ONLY](../android/content/pm/LauncherApps.ShortcutQuery.md) option contain only key information. 

### isCached

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCached(): Boolean
```

Return whether a shortcut is cached. 

### isDeclaredInManifest

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDeclaredInManifest(): Boolean
```

Return whether a shortcut is static; that is, whether a shortcut is published from AndroidManifest.xml. If`true`, the shortcut is also [isImmutable()](ShortcutInfo.md)).

When an app is upgraded and a shortcut is no longer published from AndroidManifest.xml, this will be set to`false`. If the shortcut is not pinned, then it'll disappear. However, if it's pinned, it will still be visible, [isEnabled()](ShortcutInfo.md))will be`false`and [isImmutable()](ShortcutInfo.md))will be`true`. 

### isDynamic

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDynamic(): Boolean
```

Return whether a shortcut is dynamic. 

### isEnabled

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Returns`false`if a shortcut is disabled with android.content.pm.ShortcutManager#disableShortcuts. 

### isExcludedFromSurfaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isExcludedFromSurfaces(surface: Int): Boolean
```

Return true if the shortcut is excluded from specified surface.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or [android.content.pm.ShortcutInfo#SURFACE_LAUNCHER](ShortcutInfo.md) |

### isImmutable

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isImmutable(): Boolean
```

Return if a shortcut is immutable, in which case it cannot be modified with any of [ShortcutManager](ShortcutManager.md) APIs.

All static shortcuts are immutable. When a static shortcut is pinned and is then disabled because it doesn't appear in AndroidManifest.xml for a newer version of the app, [isDeclaredInManifest()](ShortcutInfo.md))returns`false`, but the shortcut is still immutable.

All shortcuts originally published via the [ShortcutManager](ShortcutManager.md) APIs are all mutable. 

### isPinned

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPinned(): Boolean
```

Return whether a shortcut is pinned. 

### toString

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return a string representation, intended for logging. Some fields will be retracted.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ShortcutInfo!>
```
