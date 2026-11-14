Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Keyboard

```
open class Keyboard
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.inputmethodservice.Keyboard](../android/inputmethodservice/Keyboard.md) |

> [!CAUTION]
> **This class was deprecated in API level 29.**
>
> This class is deprecated because this is just a convenient UI widget class that application developers can re-implement on top of existing public APIs. If you have already depended on this class, consider copying the implementation from AOSP into your project or re-implementing a similar widget by yourselves

Loads an XML description of a keyboard and stores the attributes of the keys. A keyboard consists of rows of keys.

The layout file for a keyboard contains XML that looks like the following snippet:

```kotlin
<Keyboard
          android:keyWidth="%10p"
          android:keyHeight="50px"
          android:horizontalGap="2px"
          android:verticalGap="2px" >
      <Row android:keyWidth="32px" >
          <Key android:keyLabel="A" />
          ...
      </Row>
      ...
  </Keyboard>
  
```

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard.Key` Class for describing the position and characteristics of a single key in the keyboard. |
| open | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard.Row` Container for keys in the keyboard. |

| XML attributes ||
|---|---|
| [`android:horizontalGap`](../android/inputmethodservice/Keyboard.md) | Default horizontal gap between keys. |
| [`android:keyHeight`](../android/inputmethodservice/Keyboard.md) | Default height of a key, in pixels or percentage of display width. |
| [`android:keyWidth`](../android/inputmethodservice/Keyboard.md) | Default width of a key, in pixels or percentage of display width. |
| --- | --- |
| [`android:verticalGap`](../android/inputmethodservice/Keyboard.md) | Default vertical gap between rows of keys. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#EDGE_BOTTOM:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#EDGE_LEFT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#EDGE_RIGHT:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#EDGE_TOP:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_ALT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_CANCEL:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_DELETE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_DONE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_MODE_CHANGE:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#KEYCODE_SHIFT:kotlin.Int` <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#Keyboard(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, xmlLayoutResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a keyboard from the given xml key layout file. |
| `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#Keyboard(android.content.Context,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, xmlLayoutResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a keyboard from the given xml key layout file. |
| `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#Keyboard(android.content.Context,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, xmlLayoutResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a keyboard from the given xml key layout file. |
| `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#Keyboard(android.content.Context,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, layoutTemplateResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, characters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, columns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, horizontalPadding: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a blank keyboard from the given resource file and populates it with the specified characters in left-to-right, top-to-bottom fashion, using the specified number of columns. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getHeight()()` Returns the total height of the keyboard |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Keyboard.Key](../android/inputmethodservice/Keyboard.Key.md)!\>! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getKeys()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getMinWidth()()` <br /> |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Keyboard.Key](../android/inputmethodservice/Keyboard.Key.md)!\>! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getModifierKeys()()` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getNearestKeys(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the indices of the keys that are closest to the given point. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getShiftKeyIndex()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#isShifted()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#setShifted(kotlin.Boolean)(shiftState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |

| Protected methods ||
|---|---|
| open [Keyboard.Key](../android/inputmethodservice/Keyboard.Key.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#createKeyFromXml(android.content.res.Resources,%20android.inputmethodservice.Keyboard.Row,%20kotlin.Int,%20kotlin.Int,%20android.content.res.XmlResourceParser)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!, parent: https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard.Row!, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parser: https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!)` <br /> |
| open [Keyboard.Row](../android/inputmethodservice/Keyboard.Row.md)! | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#createRowFromXml(android.content.res.Resources,%20android.content.res.XmlResourceParser)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!, parser: https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getHorizontalGap()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getKeyHeight()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getKeyWidth()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#getVerticalGap()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#setHorizontalGap(kotlin.Int)(gap: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#setKeyHeight(kotlin.Int)(height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#setKeyWidth(kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard#setVerticalGap(kotlin.Int)(gap: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

## XML attributes

### android:horizontalGap

```
android:horizontalGap
```
Default horizontal gap between keys.

### android:keyHeight

```
android:keyHeight
```
Default height of a key, in pixels or percentage of display width.

### android:keyWidth

```
android:keyWidth
```
Default width of a key, in pixels or percentage of display width.

### android:verticalGap

```
android:verticalGap
```
Default vertical gap between rows of keys.

## Constants

### EDGE_BOTTOM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_BOTTOM: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 8

### EDGE_LEFT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_LEFT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 1

### EDGE_RIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_RIGHT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 2

### EDGE_TOP

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_TOP: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 4

### KEYCODE_ALT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ALT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -6

### KEYCODE_CANCEL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CANCEL: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -3

### KEYCODE_DELETE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DELETE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -5

### KEYCODE_DONE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DONE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -4

### KEYCODE_MODE_CHANGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MODE_CHANGE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -2

### KEYCODE_SHIFT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SHIFT: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: -1

## Public constructors

### Keyboard

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Keyboard(
    context: Context!, 
    xmlLayoutResId: Int)
```

Creates a keyboard from the given xml key layout file.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: the application or service context |
| `xmlLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource file that contains the keyboard layout and keys. |

### Keyboard

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Keyboard(
    context: Context!, 
    xmlLayoutResId: Int, 
    modeId: Int)
```

Creates a keyboard from the given xml key layout file. Weeds out rows that have a keyboard mode defined but don't match the specified mode.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: the application or service context |
| `xmlLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource file that contains the keyboard layout and keys. |
| `modeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): keyboard mode identifier |
| --- | --- |

### Keyboard

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Keyboard(
    context: Context!, 
    xmlLayoutResId: Int, 
    modeId: Int, 
    width: Int, 
    height: Int)
```

Creates a keyboard from the given xml key layout file. Weeds out rows that have a keyboard mode defined but don't match the specified mode.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: the application or service context |
| `xmlLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource file that contains the keyboard layout and keys. |
| `modeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): keyboard mode identifier |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): sets width of keyboard |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): sets height of keyboard |

### Keyboard

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Keyboard(
    context: Context!, 
    layoutTemplateResId: Int, 
    characters: CharSequence!, 
    columns: Int, 
    horizontalPadding: Int)
```

Creates a blank keyboard from the given resource file and populates it with the specified characters in left-to-right, top-to-bottom fashion, using the specified number of columns.

If the specified number of columns is -1, then the keyboard will fit as many keys as possible in each row.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: the application or service context |
| `layoutTemplateResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the layout template file, containing no keys. |
| `characters` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the list of characters to display on the keyboard. One key will be created for each character. |
| --- | --- |
| `columns` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of columns of keys to display. If this number is greater than the number of keys that can fit in a row, it will be ignored. If this number is -1, the keyboard will fit as many keys as possible in each row. |

## Public methods

### getHeight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeight(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the total height of the keyboard

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total height of the keyboard |

### getKeys

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeys(): MutableList<Keyboard.Key!>!
```

**Deprecated:** *Deprecated in Java.*

### getMinWidth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinWidth(): Int
```

**Deprecated:** *Deprecated in Java.*

### getModifierKeys

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getModifierKeys(): MutableList<Keyboard.Key!>!
```

**Deprecated:** *Deprecated in Java.*

### getNearestKeys

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNearestKeys(
    x: Int, 
    y: Int
): IntArray!
```

**Deprecated:** *Deprecated in Java.*

Returns the indices of the keys that are closest to the given point.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the x-coordinate of the point |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the y-coordinate of the point |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | the array of integer indices for the nearest keys to the given point. If the given point is out of range, then an array of size zero is returned. |

### getShiftKeyIndex

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShiftKeyIndex(): Int
```

**Deprecated:** *Deprecated in Java.*

### isShifted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShifted(): Boolean
```

**Deprecated:** *Deprecated in Java.*

### setShifted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShifted(shiftState: Boolean): Boolean
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### createKeyFromXml

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun createKeyFromXml(
    res: Resources!, 
    parent: Keyboard.Row!, 
    x: Int, 
    y: Int, 
    parser: XmlResourceParser!
): Keyboard.Key!
```

**Deprecated:** *Deprecated in Java.*

### createRowFromXml

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun createRowFromXml(
    res: Resources!, 
    parser: XmlResourceParser!
): Keyboard.Row!
```

**Deprecated:** *Deprecated in Java.*

### getHorizontalGap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getHorizontalGap(): Int
```

**Deprecated:** *Deprecated in Java.*

### getKeyHeight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getKeyHeight(): Int
```

**Deprecated:** *Deprecated in Java.*

### getKeyWidth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getKeyWidth(): Int
```

**Deprecated:** *Deprecated in Java.*

### getVerticalGap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getVerticalGap(): Int
```

**Deprecated:** *Deprecated in Java.*

### setHorizontalGap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setHorizontalGap(gap: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

### setKeyHeight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setKeyHeight(height: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

### setKeyWidth

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setKeyWidth(width: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

### setVerticalGap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setVerticalGap(gap: Int): Unit
```

**Deprecated:** *Deprecated in Java.*
