# LinkMovementMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkMovementMethod

Kotlin| [Java](LinkMovementMethod.md) 
| --- | --- |

```
open class LinkMovementMethod : ScrollingMovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.method.BaseMovementMethod](BaseMovementMethod.md) |||
| | ↳ | [android.text.method.ScrollingMovementMethod](ScrollingMovementMethod.md) ||
| | | ↳ | [android.text.method.LinkMovementMethod](LinkMovementMethod.md) |
| --- | --- | --- | --- |

A movement method that traverses links in the text buffer and scrolls if necessary. Supports clicking on links with DPad Center or Enter.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkMovementMethod](LinkMovementMethod.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](LinkMovementMethod.md))`()` <br /> |
| openstatic [MovementMethod](MovementMethod.md)! | [getInstance](LinkMovementMethod.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](LinkMovementMethod.md))`(`view:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [down](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [left](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [right](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [up](LinkMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [ScrollingMovementMethod](ScrollingMovementMethod.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [bottom](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [end](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [home](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineEnd](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineStart](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageDown](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageUp](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [top](ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | ||
| From class [BaseMovementMethod](BaseMovementMethod.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](BaseMovementMethod.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementMetaState](BaseMovementMethod.md))`(`buffer:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `buffer:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as [down](BaseMovementMethod.md))and [up](BaseMovementMethod.md)). [onKeyDown(android.widget.TextView,android.text.Spannable,int,android.view.KeyEvent)](BaseMovementMethod.md))calls this method once to handle an [KeyEvent.ACTION_DOWN](../android.view/KeyEvent.md). [onKeyOther(android.widget.TextView,android.text.Spannable,android.view.KeyEvent)](BaseMovementMethod.md))calls this method repeatedly to handle each repetition of an [KeyEvent.ACTION_MULTIPLE](../android.view/KeyEvent.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextParagraph](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)`, `buffer:` ` [Spannable](../android.text/Spannable.md)`)` <br /> Performs a next paragraph movement action. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previousParagraph](BaseMovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)`, `buffer:` ` [Spannable](../android.text/Spannable.md)`)` <br /> Performs a previous paragraph movement action. <br /> | ||

## Public constructors

### LinkMovementMethod

```
LinkMovementMethod()
```

## Public methods

### canSelectArbitrarily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canSelectArbitrarily(): Boolean
```  

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): MovementMethod!
```  

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    widget: TextView!, 
    text: Spannable!
): Unit
```  

### onTakeFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTakeFocus(
    view: TextView!, 
    text: Spannable!, 
    dir: Int
): Unit
```  

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(
    widget: TextView!, 
    buffer: Spannable!, 
    event: MotionEvent!
): Boolean
```

## Protected methods

### down

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun down(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android.widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### handleMovementKey

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleMovementKey(
    widget: TextView!, 
    buffer: Spannable!, 
    keyCode: Int, 
    movementMetaState: Int, 
    event: KeyEvent!
): Boolean
```

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android.widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!:The text buffer. |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!:The key event. |
| --- | --- |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The key code. |
| `movementMetaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The keyboard meta states used for movement. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### left

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun left(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android.widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### right

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun right(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android.widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### up

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun up(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android.widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |
