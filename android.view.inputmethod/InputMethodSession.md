# InputMethodSession

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethodSession

Kotlin| [Java](InputMethodSession.md) 
| --- | --- |

```
interface InputMethodSession
```

| [android.view.inputmethod.InputMethodSession](InputMethodSession.md) |

| Known Direct Subclasses [AbstractInputMethodService.AbstractInputMethodSessionImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractInputMethodService.AbstractInputMethodSessionImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.md) | Base class for derived classes to implement their [InputMethodSession](InputMethodSession.md) interface. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [InputMethodService.InputMethodSessionImpl](../android/inputmethodservice/InputMethodService.InputMethodSessionImpl.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputMethodService.InputMethodSessionImpl](../android/inputmethodservice/InputMethodService.InputMethodSessionImpl.md) | Concrete implementation of [AbstractInputMethodService.AbstractInputMethodSessionImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodSessionImpl.md) that provides all of the standard behavior for an input method session. | |
| --- | --- | --- | --- | --- | --- | --- |

The InputMethodSession interface provides the per-client functionality of [InputMethod](InputMethod.md) that is safe to expose to applications.

Applications will not normally use this interface themselves, instead relying on the standard interaction provided by [android.widget.TextView](../android.widget/TextView.md) and [android.widget.EditText](../android.widget/EditText.md).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| abstract | [EventCallback](../android/view/inputmethod/InputMethodSession.EventCallback.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appPrivateCommand](InputMethodSession.md))`(`action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [Bundle](../android.os/Bundle.md)!`)` Process a private command sent from the application to the input method. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchGenericMotionEvent](InputMethodSession.md))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`, `callback:` ` [InputMethodSession.EventCallback](../android/view/inputmethod/InputMethodSession.EventCallback.md)!`)` This method is called when there is a generic motion event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchKeyEvent](InputMethodSession.md))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`, `callback:` ` [InputMethodSession.EventCallback](../android/view/inputmethod/InputMethodSession.EventCallback.md)!`)` This method is called when a key is pressed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchTrackballEvent](InputMethodSession.md))`(`seq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`, `callback:` ` [InputMethodSession.EventCallback](../android/view/inputmethod/InputMethodSession.EventCallback.md)!`)` This method is called when there is a track ball event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [displayCompletions](InputMethodSession.md))`(`completions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CompletionInfo](CompletionInfo.md)!>!`)` Called by a text editor that performs auto completion, to tell the input method about the completions it has available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishInput](InputMethodSession.md))`()` This method is called when the application would like to stop receiving text input. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggleSoftInput](InputMethodSession.md))`(`showFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hideFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Toggle the soft input window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCursor](InputMethodSession.md))`(`newCursor:` ` [Rect](../android.graphics/Rect.md)!`)` This method is called when cursor location of the target input field has changed within its window. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCursorAnchorInfo](InputMethodSession.md))`(`cursorAnchorInfo:` ` [CursorAnchorInfo](CursorAnchorInfo.md)!`)` This method is called when the cursor and/or the character position relevant to text input is changed on the screen. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateExtractedText](InputMethodSession.md))`(`token:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [ExtractedText](ExtractedText.md)!`)` Called by a text editor to report its new extracted text when its contents change. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSelection](InputMethodSession.md))`(`oldSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the selection or cursor in the current target input field has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [viewClicked](InputMethodSession.md))`(`focusChanged:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This method is called when the user tapped a text view. |
| --- | --- |

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
| `data` | [Bundle](../android.os/Bundle.md)!:Any data to include with the command. |

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
| `event` | [MotionEvent](../android.view/MotionEvent.md)!:The motion event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.MotionEvent](../android.view/MotionEvent.md) 

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
| `event` | [KeyEvent](../android.view/KeyEvent.md)!:The key event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.KeyEvent](../android.view/KeyEvent.md) 

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
| `event` | [MotionEvent](../android.view/MotionEvent.md)!:The motion event. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | Whether the input method wants to handle this event. |

**See Also**

- [android.view.MotionEvent](../android.view/MotionEvent.md) 

### displayCompletions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun displayCompletions(completions: Array<CompletionInfo!>!): Unit
```

Called by a text editor that performs auto completion, to tell the input method about the completions it has available. This can be used by the input method to display them to the user to select the text to be inserted.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `completions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CompletionInfo](CompletionInfo.md)!\>!:Array of text completions that are available, starting with the best. If this array is null, any existing completions will be removed. |

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

**Deprecated:** *Starting in [android.os.Build.VERSION_CODES#S](../android/os/Build.VERSION_CODES.md) the system no longer invokes this method, instead it explicitly shows or hides the IME. An`InputMethodService`wishing to toggle its own visibility should instead invoke [android.inputmethodservice.InputMethodService#requestShowSelf](../android.inputmethodservice/InputMethodService.md))or [InputMethodService.requestHideSelf](../android.inputmethodservice/InputMethodService.md))*

Toggle the soft input window. Applications can toggle the state of the soft input window.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `showFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.inputmethod.InputMethodManager#SHOW_IMPLICIT](InputMethodManager.md), and [android.view.inputmethod.InputMethodManager#SHOW_FORCED](InputMethodManager.md) |
| `hideFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.inputmethod.InputMethodManager#HIDE_IMPLICIT_ONLY](InputMethodManager.md), and [android.view.inputmethod.InputMethodManager#HIDE_NOT_ALWAYS](InputMethodManager.md) |

### updateCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateCursor(newCursor: Rect!): Unit
```

This method is called when cursor location of the target input field has changed within its window. This is not normally called, but will only be reported if requested by the input method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newCursor` | [Rect](../android.graphics/Rect.md)!:The rectangle of the cursor currently being shown in the input field's window coordinates. |

### updateCursorAnchorInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateCursorAnchorInfo(cursorAnchorInfo: CursorAnchorInfo!): Unit
```

This method is called when the cursor and/or the character position relevant to text input is changed on the screen. This is not called by default. It will only be reported if requested by the input method.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursorAnchorInfo` | [CursorAnchorInfo](CursorAnchorInfo.md)!:Positional information relevant to text input, such as text insertion point and composition string. |

### updateExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateExtractedText(
    token: Int, 
    text: ExtractedText!
): Unit
```

Called by a text editor to report its new extracted text when its contents change. This will only be called if the input method calls [InputConnection.getExtractedText()](InputConnection.md))with the option to report updates.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The input method supplied token for identifying its request. |
| `text` | [ExtractedText](ExtractedText.md)!:The new extracted text. |

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
| --- | --- |
| `newSelEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new text offset of the cursor selection end position. |
| `candidatesStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The text offset of the current candidate text start position. |
| `candidatesEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The text offset of the current candidate text end position. |
| --- | --- |

### viewClicked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun viewClicked(focusChanged: Boolean): Unit
```

This method is called when the user tapped a text view. IMEs can't rely on this method being called because this was not part of the original IME protocol, so applications with custom text editing written before this method appeared will not call to inform the IME of this interaction.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `focusChanged` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the user changed the focused view by this click. |
