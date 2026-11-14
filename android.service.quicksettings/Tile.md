# Tile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Tile

Kotlin| [Java](../android/service/quicksettings/Tile.md) 
| --- | --- |

```
class Tile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.quicksettings.Tile](../android/service/quicksettings/Tile.md) |

A Tile holds the state of a tile that will be displayed in Quick Settings. A tile in Quick Settings exists as an icon with an accompanied label. It also may have content description for accessibility usability. The style and layout of the tile may change to match a given device.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ACTIVE](../android/service/quicksettings/Tile.md) This represents a tile that is currently active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INACTIVE](../android/service/quicksettings/Tile.md) This represents a tile that is currently in a disabled state but is still interactable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNAVAILABLE](../android/service/quicksettings/Tile.md) An unavailable state indicates that for some reason this tile is not currently available to the user, and will have no click action. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/quicksettings/Tile.md))`()` <br /> |
| [PendingIntent](../android/app/PendingIntent.md)? | [getActivityLaunchForClick](../android/service/quicksettings/Tile.md))`()` Gets the Activity [PendingIntent](../android/app/PendingIntent.md) to be launched when the tile is clicked. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getContentDescription](../android/service/quicksettings/Tile.md))`()` Gets the current content description for the tile. |
| --- | --- |
| [Icon](../android/graphics/drawable/Icon.md)! | [getIcon](../android/service/quicksettings/Tile.md))`()` Gets the current icon for the tile. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getLabel](../android/service/quicksettings/Tile.md))`()` Gets the current label for the tile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](../android/service/quicksettings/Tile.md))`()` The current state of the tile. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getStateDescription](../android/service/quicksettings/Tile.md))`()` Gets the current state description for the tile. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getSubtitle](../android/service/quicksettings/Tile.md))`()` Gets the current subtitle for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityLaunchForClick](../android/service/quicksettings/Tile.md))`(`pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)?`)` Sets an Activity [PendingIntent](../android/app/PendingIntent.md) to be launched when the tile is clicked. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentDescription](../android/service/quicksettings/Tile.md))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the current content description for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/service/quicksettings/Tile.md))`(`icon:` ` [Icon](../android/graphics/drawable/Icon.md)!`)` Sets the current icon for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLabel](../android/service/quicksettings/Tile.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the current label for the tile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setState](../android/service/quicksettings/Tile.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current state for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStateDescription](../android/service/quicksettings/Tile.md))`(`stateDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the current state description for the tile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSubtitle](../android/service/quicksettings/Tile.md))`(`subtitle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Set the subtitle for the tile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTile](../android/service/quicksettings/Tile.md))`()` Pushes the state of the Tile to Quick Settings to be displayed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/quicksettings/Tile.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Tile](../android/service/quicksettings/Tile.md)!\> | [CREATOR](../android/service/quicksettings/Tile.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getActivityLaunchForClick

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivityLaunchForClick(): PendingIntent?
```

Gets the Activity [PendingIntent](../android/app/PendingIntent.md) to be launched when the tile is clicked.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------|
| [PendingIntent](../android/app/PendingIntent.md)? | This value may be`null`. |

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

- [#STATE_UNAVAILABLE](../android/service/quicksettings/Tile.md)
- [#STATE_INACTIVE](../android/service/quicksettings/Tile.md)
- [#STATE_ACTIVE](../android/service/quicksettings/Tile.md) 

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

Sets an Activity [PendingIntent](../android/app/PendingIntent.md) to be launched when the tile is clicked. The last value set here will be launched when the user clicks in the tile, instead of forwarding the \`onClick\` message to the [TileService](../android/service/quicksettings/TileService.md). Set to`null`to handle the \`onClick\` in the \`TileService\` (This is the default behavior if this method is never called.)

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md)?:a PendingIntent for an activity to be launched onclick, or`null`to handle the clicks in the \`TileService\`. |

### setContentDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentDescription(contentDescription: CharSequence!): Unit
```

Sets the current content description for the tile. Does not take effect until [updateTile()](../android/service/quicksettings/Tile.md))is called.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:New content description to use. |

### setIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIcon(icon: Icon!): Unit
```

Sets the current icon for the tile. This icon is expected to be white on alpha, and may be tinted by the system to match it's theme. Does not take effect until [updateTile()](../android/service/quicksettings/Tile.md))is called.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `icon` | [Icon](../android/graphics/drawable/Icon.md)!:New icon to show. |

### setLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLabel(label: CharSequence!): Unit
```

Sets the current label for the tile. Does not take effect until [updateTile()](../android/service/quicksettings/Tile.md))is called.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:New label to show. |

### setState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setState(state: Int): Unit
```

Sets the current state for the tile. Does not take effect until [updateTile()](../android/service/quicksettings/Tile.md))is called.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [STATE_UNAVAILABLE](../android/service/quicksettings/Tile.md), [STATE_INACTIVE](../android/service/quicksettings/Tile.md), [STATE_ACTIVE](../android/service/quicksettings/Tile.md) |

### setStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStateDescription(stateDescription: CharSequence?): Unit
```

Sets the current state description for the tile. Does not take effect until [updateTile()](../android/service/quicksettings/Tile.md))is called.

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Tile!>
```
