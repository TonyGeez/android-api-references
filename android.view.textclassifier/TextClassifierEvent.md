# TextClassifierEvent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassifierEvent

Kotlin| [Java](https://developer.android.com/reference/android/view/textclassifier/TextClassifierEvent "View this page in Java") 

```
abstract class TextClassifierEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.textclassifier.TextClassifierEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#) |

| Known Direct Subclasses [TextClassifierEvent.ConversationActionsEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent), [TextClassifierEvent.LanguageDetectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent), [TextClassifierEvent.TextLinkifyEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent), [TextClassifierEvent.TextSelectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextSelectionEvent) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [TextClassifierEvent.ConversationActionsEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent) | This class represents events that are related to the conversation actions feature. | | [TextClassifierEvent.LanguageDetectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent) | This class represents events that are related to the language detection feature. | | [TextClassifierEvent.TextLinkifyEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent) | This class represents events that are related to the smart linkify feature. | | [TextClassifierEvent.TextSelectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextSelectionEvent) | This class represents events that are related to the smart text selection feature. | |

This class represents events that are sent by components to the [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) to report something of note that relates to a feature powered by the TextClassifier. The TextClassifier may log these events or use them to improve future responses to queries.

Each category of events has its their own subclass. Events of each type have an associated set of related properties. You can find their specification in the subclasses.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.Builder) Builder to build a text classifier event. |
| | [ConversationActionsEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent) This class represents events that are related to the conversation actions feature. |
| | [LanguageDetectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent) This class represents events that are related to the language detection feature. |
| | [TextLinkifyEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent) This class represents events that are related to the smart linkify feature. |
| | [TextSelectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextSelectionEvent) This class represents events that are related to the smart text selection feature. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_CONVERSATION_ACTIONS](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_CONVERSATION_ACTIONS:kotlin.Int) Conversation actions |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_LANGUAGE_DETECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_LANGUAGE_DETECTION:kotlin.Int) Language detection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_LINKIFY](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_LINKIFY:kotlin.Int) Linkify |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SELECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_SELECTION:kotlin.Int) Smart selection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACTIONS_GENERATED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_ACTIONS_GENERATED:kotlin.Int) TextClassifier generated some actions |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACTIONS_SHOWN](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_ACTIONS_SHOWN:kotlin.Int) Smart actions shown to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_AUTO_SELECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_AUTO_SELECTION:kotlin.Int) Something else other than user or the default TextClassifier triggered a selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COPY_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_COPY_ACTION:kotlin.Int) User clicked on Copy action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUT_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_CUT_ACTION:kotlin.Int) User clicked on Cut action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINKS_GENERATED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_LINKS_GENERATED:kotlin.Int) Some text links were generated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINK_CLICKED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_LINK_CLICKED:kotlin.Int) User clicked a link. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MANUAL_REPLY](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_MANUAL_REPLY:kotlin.Int) User composed a reply. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_OTHER_ACTION:kotlin.Int) User clicked on a custom action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OVERTYPE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_OVERTYPE:kotlin.Int) User typed over the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PASTE_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_PASTE_ACTION:kotlin.Int) User clicked on Paste action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_DESTROYED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_DESTROYED:kotlin.Int) Selection is destroyed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_DRAG](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_DRAG:kotlin.Int) User dragged+dropped the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_MODIFIED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_MODIFIED:kotlin.Int) User modified an existing selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_RESET](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_RESET:kotlin.Int) User reset the smart selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_STARTED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_STARTED:kotlin.Int) User started a new selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECT_ALL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECT_ALL:kotlin.Int) User clicked on Select All action |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SHARE_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SHARE_ACTION:kotlin.Int) User clicked on Share action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_ACTION:kotlin.Int) User clicked on a Smart action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_SELECTION_MULTI](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_SELECTION_MULTI:kotlin.Int) Smart selection triggered spanning multiple tokens (words). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_SELECTION_SINGLE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_SELECTION_SINGLE:kotlin.Int) Smart selection triggered for a single token (word). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#describeContents())`()` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getActionIndices](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getActionIndices())`()` Returns the indices of the actions relating to this event. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getEntityTypes](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getEntityTypes())`()` Returns an array of entity types. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventCategory](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getEventCategory())`()` Returns the event category. |
| open [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext)? | [getEventContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getEventContext())`()` Returns the event context. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventIndex](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getEventIndex())`()` Returns the index of this event in the series of event it belongs to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getEventType())`()` Returns the event type. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getExtras](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getExtras())`()` Returns a bundle containing non-structured extra information about this event. |
| open [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)? | [getLocale](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getLocale())`()` Returns the detected locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getModelName](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getModelName())`()` Returns the model name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getResultId](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getResultId())`()` Returns the id of the text classifier result related to this event. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getScores](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#getScores())`()` Returns the scores of the suggestions. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TextClassifierEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CATEGORY_CONVERSATION_ACTIONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_CONVERSATION_ACTIONS: Int
```

Conversation actions 

 Value: 3

**See Also**

- [android.view.textclassifier.TextClassifierEvent.ConversationActionsEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent) 

### CATEGORY_LANGUAGE_DETECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_LANGUAGE_DETECTION: Int
```

Language detection 

 Value: 4

**See Also**

- [android.view.textclassifier.TextClassifierEvent.LanguageDetectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent) 

### CATEGORY_LINKIFY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_LINKIFY: Int
```

Linkify 

 Value: 2

**See Also**

- [android.view.textclassifier.TextClassifierEvent.TextLinkifyEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent) 

### CATEGORY_SELECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_SELECTION: Int
```

Smart selection 

 Value: 1

**See Also**

- [android.view.textclassifier.TextClassifierEvent.TextSelectionEvent](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.TextSelectionEvent) 

### TYPE_ACTIONS_GENERATED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACTIONS_GENERATED: Int
```

TextClassifier generated some actions 

 Value: 20

### TYPE_ACTIONS_SHOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ACTIONS_SHOWN: Int
```

Smart actions shown to the user. 

 Value: 6

### TYPE_AUTO_SELECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_AUTO_SELECTION: Int
```

Something else other than user or the default TextClassifier triggered a selection. 

 Value: 5

### TYPE_COPY_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COPY_ACTION: Int
```

User clicked on Copy action. 

 Value: 9

### TYPE_CUT_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUT_ACTION: Int
```

User clicked on Cut action. 

 Value: 11

### TYPE_LINKS_GENERATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINKS_GENERATED: Int
```

Some text links were generated. 

 Value: 21

### TYPE_LINK_CLICKED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINK_CLICKED: Int
```

User clicked a link. 

 Value: 7

### TYPE_MANUAL_REPLY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MANUAL_REPLY: Int
```

User composed a reply. 

 Value: 19

### TYPE_OTHER_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER_ACTION: Int
```

User clicked on a custom action. 

 Value: 16

### TYPE_OVERTYPE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OVERTYPE: Int
```

User typed over the selection. 

 Value: 8

### TYPE_PASTE_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PASTE_ACTION: Int
```

User clicked on Paste action. 

 Value: 10

### TYPE_SELECTION_DESTROYED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECTION_DESTROYED: Int
```

Selection is destroyed. 

 Value: 15

### TYPE_SELECTION_DRAG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECTION_DRAG: Int
```

User dragged+dropped the selection. 

 Value: 14

### TYPE_SELECTION_MODIFIED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECTION_MODIFIED: Int
```

User modified an existing selection. 

 Value: 2

### TYPE_SELECTION_RESET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECTION_RESET: Int
```

User reset the smart selection. 

 Value: 18

### TYPE_SELECTION_STARTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECTION_STARTED: Int
```

User started a new selection. 

 Value: 1

### TYPE_SELECT_ALL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SELECT_ALL: Int
```

User clicked on Select All action 

 Value: 17

### TYPE_SHARE_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SHARE_ACTION: Int
```

User clicked on Share action. 

 Value: 12

### TYPE_SMART_ACTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SMART_ACTION: Int
```

User clicked on a Smart action. 

 Value: 13

### TYPE_SMART_SELECTION_MULTI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SMART_SELECTION_MULTI: Int
```

Smart selection triggered spanning multiple tokens (words). 

 Value: 4

### TYPE_SMART_SELECTION_SINGLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SMART_SELECTION_SINGLE: Int
```

Smart selection triggered for a single token (word). 

 Value: 3

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActionIndices

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActionIndices(): IntArray
```

Returns the indices of the actions relating to this event. Actions are usually returned by the text classifier in priority order with the most preferred action at index 0. This list gives an indication of the position of the actions that are being reported.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. |

**See Also**

- [android.view.textclassifier.TextClassifierEvent.Builder#setActionIndices(int...)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.Builder#setActionIndices(kotlin.Int)) 

### getEntityTypes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityTypes(): Array<String!>
```

Returns an array of entity types. e.g. [TextClassifier.TYPE_ADDRESS](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

**See Also**

- [android.view.textclassifier.TextClassifierEvent.Builder#setEntityTypes(String...)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent.Builder#setEntityTypes(kotlin.String)) 

### getEventCategory

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventCategory(): Int
```

Returns the event category. e.g. [CATEGORY_SELECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_SELECTION:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.textclassifier.TextClassifierEvent#CATEGORY_SELECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_SELECTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#CATEGORY_LINKIFY](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_LINKIFY:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#CATEGORY_CONVERSATION_ACTIONS](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_CONVERSATION_ACTIONS:kotlin.Int), or [android.view.textclassifier.TextClassifierEvent#CATEGORY_LANGUAGE_DETECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#CATEGORY_LANGUAGE_DETECTION:kotlin.Int) |

### getEventContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventContext(): TextClassificationContext?
```

Returns the event context.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext)? | This value may be`null`. |

### getEventIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventIndex(): Int
```

Returns the index of this event in the series of event it belongs to. 

### getEventType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventType(): Int
```

Returns the event type. e.g. [TYPE_SELECTION_STARTED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_STARTED:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_STARTED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_STARTED:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_MODIFIED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_MODIFIED:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_SELECTION_SINGLE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_SELECTION_SINGLE:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_SELECTION_MULTI](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_SELECTION_MULTI:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_AUTO_SELECTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_AUTO_SELECTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_ACTIONS_SHOWN](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_ACTIONS_SHOWN:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_LINK_CLICKED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_LINK_CLICKED:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_OVERTYPE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_OVERTYPE:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_COPY_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_COPY_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_PASTE_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_PASTE_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_CUT_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_CUT_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SHARE_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SHARE_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SMART_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_DRAG](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_DRAG:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_DESTROYED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_DESTROYED:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_OTHER_ACTION](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_OTHER_ACTION:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECT_ALL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECT_ALL:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_RESET](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_SELECTION_RESET:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_MANUAL_REPLY](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_MANUAL_REPLY:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_ACTIONS_GENERATED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_ACTIONS_GENERATED:kotlin.Int), [android.view.textclassifier.TextClassifierEvent#TYPE_LINKS_GENERATED](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent#TYPE_LINKS_GENERATED:kotlin.Int), or android.view.textclassifier.TextClassifierEvent.TYPE_READ_CLIPBOARD |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle
```

Returns a bundle containing non-structured extra information about this event.

**NOTE:**Do not modify this bundle.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getLocale

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): ULocale?
```

Returns the detected locale.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)? | This value may be`null`. |

### getModelName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModelName(): String?
```

Returns the model name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getResultId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResultId(): String?
```

Returns the id of the text classifier result related to this event.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getScores

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScores(): FloatArray
```

Returns the scores of the suggestions.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | This value cannot be`null`. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
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

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextClassifierEvent!>
```
