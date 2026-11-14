# NotificationChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotificationChannel

Kotlin| [Java](https://developer.android.com/reference/android/app/NotificationChannel "View this page in Java") 
| --- | --- |

```
class NotificationChannel : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.NotificationChannel](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#) |

A representation of settings that apply to a collection of similarly themed notifications.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_CHANNEL_ID](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#DEFAULT_CHANNEL_ID:kotlin.String) The id of the default channel for an app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_CONVERSATION](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_CONVERSATION:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_IMPORTANCE](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_IMPORTANCE:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_LAUNCHER](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_LAUNCHER:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_LOCKED_DEVICE](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_LOCKED_DEVICE:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_SOUND](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_SOUND:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_VIBRATION](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_VIBRATION:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EDIT_ZEN](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#EDIT_ZEN:kotlin.String) Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NotificationChannel](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#NotificationChannel(kotlin.String,%20kotlin.CharSequence,%20kotlin.Int))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `importance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a notification channel. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canBubble](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#canBubble())`()` Returns whether notifications posted to this channel are allowed to display outside of the notification shade, in a floating window on top of other apps. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canBypassDnd](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#canBypassDnd())`()` Whether or not notifications posted to this channel can bypass the Do Not Disturb [NotificationManager.INTERRUPTION_FILTER_PRIORITY](https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int) mode when the active policy allows priority channels to bypass notification filtering. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canShowBadge](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#canShowBadge())`()` Returns whether notifications posted to this channel can appear as badges in a Launcher application. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#describeContents())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableLights](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableLights(kotlin.Boolean))`(`lights:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether notifications posted to this channel should display notification lights, on devices that support that feature. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableVibration](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean))`(`vibration:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether notification posted to this channel should vibrate. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#)! | [getAudioAttributes](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getAudioAttributes())`()` Returns the audio attributes for sound played by notifications posted to this channel. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getConversationId](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getConversationId())`()` Returns the [id](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#getId())of the conversation backing this channel, if it's associated with a conversation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getDescription())`()` Returns the user visible description of this channel. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getGroup](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getGroup())`()` Returns what group this channel belongs to. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getId](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getId())`()` Returns the id of this channel. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getImportance](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance())`()` Returns the user specified importance e. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLightColor](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getLightColor())`()` Returns the notification light color for notifications posted to this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLockscreenVisibility](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getLockscreenVisibility())`()` Returns whether or not notifications posted to this channel are shown on the lockscreen in full or redacted form. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getName())`()` Returns the user visible name of this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOriginalImportance](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getOriginalImportance())`()` Returns the app-defined importance for this channel, prior to any user modifications. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getParentChannelId](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getParentChannelId())`()` Returns the [id](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getId())of the parent notification channel to this channel, if it's a conversation related channel. |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getSound](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getSound())`()` Returns the notification sound for this channel. |
| [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#)? | [getVibrationEffect](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationEffect())`()` Returns the [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) for notifications posted to this channel. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [getVibrationPattern](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationPattern())`()` Returns the vibration pattern for notifications posted to this channel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasUserSetImportance](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#hasUserSetImportance())`()` Returns whether the user has chosen the importance of this channel, either to affirm the initial selection from the app, or changed it to be higher or lower. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasUserSetSound](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#hasUserSetSound())`()` Returns whether the user has chosen the sound of this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#hashCode())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlockable](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#isBlockable())`()` Returns whether this channel is always blockable, even if the app is 'fixed' as non-blockable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConversation](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#isConversation())`()` Whether or not this channel represents a conversation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDemoted](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#isDemoted())`()` Returns whether the user has decided that this channel does not represent a conversation. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImportantConversation](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#isImportantConversation())`()` Whether or not notifications in this conversation are considered important. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowBubbles](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setAllowBubbles(kotlin.Boolean))`(`allowBubbles:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` As of Android 11 this value is no longer respected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlockable](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setBlockable(kotlin.Boolean))`(`blockable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows users to block notifications sent through this channel, if this channel belongs to a package that otherwise would have notifications "fixed" as enabled. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBypassDnd](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setBypassDnd(kotlin.Boolean))`(`bypassDnd:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not notifications posted to this channel can interrupt the user in [android.app.NotificationManager#INTERRUPTION_FILTER_PRIORITY](https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int) mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConversationId](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setConversationId(kotlin.String,%20kotlin.String))`(`parentChannelId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `conversationId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets this channel as being converastion-centric. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDescription](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setDescription(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the user visible description of this channel. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroup](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setGroup(kotlin.String))`(`groupId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets what group this channel belongs to. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setImportance](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setImportance(kotlin.Int))`(`importance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the level of interruption of this notification channel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightColor](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setLightColor(kotlin.Int))`(`argb:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the notification light color for notifications posted to this channel, if lights are [enabled](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableLights(kotlin.Boolean))on this channel and the device supports that feature. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLockscreenVisibility](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setLockscreenVisibility(kotlin.Int))`(`lockscreenVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets whether notifications posted to this channel appear on the lockscreen or not, and if so, whether they appear in a redacted form. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setName(kotlin.CharSequence))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the user visible name of this channel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowBadge](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setShowBadge(kotlin.Boolean))`(`showBadge:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether notifications posted to this channel can appear as application icon badges in a Launcher. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSound](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setSound(android.net.Uri,%20android.media.AudioAttributes))`(`sound:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `audioAttributes:` ` [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#)!`)` Sets the sound that should be played for notifications posted to this channel and its audio attributes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVibrationEffect](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationEffect(android.os.VibrationEffect))`(`effect:` ` [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#)?`)` Sets a [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) for notifications posted to this channel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVibrationPattern](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationPattern(kotlin.LongArray))`(`vibrationPattern:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Sets the vibration pattern for notifications posted to this channel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldShowLights](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights())`()` Returns whether notifications posted to this channel trigger notification lights. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldVibrate](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldVibrate())`()` Returns whether notifications posted to this channel always vibrate. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NotificationChannel](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### DEFAULT_CHANNEL_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_CHANNEL_ID: String
```

The id of the default channel for an app. This id is reserved by the system. All notifications posted from apps targeting [android.os.Build.VERSION_CODES#N_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int) or earlier without a notification channel specified are posted to this channel. 

 Value: "miscellaneous"

### EDIT_CONVERSATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_CONVERSATION: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing conversation settings (demoting or restoring a channel to be a Conversation, changing bubble behavior, or setting the priority of a conversation). 

 Value: "conversation"

### EDIT_IMPORTANCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_IMPORTANCE: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing importance ([setImportance(int)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setImportance(kotlin.Int))) and/or conversation priority. 

 Value: "importance"

### EDIT_LAUNCHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_LAUNCHER: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing launcher behavior (showing badges)}. 

 Value: "launcher"

### EDIT_LOCKED_DEVICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_LOCKED_DEVICE: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing behavior on devices that are locked or have a turned off display ([setLockscreenVisibility(int)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setLockscreenVisibility(kotlin.Int)), [enableLights(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableLights(kotlin.Boolean)), [setLightColor(int)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setLightColor(kotlin.Int))). 

 Value: "locked"

### EDIT_SOUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_SOUND: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing sound, like a tone picker ([setSound(android.net.Uri,android.media.AudioAttributes)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setSound(android.net.Uri,%20android.media.AudioAttributes))). 

 Value: "sound"

### EDIT_VIBRATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_VIBRATION: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing vibration ([enableVibration(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean)),[setVibrationPattern(long[])](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationPattern(kotlin.LongArray))). 

 Value: "vibration"

### EDIT_ZEN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_ZEN: String
```

Extra value for [Settings.EXTRA_CHANNEL_FILTER_LIST](https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_CHANNEL_FILTER_LIST:kotlin.String). Include to show fields that have to do with editing do not disturb bypass {(@link #setBypassDnd(boolean)}) . 

 Value: "zen"

## Public constructors

### NotificationChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotificationChannel(
    id: String!, 
    name: CharSequence!, 
    importance: Int)
```

Creates a notification channel.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The id of the channel. Must be unique per package. The value may be truncated if it is too long. |
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The user visible name of the channel. You can rename this channel when the system locale changes by listening for the [Intent.ACTION_LOCALE_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_LOCALE_CHANGED:kotlin.String) broadcast. The recommended maximum length is 40 characters; the value may be truncated if it is too long. |
| `importance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The importance of the channel. This controls how interruptive notifications posted to this channel are. Value is [android.app.NotificationManager#IMPORTANCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_NONE](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_MIN](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_LOW](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_DEFAULT](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int), or [android.app.NotificationManager#IMPORTANCE_HIGH](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int) |
| --- | --- |

## Public methods

### canBubble

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canBubble(): Boolean
```

Returns whether notifications posted to this channel are allowed to display outside of the notification shade, in a floating window on top of other apps. 
**See Also**

- [android.app.Notification#getBubbleMetadata()](https://developer.android.com/reference/kotlin/android/app/Notification#getBubbleMetadata()) 

### canBypassDnd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canBypassDnd(): Boolean
```

Whether or not notifications posted to this channel can bypass the Do Not Disturb [NotificationManager.INTERRUPTION_FILTER_PRIORITY](https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int) mode when the active policy allows priority channels to bypass notification filtering. 

### canShowBadge

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canShowBadge(): Boolean
```

Returns whether notifications posted to this channel can appear as badges in a Launcher application. Note that badging may be disabled for other reasons. 

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### enableLights

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enableLights(lights: Boolean): Unit
```

Sets whether notifications posted to this channel should display notification lights, on devices that support that feature. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)). 

### enableVibration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enableVibration(vibration: Boolean): Unit
```

Sets whether notification posted to this channel should vibrate. The vibration pattern can be set with[setVibrationPattern(long[])](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationPattern(kotlin.LongArray)). Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)). 

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAudioAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioAttributes(): AudioAttributes!
```

Returns the audio attributes for sound played by notifications posted to this channel. 

### getConversationId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConversationId(): String?
```

Returns the [id](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#getId())of the conversation backing this channel, if it's associated with a conversation. See [setConversationId(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setConversationId(kotlin.String,%20kotlin.String)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getDescription

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String!
```

Returns the user visible description of this channel. 

### getGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGroup(): String!
```

Returns what group this channel belongs to. This is used only for visually grouping channels in the UI. 

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String!
```

Returns the id of this channel. 

### getImportance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getImportance(): Int
```

Returns the user specified importance e.g. [NotificationManager.IMPORTANCE_LOW](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int) for notifications posted to this channel. Note: This value might be \> [NotificationManager.IMPORTANCE_NONE](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int), but notifications posted to this channel will not be shown to the user if the parent [NotificationChannelGroup](https://developer.android.com/reference/kotlin/android/app/NotificationChannelGroup) or app is blocked. See [NotificationChannelGroup.isBlocked()](https://developer.android.com/reference/kotlin/android/app/NotificationChannelGroup#isBlocked())and [NotificationManager.areNotificationsEnabled()](https://developer.android.com/reference/kotlin/android/app/NotificationManager#areNotificationsEnabled()).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.NotificationManager#IMPORTANCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_NONE](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_MIN](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_LOW](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_DEFAULT](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int), or [android.app.NotificationManager#IMPORTANCE_HIGH](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int) |

### getLightColor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLightColor(): Int
```

Returns the notification light color for notifications posted to this channel. Irrelevant unless [shouldShowLights()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()). 

### getLockscreenVisibility

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLockscreenVisibility(): Int
```

Returns whether or not notifications posted to this channel are shown on the lockscreen in full or redacted form. 

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): CharSequence!
```

Returns the user visible name of this channel. 

### getOriginalImportance

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOriginalImportance(): Int
```

Returns the app-defined importance for this channel, prior to any user modifications. This may differ from [getImportance()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance())if the user has changed the setting. Typically reflects the channel's initial importance set upon creation.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The original importance as set by the app. Value is [android.app.NotificationManager#IMPORTANCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_NONE](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_MIN](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_LOW](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_DEFAULT](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int), or [android.app.NotificationManager#IMPORTANCE_HIGH](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance()> 

### getParentChannelId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParentChannelId(): String?
```

Returns the [id](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getId())of the parent notification channel to this channel, if it's a conversation related channel. See [setConversationId(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setConversationId(kotlin.String,%20kotlin.String)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getSound

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSound(): Uri!
```

Returns the notification sound for this channel. 

### getVibrationEffect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVibrationEffect(): VibrationEffect?
```

Returns the [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) for notifications posted to this channel. The returned effect is derived from either the effect provided in the [setVibrationEffect(android.os.VibrationEffect)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationEffect(android.os.VibrationEffect))method, or the equivalent vibration effect of the pattern set via the[setVibrationPattern(long[])](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationPattern(kotlin.LongArray))method, based on setter method that was called last. The returned effect will be ignored in one of the following cases:

- vibration is not enabled for the channel (i.e. [shouldVibrate()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldVibrate())returns`false`).
- the effect is not supported/playable by the device. In this case, if vibration is enabled for the channel, the default channel vibration will be used instead.

<br />

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#)? | the [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) set via [setVibrationEffect(android.os.VibrationEffect)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationEffect(android.os.VibrationEffect)), or the equivalent of the vibration set via[setVibrationPattern(long[])](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#setVibrationPattern(kotlin.LongArray)). This value may be`null`. |

**See Also**

- [android.os.VibrationEffect#createWaveform(long[], int)](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#createWaveform(kotlin.LongArray,%20kotlin.Int)) 

### getVibrationPattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVibrationPattern(): LongArray!
```

Returns the vibration pattern for notifications posted to this channel. Will be ignored if vibration is not enabled ([shouldVibrate()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldVibrate())). 

### hasUserSetImportance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasUserSetImportance(): Boolean
```

Returns whether the user has chosen the importance of this channel, either to affirm the initial selection from the app, or changed it to be higher or lower. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance()> 

### hasUserSetSound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasUserSetSound(): Boolean
```

Returns whether the user has chosen the sound of this channel. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getSound()> 

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isBlockable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBlockable(): Boolean
```

Returns whether this channel is always blockable, even if the app is 'fixed' as non-blockable. 

### isConversation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConversation(): Boolean
```

Whether or not this channel represents a conversation. 

### isDemoted

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDemoted(): Boolean
```

Returns whether the user has decided that this channel does not represent a conversation. The value will always be false for channels that never claimed to be conversations - that is, for channels where [getConversationId()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getConversationId())and [getParentChannelId()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getParentChannelId())are empty. 

### isImportantConversation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isImportantConversation(): Boolean
```

Whether or not notifications in this conversation are considered important.

Important conversations may get special visual treatment, and might be able to bypass DND.

This is only valid for channels that represent conversations, that is, where [isConversation()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#isConversation())is true. 

### setAllowBubbles

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAllowBubbles(allowBubbles: Boolean): Unit
```

As of Android 11 this value is no longer respected. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/NotificationChannel#canBubble()>
- [android.app.Notification#getBubbleMetadata()](https://developer.android.com/reference/kotlin/android/app/Notification#getBubbleMetadata()) 

### setBlockable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setBlockable(blockable: Boolean): Unit
```

Allows users to block notifications sent through this channel, if this channel belongs to a package that otherwise would have notifications "fixed" as enabled. If the channel does not belong to a package that has a fixed notification permission, this method does nothing, since such channels are blockable by default and cannot be set to be unblockable.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `blockable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, allows users to block notifications on this channel. |

### setBypassDnd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setBypassDnd(bypassDnd: Boolean): Unit
```

Sets whether or not notifications posted to this channel can interrupt the user in [android.app.NotificationManager#INTERRUPTION_FILTER_PRIORITY](https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int) mode.

Apps with Do Not Disturb policy access (see [NotificationManager.isNotificationPolicyAccessGranted()](https://developer.android.com/reference/kotlin/android/app/NotificationManager#isNotificationPolicyAccessGranted())) can set up their own channels this way, but only if the channel hasn't been updated by the user since its creation.

Otherwise, this value is only modifiable by the system and the notification ranker. 

### setConversationId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setConversationId(
    parentChannelId: String, 
    conversationId: String
): Unit
```

Sets this channel as being converastion-centric. Different settings and functionality may be exposed for conversation-centric channels.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentChannelId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The [getId()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getId())id} of the generic channel that notifications of this type would be posted to in absence of a specific conversation id. For example, if this channel represents 'Messages from Person A', the parent channel would be 'Messages.' This value cannot be`null`. |
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The [ShortcutInfo.getId()](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#getId())of the shortcut representing this channel's conversation. This value cannot be`null`. |

### setDescription

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDescription(description: String!): Unit
```

Sets the user visible description of this channel.

The recommended maximum length is 300 characters; the value may be truncated if it is too long. 

### setGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setGroup(groupId: String!): Unit
```

Sets what group this channel belongs to. Group information is only used for presentation, not for behavior. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)), unless the channel is not currently part of a group.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of a group created by [NotificationManager.createNotificationChannelGroup(NotificationChannelGroup)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannelGroup(android.app.NotificationChannelGroup)). |

### setImportance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setImportance(importance: Int): Unit
```

Sets the level of interruption of this notification channel. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `importance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount the user should be interrupted by notifications from this channel. Value is [android.app.NotificationManager#IMPORTANCE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_NONE](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_MIN](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_LOW](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int), [android.app.NotificationManager#IMPORTANCE_DEFAULT](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int), or [android.app.NotificationManager#IMPORTANCE_HIGH](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int) |

### setLightColor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLightColor(argb: Int): Unit
```

Sets the notification light color for notifications posted to this channel, if lights are [enabled](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableLights(kotlin.Boolean))on this channel and the device supports that feature. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)). 

### setLockscreenVisibility

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLockscreenVisibility(lockscreenVisibility: Int): Unit
```

Sets whether notifications posted to this channel appear on the lockscreen or not, and if so, whether they appear in a redacted form. See e.g. [Notification.VISIBILITY_SECRET](https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_SECRET:kotlin.Int). Only modifiable by the system and notification ranker. 

### setName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setName(name: CharSequence!): Unit
```

Sets the user visible name of this channel.

The recommended maximum length is 40 characters; the value may be truncated if it is too long. 

### setShowBadge

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setShowBadge(showBadge: Boolean): Unit
```

Sets whether notifications posted to this channel can appear as application icon badges in a Launcher. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `showBadge` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if badges should be allowed to be shown. |

### setSound

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSound(
    sound: Uri!, 
    audioAttributes: AudioAttributes!
): Unit
```

Sets the sound that should be played for notifications posted to this channel and its audio attributes. Notification channels with an [importance](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance())of at least [NotificationManager.IMPORTANCE_DEFAULT](https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int) should have a sound. Note: An app-specific sound can be provided in the Uri parameter, but because channels are persistent for the duration of the app install, and are backed up and restored, the Uri should be stable. For this reason it is not recommended to use a [ContentResolver.SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_ANDROID_RESOURCE:kotlin.String) uri, as resource ids can change on app upgrade. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)). 

### setVibrationEffect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVibrationEffect(effect: VibrationEffect?): Unit
```

Sets a [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) for notifications posted to this channel. If the provided effect is non-null, will enable vibration on this channel (equivalent to calling [enableVibration(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean))with`true`). Otherwise vibration will be disabled unless [enableVibration(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean))is used with`true`, in which case the default vibration will be used.

The effect passed here will be returned from [getVibrationEffect()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationEffect()). If the provided [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) is an equivalent to a wave-form vibration pattern, the equivalent wave-form pattern will be returned from [getVibrationPattern()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationPattern()).

Note that some [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#) s may not be playable on some devices. In cases where such an effect is passed here, vibration will still be enabled for the channel, but the default vibration will be used. Nonetheless, the provided effect will be stored and be returned from [getVibrationEffect](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationEffect())calls, and could be used by the same channel on a different device, for example, in cases the user backs up and restores to a device that does have the ability to play the effect, where that effect will be used instead of the default. To avoid such issues that could make the vibration behavior of your notification channel differ among different devices, it's recommended that you avoid vibration effect primitives, as the support for them differs widely among devices (read [VibrationEffect.Composition](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.Composition.html#) for more on vibration primitives).

Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.html#)?:This value may be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationEffect()>
- [android.os.Vibrator#areEffectsSupported(int...)](https://developer.android.com/reference/kotlin/android/os/Vibrator.html#areEffectsSupported(kotlin.Int))
- [android.os.Vibrator#arePrimitivesSupported(int...)](https://developer.android.com/reference/kotlin/android/os/Vibrator.html#arePrimitivesSupported(kotlin.Int)) 

### setVibrationPattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVibrationPattern(vibrationPattern: LongArray!): Unit
```

Sets the vibration pattern for notifications posted to this channel. If the provided pattern is valid (non-null, non-empty with at least 1 non-zero value), will enable vibration on this channel (equivalent to calling [enableVibration(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean))with`true`). Otherwise, vibration will be disabled unless [enableVibration(boolean)](https://developer.android.com/reference/kotlin/android/app/NotificationChannel#enableVibration(kotlin.Boolean))is used with`true`, in which case the default vibration will be used. Only modifiable before the channel is submitted to [NotificationManager.createNotificationChannel(NotificationChannel)](https://developer.android.com/reference/kotlin/android/app/NotificationManager#createNotificationChannel(android.app.NotificationChannel)). 

### shouldShowLights

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldShowLights(): Boolean
```

Returns whether notifications posted to this channel trigger notification lights. 

### shouldVibrate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldVibrate(): Boolean
```

Returns whether notifications posted to this channel always vibrate. 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NotificationChannel!>
```
