Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseInputConnection

```
open class BaseInputConnection : InputConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.inputmethod.BaseInputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#) |

Base class for implementors of the InputConnection interface, taking care of most of the common behavior for providing a connection to an Editable. Implementors of this class will want to be sure to implement `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getEditable()` to provide access to their own editable object, and to refer to the documentation in `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection`.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` with new character bounds `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBounds(kotlin.Int)` whenever cursor/anchor position is changed. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` with new `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorBoundsInfo` whenever cursor/anchor position is changed. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be used together with filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` with new Insertion marker info `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerBaseline()`, etc whenever cursor/anchor position is changed. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` with new text appearance info `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getTextAppearanceInfo()`} whenever cursor/anchor position is changed. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` with new visible line bounds `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getVisibleLineBounds()` whenever cursor/anchor position is changed, the editor or its parent is scrolled or the line bounds changed due to text updates. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be combined with other filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` and update flags `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` at once, as soon as possible, regardless of cursor/anchor position changes. This flag can be used together with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

Note by default all of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, are included but specifying them can filter-out others. It can be CPU intensive to include all, filtering specific info is recommended.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`

The editor is requested to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` whenever cursor/anchor position is changed. To disable monitoring, call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int)` again with this flag off.

This flag can be used together with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`.

Note by default all of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, are included but specifying them can filter-out others. It can be CPU intensive to include all, filtering specific info is recommended.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_EXTRACTED_TEXT_MONITOR:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getExtractedText(android.view.inputmethod.ExtractedTextRequest,%20kotlin.Int)` to indicate you would like to receive updates when the extracted text changes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getTextAfterCursor(kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getTextBeforeCursor(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getSurroundingText(kotlin.Int,%20kotlin.Int,%20kotlin.Int)` to have style information returned along with the text. If not set, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getTextAfterCursor(kotlin.Int,%20kotlin.Int)` sends only the raw text, without style or other spans. If set, it may return a complex CharSequence of both text and style spans. **Editor authors**: you should strive to send text with styles if possible, but it is not required.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_CANCELLED:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture` was cancelled. This happens when the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` is or becomes invalidated while performing the gesture, for example because a new `InputConnection` was started, or due to `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#invalidateInput(android.view.View)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FAILED:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture` failed and there was no applicable `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#getFallbackText()` or it couldn't be applied for any other reason.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_FALLBACK:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture` failed but `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#getFallbackText()` was committed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_SUCCESS:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture` is successfully executed on text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNKNOWN:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when editor didn't provide any result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#HANDWRITING_GESTURE_RESULT_UNSUPPORTED:kotlin.Int`

Result for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture` is unsupported by the current editor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#INPUT_CONTENT_GRANT_READ_URI_PERMISSION:kotlin.Int`

When this flag is used, the editor will be able to request read access to the content URI contained in the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo` object.

Make sure that the content provider owning the Uri sets the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag. Otherwise `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#requestPermission()` can fail.

Although calling this API is allowed only for the IME that is currently selected, the client is able to request a temporary read-only access even after the current IME is switched to any other IME as long as the client keeps `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo` object.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#BaseInputConnection(android.view.View,%20kotlin.Boolean)(targetView: https://developer.android.com/reference/kotlin/android/view/View.html#, fullEditor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#beginBatchEdit()()` Default implementation does nothing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#clearMetaKeyStates(kotlin.Int)(states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Default implementation uses `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#clearMetaKeyState(kotlin.Long,%20kotlin.Int)` to clear the state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#closeConnection()()` Default implementation calls `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#finishComposingText()` and `setImeConsumesInput(false)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#commitCompletion(android.view.inputmethod.CompletionInfo)(text: https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo!)` Default implementation does nothing and returns false. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)(inputContentInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Default implementation which invokes `https://developer.android.com/reference/kotlin/android/view/View.html#performReceiveContent(android.view.ContentInfo)` on the target view if the view `https://developer.android.com/reference/kotlin/android/view/View.html#getReceiveContentMimeTypes()` content insertion; otherwise returns false without any side effects. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#commitCorrection(android.view.inputmethod.CorrectionInfo)(correctionInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/CorrectionInfo!)` Default implementation does nothing and returns false. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#commitText(kotlin.CharSequence,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, newCursorPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Default implementation replaces any existing composing text with the given text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#deleteSurroundingText(kotlin.Int,%20kotlin.Int)(beforeLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, afterLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation performs the deletion around the current selection position of the editable text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#deleteSurroundingTextInCodePoints(kotlin.Int,%20kotlin.Int)(beforeLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, afterLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation performs the deletion around the current selection position of the editable text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#endBatchEdit()()` Default implementation does nothing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#finishComposingText()()` The default implementation removes the composing state from the current editable text. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getComposingSpanEnd(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Return the end of the range of composing text, or -1 if there's no composing text. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getComposingSpanStart(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Return the beginning of the range of composing text, or -1 if there's no composing text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getCursorCapsMode(kotlin.Int)(reqModes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation uses TextUtils. |
| open [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getEditable()()` Return the target of edit operations. |
| open [ExtractedText](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getExtractedText(android.view.inputmethod.ExtractedTextRequest,%20kotlin.Int)(request: https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedTextRequest!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation always returns null. |
| open [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getHandler()()` Called by the system to enable application developers to specify a dedicated thread on which `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` methods are called back. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getSelectedText(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation returns the text currently selected, or null if none is selected. |
| open [SurroundingText](https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getSurroundingText(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(beforeLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, afterLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation returns the given amount of text around the current cursor position in the buffer. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getTextAfterCursor(kotlin.Int,%20kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation returns the given amount of text from the current cursor position in the buffer. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#getTextBeforeCursor(kotlin.Int,%20kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation returns the given amount of text from the current cursor position in the buffer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#performContextMenuAction(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation does nothing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#performEditorAction(kotlin.Int)(actionCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation turns this into the enter key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#performPrivateCommand(kotlin.String,%20android.os.Bundle)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` The default implementation does nothing. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#removeComposingSpans(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Removes the composing spans from the given text if any. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#replaceText(kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, newCursorPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, textAttribute: https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute?)` Replace the specific range in the editor with suggested text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#reportFullscreenMode(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Updates InputMethodManager with the current fullscreen mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#requestCursorUpdates(kotlin.Int)(cursorUpdateMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation does nothing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#sendKeyEvent(android.view.KeyEvent)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Provides standard implementation for sending a key event to the window attached to the input connection's view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#setComposingRegion(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Mark a certain region of text as composing text. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#setComposingSpans(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Removes the composing spans from the given text if any. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#setComposingText(kotlin.CharSequence,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, newCursorPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation places the given text into the editable, replacing any existing composing text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#setSelection(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` The default implementation changes the selection position in the current editable text. |
| open [TextSnapshot](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#takeSnapshot()()` Default implementation that constructs `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot` with information extracted from `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#`. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, newCursorPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, textAttribute: https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute?)`

The variant of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitText(kotlin.CharSequence,%20kotlin.Int)`. This method is used to allow the IME to provide extra information while setting up text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)(gesture: https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, consumer: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#?)`

Perform a handwriting gesture on text.

Note: A supported gesture `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()` may not have preview supported `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performSpellCheck()()`

Have the editor perform spell checking for the full content.

The editor can ignore this method call if it does not support spell checking.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#previewHandwritingGesture(android.view.inputmethod.PreviewableHandwritingGesture,%20android.os.CancellationSignal)(gesture: https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)`

Preview a handwriting gesture on text. Provides a real-time preview for a gesture to user for an ongoing gesture. e.g. as user begins to draw a circle around text, resulting selection `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture` is previewed while stylus is moving over applicable text.

Note: A supported gesture `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()` might not have preview supported `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestCursorUpdates(kotlin.Int,%20kotlin.Int)(cursorUpdateMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorUpdateFilter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called by the input method to ask the editor for calling back `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)` to notify cursor/anchor locations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(bounds: https://developer.android.com/reference/kotlin/android/graphics/RectF.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, consumer: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult!>)`

Called by input method to request the `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo` for a range of text which is covered by or in vicinity of the given `bounds`. It can be used as a supplementary method to implement the handwriting gesture API - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performHandwritingGesture(android.view.inputmethod.HandwritingGesture,%20java.util.concurrent.Executor,%20java.util.function.IntConsumer)`.

**Editor authors** : It's preferred that the editor returns a `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo` of all the text lines whose bounds intersect with the given `bounds`.

**IME authors**: This method is expensive when the text is long. Please consider that both the text bounds computation and IPC round-trip to send the data are time consuming. It's preferable to only request text bounds in smaller areas.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingRegion(kotlin.Int,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, textAttribute: https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute?)`

The variant of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingRegion(kotlin.Int,%20kotlin.Int)`. This method is used to allow the IME to provide extra information while setting up text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, newCursorPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, textAttribute: https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute?)`

The variant of `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingText(kotlin.CharSequence,%20kotlin.Int)`. This method is used to allow the IME to provide extra information while setting up composing text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setImeConsumesInput(kotlin.Boolean)(imeConsumesInput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by the input method to indicate that it consumes all input for itself, or no longer does so.

Editors should reflect that they are not receiving input by hiding the cursor if `imeConsumesInput` is `true`, and resume showing the cursor if it is `false`.

<br />

## Public constructors

### BaseInputConnection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BaseInputConnection(
    targetView: View, 
    fullEditor: Boolean)
```

| Parameters ||
|---|---|
| `targetView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): This value cannot be `null`. |

## Public methods

### beginBatchEdit

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun beginBatchEdit(): Boolean
```

Default implementation does nothing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a batch edit is now in progress, false otherwise. Since this method starts a batch edit, that means it will always return true unless the input connection is no longer valid. |

### clearMetaKeyStates

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearMetaKeyStates(states: Int): Boolean
```

Default implementation uses `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#clearMetaKeyState(kotlin.Long,%20kotlin.Int)` to clear the state.

| Parameters ||
|---|---|
| `states` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The states to be cleared, may be one or more bits as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#getMetaState()`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### closeConnection

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun closeConnection(): Unit
```

Default implementation calls `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#finishComposingText()` and `setImeConsumesInput(false)`. 
If you override this method you *must* call through to the superclass implementation.

### commitCompletion

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commitCompletion(text: CompletionInfo!): Boolean
```

Default implementation does nothing and returns false.

| Parameters ||
|---|---|
| `text` | [CompletionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo)!: The committed completion. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### commitContent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commitContent(
    inputContentInfo: InputContentInfo, 
    flags: Int, 
    opts: Bundle?
): Boolean
```

Default implementation which invokes `https://developer.android.com/reference/kotlin/android/view/View.html#performReceiveContent(android.view.ContentInfo)` on the target view if the view `https://developer.android.com/reference/kotlin/android/view/View.html#getReceiveContentMimeTypes()` content insertion; otherwise returns false without any side effects.

| Parameters ||
|---|---|
| `inputContentInfo` | [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo): Content to be inserted. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#INPUT_CONTENT_GRANT_READ_URI_PERMISSION:kotlin.Int` if the content provider allows `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` or `0` if the application does not need to call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#requestPermission()`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: optional bundle data. This can be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this request is accepted by the application, whether the request is already handled or still being handled in background, `false` otherwise. |

### commitCorrection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commitCorrection(correctionInfo: CorrectionInfo!): Boolean
```

Default implementation does nothing and returns false.

| Parameters ||
|---|---|
| `correctionInfo` | [CorrectionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CorrectionInfo)!: Detailed information about the correction. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### commitText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commitText(
    text: CharSequence!, 
    newCursorPosition: Int
): Boolean
```

Default implementation replaces any existing composing text with the given text. In addition, only if fallback mode, a key event is sent for the new text and the current editable buffer cleared.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to commit. This may include styles. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text, in Java characters. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance the cursor to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### deleteSurroundingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteSurroundingText(
    beforeLength: Int, 
    afterLength: Int
): Boolean
```

The default implementation performs the deletion around the current selection position of the editable text.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters before the cursor to be deleted, in code unit. If this is greater than the number of existing characters between the beginning of the text and the cursor, then this method does not fail but deletes all the characters in that range. |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters after the cursor to be deleted, in code unit. If this is greater than the number of existing characters between the cursor and the end of the text, then this method does not fail but deletes all the characters in that range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` when selected text is deleted, `false` when either the selection is invalid or not yet attached (i.e. selection start or end is -1), or the editable text is `null`. |

### deleteSurroundingTextInCodePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteSurroundingTextInCodePoints(
    beforeLength: Int, 
    afterLength: Int
): Boolean
```

The default implementation performs the deletion around the current selection position of the editable text.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters before the cursor to be deleted, in code points. If this is greater than the number of existing characters between the beginning of the text and the cursor, then this method does not fail but deletes all the characters in that range. |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters after the cursor to be deleted, in code points. If this is greater than the number of existing characters between the cursor and the end of the text, then this method does not fail but deletes all the characters in that range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Before Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### endBatchEdit

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun endBatchEdit(): Boolean
```

Default implementation does nothing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, you must return `true` if a batch edit is still in progress after closing the latest one (in other words, if the nesting count is still a positive number). Return `false` otherwise. For IME authors, you will always receive `true` as long as the request was sent to the editor, and receive `false` only if the input connection is no longer valid. |

### finishComposingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishComposingText(): Boolean
```

The default implementation removes the composing state from the current editable text. In addition, only if fallback mode, a key event is sent for the new text and the current editable buffer cleared.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### getComposingSpanEnd

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getComposingSpanEnd(text: Spannable): Int
```

Return the end of the range of composing text, or -1 if there's no composing text.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#): This value cannot be `null`. |

### getComposingSpanStart

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getComposingSpanStart(text: Spannable): Int
```

Return the beginning of the range of composing text, or -1 if there's no composing text.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#): This value cannot be `null`. |

### getCursorCapsMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCursorCapsMode(reqModes: Int): Int
```

The default implementation uses TextUtils.getCapsMode to get the cursor caps mode for the current selection position in the editable text, unless in fallback mode in which case 0 is always returned.

| Parameters ||
|---|---|
| `reqModes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired modes to retrieve, as defined by `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#getCapsMode(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)`. These constants are defined so that you can simply pass the current `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#inputType:kotlin.Int` value directly in to here. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the caps mode flags that are in effect at the current cursor position. See TYPE_TEXT_FLAG_CAPS_\* in `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |

### getEditable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEditable(): Editable?
```

Return the target of edit operations. The default implementation returns its own fake editable that is just used for composing text; subclasses that are real text editors should override this and supply their own.

Subclasses could override this method to turn null.

### getExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtractedText(
    request: ExtractedTextRequest!, 
    flags: Int
): ExtractedText?
```

The default implementation always returns null.

| Parameters ||
|---|---|
| `request` | [ExtractedTextRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedTextRequest)!: Description of how the text should be returned. `https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedTextRequest` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional options to control the client, either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_EXTRACTED_TEXT_MONITOR:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText?` | an `https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText` object describing the state of the text view and containing the extracted text itself, or null if the input connection is no longer valid of the editor can't comply with the request for some reason. |

### getHandler

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandler(): Handler?
```

Called by the system to enable application developers to specify a dedicated thread on which `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` methods are called back.

**Editor authors** : although you can return your custom subclasses of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`, the system only uses `https://developer.android.com/reference/kotlin/android/os/Looper.html#` returned from `https://developer.android.com/reference/kotlin/android/os/Handler.html#getLooper()`. You cannot intercept or cancel `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection` callbacks by implementing this method.

**IME authors** : This method is not intended to be called from the IME. You will always receive `null`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Handler.html#?` | This value may be `null`. |

### getSelectedText

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSelectedText(flags: Int): CharSequence?
```

The default implementation returns the text currently selected, or null if none is selected.

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

The default implementation returns the given amount of text around the current cursor position in the buffer.

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `beforeLength` or `afterLength` is negative. |

### getTextAfterCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextAfterCursor(
    length: Int, 
    flags: Int
): CharSequence?
```

The default implementation returns the given amount of text from the current cursor position in the buffer.

| Parameters ||
|---|---|
| `n` | The expected length of the text. This must be non-negative. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `n` is negative. |

### getTextBeforeCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextBeforeCursor(
    length: Int, 
    flags: Int
): CharSequence?
```

The default implementation returns the given amount of text from the current cursor position in the buffer.

| Parameters ||
|---|---|
| `n` | The expected length of the text. This must be non-negative. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `n` is negative. |

### performContextMenuAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performContextMenuAction(id: Int): Boolean
```

The default implementation does nothing.

### performEditorAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performEditorAction(actionCode: Int): Boolean
```

The default implementation turns this into the enter key.

| Parameters ||
|---|---|
| `editorAction` | This must be one of the action constants for `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`, such as `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_GO:kotlin.Int`, or the value of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionId:kotlin.Int` if a custom action is available. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### performPrivateCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performPrivateCommand(
    action: String!, 
    data: Bundle!
): Boolean
```

The default implementation does nothing.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the command to be performed. This *must* be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting commands. |
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Any data to include with the command. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the command was sent (whether or not the associated editor understood it), false if the input connection is no longer valid. |

### removeComposingSpans

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun removeComposingSpans(text: Spannable): Unit
```

Removes the composing spans from the given text if any.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#): the spannable text to remove composing spans. This value cannot be `null`. |

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

This method finishes whatever composing text is currently active and leaves the text as-it, replaces the specific range of text with the passed CharSequence, and then moves the cursor according to `newCursorPosition`. This behaves like calling `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#finishComposingText()`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setSelection(kotlin.Int,%20kotlin.Int)`, and then `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`.

Similar to `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setSelection(kotlin.Int,%20kotlin.Int)`, the order of start and end is not important. In effect, the region from start to end and the region from end to start is the same. Editor authors, be ready to accept a start that is greater than end.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): This value cannot be `null`. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new cursor position around the text. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance you to the position after the full text being inserted. Note that this means you can't position the cursor within the text. |
| `textAttribute` | [TextAttribute](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the replace command was sent to the associated editor (regardless of whether the replacement is success or not), `false` otherwise. |

### reportFullscreenMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportFullscreenMode(enabled: Boolean): Boolean
```

Updates InputMethodManager with the current fullscreen mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | For editor authors, the return value will always be ignored. For IME authors, this always returns `true` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int` and prior devices and `false` on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and later devices. |

### requestCursorUpdates

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestCursorUpdates(cursorUpdateMode: Int): Boolean
```

The default implementation does nothing.

| Parameters ||
|---|---|
| `cursorUpdateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): any combination of update modes and filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_IMMEDIATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`, and data filters: `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_CHARACTER_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_INSERTION_MARKER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_VISIBLE_LINE_BOUNDS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int`. Pass `0` to disable them. However, if an unknown flag is provided, request will be rejected and method will return `false`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the request is scheduled. `false` to indicate that when the application will not call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateCursorAnchorInfo(android.view.View,%20android.view.inputmethod.CursorAnchorInfo)`. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### sendKeyEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendKeyEvent(event: KeyEvent!): Boolean
```

Provides standard implementation for sending a key event to the window attached to the input connection's view.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!: The key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### setComposingRegion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComposingRegion(
    start: Int, 
    end: Int
): Boolean
```

Mark a certain region of text as composing text. If there was a composing region, the characters are left as they were and the composing span removed, as if `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#finishComposingText()` has been called. The default style for composing text is used.

The passed indices are clipped to the contents bounds. If the resulting region is zero-sized, no region is marked and the effect is the same as that of calling `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#finishComposingText()`. The order of start and end is not important. In effect, the region from start to end and the region from end to start is the same. Editor authors, be ready to accept a start that is greater than end.

Since this does not change the contents of the text, editors should not call `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateSelection(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` and IMEs should not receive `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onUpdateSelection(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

This has no impact on the cursor/selection position. It may result in the cursor being anywhere inside or outside the composing region, including cases where the selection and the composing region overlap partially or entirely.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region begins |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in the text at which the composing region ends |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the input connection is no longer valid. Since Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this API returned `false` when the target application does not implement this method. |

### setComposingSpans

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setComposingSpans(text: Spannable): Unit
```

Removes the composing spans from the given text if any.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#): the spannable text to remove composing spans. This value cannot be `null`. |

### setComposingText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComposingText(
    text: CharSequence!, 
    newCursorPosition: Int
): Boolean
```

The default implementation places the given text into the editable, replacing any existing composing text. The new text is marked as in a composing state with the composing style.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The composing text with styles if necessary. If no style object attached to the text, the default style for composing text is used. See `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` for how to attach style object to the text. `https://developer.android.com/reference/kotlin/android/text/SpannableString.html#` and `https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#` are two implementations of the interface `https://developer.android.com/reference/kotlin/android/text/Spanned.html#`. |
| `newCursorPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new cursor position around the text. If \> 0, this is relative to the end of the text - 1; if \<= 0, this is relative to the start of the text. So a value of 1 will always advance you to the position after the full text being inserted. Note that this means you can't position the cursor within the text, because the editor can make modifications to the text you are providing so it is not possible to correctly specify locations there. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false if the input connection is no longer valid. |

### setSelection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelection(
    start: Int, 
    end: Int
): Boolean
```

The default implementation changes the selection position in the current editable text.

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

Default implementation that constructs `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot` with information extracted from `https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot?` | `null` when `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot` cannot be fully taken. |
