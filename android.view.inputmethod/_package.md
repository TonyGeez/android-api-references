# android.view.inputmethod

# android.view.inputmethod

Kotlin | [Java](../android/view/inputmethod/_package.md)
| --- | --- |

## Interfaces

| [ConnectionlessHandwritingCallback](../android/view/inputmethod/ConnectionlessHandwritingCallback.md) | Interface to receive the result of starting a connectionless stylus handwriting session using one of [InputMethodManager.startConnectionlessStylusHandwriting(View, CursorAnchorInfo,](../android/view/inputmethod/InputMethodManager.md)), [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](../android/view/inputmethod/InputMethodManager.md)), or [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.lang.String,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](../android/view/inputmethod/InputMethodManager.md)). |
| --- | --- |
| [InputConnection](../android/view/inputmethod/InputConnection.md) | The InputConnection interface is the communication channel from an [InputMethod](../android/view/inputmethod/InputMethod.md) back to the application that is receiving its input. |
| [InputMethod](../android/view/inputmethod/InputMethod.md) | The InputMethod interface represents an input method which can generate key events and text, such as digital, email addresses, CJK characters, other language characters, and etc. |
| [InputMethodSession](../android/view/inputmethod/InputMethodSession.md) | The InputMethodSession interface provides the per-client functionality of [InputMethod](../android/view/inputmethod/InputMethod.md) that is safe to expose to applications. |
| --- | --- |

## Classes

| [BaseInputConnection](../android/view/inputmethod/BaseInputConnection.md) | Base class for implementors of the InputConnection interface, taking care of most of the common behavior for providing a connection to an Editable. |
| --- | --- |
| [CompletionInfo](../android/view/inputmethod/CompletionInfo.md) | Information about a single text completion that an editor has reported to an input method. |
| [CorrectionInfo](../android/view/inputmethod/CorrectionInfo.md) | Information about a single text correction that an editor has reported to an input method. |
| [CursorAnchorInfo](../android/view/inputmethod/CursorAnchorInfo.md) | Positional information about the text insertion point and characters in the composition string. |
| --- | --- |
| [DeleteGesture](../android/view/inputmethod/DeleteGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting an area of text using single rectangle. |
| [DeleteRangeGesture](../android/view/inputmethod/DeleteRangeGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting a range of text by defining start and end rectangles. |
| [EditorBoundsInfo](../android/view/inputmethod/EditorBoundsInfo.md) | Container of rectangular position related info for the Editor. |
| --- | --- |
| [EditorInfo](../android/view/inputmethod/EditorInfo.md) | An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position. |
| [ExtractedText](../android/view/inputmethod/ExtractedText.md) | Information about text that has been extracted for use by an input method. |
| [ExtractedTextRequest](../android/view/inputmethod/ExtractedTextRequest.md) | Description of what an input method would like from an application when extract text from its input editor. |
| --- | --- |
| [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) | Base class for stylus handwriting gestures. |
| [InlineSuggestion](../android/view/inputmethod/InlineSuggestion.md) | This class represents an inline suggestion which is made by one app and can be embedded into the UI of another. |
| [InlineSuggestionInfo](../android/view/inputmethod/InlineSuggestionInfo.md) | This class represents the description of an inline suggestion. |
| --- | --- |
| [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) | This class represents an inline suggestion request made by one app to get suggestions from the other source. |
| [InlineSuggestionsResponse](../android/view/inputmethod/InlineSuggestionsResponse.md) | This class represents an inline suggestion response. |
| [InputBinding](../android/view/inputmethod/InputBinding.md) | Information given to an [InputMethod](../android/view/inputmethod/InputMethod.md) about a client connecting to it. |
| --- | --- |
| [InputConnectionWrapper](../android/view/inputmethod/InputConnectionWrapper.md) | Wrapper class for proxying calls to another InputConnection. |
| [InputContentInfo](../android/view/inputmethod/InputContentInfo.md) | A container object with which input methods can send content files to the target application. |
| [InputMethodInfo](../android/view/inputmethod/InputMethodInfo.md) | This class is used to specify meta information of an input method. |
| --- | --- |
| [InputMethodManager](../android/view/inputmethod/InputMethodManager.md) | Central system API to the overall input method framework (IMF) architecture, which arbitrates interaction between applications and the current input method. |
| [InputMethodSubtype](../android/view/inputmethod/InputMethodSubtype.md) | This class is used to specify meta information of a subtype contained in an input method editor (IME). |
| [InsertGesture](../android/view/inputmethod/InsertGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for inserting text at the defined insertion point. |
| --- | --- |
| [InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. |
| [JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting or inserting whitespace in text. |
| [PreviewableHandwritingGesture](../android/view/inputmethod/PreviewableHandwritingGesture.md) | A [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) that can be [previewed](../android/view/inputmethod/InputConnection.md)). |
| --- | --- |
| [RemoveSpaceGesture](../android/view/inputmethod/RemoveSpaceGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for removing whitespace from text. |
| [SelectGesture](../android/view/inputmethod/SelectGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for selecting an area of text using single rectangle. |
| [SelectRangeGesture](../android/view/inputmethod/SelectRangeGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for selecting a range of text by defining start and end rectangles. |
| --- | --- |
| [SurroundingText](../android/view/inputmethod/SurroundingText.md) | Information about the surrounding text around the cursor for use by an input method. |
| [TextAppearanceInfo](../android/view/inputmethod/TextAppearanceInfo.md) | Information about text appearance in an editor, passed through [CursorAnchorInfo](../android/view/inputmethod/CursorAnchorInfo.md) for use by [InputMethodService](../android/inputmethodservice/InputMethodService.md). |
| [TextAttribute](../android/view/inputmethod/TextAttribute.md) | The data class that IME can take extra information to applications when setting the text. |
| --- | --- |
| [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md) | The text bounds information of a slice of text in the editor. |
| [TextBoundsInfoResult](../android/view/inputmethod/TextBoundsInfoResult.md) | The object that holds the result of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](../android/view/inputmethod/InputConnection.md)) call. |
| [TextSnapshot](../android/view/inputmethod/TextSnapshot.md) | An immutable data snapshot of text editing state. |
| --- | --- |
