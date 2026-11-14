# android.view.inputmethod

# android.view.inputmethod

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [ConnectionlessHandwritingCallback](ConnectionlessHandwritingCallback.md) | Interface to receive the result of starting a connectionless stylus handwriting session using one of [InputMethodManager.startConnectionlessStylusHandwriting(View, CursorAnchorInfo,](InputMethodManager.md)), [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](InputMethodManager.md)), or [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.lang.String,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](InputMethodManager.md)). |
| --- | --- |
| [InputConnection](InputConnection.md) | The InputConnection interface is the communication channel from an [InputMethod](InputMethod.md) back to the application that is receiving its input. |
| [InputMethod](InputMethod.md) | The InputMethod interface represents an input method which can generate key events and text, such as digital, email addresses, CJK characters, other language characters, and etc. |
| [InputMethodSession](InputMethodSession.md) | The InputMethodSession interface provides the per-client functionality of [InputMethod](InputMethod.md) that is safe to expose to applications. |
| --- | --- |

## Classes

| [BaseInputConnection](BaseInputConnection.md) | Base class for implementors of the InputConnection interface, taking care of most of the common behavior for providing a connection to an Editable. |
| --- | --- |
| [CompletionInfo](CompletionInfo.md) | Information about a single text completion that an editor has reported to an input method. |
| [CorrectionInfo](CorrectionInfo.md) | Information about a single text correction that an editor has reported to an input method. |
| [CursorAnchorInfo](CursorAnchorInfo.md) | Positional information about the text insertion point and characters in the composition string. |
| --- | --- |
| [DeleteGesture](DeleteGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for deleting an area of text using single rectangle. |
| [DeleteRangeGesture](DeleteRangeGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for deleting a range of text by defining start and end rectangles. |
| [EditorBoundsInfo](EditorBoundsInfo.md) | Container of rectangular position related info for the Editor. |
| --- | --- |
| [EditorInfo](EditorInfo.md) | An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position. |
| [ExtractedText](ExtractedText.md) | Information about text that has been extracted for use by an input method. |
| [ExtractedTextRequest](ExtractedTextRequest.md) | Description of what an input method would like from an application when extract text from its input editor. |
| --- | --- |
| [HandwritingGesture](HandwritingGesture.md) | Base class for stylus handwriting gestures. |
| [InlineSuggestion](InlineSuggestion.md) | This class represents an inline suggestion which is made by one app and can be embedded into the UI of another. |
| [InlineSuggestionInfo](InlineSuggestionInfo.md) | This class represents the description of an inline suggestion. |
| --- | --- |
| [InlineSuggestionsRequest](InlineSuggestionsRequest.md) | This class represents an inline suggestion request made by one app to get suggestions from the other source. |
| [InlineSuggestionsResponse](InlineSuggestionsResponse.md) | This class represents an inline suggestion response. |
| [InputBinding](InputBinding.md) | Information given to an [InputMethod](InputMethod.md) about a client connecting to it. |
| --- | --- |
| [InputConnectionWrapper](InputConnectionWrapper.md) | Wrapper class for proxying calls to another InputConnection. |
| [InputContentInfo](InputContentInfo.md) | A container object with which input methods can send content files to the target application. |
| [InputMethodInfo](InputMethodInfo.md) | This class is used to specify meta information of an input method. |
| --- | --- |
| [InputMethodManager](InputMethodManager.md) | Central system API to the overall input method framework (IMF) architecture, which arbitrates interaction between applications and the current input method. |
| [InputMethodSubtype](InputMethodSubtype.md) | This class is used to specify meta information of a subtype contained in an input method editor (IME). |
| [InsertGesture](InsertGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for inserting text at the defined insertion point. |
| --- | --- |
| [InsertModeGesture](InsertModeGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. |
| [JoinOrSplitGesture](JoinOrSplitGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for deleting or inserting whitespace in text. |
| [PreviewableHandwritingGesture](PreviewableHandwritingGesture.md) | A [HandwritingGesture](HandwritingGesture.md) that can be [previewed](InputConnection.md)). |
| --- | --- |
| [RemoveSpaceGesture](RemoveSpaceGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for removing whitespace from text. |
| [SelectGesture](SelectGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for selecting an area of text using single rectangle. |
| [SelectRangeGesture](SelectRangeGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for selecting a range of text by defining start and end rectangles. |
| --- | --- |
| [SurroundingText](SurroundingText.md) | Information about the surrounding text around the cursor for use by an input method. |
| [TextAppearanceInfo](TextAppearanceInfo.md) | Information about text appearance in an editor, passed through [CursorAnchorInfo](CursorAnchorInfo.md) for use by [InputMethodService](../android.inputmethodservice/InputMethodService.md). |
| [TextAttribute](TextAttribute.md) | The data class that IME can take extra information to applications when setting the text. |
| --- | --- |
| [TextBoundsInfo](TextBoundsInfo.md) | The text bounds information of a slice of text in the editor. |
| [TextBoundsInfoResult](TextBoundsInfoResult.md) | The object that holds the result of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md)) call. |
| [TextSnapshot](TextSnapshot.md) | An immutable data snapshot of text editing state. |
| --- | --- |
