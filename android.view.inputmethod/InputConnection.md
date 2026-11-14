Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputConnection

```
interface InputConnection
```

| [android.view.inputmethod.InputConnection](InputConnection.md) |

Known Direct Subclasses [BaseInputConnection](BaseInputConnection.md), [InputConnectionWrapper](InputConnectionWrapper.md) [BaseInputConnection](BaseInputConnection.md) Base class for implementors of the InputConnection interface, taking care of most of the common behavior for providing a connection to an Editable.
[InputConnectionWrapper](InputConnectionWrapper.md) Wrapper class for proxying calls to another InputConnection.

The InputConnection interface is the communication channel from an InputMethod back to the application that is receiving its input. It is used to perform such things as reading text around the cursor, committing text to the text box, and sending raw key events to the application.

Starting from API Level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, the system can deal with the situation where the application directly implements this class but one or more of the following methods are not implemented.

- getSelectedText, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD:kotlin.Int`.
- setComposingRegion, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD:kotlin.Int`.
- commitCorrection, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`.
- requestCursorUpdates, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`.
- deleteSurroundingTextInCodePoints, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`.
- getHandler, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`.
- closeConnection, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`.
- commitContent, which was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`.

### Implementing an IME or an editor

Text input is the result of the synergy of two essential components: an Input Method Engine (IME) and an editor. The IME can be a software keyboard, a handwriting interface, an emoji palette, a speech-to-text engine, and so on. There are typically several IMEs installed on any given Android device. In Android, IMEs extend `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`. For more information about how to create an IME, see the [Creating an input method](https://developer.android.com/guide/topics/text/creating-input-method.html) guide. The editor is the component that receives text and displays it. Typically, this is an `https://developer.android.com/reference/kotlin/android/widget/EditText.html#` instance, but some applications may choose to implement their own editor for various reasons. This is a large and complicated task, and an application that does this needs to make sure the behavior is consistent with standard EditText behavior in Android. An editor needs to interact with the IME, receiving commands through this InputConnection interface, and sending commands through InputMethodManager. An editor should start by implementing onCreateInputConnection to return its own input connection.

If you are implementing your own IME, you will need to call the methods in this interface to interact with the application. Be sure to test your IME with a wide range of applications, including browsers and rich text editors, as some may have peculiarities you need to deal with. Remember your IME may not be the only source of changes on the text, and try to be as conservative as possible in the data you send and as liberal as possible in the data you receive.

If you are implementing your own editor, you will probably need to provide your own subclass of BaseInputConnection to answer to the commands from IMEs. Please be sure to test your editor with as many IMEs as you can as their behavior can vary a lot. Also be sure to test with various languages, including CJK languages and right-to-left languages like Arabic, as these may have different input requirements. When in doubt about the behavior you should adopt for a particular call, please mimic the default TextView implementation in the latest Android version, and if you decide to drift from it, please consider carefully that inconsistencies in text editor behavior is almost universally felt as a bad thing by users.

### Cursors, selections and compositions

In Android, the cursor and the selection are one and the same thing. A "cursor" is just the special case of a zero-sized selection. As such, this documentation uses them interchangeably. Any method acting "before the cursor" would act before the start of the selection if there is one, and any method acting "after the cursor" would act after the end of the selection.

An editor needs to be able to keep track of a currently "composing" region, like the standard edition widgets do. The composition is marked in a specific style: see `https://developer.android.com/reference/kotlin/android/text/Spanned.html#SPAN_COMPOSING:kotlin.Int`. IMEs use this to help the user keep track of what part of the text they are currently focusing on, and interact with the editor using setComposingText, setComposingRegion and finishComposingText. The composing region and the selection are completely independent of each other, and the IME may use them however they see fit.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int` The editor is requested to call updateCursorAnchorInfo with new character bounds getCharacterBounds whenever cursor/anchor position is changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` The editor is requested to call updateCursorAnchorInfo with new EditorBoundsInfo whenever cursor/anchor position is changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` The editor is requested to call updateCursorAnchorInfo with new Insertion marker info getInsertionMarkerFlags, getInsertionMarkerBaseline, etc whenever cursor/anchor position is changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` The editor is requested to call updateCursorAnchorInfo with new text appearance info getTextAppearanceInfo} whenever cursor/anchor position is changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int` The editor is requested to call updateCursorAnchorInfo with new visible line bounds getVisibleLineBounds whenever cursor/anchor position is changed, the editor or its parent is scrolled or the line bounds changed due to text updates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` The editor is requested to call updateCursorAnchorInfo at once, as soon as possible, regardless of cursor/anchor position changes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int` The editor is requested to call updateCursorAnchorInfo whenever cursor/anchor position is changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_EXTRACTED_TEXT_MONITOR:kotlin.Int` Flag for use with getExtractedText to indicate you would like to receive updates when the extracted text changes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` Flag for use with getTextAfterCursor, getTextBeforeCursor and getSurroundingText to have style information returned along with the text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_CANCELLED:kotlin.Int` Result for performHandwritingGesture when HandwritingGesture was cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FAILED:kotlin.Int` Result for performHandwritingGesture when HandwritingGesture failed and there was no applicable getFallbackText or it couldn't be applied for any other reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FALLBACK:kotlin.Int` Result for performHandwritingGesture when HandwritingGesture failed but getFallbackText was committed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_SUCCESS:kotlin.Int` Result for performHandwritingGesture when HandwritingGesture is successfully executed on text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNKNOWN:kotlin.Int` Result for performHandwritingGesture when editor didn't provide any result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNSUPPORTED:kotlin.Int` Result for performHandwritingGesture when HandwritingGesture is unsupported by the current editor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#INPUT_CONTENT_GRANT_READ_URI_PERMISSION:kotlin.Int` When this flag is used, the editor will be able to request read access to the content URI contained in the InputContentInfo object. |

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | beginBatchEdit Tell the editor that you are starting a batch of editor operations. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | clearMetaKeyStates Clear the given meta key pressed states in the given input connection. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | closeConnection Called by the system up to only once to notify that the system is about to invalidate connection between the input method and the application. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | commitCompletion Commit a completion the user has selected from the possible ones previously reported to displayCompletions or displayCompletions. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | commitContent Called by the input method to commit content such as a PNG image to the editor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | commitCorrection Commit a correction automatically performed on the raw user's input. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | commitText Commit text to the text box and set the new cursor position. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | commitText The variant of commitText. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | deleteSurroundingText Delete beforeLength characters of text before the current cursor position, and delete afterLength characters of text after the current cursor position, excluding the selection. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | deleteSurroundingTextInCodePoints A variant of deleteSurroundingText. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | endBatchEdit Tell the editor that you are done with a batch edit previously initiated with beginBatchEdit. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | finishComposingText Have the text editor finish whatever composing text is currently active. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCursorCapsMode Retrieve the current capitalization mode in effect at the current cursor position in the text. |
| abstract [ExtractedText](ExtractedText.md)? | getExtractedText Retrieve the current text in the input connection's editor, and monitor for any changes to it. |
| abstract [Handler](../android.os/Handler.md)? | getHandler Called by the system to enable application developers to specify a dedicated thread on which InputConnection methods are called back. |
| --- | --- |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getSelectedText Gets the selected text, if any. |
| open [SurroundingText](SurroundingText.md)? | getSurroundingText Gets the surrounding text around the current cursor, with beforeLength characters of text before the cursor (start of the selection), afterLength characters of text after the cursor (end of the selection), and all of the selected text. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getTextAfterCursor Get n characters of text after the current cursor position. |
| --- | --- |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getTextBeforeCursor Get n characters of text before the current cursor position. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performContextMenuAction Perform a context menu action on the field. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performEditorAction Have the editor perform an action it has said it can do. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | performHandwritingGesture Perform a handwriting gesture on text. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performPrivateCommand API to send private commands from an input method to its connected editor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | performSpellCheck Have the editor perform spell checking for the full content. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | previewHandwritingGesture Preview a handwriting gesture on text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | replaceText Replace the specific range in the editor with suggested text. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | reportFullscreenMode Called back when the connected IME switches between fullscreen and normal modes. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestCursorUpdates Called by the input method to ask the editor for calling back updateCursorAnchorInfo to notify cursor/anchor locations. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requestCursorUpdates Called by the input method to ask the editor for calling back updateCursorAnchorInfo to notify cursor/anchor locations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestTextBoundsInfo Called by input method to request the TextBoundsInfo for a range of text which is covered by or in vicinity of the given `bounds`. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | sendKeyEvent Send a key event to the process that is currently attached through this input connection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setComposingRegion Mark a certain region of text as composing text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setComposingRegion The variant of setComposingRegion. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setComposingText Replace the currently composing text with the given text, and set the new cursor position. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setComposingText The variant of setComposingText. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setImeConsumesInput Called by the input method to indicate that it consumes all input for itself, or no longer does so. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setSelection Set the selection of the text editor. |
| open [TextSnapshot](TextSnapshot.md)? | takeSnapshot Called by the system when it needs to take a snapshot of multiple text-related data in an atomic manner. |

## Constants

### CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS: Int
```

The editor is requested to call updateCursorAnchorInfo with new character bounds getCharacterBounds whenever cursor/anchor position is changed. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

 Value: 8

### CURSOR_UPDATE_FILTER_EDITOR_BOUNDS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_FILTER_EDITOR_BOUNDS: Int
```

The editor is requested to call updateCursorAnchorInfo with new EditorBoundsInfo whenever cursor/anchor position is changed. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be used together with filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

 Value: 4

### CURSOR_UPDATE_FILTER_INSERTION_MARKER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_FILTER_INSERTION_MARKER: Int
```

The editor is requested to call updateCursorAnchorInfo with new Insertion marker info getInsertionMarkerFlags, getInsertionMarkerBaseline, etc whenever cursor/anchor position is changed. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

 Value: 16

### CURSOR_UPDATE_FILTER_TEXT_APPEARANCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_FILTER_TEXT_APPEARANCE: Int
```

The editor is requested to call updateCursorAnchorInfo with new text appearance info getTextAppearanceInfo} whenever cursor/anchor position is changed. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

 Value: 64

### CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS: Int
```

The editor is requested to call updateCursorAnchorInfo with new visible line bounds getVisibleLineBounds whenever cursor/anchor position is changed, the editor or its parent is scrolled or the line bounds changed due to text updates. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

 Value: 32

### CURSOR_UPDATE_IMMEDIATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_IMMEDIATE: Int
```

The editor is requested to call updateCursorAnchorInfo at once, as soon as possible, regardless of cursor/anchor position changes. This flag can be used together with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

Note by default all of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, are included but specifying them can filter-out others. It can be CPU intensive to include all, filtering specific info is recommended.

 Value: 1

### CURSOR_UPDATE_MONITOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_UPDATE_MONITOR: Int
```

The editor is requested to call updateCursorAnchorInfo whenever cursor/anchor position is changed. To disable monitoring, call requestCursorUpdates again with this flag off.

This flag can be used together with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`.

Note by default all of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, are included but specifying them can filter-out others. It can be CPU intensive to include all, filtering specific info is recommended.

 Value: 2

### GET_EXTRACTED_TEXT_MONITOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_EXTRACTED_TEXT_MONITOR: Int
```

Flag for use with getExtractedText to indicate you would like to receive updates when the extracted text changes.

 Value: 1

### GET_TEXT_WITH_STYLES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_TEXT_WITH_STYLES: Int
```

Flag for use with getTextAfterCursor, getTextBeforeCursor and getSurroundingText to have style information returned along with the text. If not set, getTextAfterCursor sends only the raw text, without style or other spans. If set, it may return a complex CharSequence of both text and style spans. **Editor authors**: you should strive to send text with styles if possible, but it is not required.

 Value: 1

### HANDWRITING_GESTURE_RESULT_CANCELLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_CANCELLED: Int
```

Result for performHandwritingGesture when HandwritingGesture was cancelled. This happens when the InputConnection is or becomes invalidated while performing the gesture, for example because a new `InputConnection` was started, or due to invalidateInput.

 Value: 4

### HANDWRITING_GESTURE_RESULT_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_FAILED: Int
```

Result for performHandwritingGesture when HandwritingGesture failed and there was no applicable getFallbackText or it couldn't be applied for any other reason.

 Value: 3

### HANDWRITING_GESTURE_RESULT_FALLBACK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_FALLBACK: Int
```

Result for performHandwritingGesture when HandwritingGesture failed but getFallbackText was committed.

 Value: 5

### HANDWRITING_GESTURE_RESULT_SUCCESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_SUCCESS: Int
```

Result for performHandwritingGesture when HandwritingGesture is successfully executed on text.

 Value: 1

### HANDWRITING_GESTURE_RESULT_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_UNKNOWN: Int
```

Result for performHandwritingGesture when editor didn't provide any result.

 Value: 0

### HANDWRITING_GESTURE_RESULT_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANDWRITING_GESTURE_RESULT_UNSUPPORTED: Int
```

Result for performHandwritingGesture when HandwritingGesture is unsupported by the current editor.

 Value: 2

### INPUT_CONTENT_GRANT_READ_URI_PERMISSION

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INPUT_CONTENT_GRANT_READ_URI_PERMISSION: Int
```

When this flag is used, the editor will be able to request read access to the content URI contained in the InputContentInfo object.

Make sure that the content provider owning the Uri sets the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag. Otherwise requestPermission can fail.

Although calling this API is allowed only for the IME that is currently selected, the client is able to request a temporary read-only access even after the current IME is switched to any other IME as long as the client keeps InputContentInfo object.

 Value: 1

## Public methods

### beginBatchEdit

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun beginBatchEdit(): Boolean
```

Tell the editor that you are starting a batch of editor operations. The editor will try to avoid sending you updates about its state until endBatchEdit is called. Batch edits nest.

**IME authors:** use this to avoid getting calls to onUpdateSelection corresponding to intermediate state. Also, use this to avoid flickers that may arise from displaying intermediate state. Be sure to call endBatchEdit for each call to this, or you may block updates in the editor.

**Editor authors:** while a batch edit is in progress, take care not to send updates to the input method and not to update the display. IMEs use this intensively to this effect. Also please note that batch edits need to nest correctly.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a batch edit is now in progress, false otherwise. Since this method starts a batch edit, that means it will always return true unless the input connection is no longer valid. |

### clearMetaKeyStates

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clearMetaKeyStates(states: Int): Boolean
```

Clear the given meta key pressed states in the given input connection.

This can be used by the IME to clear the meta key states set by a hardware keyboard with latched meta keys, if the editor keeps track of these.

| Parameters ||
|---|---|
| `states` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The states to be cleared, may be one or more bits as per getMetaState. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### closeConnection

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun closeConnection(): Unit
```

Called by the system up to only once to notify that the system is about to invalidate connection between the input method and the application.

**Editor authors** : You can clear all the nested batch edit right now and you no longer need to handle subsequent callbacks on this connection, including beginBatchEdit}. Note that although the system tries to call this method whenever possible, there may be a chance that this method is not called in some exceptional situations.

Note: This does nothing when called from input methods.

### commitCompletion

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun commitCompletion(text: CompletionInfo!): Boolean
```

Commit a completion the user has selected from the possible ones previously reported to displayCompletions or displayCompletions. This will result in the same behavior as if the user had selected the completion from the actual UI. In all other respects, this behaves like commitText.

**IME authors:** please take care to send the same object that you received through onDisplayCompletions.

**Editor authors:** if you never call displayCompletions or displayCompletions then a well-behaved IME should never call this on your input connection, but be ready to deal with misbehaving IMEs without crashing.

Calling this method (with a valid CompletionInfo object) will cause the editor to call onUpdateSelection on the current IME after the batch input is over. **Editor authors** , for this to happen you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress.

| Parameters ||
|---|---|
| `text` | [CompletionInfo](CompletionInfo.md)!: The committed completion. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### commitContent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun commitContent(
    inputContentInfo: InputContentInfo, 
    flags: Int, 
    opts: Bundle?
): Boolean
```

Called by the input method to commit content such as a PNG image to the editor.

In order to avoid a variety of compatibility issues, this focuses on a simple use case, where editors and IMEs are expected to work cooperatively as follows:

- Editor must keep `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#contentMimeTypes:kotlin.Array` equal to `null` if it does not support this method at all.
- Editor can ignore this request when the MIME type specified in `inputContentInfo` does not match any of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#contentMimeTypes:kotlin.Array`.
- Editor can ignore the cursor position when inserting the provided content.
- Editor can return `true` asynchronously, even before it starts loading the content.
- Editor should provide a way to delete the content inserted by this method or to revert the effect caused by this method.
- IME should not call this method when there is any composing text, in case calling this method causes a focus change.
- IME should grant a permission for the editor to read the content. See `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#packageName:kotlin.String` about how to obtain the package name of the editor.

| Parameters ||
|---|---|
| `inputContentInfo` | [InputContentInfo](InputContentInfo.md): Content to be inserted. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#INPUT_CONTENT_GRANT_READ_URI_PERMISSION:kotlin.Int` if the content provider allows `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` or `0` if the application does not need to call requestPermission. |
| `opts` | [Bundle](../android.os/Bundle.md)?: optional bundle data. This can be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this request is accepted by the application, whether the request is already handled or still being handled in background, `false` otherwise. |

### commitCorrection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun commitCorrection(correctionInfo: CorrectionInfo!): Boolean
```

Commit a correction automatically performed on the raw user's input. A typical example would be to correct typos using a dictionary.

Calling this method will cause the editor to call onUpdateSelection on the current IME after the batch input is over. **Editor authors** , for this to happen you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress.

| Parameters ||
|---|---|
| `correctionInfo` | [CorrectionInfo](CorrectionInfo.md)!: Detailed information about the correction. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### commitText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun commitText(
    text: CharSequence!, 
    newCursorPosition: Int
): Boolean
```

Commit text to the text box and set the new cursor position.

This method removes the contents of the currently composing text and replaces it with the passed CharSequence, and then moves the cursor according to `newCursorPosition`. If there is no composing text when this method is called, the new text is inserted at the cursor position, removing text inside the selection if any. This behaves like calling setComposingText then finishComposingText.

Calling this method will cause the editor to call onUpdateSelection on the current IME after the batch input is over. **Editor authors** , for this to happen you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to commit. This may include styles. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text, in Java characters. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance the cursor to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### commitText

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commitText(
    text: CharSequence, 
    newCursorPosition: Int, 
    textAttribute: TextAttribute?
): Boolean
```

The variant of commitText. This method is used to allow the IME to provide extra information while setting up text.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The text to commit. This may include styles. This value cannot be `null`. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text, in Java characters. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance the cursor to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |
| `textAttribute` | [TextAttribute](TextAttribute.md)?: The extra information about the text. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### deleteSurroundingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun deleteSurroundingText(
    beforeLength: Int, 
    afterLength: Int
): Boolean
```

Delete beforeLength characters of text before the current cursor position, and delete afterLength characters of text after the current cursor position, excluding the selection. Before and after refer to the order of the characters in the string, not to their visual representation: this means you don't have to figure out the direction of the text and can just use the indices as-is.

The lengths are supplied in Java chars, not in code points or in glyphs.

Since this method only operates on text before and after the selection, it can't affect the contents of the selection. This may affect the composing span if the span includes characters that are to be deleted, but otherwise will not change it. If some characters in the composing span are deleted, the composing span will persist but get shortened by however many chars inside it have been removed.

**IME authors:** please be careful not to delete only half of a surrogate pair. Also take care not to delete more characters than are in the editor, as that may have ill effects on the application. Calling this method will cause the editor to call onUpdateSelection on your service after the batch input is over.

**Editor authors:** please be careful of race conditions in implementing this call. An IME can make a change to the text or change the selection position and use this method right away; you need to make sure the effects are consistent with the results of the latest edits. Also, although the IME should not send lengths bigger than the contents of the string, you should check the values for overflows and trim the indices to the size of the contents to avoid crashes. Since this changes the contents of the editor, you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters before the cursor to be deleted, in code unit. If this is greater than the number of existing characters between the beginning of the text and the cursor, then this method does not fail but deletes all the characters in that range. |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters after the cursor to be deleted, in code unit. If this is greater than the number of existing characters between the cursor and the end of the text, then this method does not fail but deletes all the characters in that range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### deleteSurroundingTextInCodePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun deleteSurroundingTextInCodePoints(
    beforeLength: Int, 
    afterLength: Int
): Boolean
```

A variant of deleteSurroundingText. Major differences are:

- The lengths are supplied in code points, not in Java chars or in glyphs.
- This method does nothing if there are one or more invalid surrogate pairs in the requested range.

<br />

**Editor authors:** In addition to the requirement in deleteSurroundingText, make sure to do nothing when one ore more invalid surrogate pairs are found in the requested range.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters before the cursor to be deleted, in code points. If this is greater than the number of existing characters between the beginning of the text and the cursor, then this method does not fail but deletes all the characters in that range. |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters after the cursor to be deleted, in code points. If this is greater than the number of existing characters between the cursor and the end of the text, then this method does not fail but deletes all the characters in that range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Before Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

**See Also**

- deleteSurroundingText

### endBatchEdit

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun endBatchEdit(): Boolean
```

Tell the editor that you are done with a batch edit previously initiated with beginBatchEdit. This ends the latest batch only.

**IME authors:** make sure you call this exactly once for each call to beginBatchEdit.

**Editor authors:** please be careful about batch edit nesting. Updates still to be held back until the end of the last batch edit. In case you are delegating this API call to the one obtained from onCreateInputConnection, there was an off-by-one that had returned `true` when its nested batch edit count becomes `0` as a result of invoking this API. This bug is fixed in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, you must return `true` if a batch edit is still in progress after closing the latest one (in other words, if the nesting count is still a positive number). Return `false` otherwise. For IME authors, you will always receive `true` as long as the request was sent to the editor, and receive `false` only if the input connection is no longer valid. |

### finishComposingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun finishComposingText(): Boolean
```

Have the text editor finish whatever composing text is currently active. This simply leaves the text as-is, removing any special composing styling or other state that was around it. The cursor position remains unchanged.

**IME authors:** be aware that this call may be expensive with some editors.

**Editor authors:** please note that the cursor may be anywhere in the contents when this is called, including in the middle of the composing span or in a completely unrelated place. It must not move.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### getCursorCapsMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCursorCapsMode(reqModes: Int): Int
```

Retrieve the current capitalization mode in effect at the current cursor position in the text. See getCapsMode for more information.

This method may fail either if the input connection has become invalid (such as its process crashing) or the client is taking too long to respond with the text (it is given a couple seconds to return). In either case, 0 is returned.

This method does not affect the text in the editor in any way, nor does it affect the selection or composing spans.

**Editor authors:** please be careful of race conditions in implementing this call. An IME can change the cursor position and use this method right away; you need to make sure the returned value is consistent with the results of the latest edits and changes to the cursor position.

| Parameters ||
|---|---|
| `reqModes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired modes to retrieve, as defined by getCapsMode. These constants are defined so that you can simply pass the current `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#inputType:kotlin.Int` value directly in to here. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the caps mode flags that are in effect at the current cursor position. See TYPE_TEXT_FLAG_CAPS_\* in `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |

### getExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getExtractedText(
    request: ExtractedTextRequest!, 
    flags: Int
): ExtractedText?
```

Retrieve the current text in the input connection's editor, and monitor for any changes to it. This function returns with the current text, and optionally the input connection can send updates to the input method when its text changes.

This method may fail either if the input connection has become invalid (such as its process crashing) or the client is taking too long to respond with the text (it is given a couple seconds to return). In either case, null is returned.

Editor authors: as a general rule, try to comply with the fields in `request` for how many chars to return, but if performance or convenience dictates otherwise, please feel free to do what is most appropriate for your case. Also, if the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_EXTRACTED_TEXT_MONITOR:kotlin.Int` flag is set, you should be calling updateExtractedText whenever you call updateSelection.

| Parameters ||
|---|---|
| `request` | [ExtractedTextRequest](ExtractedTextRequest.md)!: Description of how the text should be returned. ExtractedTextRequest |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional options to control the client, either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_EXTRACTED_TEXT_MONITOR:kotlin.Int`. |

| Return ||
|---|---|
| ExtractedText | an ExtractedText object describing the state of the text view and containing the extracted text itself, or null if the input connection is no longer valid of the editor can't comply with the request for some reason. |

### getHandler

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getHandler(): Handler?
```

Called by the system to enable application developers to specify a dedicated thread on which InputConnection methods are called back.

**Editor authors** : although you can return your custom subclasses of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`, the system only uses `https://developer.android.com/reference/kotlin/android/os/Looper.html#` returned from getLooper. You cannot intercept or cancel InputConnection callbacks by implementing this method.

**IME authors** : This method is not intended to be called from the IME. You will always receive `null`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler.html#?` | `null` to use the default `https://developer.android.com/reference/kotlin/android/os/Handler.html#`. |

### getSelectedText

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSelectedText(flags: Int): CharSequence?
```

Gets the selected text, if any.

This method may fail if either the input connection has become invalid (such as its process crashing) or the client is taking too long to respond with the text (it is given a couple of seconds to return). In either case, null is returned.

This method must not cause any changes in the editor's state.

If `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` is supplied as flags, the editor should return a `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` with all the spans set on the text.

**IME authors:** please consider this will trigger an IPC round-trip that will take some time. Assume this method consumes a lot of time. If you are using this to get the initial text around the cursor, you may consider using getInitialTextBeforeCursor, getInitialSelectedText, and getInitialTextAfterCursor to prevent IPC costs.

**Editor authors:** please be careful of race conditions in implementing this call. An IME can make a change to the text or change the selection position and use this method right away; you need to make sure the returned value is consistent with the results of the latest edits.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text that is currently selected, if any, or `null` if no text is selected. |

### getSurroundingText

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurroundingText(
    beforeLength: Int, 
    afterLength: Int, 
    flags: Int
): SurroundingText?
```

Gets the surrounding text around the current cursor, with beforeLength characters of text before the cursor (start of the selection), afterLength characters of text after the cursor (end of the selection), and all of the selected text. The range are for java characters, not glyphs that can be multiple characters.

This method may fail either if the input connection has become invalid (such as its process crashing), or the client is taking too long to respond with the text (it is given a couple seconds to return), or the protocol is not supported. In any of these cases, null is returned.

This method does not affect the text in the editor in any way, nor does it affect the selection or composing spans.

If `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` is supplied as flags, the editor should return a `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` with all the spans set on the text.

**IME authors:** please consider this will trigger an IPC round-trip that will take some time. Assume this method consumes a lot of time. If you are using this to get the initial surrounding text around the cursor, you may consider using getInitialTextBeforeCursor, getInitialSelectedText, and getInitialTextAfterCursor to prevent IPC costs.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text before the cursor. Value is 0 or greater |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text after the cursor. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| SurroundingText | an SurroundingText object describing the surrounding text and state of selection, or null if the input connection is no longer valid, or the editor can't comply with the request for some reason, or the application does not implement this method. The length of the returned text might be less than the sum of beforeLength and afterLength . |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `beforeLength` or `afterLength` is negative. |

### getTextAfterCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTextAfterCursor(
    n: Int, 
    flags: Int
): CharSequence?
```

Get n characters of text after the current cursor position.

This method may fail either if the input connection has become invalid (such as its process crashing) or the client is taking too long to respond with the text (it is given a couple seconds to return). In either case, null is returned.

This method does not affect the text in the editor in any way, nor does it affect the selection or composing spans.

If `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` is supplied as flags, the editor should return a `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` with all the spans set on the text.

**IME authors:** please consider this will trigger an IPC round-trip that will take some time. Assume this method consumes a lot of time. If you are using this to get the initial text around the cursor, you may consider using getInitialTextBeforeCursor, getInitialSelectedText, and getInitialTextAfterCursor to prevent IPC costs.

**Editor authors:** please be careful of race conditions in implementing this call. An IME can make a change to the text and use this method right away; you need to make sure the returned value is consistent with the result of the latest edits. Also, you may return less than n characters if performance dictates so, but keep in mind IMEs are relying on this for many functions: you should not, for example, limit the returned value to the current line, and specifically do not return 0 characters unless the cursor is really at the end of the text.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text. This must be non-negative. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text after the cursor position; the length of the returned text might be less than n. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `n` is negative. |

### getTextBeforeCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTextBeforeCursor(
    n: Int, 
    flags: Int
): CharSequence?
```

Get n characters of text before the current cursor position.

This method may fail either if the input connection has become invalid (such as its process crashing) or the editor is taking too long to respond with the text (it is given a couple seconds to return). In either case, null is returned. This method does not affect the text in the editor in any way, nor does it affect the selection or composing spans.

If `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` is supplied as flags, the editor should return a `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` with all the spans set on the text.

**IME authors:** please consider this will trigger an IPC round-trip that will take some time. Assume this method consumes a lot of time. Also, please keep in mind the Editor may choose to return less characters than requested even if they are available for performance reasons. If you are using this to get the initial text around the cursor, you may consider using getInitialTextBeforeCursor, getInitialSelectedText, and getInitialTextAfterCursor to prevent IPC costs.

**Editor authors:** please be careful of race conditions in implementing this call. An IME can make a change to the text and use this method right away; you need to make sure the returned value is consistent with the result of the latest edits. Also, you may return less than n characters if performance dictates so, but keep in mind IMEs are relying on this for many functions: you should not, for example, limit the returned value to the current line, and specifically do not return 0 characters unless the cursor is really at the start of the text.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text. This must be non-negative. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text before the cursor position; the length of the returned text might be less than n. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `n` is negative. |

### performContextMenuAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performContextMenuAction(id: Int): Boolean
```

Perform a context menu action on the field. The given id may be one of: `https://developer.android.com/reference/kotlin/android/R.id.html#selectAll:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#startSelectingText:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#stopSelectingText:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#cut:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#copy:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#paste:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.id.html#copyUrl:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/R.id.html#switchInputMethod:kotlin.Int`

### performEditorAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performEditorAction(editorAction: Int): Boolean
```

Have the editor perform an action it has said it can do.

This is typically used by IMEs when the user presses the key associated with the action.

| Parameters ||
|---|---|
| `editorAction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): This must be one of the action constants for `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`, such as `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_GO:kotlin.Int`, or the value of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionId:kotlin.Int` if a custom action is available. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### performHandwritingGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performHandwritingGesture(
    gesture: HandwritingGesture, 
    executor: Executor?, 
    consumer: IntConsumer?
): Unit
```

Perform a handwriting gesture on text.

Note: A supported gesture getSupportedHandwritingGestures may not have preview supported getSupportedHandwritingGesturePreviews.

| Parameters ||
|---|---|
| `gesture` | [HandwritingGesture](HandwritingGesture.md): the gesture to perform. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: The executor to run the callback on. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `consumer` | [IntConsumer](../java.util.function/IntConsumer.md)?: if the caller passes a non-null consumer, the editor must invoke this with one of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_SUCCESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FAILED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_CANCELLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FALLBACK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNSUPPORTED:kotlin.Int` after applying the `gesture` has completed. Will be invoked on the given `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`. Default implementation provides a callback to `https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#` with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNSUPPORTED:kotlin.Int`. |
| --- | --- |

**See Also**

- previewHandwritingGesture

### performPrivateCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun performPrivateCommand(
    action: String!, 
    data: Bundle!
): Boolean
```

API to send private commands from an input method to its connected editor. This can be used to provide domain-specific features that are only known between certain input methods and their clients. Note that because the InputConnection protocol is asynchronous, you have no way to get a result back or know if the client understood the command; you can use the information in EditorInfo to determine if a client supports a particular command.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the command to be performed. This *must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting commands. |
| `data` | [Bundle](../android.os/Bundle.md)!: Any data to include with the command. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the command was sent (whether or not the associated editor understood it), false if the input connection is no longer valid. |

### performSpellCheck

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performSpellCheck(): Boolean
```

Have the editor perform spell checking for the full content.

The editor can ignore this method call if it does not support spell checking.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, the return value will always be ignored. For IME authors, this method returns true if the spell check request was sent (whether or not the associated editor supports spell checking), false if the input connection is no longer valid. |

### previewHandwritingGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun previewHandwritingGesture(
    gesture: PreviewableHandwritingGesture, 
    cancellationSignal: CancellationSignal?
): Boolean
```

Preview a handwriting gesture on text. Provides a real-time preview for a gesture to user for an ongoing gesture. e.g. as user begins to draw a circle around text, resulting selection SelectGesture is previewed while stylus is moving over applicable text.

Note: A supported gesture getSupportedHandwritingGestures might not have preview supported getSupportedHandwritingGesturePreviews.

| Parameters ||
|---|---|
| `gesture` | [PreviewableHandwritingGesture](PreviewableHandwritingGesture.md): the gesture to preview. Preview support for a gesture (regardless of whether implemented by editor) can be determined if gesture subclasses PreviewableHandwritingGesture. Supported previewable gestures include SelectGesture, SelectRangeGesture, DeleteGesture and DeleteRangeGesture. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: signal to cancel an ongoing preview. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on successfully sending command to Editor, false if not implemented by editor or the input connection is no longer valid or preview was cancelled with `https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#`. |

**See Also**

- performHandwritingGesture

### replaceText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceText(
    start: Int, 
    end: Int, 
    text: CharSequence, 
    newCursorPosition: Int, 
    textAttribute: TextAttribute?
): Boolean
```

Replace the specific range in the editor with suggested text.

This method finishes whatever composing text is currently active and leaves the text as-it, replaces the specific range of text with the passed CharSequence, and then moves the cursor according to `newCursorPosition`. This behaves like calling finishComposingText, setSelection, and then commitText.

Similar to setSelection, the order of start and end is not important. In effect, the region from start to end and the region from end to start is the same. Editor authors, be ready to accept a start that is greater than end.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character index where the replacement should start. Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character index where the replacement should end. Value is 0 or greater |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text to replace. This may include styles. This value cannot be `null`. |
| --- | --- |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new cursor position around the text. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance you to the position after the full text being inserted. Note that this means you can't position the cursor within the text. |
| `textAttribute` | [TextAttribute](TextAttribute.md)?: The extra information about the text. This value may be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the replace command was sent to the associated editor (regardless of whether the replacement is success or not), `false` otherwise. |

### reportFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun reportFullscreenMode(enabled: Boolean): Boolean
```

Called back when the connected IME switches between fullscreen and normal modes.

<br />

**Editor authors:** There is a bug on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and later devices that this method is called back on the main thread even when getHandler is overridden. This bug is fixed in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`.

<br />

**IME authors:** On `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and later devices, input methods are no longer allowed to directly call this method at any time. To signal this event in the target application, input methods should always call updateFullscreenMode instead. This approach should work on API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int` and prior devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, the return value will always be ignored. For IME authors, this always returns `true` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int` and prior devices and `false` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and later devices. |

**See Also**

- isFullscreenMode

### requestCursorUpdates

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun requestCursorUpdates(cursorUpdateMode: Int): Boolean
```

Called by the input method to ask the editor for calling back updateCursorAnchorInfo to notify cursor/anchor locations.

| Parameters ||
|---|---|
| `cursorUpdateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): any combination of update modes and filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`, and data filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`. Pass `0` to disable them. However, if an unknown flag is provided, request will be rejected and method will return `false`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the request is scheduled. `false` to indicate that when the application will not call updateCursorAnchorInfo. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### requestCursorUpdates

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestCursorUpdates(
    cursorUpdateMode: Int, 
    cursorUpdateFilter: Int
): Boolean
```

Called by the input method to ask the editor for calling back updateCursorAnchorInfo to notify cursor/anchor locations.

| Parameters ||
|---|---|
| `cursorUpdateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): combination of update modes: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int` |
| `cursorUpdateFilter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): any combination of data filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`. Pass `0` to disable them. However, if an unknown flag is provided, request will be rejected and method will return `false`. . Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the request is scheduled. `false` to indicate that when the application will not call updateCursorAnchorInfo. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### requestTextBoundsInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestTextBoundsInfo(
    bounds: RectF, 
    executor: Executor, 
    consumer: Consumer<TextBoundsInfoResult!>
): Unit
```

Called by input method to request the TextBoundsInfo for a range of text which is covered by or in vicinity of the given `bounds`. It can be used as a supplementary method to implement the handwriting gesture API - performHandwritingGesture.

**Editor authors** : It's preferred that the editor returns a TextBoundsInfo of all the text lines whose bounds intersect with the given `bounds`.

**IME authors**: This method is expensive when the text is long. Please consider that both the text bounds computation and IPC round-trip to send the data are time consuming. It's preferable to only request text bounds in smaller areas.

| Parameters ||
|---|---|
| `bounds` | [RectF](../android.graphics/RectF.md): the interested area where the text bounds are requested, in the screen coordinates. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `consumer` | [Consumer](../java.util.function/Consumer.md)\< [TextBoundsInfoResult](TextBoundsInfoResult.md)!\>: the callback invoked by editor to return the result. It must return a non-null object. |
| --- | --- |

**See Also**

- TextBoundsInfo
- TextBoundsInfoResult

### sendKeyEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun sendKeyEvent(event: KeyEvent!): Boolean
```

Send a key event to the process that is currently attached through this input connection. The event will be dispatched like a normal key event, to the currently focused view; this generally is the view that is providing this InputConnection, but due to the asynchronous nature of this protocol that can not be guaranteed and the focus may have changed by the time the event is received.

This method can be used to send key events to the application. For example, an on-screen keyboard may use this method to simulate a hardware keyboard. There are three types of standard keyboards, numeric (12-key), predictive (20-key) and ALPHA (QWERTY). You can specify the keyboard type by specify the device id of the key event.

You will usually want to set the flag `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#FLAG_SOFT_KEYBOARD:kotlin.Int` on all key event objects you give to this API; the flag will not be set for you.

Note that it's discouraged to send such key events in normal operation; this is mainly for use with `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` type text fields. Use the #commitText family of methods to send text to the application instead.

| Parameters ||
|---|---|
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: The key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`
- `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#NUMERIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#PREDICTIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#ALPHA:kotlin.Int`

### setComposingRegion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setComposingRegion(
    start: Int, 
    end: Int
): Boolean
```

Mark a certain region of text as composing text. If there was a composing region, the characters are left as they were and the composing span removed, as if finishComposingText has been called. The default style for composing text is used.

The passed indices are clipped to the contents bounds. If the resulting region is zero-sized, no region is marked and the effect is the same as that of calling finishComposingText. The order of start and end is not important. In effect, the region from start to end and the region from end to start is the same. Editor authors, be ready to accept a start that is greater than end.

Since this does not change the contents of the text, editors should not call updateSelection and IMEs should not receive onUpdateSelection.

This has no impact on the cursor/selection position. It may result in the cursor being anywhere inside or outside the composing region, including cases where the selection and the composing region overlap partially or entirely.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region begins |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region ends |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### setComposingRegion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComposingRegion(
    start: Int, 
    end: Int, 
    textAttribute: TextAttribute?
): Boolean
```

The variant of setComposingRegion. This method is used to allow the IME to provide extra information while setting up text.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region begins |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region ends |
| `textAttribute` | [TextAttribute](TextAttribute.md)?: The extra information about the text. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### setComposingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setComposingText(
    text: CharSequence!, 
    newCursorPosition: Int
): Boolean
```

Replace the currently composing text with the given text, and set the new cursor position. Any composing text set previously will be removed automatically.

If there is any composing span currently active, all characters that it comprises are removed. The passed text is added in its place, and a composing span is added to this text. If there is no composing span active, the passed text is added at the cursor position (removing selected characters first if any), and a composing span is added on the new text. Finally, the cursor is moved to the location specified by `newCursorPosition`.

This is usually called by IMEs to add or remove or change characters in the composing span. Calling this method will cause the editor to call onUpdateSelection on the current IME after the batch input is over.

**Editor authors:** please keep in mind the text may be very similar or completely different than what was in the composing span at call time, or there may not be a composing span at all. Please note that although it's not typical use, the string may be empty. Treat this normally, replacing the currently composing text with an empty string. Also, be careful with the cursor position. IMEs rely on this working exactly as described above. Since this changes the contents of the editor, you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress. Note that this method can set the cursor position on either edge of the composing text or entirely outside it, but the IME may also go on to move the cursor position to within the composing text in a subsequent call so you should make no assumption at all: the composing text and the selection are entirely independent.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The composing text with styles if necessary. If no style object attached to the text, the default style for composing text is used. See `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` for how to attach style object to the text. `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` and `https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#` are two implementations of the interface `https://developer.android.com/reference/kotlin/android/text/Spanned.html#`. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance you to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### setComposingText

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComposingText(
    text: CharSequence, 
    newCursorPosition: Int, 
    textAttribute: TextAttribute?
): Boolean
```

The variant of setComposingText. This method is used to allow the IME to provide extra information while setting up composing text.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The composing text with styles if necessary. If no style object attached to the text, the default style for composing text is used. See `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` for how to attach style object to the text. `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` and `https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#` are two implementations of the interface `https://developer.android.com/reference/kotlin/android/text/Spanned.html#`. This value cannot be `null`. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance you to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |
| `textAttribute` | [TextAttribute](TextAttribute.md)?: The extra information about the text. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### setImeConsumesInput

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImeConsumesInput(imeConsumesInput: Boolean): Boolean
```

Called by the input method to indicate that it consumes all input for itself, or no longer does so.

Editors should reflect that they are not receiving input by hiding the cursor if `imeConsumesInput` is `true`, and resume showing the cursor if it is `false`.

| Parameters ||
|---|---|
| `imeConsumesInput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` when the IME is consuming input and the cursor should be hidden, `false` when input to the editor resumes and the cursor should be shown again. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, the return value will always be ignored. For IME authors, this method returns `true` if the request was sent (whether or not the associated editor does something based on this request), `false` if the input connection is no longer valid. |

### setSelection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSelection(
    start: Int, 
    end: Int
): Boolean
```

Set the selection of the text editor. To set the cursor position, start and end should have the same value.

Since this moves the cursor, calling this method will cause the editor to call onUpdateSelection on the current IME after the batch input is over. **Editor authors** , for this to happen you need to make the changes known to the input method by calling updateSelection, but be careful to wait until the batch edit is over if one is in progress.

This has no effect on the composing region which must stay unchanged. The order of start and end is not important. In effect, the region from start to end and the region from end to start is the same. Editor authors, be ready to accept a start that is greater than end.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character index where the selection should start. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character index where the selection should end. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### takeSnapshot

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun takeSnapshot(): TextSnapshot?
```

Called by the system when it needs to take a snapshot of multiple text-related data in an atomic manner.

**Editor authors** : Supporting this method is strongly encouraged. Atomically taken TextSnapshot is going to be really helpful for the system when optimizing IPCs in a safe and deterministic manner. Return `null` if an atomically taken TextSnapshot is unavailable. The system continues supporting such a scenario gracefully.

**IME authors** : Currently IMEs cannot call this method directly and always receive `null` as the result.

| Return ||
|---|---|
| TextSnapshot | `null` if TextSnapshot is unavailable and/or this API is called from IMEs. |
