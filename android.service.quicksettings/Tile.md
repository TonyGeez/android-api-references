# Tile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Tile

Kotlin| [Java](https://developer.android.com/reference/android/service/quicksettings/Tile "View this page in Java") 
| --- | --- |

```
class Tile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.quicksettings.Tile](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#) |

A Tile holds the state of a tile that will be displayed in Quick Settings. A tile in Quick Settings exists as an icon with an accompanied label. It also may have content description for accessibility usability. The style and layout of the tile may change to match a given device.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_ACTIVE:kotlin.Int) This represents a tile that is currently active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_INACTIVE:kotlin.Int) This represents a tile that is currently in a disabled state but is still interactable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_UNAVAILABLE:kotlin.Int) An unavailable state indicates that for some reason this tile is not currently available to the user, and will have no click action. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#describeContents())`()` <br /> |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | [getActivityLaunchForClick](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getActivityLaunchForClick())`()` Gets the Activity [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to be launched when the tile is clicked. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getContentDescription](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getContentDescription())`()` Gets the current content description for the tile. |
| --- | --- |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)! | [getIcon](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getIcon())`()` Gets the current icon for the tile. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getLabel](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getLabel())`()` Gets the current label for the tile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getState())`()` The current state of the tile. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getStateDescription](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getStateDescription())`()` Gets the current state description for the tile. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getSubtitle](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#getSubtitle())`()` Gets the current subtitle for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityLaunchForClick](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setActivityLaunchForClick(android.app.PendingIntent))`(`pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)?`)` Sets an Activity [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to be launched when the tile is clicked. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentDescription](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setContentDescription(kotlin.CharSequence))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the current content description for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setIcon(android.graphics.drawable.Icon))`(`icon:` ` [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)!`)` Sets the current icon for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLabel](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setLabel(kotlin.CharSequence))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the current label for the tile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setState](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setState(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current state for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStateDescription](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setStateDescription(kotlin.CharSequence))`(`stateDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the current state description for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSubtitle](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#setSubtitle(kotlin.CharSequence))`(`subtitle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Set the subtitle for the tile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTile](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())`()` Pushes the state of the Tile to Quick Settings to be displayed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Tile](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STATE_ACTIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ACTIVE: Int
```

This represents a tile that is currently active. (e.g. wifi is connected, bluetooth is on, cast is casting). This is the default state. 

 Value: 2

### STATE_INACTIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_INACTIVE: Int
```

This represents a tile that is currently in a disabled state but is still interactable. A disabled state indicates that the tile is not currently active (e.g. wifi disconnected or bluetooth disabled), but is still interactable by the user to modify this state. Tiles that have boolean states should use this to represent one of their states. The tile's icon will be tinted differently to reflect this state, but still be distinct from unavailable. 

 Value: 1

### STATE_UNAVAILABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_UNAVAILABLE: Int
```

An unavailable state indicates that for some reason this tile is not currently available to the user, and will have no click action. The tile's icon will be tinted differently to reflect this state. 

 Value: 0

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActivityLaunchForClick

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivityLaunchForClick(): PendingIntent?
```

Gets the Activity [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to be launched when the tile is clicked.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | This value may be`null`. |

### getContentDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentDescription(): CharSequence!
```

Gets the current content description for the tile. 

### getIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Icon!
```

Gets the current icon for the tile. 

### getLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): CharSequence!
```

Gets the current label for the tile. 

### getState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

The current state of the tile. 
**See Also**

- [#STATE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_UNAVAILABLE:kotlin.Int)
- [#STATE_INACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_INACTIVE:kotlin.Int)
- [#STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_ACTIVE:kotlin.Int) 

### getStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStateDescription(): CharSequence?
```

Gets the current state description for the tile.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getSubtitle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubtitle(): CharSequence?
```

Gets the current subtitle for the tile.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### setActivityLaunchForClick

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActivityLaunchForClick(pendingIntent: PendingIntent?): Unit
```

Sets an Activity [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to be launched when the tile is clicked. The last value set here will be launched when the user clicks in the tile, instead of forwarding the \`onClick\` message to the [TileService](https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService). Set to`null`to handle the \`onClick\` in the \`TileService\` (This is the default behavior if this method is never called.)

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)?:a PendingIntent for an activity to be launched onclick, or`null`to handle the clicks in the \`TileService\`. |

### setContentDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentDescription(contentDescription: CharSequence!): Unit
```

Sets the current content description for the tile. Does not take effect until [updateTile()](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())is called.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:New content description to use. |

### setIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIcon(icon: Icon!): Unit
```

Sets the current icon for the tile. This icon is expected to be white on alpha, and may be tinted by the system to match it's theme. Does not take effect until [updateTile()](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())is called.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `icon` | [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)!:New icon to show. |

### setLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLabel(label: CharSequence!): Unit
```

Sets the current label for the tile. Does not take effect until [updateTile()](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())is called.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:New label to show. |

### setState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setState(state: Int): Unit
```

Sets the current state for the tile. Does not take effect until [updateTile()](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())is called.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [STATE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_UNAVAILABLE:kotlin.Int), [STATE_INACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_INACTIVE:kotlin.Int), [STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#STATE_ACTIVE:kotlin.Int) |

### setStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStateDescription(stateDescription: CharSequence?): Unit
```

Sets the current state description for the tile. Does not take effect until [updateTile()](https://developer.android.com/reference/kotlin/android/service/quicksettings/Tile#updateTile())is called.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stateDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:New state description to use. This value may be`null`. |

### setSubtitle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSubtitle(subtitle: CharSequence?): Unit
```

Set the subtitle for the tile. Will be displayed as the secondary label.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `subtitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:the subtitle to show. This value may be`null`. |

### updateTile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateTile(): Unit
```

Pushes the state of the Tile to Quick Settings to be displayed. 

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Tile!>
```
