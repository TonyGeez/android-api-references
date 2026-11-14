# ShortcutInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShortcutInfo

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/ShortcutInfo "View this page in Java") 

```
class ShortcutInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) |

Represents a shortcut that can be published via [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder) Builder class for [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_APP_CHANGED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_APP_CHANGED:kotlin.Int) Shortcut has been disabled due to changes to the publisher app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_BACKUP_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_BACKUP_NOT_SUPPORTED:kotlin.Int) Shortcut has not been restored because the publisher app does not support backup and restore. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_BY_APP](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_BY_APP:kotlin.Int) Shortcut has been disabled by the publisher app with the [ShortcutManager.disableShortcuts(List)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#disableShortcuts(kotlin.collections.MutableList))API. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_NOT_DISABLED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_NOT_DISABLED:kotlin.Int) Shortcut is not disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_OTHER_RESTORE_ISSUE](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_OTHER_RESTORE_ISSUE:kotlin.Int) Shortcut has not been restored for unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_SIGNATURE_MISMATCH](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_SIGNATURE_MISMATCH:kotlin.Int) Shortcut has not been restored because the publisher app's signature has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_UNKNOWN:kotlin.Int) Shortcut is disabled for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISABLED_REASON_VERSION_LOWER](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_VERSION_LOWER:kotlin.Int) Shortcut has been restored from the previous device, but the publisher app on the current device is of a lower version. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SHORTCUT_CATEGORY_CONVERSATION](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#SHORTCUT_CATEGORY_CONVERSATION:kotlin.String) Shortcut category for messaging related actions, such as chat. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#SURFACE_LAUNCHER:kotlin.Int) Indicates system surfaces managed by a launcher app. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) | [createFromGenericDocument](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#createFromGenericDocument(android.content.Context,%20android.app.appsearch.GenericDocument))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `document:` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#)`)` Convert a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#) into a ShortcutInfo. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#describeContents())`()` <br /> |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | [getActivity](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getActivity())`()` Return the target activity. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability)!\> | [getCapabilities](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getCapabilities())`()` Return a list of [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability) associated with the shortcut. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/CapabilityParams)!\> | [getCapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getCapabilityParams(android.content.pm.Capability))`(`capability:` ` [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability)`)` Returns the [CapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/CapabilityParams) in associated with given capability. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getCategories](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getCategories())`()` Return the shortcut's categories. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDisabledMessage](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getDisabledMessage())`()` Return the message that should be shown when the user attempts to start a shortcut that is disabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisabledReason](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getDisabledReason())`()` Returns why a shortcut has been disabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExcludedFromSurfaces](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getExcludedFromSurfaces())`()` Returns a bitmask of all surfaces this shortcut is excluded from. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getExtras())`()` Extras that the app can set for any purpose. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getId())`()` Returns the ID of a shortcut. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | [getIntent](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getIntent())`()` Returns the intent that is executed when the user selects this shortcut. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\>? | [getIntents](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getIntents())`()` Return the intent set with[Builder.setIntents(Intent[])](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntents(kotlin.Array)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastChangedTimestamp](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getLastChangedTimestamp())`()` Last time when any of the fields was updated. |
| [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#)? | [getLocusId](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getLocusId())`()` Gets the [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#) associated with this shortcut. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getLongLabel](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getLongLabel())`()` Return the long description of a shortcut. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackage](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getPackage())`()` Return the package name of the publisher app. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRank](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getRank())`()` "Rank" of a shortcut, which is a non-negative, sequential value that's unique for each [getActivity](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getActivity())for each of the two types of shortcuts (static and dynamic). |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getShortLabel](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getShortLabel())`()` Return the short description of a shortcut. |
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)! | [getUserHandle](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getUserHandle())`()` [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) on which the publisher created this shortcut. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKeyFieldsOnly](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#hasKeyFieldsOnly())`()` Return whether a shortcut only contains "key" information only or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCached](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isCached())`()` Return whether a shortcut is cached. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeclaredInManifest](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isDeclaredInManifest())`()` Return whether a shortcut is static; that is, whether a shortcut is published from AndroidManifest. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDynamic](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isDynamic())`()` Return whether a shortcut is dynamic. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isEnabled())`()` Returns`false`if a shortcut is disabled with android. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExcludedFromSurfaces](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isExcludedFromSurfaces(kotlin.Int))`(`surface:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the shortcut is excluded from specified surface. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImmutable](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isImmutable())`()` Return if a shortcut is immutable, in which case it cannot be modified with any of [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager) APIs. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPinned](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isPinned())`()` Return whether a shortcut is pinned. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#toString())`()` Return a string representation, intended for logging. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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

Shortcut has been disabled by the publisher app with the [ShortcutManager.disableShortcuts(List)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#disableShortcuts(kotlin.collections.MutableList))API. 

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

Convert a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#) into a ShortcutInfo.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Client context This value cannot be`null`. |
| `document` | [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#):An instance of [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#) that represents the shortcut. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) | This value cannot be`null`. |

### describeContents

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActivity

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivity(): ComponentName?
```

Return the target activity.

This has nothing to do with the activity that this shortcut will launch. Launcher apps should show the launcher icon for the returned activity alongside this shortcut.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setActivity](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setActivity(android.content.ComponentName)) 

### getCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilities(): MutableList<Capability!>
```

Return a list of [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability) associated with the shortcut.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability)!> | This value cannot be`null`. |

### getCapabilityParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilityParams(capability: Capability): MutableList<CapabilityParams!>
```

Returns the [CapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/CapabilityParams) in associated with given capability.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability): [Capability](https://developer.android.com/reference/kotlin/android/content/pm/Capability) associated with the shortcut. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CapabilityParams](https://developer.android.com/reference/kotlin/android/content/pm/CapabilityParams)!> | This value cannot be`null`. |

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

- [android.content.pm.ShortcutInfo.Builder#setCategories(Set)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setCategories(kotlin.collections.MutableSet)) 

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

- [android.content.pm.ShortcutInfo.Builder#setDisabledMessage(CharSequence)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setDisabledMessage(kotlin.CharSequence)) 

### getDisabledReason

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisabledReason(): Int
```

Returns why a shortcut has been disabled.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.pm.ShortcutInfo#DISABLED_REASON_NOT_DISABLED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_NOT_DISABLED:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_BY_APP](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_BY_APP:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_APP_CHANGED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_APP_CHANGED:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_UNKNOWN:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_VERSION_LOWER](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_VERSION_LOWER:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_BACKUP_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_BACKUP_NOT_SUPPORTED:kotlin.Int), [android.content.pm.ShortcutInfo#DISABLED_REASON_SIGNATURE_MISMATCH](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_SIGNATURE_MISMATCH:kotlin.Int), or [android.content.pm.ShortcutInfo#DISABLED_REASON_OTHER_RESTORE_ISSUE](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#DISABLED_REASON_OTHER_RESTORE_ISSUE:kotlin.Int) |

### getExcludedFromSurfaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludedFromSurfaces(): Int
```

Returns a bitmask of all surfaces this shortcut is excluded from.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or [android.content.pm.ShortcutInfo#SURFACE_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#SURFACE_LAUNCHER:kotlin.Int) |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setExcludedFromSurfaces(int)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setExcludedFromSurfaces(kotlin.Int)) 

### getExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): PersistableBundle?
```

Extras that the app can set for any purpose.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)? | This value may be`null`. |

**See Also**

- [android.content.pm.ShortcutInfo.Builder#setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setExtras(android.os.PersistableBundle)) 

### getId

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Returns the ID of a shortcut.

Shortcut IDs are unique within each publisher app and must be stable across devices so that shortcuts will still be valid when restored on a different device. See [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager) for details.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getIntent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIntent(): Intent?
```

Returns the intent that is executed when the user selects this shortcut. If setIntents() was used, then return the last intent in the array.

Launcher apps**cannot** see the intent. If a [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) is obtained via [LauncherApps](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps), then this method will always return null. Launchers can only start a shortcut intent with android.content.pm.LauncherApps#startShortcut. 
**See Also**

- [android.content.pm.ShortcutInfo.Builder#setIntent(Intent)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntent(android.content.Intent)) 

### getIntents

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIntents(): Array<Intent!>?
```

Return the intent set with[Builder.setIntents(Intent[])](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setIntents(kotlin.Array)).

Launcher apps**cannot** see the intents. If a [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#) is obtained via [LauncherApps](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps), then this method will always return null. Launchers can only start a shortcut intent with android.content.pm.LauncherApps#startShortcut. 
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

Gets the [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#) associated with this shortcut.

Used by the device's intelligence services to correlate objects (such as [Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#) and [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.html#)) that are correlated.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#)? | This value may be`null`. |

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

- [android.content.pm.ShortcutInfo.Builder#setLongLabel(CharSequence)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setLongLabel(kotlin.CharSequence)) 

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

"Rank" of a shortcut, which is a non-negative, sequential value that's unique for each [getActivity](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getActivity())for each of the two types of shortcuts (static and dynamic).

*Floating shortcuts* , or shortcuts that are neither static nor dynamic, will all have rank 0, because they aren't sorted. See the [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager)'s class javadoc for details. 
**See Also**

- [android.content.pm.ShortcutInfo.Builder#setRank(int)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setRank(kotlin.Int)) 

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

- [android.content.pm.ShortcutInfo.Builder#setShortLabel(CharSequence)](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.Builder#setShortLabel(kotlin.CharSequence)) 

### getUserHandle

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserHandle(): UserHandle!
```

[UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) on which the publisher created this shortcut. 

### hasKeyFieldsOnly

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasKeyFieldsOnly(): Boolean
```

Return whether a shortcut only contains "key" information only or not. If true, only the following fields are available.

- [getId()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getId())
- [getPackage()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getPackage())
- [getActivity()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getActivity())
- [getLastChangedTimestamp()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getLastChangedTimestamp())
- [isDynamic()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isDynamic())
- [isPinned()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isPinned())
- [isDeclaredInManifest()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isDeclaredInManifest())
- [isImmutable()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isImmutable())
- [isEnabled()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isEnabled())
- [getUserHandle()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#getUserHandle())

<br />

For performance reasons, shortcuts passed to [LauncherApps.Callback.onShortcutsChanged(String, List, UserHandle)](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.Callback#onShortcutsChanged(kotlin.String,%20kotlin.collections.MutableList,%20android.os.UserHandle))as well as those returned from [LauncherApps.getShortcuts(ShortcutQuery, UserHandle)](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps#getShortcuts(android.content.pm.LauncherApps.ShortcutQuery,%20android.os.UserHandle))while using the [ShortcutQuery.FLAG_GET_KEY_FIELDS_ONLY](https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.ShortcutQuery#FLAG_GET_KEY_FIELDS_ONLY:kotlin.Int) option contain only key information. 

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

Return whether a shortcut is static; that is, whether a shortcut is published from AndroidManifest.xml. If`true`, the shortcut is also [isImmutable()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isImmutable()).

When an app is upgraded and a shortcut is no longer published from AndroidManifest.xml, this will be set to`false`. If the shortcut is not pinned, then it'll disappear. However, if it's pinned, it will still be visible, [isEnabled()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isEnabled())will be`false`and [isImmutable()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isImmutable())will be`true`. 

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
| `surface` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or [android.content.pm.ShortcutInfo#SURFACE_LAUNCHER](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#SURFACE_LAUNCHER:kotlin.Int) |

### isImmutable

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isImmutable(): Boolean
```

Return if a shortcut is immutable, in which case it cannot be modified with any of [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager) APIs.

All static shortcuts are immutable. When a static shortcut is pinned and is then disabled because it doesn't appear in AndroidManifest.xml for a newer version of the app, [isDeclaredInManifest()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo#isDeclaredInManifest())returns`false`, but the shortcut is still immutable.

All shortcuts originally published via the [ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager) APIs are all mutable. 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ShortcutInfo!>
```
