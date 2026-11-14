# TextClassifierEvent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassifierEvent

Kotlin| [Java](../android/view/textclassifier/TextClassifierEvent.md) 
| --- | --- |

```
abstract class TextClassifierEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextClassifierEvent](../android/view/textclassifier/TextClassifierEvent.md) |

| Known Direct Subclasses [TextClassifierEvent.ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md), [TextClassifierEvent.LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md), [TextClassifierEvent.TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md), [TextClassifierEvent.TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [TextClassifierEvent.ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md) | This class represents events that are related to the conversation actions feature. | | [TextClassifierEvent.LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md) | This class represents events that are related to the language detection feature. | | [TextClassifierEvent.TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md) | This class represents events that are related to the smart linkify feature. | | [TextClassifierEvent.TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) | This class represents events that are related to the smart text selection feature. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class represents events that are sent by components to the [TextClassifier](../android/view/textclassifier/TextClassifier.md) to report something of note that relates to a feature powered by the TextClassifier. The TextClassifier may log these events or use them to improve future responses to queries.

Each category of events has its their own subclass. Events of each type have an associated set of related properties. You can find their specification in the subclasses.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](../android/view/textclassifier/TextClassifierEvent.Builder.md) Builder to build a text classifier event. |
| | [ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md) This class represents events that are related to the conversation actions feature. |
| | [LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md) This class represents events that are related to the language detection feature. |
| --- | --- |
| | [TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md) This class represents events that are related to the smart linkify feature. |
| | [TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) This class represents events that are related to the smart text selection feature. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_CONVERSATION_ACTIONS](../android/view/textclassifier/TextClassifierEvent.md) Conversation actions |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_LANGUAGE_DETECTION](../android/view/textclassifier/TextClassifierEvent.md) Language detection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_LINKIFY](../android/view/textclassifier/TextClassifierEvent.md) Linkify |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SELECTION](../android/view/textclassifier/TextClassifierEvent.md) Smart selection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACTIONS_GENERATED](../android/view/textclassifier/TextClassifierEvent.md) TextClassifier generated some actions |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ACTIONS_SHOWN](../android/view/textclassifier/TextClassifierEvent.md) Smart actions shown to the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_AUTO_SELECTION](../android/view/textclassifier/TextClassifierEvent.md) Something else other than user or the default TextClassifier triggered a selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COPY_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on Copy action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUT_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on Cut action. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINKS_GENERATED](../android/view/textclassifier/TextClassifierEvent.md) Some text links were generated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINK_CLICKED](../android/view/textclassifier/TextClassifierEvent.md) User clicked a link. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MANUAL_REPLY](../android/view/textclassifier/TextClassifierEvent.md) User composed a reply. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on a custom action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OVERTYPE](../android/view/textclassifier/TextClassifierEvent.md) User typed over the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PASTE_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on Paste action. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_DESTROYED](../android/view/textclassifier/TextClassifierEvent.md) Selection is destroyed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_DRAG](../android/view/textclassifier/TextClassifierEvent.md) User dragged+dropped the selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_MODIFIED](../android/view/textclassifier/TextClassifierEvent.md) User modified an existing selection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_RESET](../android/view/textclassifier/TextClassifierEvent.md) User reset the smart selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECTION_STARTED](../android/view/textclassifier/TextClassifierEvent.md) User started a new selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SELECT_ALL](../android/view/textclassifier/TextClassifierEvent.md) User clicked on Select All action |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SHARE_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on Share action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_ACTION](../android/view/textclassifier/TextClassifierEvent.md) User clicked on a Smart action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_SELECTION_MULTI](../android/view/textclassifier/TextClassifierEvent.md) Smart selection triggered spanning multiple tokens (words). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SMART_SELECTION_SINGLE](../android/view/textclassifier/TextClassifierEvent.md) Smart selection triggered for a single token (word). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/textclassifier/TextClassifierEvent.md))`()` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getActionIndices](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the indices of the actions relating to this event. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getEntityTypes](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns an array of entity types. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventCategory](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the event category. |
| open [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md)? | [getEventContext](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the event context. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventIndex](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the index of this event in the series of event it belongs to. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the event type. |
| open [Bundle](../android/os/Bundle.md) | [getExtras](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns a bundle containing non-structured extra information about this event. |
| open [ULocale](../android/icu/util/ULocale.md)? | [getLocale](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the detected locale. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getModelName](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the model name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getResultId](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the id of the text classifier result related to this event. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getScores](../android/view/textclassifier/TextClassifierEvent.md))`()` Returns the scores of the suggestions. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/textclassifier/TextClassifierEvent.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/textclassifier/TextClassifierEvent.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextClassifierEvent](../android/view/textclassifier/TextClassifierEvent.md)!\> | [CREATOR](../android/view/textclassifier/TextClassifierEvent.md) <br /> |

## Constants

### CATEGORY_CONVERSATION_ACTIONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_CONVERSATION_ACTIONS: Int
```

Conversation actions 

 Value: 3

**See Also**

- [android.view.textclassifier.TextClassifierEvent.ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md) 

### CATEGORY_LANGUAGE_DETECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_LANGUAGE_DETECTION: Int
```

Language detection 

 Value: 4

**See Also**

- [android.view.textclassifier.TextClassifierEvent.LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md) 

### CATEGORY_LINKIFY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_LINKIFY: Int
```

Linkify 

 Value: 2

**See Also**

- [android.view.textclassifier.TextClassifierEvent.TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md) 

### CATEGORY_SELECTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_SELECTION: Int
```

Smart selection 

 Value: 1

**See Also**

- [android.view.textclassifier.TextClassifierEvent.TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

- [android.view.textclassifier.TextClassifierEvent.Builder#setActionIndices(int...)](../android/view/textclassifier/TextClassifierEvent.Builder.md)) 

### getEntityTypes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntityTypes(): Array<String!>
```

Returns an array of entity types. e.g. [TextClassifier.TYPE_ADDRESS](../android/view/textclassifier/TextClassifier.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

**See Also**

- [android.view.textclassifier.TextClassifierEvent.Builder#setEntityTypes(String...)](../android/view/textclassifier/TextClassifierEvent.Builder.md)) 

### getEventCategory

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventCategory(): Int
```

Returns the event category. e.g. [CATEGORY_SELECTION](../android/view/textclassifier/TextClassifierEvent.md).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.textclassifier.TextClassifierEvent#CATEGORY_SELECTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#CATEGORY_LINKIFY](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#CATEGORY_CONVERSATION_ACTIONS](../android/view/textclassifier/TextClassifierEvent.md), or [android.view.textclassifier.TextClassifierEvent#CATEGORY_LANGUAGE_DETECTION](../android/view/textclassifier/TextClassifierEvent.md) |

### getEventContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEventContext(): TextClassificationContext?
```

Returns the event context.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md)? | This value may be`null`. |

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

Returns the event type. e.g. [TYPE_SELECTION_STARTED](../android/view/textclassifier/TextClassifierEvent.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_STARTED](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_MODIFIED](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_SELECTION_SINGLE](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_SELECTION_MULTI](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_AUTO_SELECTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_ACTIONS_SHOWN](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_LINK_CLICKED](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_OVERTYPE](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_COPY_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_PASTE_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_CUT_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SHARE_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SMART_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_DRAG](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_DESTROYED](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_OTHER_ACTION](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECT_ALL](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_SELECTION_RESET](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_MANUAL_REPLY](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_ACTIONS_GENERATED](../android/view/textclassifier/TextClassifierEvent.md), [android.view.textclassifier.TextClassifierEvent#TYPE_LINKS_GENERATED](../android/view/textclassifier/TextClassifierEvent.md), or android.view.textclassifier.TextClassifierEvent.TYPE_READ_CLIPBOARD |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle
```

Returns a bundle containing non-structured extra information about this event.

**NOTE:**Do not modify this bundle.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android/os/Bundle.md) | This value cannot be`null`. |

### getLocale

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): ULocale?
```

Returns the detected locale.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ULocale](../android/icu/util/ULocale.md)? | This value may be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextClassifierEvent!>
```
