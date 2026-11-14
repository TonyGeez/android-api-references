Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RingtoneManager

Kotlin | [Java](https://developer.android.com/reference/android/media/RingtoneManager "View this page in Java")

```
open class RingtoneManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.RingtoneManager](https://developer.android.com/reference/kotlin/android/media/RingtoneManager#) |

RingtoneManager provides access to ringtones, notification, and other types of sounds. It manages querying the different media providers and combines the results into a single cursor. It also provides a `https://developer.android.com/reference/kotlin/android/media/Ringtone` for each ringtone. We generically call these sounds ringtones, however the `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int` refers to the type of sounds that are suitable for the phone ringer.

To show a ringtone picker to the user, use the `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String` intent to launch the picker as a subactivity.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String` Activity Action: Shows a ringtone picker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_DEFAULT_URI:kotlin.String` Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_EXISTING_URI:kotlin.String` Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_INCLUDE_DRM:kotlin.String` Given to the ringtone picker as a boolean. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_PICKED_URI:kotlin.String` Returned from the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_SHOW_DEFAULT:kotlin.String` Given to the ringtone picker as a boolean. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_SHOW_SILENT:kotlin.String` Given to the ringtone picker as a boolean. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_TITLE:kotlin.String` Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_TYPE:kotlin.String` Given to the ringtone picker as an int. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ID_COLUMN_INDEX:kotlin.Int` The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the row ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TITLE_COLUMN_INDEX:kotlin.Int` The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the title. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALARM:kotlin.Int` Type that refers to sounds that are used for the alarm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALL:kotlin.Int` All types of sounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_NOTIFICATION:kotlin.Int` Type that refers to sounds that are used for notifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int` Type that refers to sounds that are used for the phone ringer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#URI_COLUMN_INDEX:kotlin.Int` The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the media provider's URI. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#RingtoneManager(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!)` Constructs a RingtoneManager. |
| `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#RingtoneManager(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Constructs a RingtoneManager. |

| Public methods ||
|---|---|
| open static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the current default sound's `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()()` Returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` of all the ringtones available. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getDefaultType(android.net.Uri)(defaultRingtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Returns the type of a default `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. |
| open static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getDefaultUri(kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for the default ringtone of a particular type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getIncludeDrm()()` Returns whether DRM ringtones will be included. |
| open [Ringtone](https://developer.android.com/reference/kotlin/android/media/Ringtone)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtone(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets a `https://developer.android.com/reference/kotlin/android/media/Ringtone` for the ringtone at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`. |
| open static [Ringtone](https://developer.android.com/reference/kotlin/android/media/Ringtone)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtone(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Returns a `https://developer.android.com/reference/kotlin/android/media/Ringtone` for a given sound URI. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtonePosition(android.net.Uri)(ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Gets the position of a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` within this `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#`. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtoneUri(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for the ringtone at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`. |
| open static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtoneUriForPhoneAccountHandle(android.content.Context,%20android.telecom.PhoneAccountHandle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, phoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#?)` Gets TYPE_RINGTONE's `https://developer.android.com/reference/kotlin/android/net/Uri.html#` by id of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getStopPreviousRingtone()()` <br /> |
| open static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getValidRingtoneUri(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Returns a valid ringtone URI. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#hasHapticChannels(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` contains haptic channels. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#hasHapticChannels(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` from a given sound URI contains haptics channels or not. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#hasHapticChannels(android.net.Uri)(ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` from a given sound URI contains haptic channels or not. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#inferStreamType()()` Infers the volume stream type based on what type of ringtones this manager is returning. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#isDefault(android.net.Uri)(ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Returns whether the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` is one of the default ringtones. |
| open static [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#openDefaultRingtoneUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Opens a raw file descriptor to read the data under the given default URI. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Sets the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the default sound for a given sound type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setIncludeDrm(kotlin.Boolean)(includeDrm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to include DRM ringtones. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setRingtoneUri(android.content.Context,%20android.net.Uri,%20android.telecom.PhoneAccountHandle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, phoneAccountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#?)` Sets the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the sound by `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` for TYPE_RINGTONE. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setStopPreviousRingtone(kotlin.Boolean)(stopPreviousRingtone: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether retrieving another `https://developer.android.com/reference/kotlin/android/media/Ringtone` will stop playing the previously retrieved `https://developer.android.com/reference/kotlin/android/media/Ringtone`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setType(kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets which type(s) of ringtones will be listed by this. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#stopPreviousRingtone()()` Stops playing the last `https://developer.android.com/reference/kotlin/android/media/Ringtone` retrieved from this. |

## Constants

### ACTION_RINGTONE_PICKER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RINGTONE_PICKER: String
```

Activity Action: Shows a ringtone picker.

Input: `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_EXISTING_URI:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_SHOW_DEFAULT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_SHOW_SILENT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_TYPE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_DEFAULT_URI:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_TITLE:kotlin.String`,

Output: `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_PICKED_URI:kotlin.String`.

 Value: "android.intent.action.RINGTONE_PICKER"

### EXTRA_RINGTONE_DEFAULT_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_DEFAULT_URI: String
```

Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the ringtone to play when the user attempts to preview the "Default" ringtone. This can be one of `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri` to have the "Default" point to the current sound for the given default sound type. If you are showing a ringtone picker for some other type of sound, you are free to provide any `https://developer.android.com/reference/kotlin/android/net/Uri.html#` here.

 Value: "android.intent.extra.ringtone.DEFAULT_URI"

### EXTRA_RINGTONE_EXISTING_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_EXISTING_URI: String
```

Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the current ringtone, which will be used to show a checkmark next to the item for this `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. If showing an item for "Default" (@see `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_SHOW_DEFAULT:kotlin.String`), this can also be one of `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri` to have the "Default" item checked.

 Value: "android.intent.extra.ringtone.EXISTING_URI"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String`

### EXTRA_RINGTONE_INCLUDE_DRM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_INCLUDE_DRM: String
```

**Deprecated:** *DRM ringtones are no longer supported*

Given to the ringtone picker as a boolean. Whether to include DRM ringtones.

 Value: "android.intent.extra.ringtone.INCLUDE_DRM"

### EXTRA_RINGTONE_PICKED_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_PICKED_URI: String
```

Returned from the ringtone picker as a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`.

It will be one of:
- the picked ringtone,
- a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` that equals `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri` if the default was chosen,
- null if the "Silent" item was picked.

 Value: "android.intent.extra.ringtone.PICKED_URI"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String`

### EXTRA_RINGTONE_SHOW_DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_SHOW_DEFAULT: String
```

Given to the ringtone picker as a boolean. Whether to show an item for "Default".

 Value: "android.intent.extra.ringtone.SHOW_DEFAULT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String`

### EXTRA_RINGTONE_SHOW_SILENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_SHOW_SILENT: String
```

Given to the ringtone picker as a boolean. Whether to show an item for "Silent". If the "Silent" item is picked, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_PICKED_URI:kotlin.String` will be null.

 Value: "android.intent.extra.ringtone.SHOW_SILENT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ACTION_RINGTONE_PICKER:kotlin.String`

### EXTRA_RINGTONE_TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_TITLE: String
```

Given to the ringtone picker as a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`. The title to show for the ringtone picker. This has a default value that is suitable in most cases.

 Value: "android.intent.extra.ringtone.TITLE"

### EXTRA_RINGTONE_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE_TYPE: String
```

Given to the ringtone picker as an int. Specifies which ringtone type(s) should be shown in the picker. One or more of `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_NOTIFICATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALARM:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALL:kotlin.Int` (bitwise-ored together).

 Value: "android.intent.extra.ringtone.TYPE"

### ID_COLUMN_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ID_COLUMN_INDEX: Int
```

The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the row ID.

 Value: 0

### TITLE_COLUMN_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TITLE_COLUMN_INDEX: Int
```

The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the title.

 Value: 1

### TYPE_ALARM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ALARM: Int
```

Type that refers to sounds that are used for the alarm.

 Value: 4

### TYPE_ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ALL: Int
```

All types of sounds.

 Value: 7

### TYPE_NOTIFICATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_NOTIFICATION: Int
```

Type that refers to sounds that are used for notifications.

 Value: 2

### TYPE_RINGTONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_RINGTONE: Int
```

Type that refers to sounds that are used for the phone ringer.

 Value: 1

### URI_COLUMN_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val URI_COLUMN_INDEX: Int
```

The column index (in the cursor returned by `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getCursor()` for the media provider's URI.

 Value: 2

## Public constructors

### RingtoneManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtoneManager(activity: Activity!)
```

Constructs a RingtoneManager. This constructor is recommended as its constructed instance manages cursor(s).

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: The activity used to get a managed cursor. |

### RingtoneManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtoneManager(context: Context!)
```

Constructs a RingtoneManager. The instance constructed by this constructor will not manage the cursor(s), so the client should handle this itself.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context to used to get a cursor. |

## Public methods

### getActualDefaultRingtoneUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getActualDefaultRingtoneUri(
    context: Context!, 
    type: Int
): Uri!
```

Gets the current default sound's `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. This will give the actual sound `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, instead of using this, most clients can use `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: A context used for querying. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type whose default sound should be returned. One of `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_NOTIFICATION:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALARM:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` pointing to the default sound for the sound type. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int,%20android.net.Uri)`

### getCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCursor(): Cursor!
```

Returns a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` of all the ringtones available. The returned cursor will be the same cursor returned each time this method is called, so do not android.database.Cursor#close() the cursor. The cursor can be `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()` safely.

If `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#RingtoneManager(android.app.Activity)` was not used, the caller should manage the returned cursor through its activity's life cycle to prevent leaking the cursor.

Note that the list of ringtones available will differ depending on whether the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#!` | A `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` of all the ringtones available. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#ID_COLUMN_INDEX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TITLE_COLUMN_INDEX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#URI_COLUMN_INDEX:kotlin.Int`

### getDefaultType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultType(defaultRingtoneUri: Uri!): Int
```

Returns the type of a default `https://developer.android.com/reference/kotlin/android/net/Uri.html#`.

| Parameters ||
|---|---|
| `defaultRingtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The default `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. For example, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The type of the defaultRingtoneUri, or -1. |

### getDefaultUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultUri(type: Int): Uri!
```

Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for the default ringtone of a particular type. Rather than returning the actual ringtone's sound `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, this will return the symbolic `https://developer.android.com/reference/kotlin/android/net/Uri.html#` which will resolved to the actual sound when played.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ringtone type whose default should be returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the default ringtone for the given type. |

### getIncludeDrm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIncludeDrm(): Boolean
```

**Deprecated:** *DRM ringtones are no longer supported*

Returns whether DRM ringtones will be included.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether DRM ringtones will be included. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setIncludeDrm(kotlin.Boolean)`

### getRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRingtone(position: Int): Ringtone!
```

Gets a `https://developer.android.com/reference/kotlin/android/media/Ringtone` for the ringtone at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position (in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`) of the ringtone. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/Ringtone!` | A `https://developer.android.com/reference/kotlin/android/media/Ringtone` pointing to the ringtone. |

### getRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getRingtone(
    context: Context!, 
    ringtoneUri: Uri!
): Ringtone!
```

Returns a `https://developer.android.com/reference/kotlin/android/media/Ringtone` for a given sound URI.

If the given URI cannot be opened for any reason, this method will attempt to fallback on another sound. If it cannot find any, it will return null.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: A context used to query. |
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of a sound or ringtone. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/Ringtone!` | A `https://developer.android.com/reference/kotlin/android/media/Ringtone` for the given URI, or null. |

### getRingtonePosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRingtonePosition(ringtoneUri: Uri!): Int
```

Gets the position of a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` within this `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#`.

| Parameters ||
|---|---|
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to retreive the position of. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The position of the `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, or -1 if it cannot be found. |

### getRingtoneUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRingtoneUri(position: Int): Uri!
```

Gets a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for the ringtone at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position (in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`) of the ringtone. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` pointing to the ringtone. |

### getRingtoneUriForPhoneAccountHandle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getRingtoneUriForPhoneAccountHandle(
    context: Context, 
    phoneAccountHandle: PhoneAccountHandle?
): Uri?
```

Gets TYPE_RINGTONE's `https://developer.android.com/reference/kotlin/android/net/Uri.html#` by id of `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): A context used for querying. This value cannot be `null`. |
| `phoneAccountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#)?: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` whose sound should be returned. If null, the default ringtone will be returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` pointing to the sound for TYPE_RINGTONE. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setRingtoneUri(android.content.Context,%20android.net.Uri,%20android.telecom.PhoneAccountHandle)`

### getStopPreviousRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStopPreviousRingtone(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setStopPreviousRingtone(kotlin.Boolean)`

### getValidRingtoneUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getValidRingtoneUri(context: Context!): Uri!
```

Returns a valid ringtone URI. No guarantees on which it returns. If it cannot find one, returns null. If it can only find one on external storage and the caller doesn't have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission, returns null.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The context to use for querying. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | A ringtone URI, or null if one cannot be found. |

### hasHapticChannels

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasHapticChannels(position: Int): Boolean
```

Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` at the given position in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` contains haptic channels.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position (in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`) of the ringtone. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the ringtone contains haptic channels. |

### hasHapticChannels

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun hasHapticChannels(
    context: Context, 
    ringtoneUri: Uri
): Boolean
```

Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` from a given sound URI contains haptics channels or not.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use when resolving the Uri. This value cannot be `null`. |
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of a sound or ringtone. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the ringtone contains haptic channels. |

### hasHapticChannels

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun hasHapticChannels(ringtoneUri: Uri): Boolean
```

Returns if the `https://developer.android.com/reference/kotlin/android/media/Ringtone` from a given sound URI contains haptic channels or not. As this function doesn't has a context to resolve the uri, the result may be wrong if the uri cannot be resolved correctly. Use `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#hasHapticChannels(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#hasHapticChannels(android.content.Context,%20android.net.Uri)` instead when possible.

| Parameters ||
|---|---|
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of a sound or ringtone. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the ringtone contains haptic channels. |

### inferStreamType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inferStreamType(): Int
```

Infers the volume stream type based on what type of ringtones this manager is returning.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The stream type. |

### isDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isDefault(ringtoneUri: Uri!): Boolean
```

Returns whether the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` is one of the default ringtones.

| Parameters ||
|---|---|
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The ringtone `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to be checked. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` is a default. |

### openDefaultRingtoneUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun openDefaultRingtoneUri(
    context: Context, 
    uri: Uri
): AssetFileDescriptor?
```

Opens a raw file descriptor to read the data under the given default URI.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the Context to use when resolving the Uri. This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The desired default URI to open. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | a new AssetFileDescriptor pointing to the file. You own this descriptor and are responsible for closing it when done. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if the provided URI could not be opened. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getDefaultUri(kotlin.Int)`

### setActualDefaultRingtoneUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setActualDefaultRingtoneUri(
    context: Context!, 
    type: Int, 
    ringtoneUri: Uri!
): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the default sound for a given sound type.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: A context used for querying. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type whose default sound should be set. One of `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_NOTIFICATION:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALARM:kotlin.Int`. |
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` pointing to the default sound to set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int)`

### setIncludeDrm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIncludeDrm(includeDrm: Boolean): Unit
```

**Deprecated:** *DRM ringtones are no longer supported*

Sets whether to include DRM ringtones.

| Parameters ||
|---|---|
| `includeDrm` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to include DRM ringtones. Obsolete - no longer has any effect |

### setRingtoneUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setRingtoneUri(
    context: Context, 
    ringtoneUri: Uri?, 
    phoneAccountHandle: PhoneAccountHandle?
): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` of the sound by `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` for TYPE_RINGTONE.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): A context used for querying. This value cannot be `null`. |
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: A `https://developer.android.com/reference/kotlin/android/net/Uri.html#` pointing to the sound to set. This parameter can be null, in which case the API behaves like `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int,%20android.net.Uri)`. |
| `phoneAccountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#)?: The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` whose sound should be set. This parameter can be null, in which case the API behaves like `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#setActualDefaultRingtoneUri(android.content.Context,%20kotlin.Int,%20android.net.Uri)`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#getRingtoneUriForPhoneAccountHandle(android.content.Context,%20android.telecom.PhoneAccountHandle)`

### setStopPreviousRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStopPreviousRingtone(stopPreviousRingtone: Boolean): Unit
```

Whether retrieving another `https://developer.android.com/reference/kotlin/android/media/Ringtone` will stop playing the previously retrieved `https://developer.android.com/reference/kotlin/android/media/Ringtone`.

If this is false, make sure to `https://developer.android.com/reference/kotlin/android/media/Ringtone#stop()` any previous ringtones to free resources.

| Parameters ||
|---|---|
| `stopPreviousRingtone` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the previously retrieved `https://developer.android.com/reference/kotlin/android/media/Ringtone` will be stopped. |

### setType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setType(type: Int): Unit
```

Sets which type(s) of ringtones will be listed by this.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type(s), one or more of `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_RINGTONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_NOTIFICATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALARM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#TYPE_ALL:kotlin.Int`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager#EXTRA_RINGTONE_TYPE:kotlin.String`

### stopPreviousRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopPreviousRingtone(): Unit
```

Stops playing the last `https://developer.android.com/reference/kotlin/android/media/Ringtone` retrieved from this.
