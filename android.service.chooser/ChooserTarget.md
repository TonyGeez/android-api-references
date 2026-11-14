Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChooserTarget

Kotlin | [Java](ChooserTarget.md)
| --- | --- |

```
class ChooserTarget : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.chooser.ChooserTarget](ChooserTarget.md) |

> [!CAUTION]
> **This class was deprecated in API level 30.**
>
> For publishing direct share targets, please follow the instructions in https://developer.android.com/training/sharing/receive.html#providing-direct-share-targets instead.

A ChooserTarget represents a deep-link into an application as returned by a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService`.

A chooser target represents a specific deep link target into an application exposed for selection by the user. This might be a frequently emailed contact, a recently active group messaging conversation, a folder in a cloud storage app, a collection of related items published on a social media service or any other contextually relevant grouping of target app + relevant metadata.

Creators of chooser targets should consult the relevant design guidelines for the type of target they are presenting. For example, targets involving people should be presented with a circular icon.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#ChooserTarget(kotlin.CharSequence,%20android.graphics.drawable.Icon,%20kotlin.Float,%20android.content.ComponentName,%20android.os.Bundle)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, icon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#!, score: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, intentExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Construct a deep link target for presentation by a chooser UI. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [ComponentName](../android.content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#getComponentName()()` Returns the ComponentName of the Activity that should be launched for this ChooserTarget. |
| [Icon](../android.graphics.drawable/Icon.md)! | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#getIcon()()` Returns the icon representing this target for display to a user. |
| --- | --- |
| [Bundle](../android.os/Bundle.md)! | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#getIntentExtras()()` Returns the Bundle of extras to be added to an intent launched to this target. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#getScore()()` Returns the ranking score supplied by the creator of this ChooserTarget. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#getTitle()()` Returns the title of this target for display to a user. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ChooserTarget](ChooserTarget.md)!\> | `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### ChooserTarget

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ChooserTarget(
    title: CharSequence!, 
    icon: Icon!, 
    score: Float, 
    componentName: ComponentName!, 
    intentExtras: Bundle?)
```

Construct a deep link target for presentation by a chooser UI.

A target is composed of a title and an icon for presentation to the user. The UI presenting this target may truncate the title if it is too long to be presented in the available space, as well as crop, resize or overlay the supplied icon.

The creator of a target may supply a ranking score. This score is assumed to be relative to the other targets supplied by the same `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService#onGetChooserTargets(android.content.ComponentName,%20android.content.IntentFilter)`. Scores should be in the range from 0.0f (unlikely match) to 1.0f (very relevant match). Scores for a set of targets do not need to sum to 1.

The ComponentName must be the name of an Activity component in the creator's own package, or an exported component from any other package. You may provide an optional Bundle of extras that will be merged into the final intent before it is sent to the target Activity; use this to add any additional data about the deep link that the target activity will read. e.g. conversation IDs, email addresses, etc.

Take care not to place custom `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` types into the extras bundle, as the system will not be able to unparcel them to merge them.

| Parameters ||
|---|---|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: title of this target that will be shown to a user |
| `icon` | [Icon](../android.graphics.drawable/Icon.md)!: icon to represent this target |
| `score` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): ranking score for this target between 0.0f and 1.0f, inclusive |
| --- | --- |
| `componentName` | [ComponentName](../android.content/ComponentName.md)!: Name of the component to be launched if this target is chosen |
| `intentExtras` | [Bundle](../android.os/Bundle.md)?: Bundle of extras to merge with the extras of the launched intent. This value may be `null`. |

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getComponentName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponentName(): ComponentName!
```

**Deprecated:** *Deprecated in Java.*

Returns the ComponentName of the Activity that should be launched for this ChooserTarget.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` | the name of the target Activity to launch |

### getIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIcon(): Icon!
```

**Deprecated:** *Deprecated in Java.*

Returns the icon representing this target for display to a user. The UI displaying the icon may crop, resize or overlay this icon.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#!` | the icon representing this target, intended to be shown to a user |

### getIntentExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntentExtras(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Returns the Bundle of extras to be added to an intent launched to this target.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | the extras to merge with the extras of the intent being launched |

### getScore

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScore(): Float
```

**Deprecated:** *Deprecated in Java.*

Returns the ranking score supplied by the creator of this ChooserTarget. Values are between 0.0f and 1.0f. The UI displaying the target may take this score into account when sorting and merging targets from multiple sources.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the ranking score for this target between 0.0f and 1.0f, inclusive |

### getTitle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTitle(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the title of this target for display to a user. The UI displaying the title may truncate this title if it is too long to be displayed in full.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | the title of this target, intended to be shown to a user |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ChooserTarget!>
```

**Deprecated:** *Deprecated in Java.*
