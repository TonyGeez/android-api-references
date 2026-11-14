Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DragEvent

Kotlin | [Java](DragEvent.md)
| --- | --- |

```
open class DragEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.DragEvent](DragEvent.md) |

Represents an event that is sent out by the system at various times during a drag and drop operation. It is a data structure that contains several important pieces of data about the operation and the underlying data.

View objects that receive a DragEvent call getAction, which returns an action type that indicates the state of the drag and drop operation. This allows a View object to react to a change in state by changing its appearance or performing other actions. For example, a View can react to the `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` action type by by changing one or more colors in its displayed image.

During a drag and drop operation, the system displays an image that the user drags. This image is called a drag shadow. Several action types reflect the position of the drag shadow relative to the View receiving the event.

Most methods return valid data only for certain event actions. This is summarized in the following table. Each possible getAction value is listed in the first column. The other columns indicate which method or methods return valid data for that getAction() value:

| getAction() Value | getClipDescription() | getLocalState() | getX() | getY() | getClipData() | getResult() |
|---|---|---|---|---|---|---|
| ACTION_DRAG_STARTED | X | X | X | X | | |
| ACTION_DRAG_ENTERED | X | X | | | | |
| ACTION_DRAG_LOCATION | X | X | X | X | | |
| --- | --- | --- | --- | --- | --- | --- |
| ACTION_DRAG_EXITED | X | X | | | | |
| ACTION_DROP | X | X | X | X | X | |
| ACTION_DRAG_ENDED | | X | | | | X |
| --- | --- | --- | --- | --- | --- | --- |

The getAction, getLocalState describeContents, writeToParcel, and toString methods always return valid data.

> [!NOTE]
>
> ### Developer Guides
>
> For a guide to implementing drag and drop features, read the [Drag and Drop](https://developer.android.com/guide/topics/ui/drag-drop.html) developer guide.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int` Action constant returned by getAction: Signals to a View that the drag and drop operation has concluded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` Action constant returned by getAction: Signals to a View that the drag point has entered the bounding box of the View. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_EXITED:kotlin.Int` Action constant returned by getAction: Signals that the user has moved the drag shadow out of the bounding box of the View or into a descendant view that can accept the data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_LOCATION:kotlin.Int` Action constant returned by getAction: Sent to a View after `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` while the drag shadow is still within the View object's bounding box, but not within a descendant view that can accept the data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` Action constant returned by getAction: Signals the start of a drag and drop operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` Action constant returned by getAction: Signals to a View that the user has released the drag shadow, and the drag point is within the bounding box of the View and not within a descendant view that can accept the data. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Returns information about the `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` representation of this DragEvent object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAction Inspect the action value of this event. |
| open [ClipData](../android.content/ClipData.md)! | getClipData Returns the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object sent to the system as part of the call to startDragAndDrop. |
| --- | --- |
| open [ClipDescription](../android.content/ClipDescription.md)! | getClipDescription Returns the `https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#` object contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object sent to the system as part of the call to startDragAndDrop. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | getLocalState Returns the local state object sent to the system as part of the call to startDragAndDrop. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getResult Returns an indication of the result of the drag and drop operation. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getX Gets the X coordinate of the drag point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getY Gets the Y coordinate of the drag point. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string containing a concise, human-readable representation of this DragEvent object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Creates a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` object from this DragEvent object. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [DragEvent](DragEvent.md)!\> | `https://developer.android.com/reference/kotlin/android/view/DragEvent#CREATOR:android.os.Parcelable.Creator` A container for creating a DragEvent from a Parcel. |

## Constants

### ACTION_DRAG_ENDED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG_ENDED: Int
```

Action constant returned by getAction: Signals to a View that the drag and drop operation has concluded. A View that changed its appearance during the operation should return to its usual drawing state in response to this event.

All views with listeners that returned boolean `true` for the ACTION_DRAG_STARTED event will receive the ACTION_DRAG_ENDED event even if they are not currently visible when the drag ends. Views removed during the drag operation won't receive the ACTION_DRAG_ENDED event.

The View object can call getResult to see the result of the operation. If a View returned `true` in response to `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`, then getResult() returns `true`, otherwise it returns `false`.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int`
- getResult

### ACTION_DRAG_ENTERED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG_ENTERED: Int
```

Action constant returned by getAction: Signals to a View that the drag point has entered the bounding box of the View.

If the View can accept a drop, it can react to ACTION_DRAG_ENTERED by changing its appearance in a way that tells the user that the View is the current drop target.
The system stops sending ACTION_DRAG_LOCATION events to a View once the user moves the drag shadow out of the View object's bounding box or into a descendant view that can accept the data. If the user moves the drag shadow back into the View object's bounding box or out of a descendant view that can accept the data, the View receives an ACTION_DRAG_ENTERED again before receiving any more ACTION_DRAG_LOCATION events.

<br />

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_LOCATION:kotlin.Int`

### ACTION_DRAG_EXITED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG_EXITED: Int
```

Action constant returned by getAction: Signals that the user has moved the drag shadow out of the bounding box of the View or into a descendant view that can accept the data. The View can react by changing its appearance in a way that tells the user that View is no longer the immediate drop target.

After the system sends an ACTION_DRAG_EXITED event to the View, the View receives no more ACTION_DRAG_LOCATION events until the user drags the drag shadow back over the View.

 Value: 6

### ACTION_DRAG_LOCATION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG_LOCATION: Int
```

Action constant returned by getAction: Sent to a View after `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` while the drag shadow is still within the View object's bounding box, but not within a descendant view that can accept the data. The getX and getY methods supply the X and Y position of the drag point within the View object's bounding box.

A View receives an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` event before receiving any ACTION_DRAG_LOCATION events.

The system stops sending ACTION_DRAG_LOCATION events to a View once the user moves the drag shadow out of the View object's bounding box or into a descendant view that can accept the data. If the user moves the drag shadow back into the View object's bounding box or out of a descendant view that can accept the data, the View receives an ACTION_DRAG_ENTERED again before receiving any more ACTION_DRAG_LOCATION events.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int`
- getX
- getY

### ACTION_DRAG_STARTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG_STARTED: Int
```

Action constant returned by getAction: Signals the start of a drag and drop operation. The View should return `true` from its onDragEvent handler method or onDrag listener if it can accept a drop. The onDragEvent() or onDrag() methods usually inspect the metadata from getClipDescription to determine if they can accept the data contained in this drag. For an operation that doesn't represent data transfer, these methods may perform other actions to determine whether or not the View should accept the data. If the View wants to indicate that it is a valid drop target, it can also react by changing its appearance.

Views added or becoming visible for the first time during a drag operation receive this event when they are added or becoming visible.

A View only receives further drag events for the drag operation if it returns `true` in response to ACTION_DRAG_STARTED.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int`
- getX
- getY

### ACTION_DROP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DROP: Int
```

Action constant returned by getAction: Signals to a View that the user has released the drag shadow, and the drag point is within the bounding box of the View and not within a descendant view that can accept the data. The View should retrieve the data from the DragEvent by calling getClipData. The methods getX and getY return the X and Y position of the drop point within the View object's bounding box.

The View should return `true` from its onDragEvent handler or onDrag listener if it accepted the drop, and `false` if it ignored the drop.

The View can also react to this action by changing its appearance.

 Value: 3

**See Also**

- getClipData
- getX
- getY

## Public methods

### describeContents

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Returns information about the `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` representation of this DragEvent object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Information about the `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` representation. |

### getAction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAction(): Int
```

Inspect the action value of this event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of the following action constants, in the order in which they usually occur during a drag and drop operation: - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_LOCATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_EXITED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int` |

### getClipData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipData(): ClipData!
```

Returns the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object sent to the system as part of the call to startDragAndDrop. This method only returns valid data if the event action is `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ClipData.html#!` | The ClipData sent to the system by startDragAndDrop(). |

### getClipDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipDescription(): ClipDescription!
```

Returns the `https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#` object contained in the `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` object sent to the system as part of the call to startDragAndDrop. The drag handler or listener for a View can use the metadata in this object to decide if the View can accept the dragged View object's data.

This method returns valid data for all event actions except for `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#!` | The ClipDescription that was part of the ClipData sent to the system by startDragAndDrop(). |

### getLocalState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocalState(): Any!
```

Returns the local state object sent to the system as part of the call to startDragAndDrop. The object is intended to provide local information about the drag and drop operation. For example, it can indicate whether the drag and drop operation is a copy or a move.

The local state is available only to views in the activity which has started the drag operation. In all other activities this method will return null

This method returns valid data for all event actions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The local state object sent to the system by startDragAndDrop(). |

### getResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResult(): Boolean
```

Returns an indication of the result of the drag and drop operation. This method only returns valid data if the action type is `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int`. The return value depends on what happens after the user releases the drag shadow.

If the user releases the drag shadow on a View that can accept a drop, the system sends an `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` event to the View object's drag event listener. If the listener returns `true`, then getResult() will return `true`. If the listener returns `false`, then getResult() returns `false`.

Notice that getResult() also returns `false` if no `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` is sent. This happens, for example, when the user releases the drag shadow over an area outside of the application. In this case, the system sends out `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int` for the current operation, but never sends out `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a drag event listener returned `true` in response to `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`. If the system did not send `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int` before `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_ENDED:kotlin.Int`, or if the listener returned `false` in response to `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`, then `false` is returned. |

### getX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getX(): Float
```

Gets the X coordinate of the drag point. The value is only valid if the event action is `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_LOCATION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The current drag point's X coordinate |

### getY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getY(): Float
```

Gets the Y coordinate of the drag point. The value is only valid if the event action is `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_STARTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DRAG_LOCATION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/DragEvent#ACTION_DROP:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The current drag point's Y coordinate |

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string containing a concise, human-readable representation of this DragEvent object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of the DragEvent object. |

### writeToParcel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Creates a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` object from this DragEvent object.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): A `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` object in which to put the DragEvent object. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags to store in the Parcel. |

## Properties

### CREATOR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<DragEvent!>
```

A container for creating a DragEvent from a Parcel.
