# InputMethodSession

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodSession

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/InputMethodSession "View this page in Java") 

```
interface InputMethodSession
```

| [android.view.inputmethod.InputMethodSession](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#) |

| Known Direct Subclasses [AbstractInputMethodService.AbstractInputMethodSessionImpl](https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.html#) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractInputMethodService.AbstractInputMethodSessionImpl](https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.html#) | Base class for derived classes to implement their [InputMethodSession](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#) interface. | |

| Known Indirect Subclasses [InputMethodService.InputMethodSessionImpl](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl.html#) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputMethodService.InputMethodSessionImpl](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.InputMethodSessionImpl.html#) | Concrete implementation of [AbstractInputMethodService.AbstractInputMethodSessionImpl](https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.html#) that provides all of the standard behavior for an input method session. | |

The InputMethodSession interface provides the per-client functionality of [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) that is safe to expose to applications.

Applications will not normally use this interface themselves, instead relying on the standard interaction provided by [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) and [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| abstract | [EventCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession.EventCallback) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appPrivateCommand](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#appPrivateCommand(kotlin.String,%20android.os.Bundle))`(`action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Process a private command sent from the application to the input method. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchGenericMotionEvent](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#dispatchGenericMotionEvent(kotlin.Int,%20android.view.MotionEvent,%20android.view.inputmethod.InputMethodSession.EventCallback))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`, `callback:` ` [InputMethodSession.EventCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession.EventCallback)!`)` This method is called when there is a generic motion event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchKeyEvent](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#dispatchKeyEvent(kotlin.Int,%20android.view.KeyEvent,%20android.view.inputmethod.InputMethodSession.EventCallback))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`, `callback:` ` [InputMethodSession.EventCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession.EventCallback)!`)` This method is called when a key is pressed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchTrackballEvent](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#dispatchTrackballEvent(kotlin.Int,%20android.view.MotionEvent,%20android.view.inputmethod.InputMethodSession.EventCallback))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`, `callback:` ` [InputMethodSession.EventCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession.EventCallback)!`)` This method is called when there is a track ball event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [displayCompletions](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#displayCompletions(kotlin.Array))`(`completions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CompletionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo)!>!`)` Called by a text editor that performs auto completion, to tell the input method about the completions it has available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishInput](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#finishInput())`()` This method is called when the application would like to stop receiving text input. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggleSoftInput](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#toggleSoftInput(kotlin.Int,%20kotlin.Int))`(`showFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hideFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Toggle the soft input window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCursor](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#updateCursor(android.graphics.Rect))`(`newCursor:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` This method is called when cursor location of the target input field has changed within its window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#updateCursorAnchorInfo(android.view.inputmethod.CursorAnchorInfo))`(`cursorAnchorInfo:` ` [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo)!`)` This method is called when the cursor and/or the character position relevant to text input is changed on the screen. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateExtractedText](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#updateExtractedText(kotlin.Int,%20android.view.inputmethod.ExtractedText))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [ExtractedText](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText)!`)` Called by a text editor to report its new extracted text when its contents change. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSelection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#updateSelection(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`oldSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the selection or cursor in the current target input field has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [viewClicked](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#viewClicked(kotlin.Boolean))`(`focusChanged:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when the user tapped a text view. |

## Public methods

### appPrivateCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun appPrivateCommand(
    action: String!, 
    data: Bundle!
): Unit
```

Process a private command sent from the application to the input method. This can be used to provide domain-specific features that are only known between certain input methods and their clients.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of the command to be performed. This*must*be a scoped name, i.e. prefixed with a package name you own, so that different developers will not create conflicting commands. |
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Any data to include with the command. |

### dispatchGenericMotionEvent

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dispatchGenericMotionEvent(
    seq: Int, 
    event: MotionEvent!, 
    callback: InputMethodSession.EventCallback!
): Unit
```

This method is called when there is a generic motion event.

If the input method wants to handle this event, return true, otherwise return false and the caller (i.e. the application) will handle the event.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!:The motion event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#) 

### dispatchKeyEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dispatchKeyEvent(
    seq: Int, 
    event: KeyEvent!, 
    callback: InputMethodSession.EventCallback!
): Unit
```

This method is called when a key is pressed. When done with the event, the implementation must call back on callback with its result.

If the input method wants to handle this event, return true, otherwise return false and the caller (i.e. the application) will handle the event.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:The key event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#) 

### dispatchTrackballEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dispatchTrackballEvent(
    seq: Int, 
    event: MotionEvent!, 
    callback: InputMethodSession.EventCallback!
): Unit
```

This method is called when there is a track ball event.

If the input method wants to handle this event, return true, otherwise return false and the caller (i.e. the application) will handle the event.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!:The motion event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#) 

### displayCompletions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun displayCompletions(completions: Array<CompletionInfo!>!): Unit
```

Called by a text editor that performs auto completion, to tell the input method about the completions it has available. This can be used by the input method to display them to the user to select the text to be inserted.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `completions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CompletionInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo)!\>!:Array of text completions that are available, starting with the best. If this array is null, any existing completions will be removed. |

### finishInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun finishInput(): Unit
```

This method is called when the application would like to stop receiving text input. 

### toggleSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toggleSoftInput(
    showFlags: Int, 
    hideFlags: Int
): Unit
```

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) the system no longer invokes this method, instead it explicitly shows or hides the IME. An`InputMethodService`wishing to toggle its own visibility should instead invoke [android.inputmethodservice.InputMethodService#requestShowSelf](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestShowSelf(kotlin.Int))or [InputMethodService.requestHideSelf](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#requestHideSelf(kotlin.Int))*

Toggle the soft input window. Applications can toggle the state of the soft input window.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.inputmethod.InputMethodManager#SHOW_IMPLICIT](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int), and [android.view.inputmethod.InputMethodManager#SHOW_FORCED](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_FORCED:kotlin.Int) |
| `hideFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.inputmethod.InputMethodManager#HIDE_IMPLICIT_ONLY](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_IMPLICIT_ONLY:kotlin.Int), and [android.view.inputmethod.InputMethodManager#HIDE_NOT_ALWAYS](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#HIDE_NOT_ALWAYS:kotlin.Int) |

### updateCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateCursor(newCursor: Rect!): Unit
```

This method is called when cursor location of the target input field has changed within its window. This is not normally called, but will only be reported if requested by the input method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newCursor` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The rectangle of the cursor currently being shown in the input field's window coordinates. |

### updateCursorAnchorInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateCursorAnchorInfo(cursorAnchorInfo: CursorAnchorInfo!): Unit
```

This method is called when the cursor and/or the character position relevant to text input is changed on the screen. This is not called by default. It will only be reported if requested by the input method.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursorAnchorInfo` | [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo)!:Positional information relevant to text input, such as text insertion point and composition string. |

### updateExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateExtractedText(
    token: Int, 
    text: ExtractedText!
): Unit
```

Called by a text editor to report its new extracted text when its contents change. This will only be called if the input method calls [InputConnection.getExtractedText()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#getExtractedText(android.view.inputmethod.ExtractedTextRequest,%20kotlin.Int))with the option to report updates.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The input method supplied token for identifying its request. |
| `text` | [ExtractedText](https://developer.android.com/reference/kotlin/android/view/inputmethod/ExtractedText)!:The new extracted text. |

### updateSelection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateSelection(
    oldSelStart: Int, 
    oldSelEnd: Int, 
    newSelStart: Int, 
    newSelEnd: Int, 
    candidatesStart: Int, 
    candidatesEnd: Int
): Unit
```

This method is called when the selection or cursor in the current target input field has changed.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `oldSelStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous text offset of the cursor selection start position. |
| `oldSelEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous text offset of the cursor selection end position. |
| `newSelStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new text offset of the cursor selection start position. |
| `newSelEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new text offset of the cursor selection end position. |
| `candidatesStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The text offset of the current candidate text start position. |
| `candidatesEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The text offset of the current candidate text end position. |

### viewClicked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun viewClicked(focusChanged: Boolean): Unit
```

This method is called when the user tapped a text view. IMEs can't rely on this method being called because this was not part of the original IME protocol, so applications with custom text editing written before this method appeared will not call to inform the IME of this interaction.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `focusChanged` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the user changed the focused view by this click. |
