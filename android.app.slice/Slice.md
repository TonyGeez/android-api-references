Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Slice

```
class Slice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.Slice](Slice.md) |

> [!CAUTION]
> **This class was deprecated in API level 35.**
>
> Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#`.

A slice is a piece of app content and actions that can be surfaced outside of the app.

They are constructed using `https://developer.android.com/reference/kotlin/android/app/slice/Slice.Builder` in a tree structure that provides the OS some information about how the content should be displayed.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/slice/Slice.Builder` A Builder used to construct `https://developer.android.com/reference/kotlin/android/app/slice/Slice#`s |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#EXTRA_RANGE_VALUE:kotlin.String` Key to retrieve an extra added to an intent when the value of an input range is changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#EXTRA_TOGGLE_STATE:kotlin.String` Key to retrieve an extra added to an intent when a control is changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ACTIONS:kotlin.String` Hint that this slice contains a number of actions that can be grouped together in a sort of controls area of the UI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ERROR:kotlin.String` A hint to indicate that this slice represents an error. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_HORIZONTAL:kotlin.String` Hint that list items within this slice or subslice would appear better if organized horizontally. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_KEYWORDS:kotlin.String` A hint to indicate that the contents of this subslice represent a list of keywords related to the parent slice. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LARGE:kotlin.String` Hint that this content is important and should be larger when displayed if possible. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LAST_UPDATED:kotlin.String` Hint indicating an item representing when the content was created or last updated. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST:kotlin.String` Hint that all sub-items/sub-slices within this content should be considered to have `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String` Hint that this item is part of a list and should be formatted as if is part of a list. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_NO_TINT:kotlin.String` Hint to indicate that this content should not be tinted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PARTIAL:kotlin.String` Hint to indicate that this slice is incomplete and an update will be sent once loading is complete. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PERMISSION_REQUEST:kotlin.String` A hint to indicate that this slice represents a permission request for showing slices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SEE_MORE:kotlin.String` A hint representing that this item should be used to indicate that there's more content associated with this slice. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SELECTED:kotlin.String` Hint indicating that this item (and its sub-items) are the current selection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SHORTCUT:kotlin.String` Hint to indicate that this content should only be displayed if the slice is presented as a shortcut. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SUMMARY:kotlin.String` Hint indicating this content should be shown instead of the normal content when the slice is in small format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TITLE:kotlin.String` Hint that this content is a title of other content in the slice. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TTL:kotlin.String` Hint indicating an item representing a time-to-live for the content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_COLOR:kotlin.String` Subtype to tag an item as representing a color. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_CONTENT_DESCRIPTION:kotlin.String` Subtype to tag an item to use as a content description. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_LAYOUT_DIRECTION:kotlin.String` Subtype to indicate that this item indicates the layout direction for content in the slice. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MAX:kotlin.String` Subtype to tag an item as representing the max int value for a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_RANGE:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MESSAGE:kotlin.String` Subtype to indicate that this is a message as part of a communication sequence in this slice. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MILLIS:kotlin.String` Subtype to tag an item as representing a time in milliseconds since midnight, January 1, 1970 UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_PRIORITY:kotlin.String` Subtype to tag an item representing priority. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_RANGE:kotlin.String` Subtype to tag an item as representing a range. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_SOURCE:kotlin.String` Subtype to tag the source (i.e. sender) of a |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_TOGGLE:kotlin.String` Subtype to indicate that this content has a toggle action associated with it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_VALUE:kotlin.String` Subtype to tag an item as representing the current int value for a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_RANGE:kotlin.String`. |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/slice/Slice#Slice(android.os.Parcel)(in: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#getHints()()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SliceItem](SliceItem.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#getItems()()` <br /> |
| --- | --- |
| [SliceSpec](SliceSpec.md)? | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#getSpec()()` <br /> |
| [Uri](../android.net/Uri.md)! | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#getUri()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#isCallerNeeded()()` Returns whether the caller for this slice matters. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#toString()()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Slice](Slice.md)!\> | `https://developer.android.com/reference/kotlin/android/app/slice/Slice#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### EXTRA_RANGE_VALUE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RANGE_VALUE: String
```

**Deprecated:** *Deprecated in Java.*

Key to retrieve an extra added to an intent when the value of an input range is changed.

 Value: "android.app.slice.extra.RANGE_VALUE"

### EXTRA_TOGGLE_STATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TOGGLE_STATE: String
```

**Deprecated:** *Deprecated in Java.*

Key to retrieve an extra added to an intent when a control is changed.

 Value: "android.app.slice.extra.TOGGLE_STATE"

### HINT_ACTIONS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_ACTIONS: String
```

**Deprecated:** *Deprecated in Java.*

Hint that this slice contains a number of actions that can be grouped together in a sort of controls area of the UI.

 Value: "actions"

### HINT_ERROR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_ERROR: String
```

**Deprecated:** *Deprecated in Java.*

A hint to indicate that this slice represents an error.

 Value: "error"

### HINT_HORIZONTAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_HORIZONTAL: String
```

**Deprecated:** *Deprecated in Java.*

Hint that list items within this slice or subslice would appear better if organized horizontally.

 Value: "horizontal"

### HINT_KEYWORDS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_KEYWORDS: String
```

**Deprecated:** *Deprecated in Java.*

A hint to indicate that the contents of this subslice represent a list of keywords related to the parent slice. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String`.

 Value: "keywords"

### HINT_LARGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_LARGE: String
```

**Deprecated:** *Deprecated in Java.*

Hint that this content is important and should be larger when displayed if possible.

 Value: "large"

### HINT_LAST_UPDATED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_LAST_UPDATED: String
```

**Deprecated:** *Deprecated in Java.*

Hint indicating an item representing when the content was created or last updated.

 Value: "last_updated"

### HINT_LIST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_LIST: String
```

**Deprecated:** *Deprecated in Java.*

Hint that all sub-items/sub-slices within this content should be considered to have `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String`.

 Value: "list"

### HINT_LIST_ITEM

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_LIST_ITEM: String
```

**Deprecated:** *Deprecated in Java.*

Hint that this item is part of a list and should be formatted as if is part of a list.

 Value: "list_item"

### HINT_NO_TINT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_NO_TINT: String
```

**Deprecated:** *Deprecated in Java.*

Hint to indicate that this content should not be tinted.

 Value: "no_tint"

### HINT_PARTIAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_PARTIAL: String
```

**Deprecated:** *Deprecated in Java.*

Hint to indicate that this slice is incomplete and an update will be sent once loading is complete. Slices which contain HINT_PARTIAL will not be cached by the OS and should not be cached by apps.

 Value: "partial"

### HINT_PERMISSION_REQUEST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_PERMISSION_REQUEST: String
```

**Deprecated:** *Deprecated in Java.*

A hint to indicate that this slice represents a permission request for showing slices.

 Value: "permission_request"

### HINT_SEE_MORE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_SEE_MORE: String
```

**Deprecated:** *Deprecated in Java.*

A hint representing that this item should be used to indicate that there's more content associated with this slice.

 Value: "see_more"

### HINT_SELECTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_SELECTED: String
```

**Deprecated:** *Deprecated in Java.*

Hint indicating that this item (and its sub-items) are the current selection.

 Value: "selected"

### HINT_SHORTCUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_SHORTCUT: String
```

**Deprecated:** *Deprecated in Java.*

Hint to indicate that this content should only be displayed if the slice is presented as a shortcut.

 Value: "shortcut"

### HINT_SUMMARY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_SUMMARY: String
```

**Deprecated:** *Deprecated in Java.*

Hint indicating this content should be shown instead of the normal content when the slice is in small format.

 Value: "summary"

### HINT_TITLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_TITLE: String
```

**Deprecated:** *Deprecated in Java.*

Hint that this content is a title of other content in the slice. This can also indicate that the content should be used in the shortcut representation of the slice (icon, label, action), normally this should be indicated by adding the hint on the action containing that content.

 Value: "title"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String`

### HINT_TTL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_TTL: String
```

**Deprecated:** *Deprecated in Java.*

Hint indicating an item representing a time-to-live for the content.

 Value: "ttl"

### SUBTYPE_COLOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_COLOR: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item as representing a color. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String`.

 Value: "color"

### SUBTYPE_CONTENT_DESCRIPTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_CONTENT_DESCRIPTION: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item to use as a content description. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String`.

 Value: "content_description"

### SUBTYPE_LAYOUT_DIRECTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_LAYOUT_DIRECTION: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to indicate that this item indicates the layout direction for content in the slice. Expected to be an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String`.

 Value: "layout_direction"

### SUBTYPE_MAX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_MAX: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item as representing the max int value for a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_RANGE:kotlin.String`. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String`.

 Value: "max"

### SUBTYPE_MESSAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_MESSAGE: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to indicate that this is a message as part of a communication sequence in this slice. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String`.

 Value: "message"

### SUBTYPE_MILLIS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_MILLIS: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item as representing a time in milliseconds since midnight, January 1, 1970 UTC.

 Value: "millis"

### SUBTYPE_PRIORITY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_PRIORITY: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item representing priority. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String`.

 Value: "priority"

### SUBTYPE_RANGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_RANGE: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item as representing a range. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String` containing a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_VALUE:kotlin.String` and possibly a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MAX:kotlin.String`.

 Value: "range"

### SUBTYPE_SOURCE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_SOURCE: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag the source (i.e. sender) of a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MESSAGE:kotlin.String`. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_IMAGE:kotlin.String` or an `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String` containing them.

 Value: "source"

### SUBTYPE_TOGGLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_TOGGLE: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to indicate that this content has a toggle action associated with it. To indicate that the toggle is on, use `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SELECTED:kotlin.String`. When the toggle state changes, the intent associated with it will be sent along with an extra `https://developer.android.com/reference/kotlin/android/app/slice/Slice#EXTRA_TOGGLE_STATE:kotlin.String` which can be retrieved to see the new state of the toggle.

 Value: "toggle"

### SUBTYPE_VALUE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBTYPE_VALUE: String
```

**Deprecated:** *Deprecated in Java.*

Subtype to tag an item as representing the current int value for a `https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_RANGE:kotlin.String`. Expected to be on an item of format `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String`.

 Value: "value"

## Protected constructors

### Slice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Slice(in: Parcel!)
```

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getHints

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHints(): MutableList<String!>!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | All hints associated with this Slice. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LARGE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ACTIONS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SELECTED:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_NO_TINT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SHORTCUT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_HORIZONTAL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PARTIAL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SEE_MORE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_KEYWORDS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ERROR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TTL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LAST_UPDATED:kotlin.String` - `https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PERMISSION_REQUEST:kotlin.String` |

### getItems

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getItems(): MutableList<SliceItem!>!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/slice/SliceItem!>!` | All child `https://developer.android.com/reference/kotlin/android/app/slice/SliceItem`s that this Slice contains. |

### getSpec

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpec(): SliceSpec?
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/slice/SliceSpec?` | The spec for this slice. This value may be `null`. |

### getUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUri(): Uri!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The Uri that this Slice represents. |

### isCallerNeeded

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCallerNeeded(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the caller for this slice matters.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/slice/Slice.Builder#setCallerNeeded(kotlin.Boolean)`

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of this slice. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Slice!>
```

**Deprecated:** *Deprecated in Java.*
