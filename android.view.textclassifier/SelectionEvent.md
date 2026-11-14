Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectionEvent

Kotlin | [Java](SelectionEvent.md)
| --- | --- |

```
class SelectionEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.SelectionEvent](SelectionEvent.md) |

A selection event. Specify index parameters as word token indices.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_ABANDON:kotlin.Int` User abandoned the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int` User copied the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_CUT:kotlin.Int` User cut the selection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_DRAG:kotlin.Int` User dragged+dropped the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OTHER:kotlin.Int` User performed an action on the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OVERTYPE:kotlin.Int` User typed over the selection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_PASTE:kotlin.Int` User pasted over the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_RESET:kotlin.Int` User reset the smart selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SELECT_ALL:kotlin.Int` User activated Select All |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SHARE:kotlin.Int` User shared the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SMART_SHARE:kotlin.Int` User clicked the textAssist menu item. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_AUTO_SELECTION:kotlin.Int` Something else other than User or the default TextClassifier triggered a selection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_MODIFIED:kotlin.Int` User modified an existing selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_STARTED:kotlin.Int` User started a new selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_MULTI:kotlin.Int` Smart selection triggered spanning multiple tokens (words). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_SINGLE:kotlin.Int` Smart selection triggered for a single token (word). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_LINK:kotlin.Int` Selection was invoked by the user tapping on a link. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_MANUAL:kotlin.Int` Selection was invoked by the user long pressing, double tapping, or dragging to select. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_UNKNOWN:kotlin.Int` Unknown invocation method |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| static [SelectionEvent](SelectionEvent.md) | createSelectionActionEvent Creates an event specifying an action taken on a selection. |
| static [SelectionEvent](SelectionEvent.md) | createSelectionActionEvent Creates an event specifying an action taken on a selection. |
| static [SelectionEvent](SelectionEvent.md) | createSelectionModifiedEvent Creates a "selection modified" event. |
| --- | --- |
| static [SelectionEvent](SelectionEvent.md) | createSelectionModifiedEvent Creates a "selection modified" event. |
| static [SelectionEvent](SelectionEvent.md) | createSelectionModifiedEvent Creates a "selection modified" event. |
| static [SelectionEvent](SelectionEvent.md) | createSelectionStartedEvent Creates a "selection started" event. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getDurationSincePreviousEvent Returns the duration in ms between when this event was triggered and when the previous event in the selection session was triggered. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getDurationSinceSessionStart Returns the duration in ms between when this event was triggered and when the first event in the selection session was triggered. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEnd Returns the end index of this events relative to the index of the start selection event in the selection session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getEntityType Returns the type of entity that is associated with this event. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEventIndex Returns the index (e.g. 1st event, 2nd event, etc.) of this event in the selection session. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getEventTime Returns the time this event was triggered. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEventType Returns the type of event that was triggered. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInvocationMethod Returns the way the selection mode was invoked. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getPackageName Returns the package name of the app that this event originated in. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getResultId Returns the id of the text classifier result associated with this event. |
| --- | --- |
| [TextClassificationSessionId](TextClassificationSessionId.md)? | getSessionId Returns the selection session id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSmartEnd Returns the end index of this events relative to the index of the smart selection event in the selection session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSmartStart Returns the start index of this events relative to the index of the smart selection event in the selection session. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStart Returns the start index of this events relative to the index of the start selection event in the selection session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getWidgetType Returns the type of widget that was involved in triggering this event. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getWidgetVersion Returns a string version info for the widget this event was triggered in. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isTerminal Returns true if the eventType is a terminal event type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SelectionEvent](SelectionEvent.md)!\> | `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACTION_ABANDON

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ABANDON: Int
```

User abandoned the selection.

 Value: 107

### ACTION_COPY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_COPY: Int
```

User copied the selection.

 Value: 101

### ACTION_CUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CUT: Int
```

User cut the selection.

 Value: 103

### ACTION_DRAG

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DRAG: Int
```

User dragged+dropped the selection.

 Value: 106

### ACTION_OTHER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_OTHER: Int
```

User performed an action on the selection.

 Value: 108

### ACTION_OVERTYPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_OVERTYPE: Int
```

User typed over the selection.

 Value: 100

### ACTION_PASTE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASTE: Int
```

User pasted over the selection.

 Value: 102

### ACTION_RESET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RESET: Int
```

User reset the smart selection.

 Value: 201

### ACTION_SELECT_ALL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SELECT_ALL: Int
```

User activated Select All

 Value: 200

### ACTION_SHARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHARE: Int
```

User shared the selection.

 Value: 104

### ACTION_SMART_SHARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SMART_SHARE: Int
```

User clicked the textAssist menu item.

 Value: 105

### EVENT_AUTO_SELECTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_AUTO_SELECTION: Int
```

Something else other than User or the default TextClassifier triggered a selection.

 Value: 5

### EVENT_SELECTION_MODIFIED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_SELECTION_MODIFIED: Int
```

User modified an existing selection.

 Value: 2

### EVENT_SELECTION_STARTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_SELECTION_STARTED: Int
```

User started a new selection.

 Value: 1

### EVENT_SMART_SELECTION_MULTI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_SMART_SELECTION_MULTI: Int
```

Smart selection triggered spanning multiple tokens (words).

 Value: 4

### EVENT_SMART_SELECTION_SINGLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_SMART_SELECTION_SINGLE: Int
```

Smart selection triggered for a single token (word).

 Value: 3

### INVOCATION_LINK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVOCATION_LINK: Int
```

Selection was invoked by the user tapping on a link.

 Value: 2

### INVOCATION_MANUAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVOCATION_MANUAL: Int
```

Selection was invoked by the user long pressing, double tapping, or dragging to select.

 Value: 1

### INVOCATION_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVOCATION_UNKNOWN: Int
```

Unknown invocation method

 Value: 0

## Public methods

### createSelectionActionEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionActionEvent(
    start: Int, 
    end: Int, 
    actionType: Int
): SelectionEvent
```

Creates an event specifying an action taken on a selection. Use when the user clicks on an action to act on the selected text.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start (inclusive) index of the selection |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end (exclusive) index of the selection |
| `actionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the action that was performed on the selection. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OVERTYPE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SMART_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_DRAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_ABANDON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SELECT_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_RESET:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if end is less than start |

### createSelectionActionEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionActionEvent(
    start: Int, 
    end: Int, 
    actionType: Int, 
    classification: TextClassification
): SelectionEvent
```

Creates an event specifying an action taken on a selection. Use when the user clicks on an action to act on the selected text and the selection's entity type is known.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start (inclusive) index of the selection |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end (exclusive) index of the selection |
| `actionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the action that was performed on the selection. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OVERTYPE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SMART_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_DRAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_ABANDON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SELECT_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_RESET:kotlin.Int` |
| --- | --- |
| `classification` | [TextClassification](TextClassification.md): the TextClassification object returned by the TextClassifier that classified the selected text. This value cannot be `null`. |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If actionType is not a valid SelectionEvent actionType |

### createSelectionModifiedEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionModifiedEvent(
    start: Int, 
    end: Int
): SelectionEvent
```

Creates a "selection modified" event. Use when the user modifies the selection.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start (inclusive) index of the selection |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end (exclusive) index of the selection |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if end is less than start |

### createSelectionModifiedEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionModifiedEvent(
    start: Int, 
    end: Int, 
    classification: TextClassification
): SelectionEvent
```

Creates a "selection modified" event. Use when the user modifies the selection and the selection's entity type is known.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start (inclusive) index of the selection |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end (exclusive) index of the selection |
| `classification` | [TextClassification](TextClassification.md): the TextClassification object returned by the TextClassifier that classified the selected text. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if end is less than start |

### createSelectionModifiedEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionModifiedEvent(
    start: Int, 
    end: Int, 
    selection: TextSelection
): SelectionEvent
```

Creates a "selection modified" event. Use when a TextClassifier modifies the selection.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start (inclusive) index of the selection |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end (exclusive) index of the selection |
| `selection` | [TextSelection](TextSelection.md): the TextSelection object returned by the TextClassifier for the specified selection. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if end is less than start |

### createSelectionStartedEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSelectionStartedEvent(
    invocationMethod: Int, 
    start: Int
): SelectionEvent
```

Creates a "selection started" event.

| Parameters ||
|---|---|
| `invocationMethod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the way the selection was triggered. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_MANUAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_LINK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_UNKNOWN:kotlin.Int` |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the selected text |

| Return ||
|---|---|
| SelectionEvent | This value cannot be `null`. |

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDurationSincePreviousEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDurationSincePreviousEvent(): Long
```

Returns the duration in ms between when this event was triggered and when the previous event in the selection session was triggered.

### getDurationSinceSessionStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDurationSinceSessionStart(): Long
```

Returns the duration in ms between when this event was triggered and when the first event in the selection session was triggered.

### getEnd

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnd(): Int
```

Returns the end index of this events relative to the index of the start selection event in the selection session.

### getEntityType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEntityType(): String
```

Returns the type of entity that is associated with this event. e.g. `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String` . This value cannot be `null`. |

### getEventIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEventIndex(): Int
```

Returns the index (e.g. 1st event, 2nd event, etc.) of this event in the selection session.

### getEventTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEventTime(): Long
```

Returns the time this event was triggered.

### getEventType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEventType(): Int
```

Returns the type of event that was triggered. e.g. `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OVERTYPE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SMART_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_DRAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_ABANDON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SELECT_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_STARTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_MODIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_SINGLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_MULTI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_AUTO_SELECTION:kotlin.Int` |

### getInvocationMethod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInvocationMethod(): Int
```

Returns the way the selection mode was invoked.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_MANUAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_LINK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#INVOCATION_UNKNOWN:kotlin.Int` |

### getPackageName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Returns the package name of the app that this event originated in.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getResultId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultId(): String?
```

Returns the id of the text classifier result associated with this event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getSessionId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionId(): TextClassificationSessionId?
```

Returns the selection session id.

| Return ||
|---|---|
| TextClassificationSessionId | This value may be `null`. |

### getSmartEnd

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSmartEnd(): Int
```

Returns the end index of this events relative to the index of the smart selection event in the selection session.

### getSmartStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSmartStart(): Int
```

Returns the start index of this events relative to the index of the smart selection event in the selection session.

### getStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStart(): Int
```

Returns the start index of this events relative to the index of the start selection event in the selection session.

### getWidgetType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidgetType(): String
```

Returns the type of widget that was involved in triggering this event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDITTEXT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNSELECTABLE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_WEBVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDIT_WEBVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_EDITTEXT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_UNSELECTABLE_TEXTVIEW:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_NOTIFICATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CLIPBOARD:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNKNOWN:kotlin.String` . This value cannot be `null`. |

### getWidgetVersion

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidgetVersion(): String?
```

Returns a string version info for the widget this event was triggered in.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isTerminal

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isTerminal(eventType: Int): Boolean
```

Returns true if the eventType is a terminal event type. Otherwise returns false. A terminal event is an event that ends a selection interaction.

| Parameters ||
|---|---|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OVERTYPE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SMART_SHARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_DRAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_ABANDON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_SELECT_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#ACTION_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_STARTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SELECTION_MODIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_SINGLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_SMART_SELECTION_MULTI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent#EVENT_AUTO_SELECTION:kotlin.Int` |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SelectionEvent!>
```
