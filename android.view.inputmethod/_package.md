# android.view.inputmethod

# android.view.inputmethod

Kotlin | [Java](https://developer.android.com/reference/android/view/inputmethod/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [ConnectionlessHandwritingCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback) | Interface to receive the result of starting a connectionless stylus handwriting session using one of [InputMethodManager.startConnectionlessStylusHandwriting(View, CursorAnchorInfo,](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)), [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)), or [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.lang.String,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)). |
| --- | --- |
| [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection) | The InputConnection interface is the communication channel from an [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) back to the application that is receiving its input. |
| [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) | The InputMethod interface represents an input method which can generate key events and text, such as digital, email addresses, CJK characters, other language characters, and etc. |
| [InputMethodSession](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession) | The InputMethodSession interface provides the per-client functionality of [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) that is safe to expose to applications. |
| --- | --- |

## Classes

| [BaseInputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/BaseInputConnection) | Base class for implementors of the InputConnection interface, taking care of most of the common behavior for providing a connection to an Editable. |
| --- | --- |
| [CompletionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo) | Information about a single text completion that an editor has reported to an input method. |
| [CorrectionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CorrectionInfo) | Information about a single text correction that an editor has reported to an input method. |
| [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo) | Positional information about the text insertion point and characters in the composition string. |
| --- | --- |
| [DeleteGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for deleting an area of text using single rectangle. |
| [DeleteRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteRangeGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for deleting a range of text by defining start and end rectangles. |
| [EditorBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorBoundsInfo) | Container of rectangular position related info for the Editor. |
| --- | --- |
| [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo) | An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position. |
| [ExtractedText](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText) | Information about text that has been extracted for use by an input method. |
| [ExtractedTextRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedTextRequest) | Description of what an input method would like from an application when extract text from its input editor. |
| --- | --- |
| [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) | Base class for stylus handwriting gestures. |
| [InlineSuggestion](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestion) | This class represents an inline suggestion which is made by one app and can be embedded into the UI of another. |
| [InlineSuggestionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionInfo) | This class represents the description of an inline suggestion. |
| --- | --- |
| [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest) | This class represents an inline suggestion request made by one app to get suggestions from the other source. |
| [InlineSuggestionsResponse](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsResponse) | This class represents an inline suggestion response. |
| [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding) | Information given to an [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) about a client connecting to it. |
| --- | --- |
| [InputConnectionWrapper](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnectionWrapper) | Wrapper class for proxying calls to another InputConnection. |
| [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo) | A container object with which input methods can send content files to the target application. |
| [InputMethodInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodInfo) | This class is used to specify meta information of an input method. |
| --- | --- |
| [InputMethodManager](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager) | Central system API to the overall input method framework (IMF) architecture, which arbitrates interaction between applications and the current input method. |
| [InputMethodSubtype](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype) | This class is used to specify meta information of a subtype contained in an input method editor (IME). |
| [InsertGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for inserting text at the defined insertion point. |
| --- | --- |
| [InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. |
| [JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for deleting or inserting whitespace in text. |
| [PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture) | A [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) that can be [previewed](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#previewHandwritingGesture(android.view.inputmethod.PreviewableHandwritingGesture,%20android.os.CancellationSignal)). |
| --- | --- |
| [RemoveSpaceGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/RemoveSpaceGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for removing whitespace from text. |
| [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for selecting an area of text using single rectangle. |
| [SelectRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for selecting a range of text by defining start and end rectangles. |
| --- | --- |
| [SurroundingText](https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText) | Information about the surrounding text around the cursor for use by an input method. |
| [TextAppearanceInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo) | Information about text appearance in an editor, passed through [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo) for use by [InputMethodService](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#). |
| [TextAttribute](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute) | The data class that IME can take extra information to applications when setting the text. |
| --- | --- |
| [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo) | The text bounds information of a slice of text in the editor. |
| [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult) | The object that holds the result of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) call. |
| [TextSnapshot](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot) | An immutable data snapshot of text editing state. |
| --- | --- |
