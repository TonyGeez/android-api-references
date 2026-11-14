Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleCustomizationAction

```
class SimpleCustomizationAction : CustomizationAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.hardware.input.CustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationAction) ||
| | ↳ | [android.hardware.input.SimpleCustomizationAction](https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#) |

Represents predefined simple actions, such as Volume up/down, Screenshot, etc.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_ASSIST:kotlin.Int` Action type: Assist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BACK:kotlin.Int` Action type: Back. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_DOWN:kotlin.Int` Action type: Brightness down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_UP:kotlin.Int` Action type: Brightness up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CALCULATOR:kotlin.Int` Action type: Calculator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CLOSE_WINDOW:kotlin.Int` Action type: Close window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_INSERT:kotlin.Int` Action type: Contextual Insert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_QUERY:kotlin.Int` Action type: Contextual Query. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_SEARCH:kotlin.Int` Action type: Contextual Search. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_COPY:kotlin.Int` Action type: Copy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CUT:kotlin.Int` Action type: Cut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DICTATION:kotlin.Int` Action type: Dictation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DO_NOTHING:kotlin.Int` Action type: Do nothing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_EMOJI_MENU:kotlin.Int` Action type: Emoji menu. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_FORWARD:kotlin.Int` Action type: Forward. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_LOCK:kotlin.Int` Action type: Lock screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_NEXT:kotlin.Int` Action type: Media next. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PLAY_PAUSE:kotlin.Int` Action type: Media play/pause. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PREVIOUS:kotlin.Int` Action type: Media previous. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PARTIAL_SCREENSHOT:kotlin.Int` Action type: Partial Screenshot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PASTE:kotlin.Int` Action type: Paste. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PRINT_SCREEN:kotlin.Int` Action type: Print screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SCREEN_CAPTURE:kotlin.Int` Action type: Screen capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SHOW_DESKTOP:kotlin.Int` Action type: Show desktop. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SWITCH_INPUT_LANGUAGE:kotlin.Int` Action type: Language Switch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOICE_ASSIST:kotlin.Int` Action type: Voice Assist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_DOWN:kotlin.Int` Action type: Volume down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_MUTE:kotlin.Int` Action type: Volume mute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_UP:kotlin.Int` Action type: Volume up. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#SimpleCustomizationAction(kotlin.Int)(actionType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#` with the specified action type. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#getType()()` Returns the specific type of action to be performed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#hashCode()()` Returns a hash code value for the object. |

## Constants

### TYPE_ASSIST

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ASSIST: Int
```

Action type: Assist.

Specifies the action to launch the default assistant for textual input when the peripheral input is triggered.

 Value: 21

### TYPE_BACK

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BACK: Int
```

Action type: Back.

Specifies the action to go back when the peripheral input is triggered.

 Value: 1

### TYPE_BRIGHTNESS_DOWN

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BRIGHTNESS_DOWN: Int
```

Action type: Brightness down.

Specifies the action to decrease screen brightness when the peripheral input is triggered.

 Value: 2

### TYPE_BRIGHTNESS_UP

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BRIGHTNESS_UP: Int
```

Action type: Brightness up.

Specifies the action to increase screen brightness when the peripheral input is triggered.

 Value: 3

### TYPE_CALCULATOR

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CALCULATOR: Int
```

Action type: Calculator.

Specifies the action to launch calculator app when the peripheral input is triggered.

 Value: 4

### TYPE_CLOSE_WINDOW

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CLOSE_WINDOW: Int
```

Action type: Close window.

Specifies the action to close the currently focused window when the peripheral input is triggered.

 Value: 19

### TYPE_CONTEXTUAL_INSERT

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CONTEXTUAL_INSERT: Int
```

Action type: Contextual Insert.

Specifies the action to trigger a contextual panel for inserting content into the focused input field when the peripheral input is triggered.

 Value: 22

### TYPE_CONTEXTUAL_QUERY

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CONTEXTUAL_QUERY: Int
```

Action type: Contextual Query.

Specifies the action to launch the contextual cursor. When available, this intelligent pointer analyzes screen elements beneath the cursor (such as images or text paragraphs) and displays contextual suggestions to discover available actions (like copy, translate, or share) when the peripheral input is triggered.

 Value: 24

### TYPE_CONTEXTUAL_SEARCH

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CONTEXTUAL_SEARCH: Int
```

Action type: Contextual Search.

Specifies the action to launch a search experience that allows the user to search for information about any content displayed on the screen - using gestures like circling, highlighting, or tapping - without switching apps, when the peripheral input is triggered.

 Value: 23

### TYPE_COPY

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_COPY: Int
```

Action type: Copy.

Specifies the action to trigger copying of any pre-selected content onto the clipboard when the peripheral input is triggered.

 Value: 26

### TYPE_CUT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CUT: Int
```

Action type: Cut.

Specifies the action to trigger cutting of any pre-selected content onto the clipboard when the peripheral input is triggered.

 Value: 28

### TYPE_DICTATION

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DICTATION: Int
```

Action type: Dictation.

Specifies the action to start dictation when the peripheral input is triggered.

 Value: 5

### TYPE_DO_NOTHING

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DO_NOTHING: Int
```

Action type: Do nothing.

Specifies that no action should occur when the peripheral input is triggered, effectively swallowing the default hardware behavior.

 Value: 18

### TYPE_EMOJI_MENU

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_EMOJI_MENU: Int
```

Action type: Emoji menu.

Specifies the action to show emoji menu when the peripheral input is triggered.

 Value: 6

### TYPE_FORWARD

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FORWARD: Int
```

Action type: Forward.

Specifies the action to go forward when the peripheral input is triggered.

 Value: 7

### TYPE_LOCK

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LOCK: Int
```

Action type: Lock screen.

Specifies the action to lock screen when the peripheral input is triggered.

 Value: 8

### TYPE_MEDIA_NEXT

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MEDIA_NEXT: Int
```

Action type: Media next.

Specifies the action to skip to the next media track when the peripheral input is triggered.

 Value: 9

### TYPE_MEDIA_PLAY_PAUSE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MEDIA_PLAY_PAUSE: Int
```

Action type: Media play/pause.

Specifies the action to toggle media play/pause when the peripheral input is triggered.

 Value: 10

### TYPE_MEDIA_PREVIOUS

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MEDIA_PREVIOUS: Int
```

Action type: Media previous.

Specifies the action to skip to the previous media track when the peripheral input is triggered.

 Value: 11

### TYPE_PARTIAL_SCREENSHOT

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PARTIAL_SCREENSHOT: Int
```

Action type: Partial Screenshot.

Specifies the action to activate the system region capture utility to take a partial screenshot when the peripheral input is triggered.

 Value: 20

### TYPE_PASTE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PASTE: Int
```

Action type: Paste.

Specifies the action to trigger pasting of the current clipboard content into the focused input field when the peripheral input is triggered.

 Value: 27

### TYPE_PRINT_SCREEN

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PRINT_SCREEN: Int
```

Action type: Print screen.

Specifies the action to take a snapshot that is first sent to the foreground app for handling. If the app does not consume it, the framework captures the screen, mimicking `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_SYSRQ:kotlin.Int`.

 Value: 12

### TYPE_SCREEN_CAPTURE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SCREEN_CAPTURE: Int
```

Action type: Screen capture.

Specifies the action to trigger a global framework-level screenshot. Unlike `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PRINT_SCREEN:kotlin.Int`, this action bypasses the foreground app and typically displays system UI tools for editing or sharing.

 Value: 13

### TYPE_SHOW_DESKTOP

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SHOW_DESKTOP: Int
```

Action type: Show desktop.

Specifies the action to show desktop when the peripheral input is triggered.

 Value: 14

### TYPE_SWITCH_INPUT_LANGUAGE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SWITCH_INPUT_LANGUAGE: Int
```

Action type: Language Switch.

Specifies the action to trigger toggling the current input language when the peripheral input is triggered.

It can be used for example to switch between English and Japanese on a QWERTY keyboard.

 Value: 29

### TYPE_VOICE_ASSIST

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VOICE_ASSIST: Int
```

Action type: Voice Assist.

Specifies the action to launch the default assistant for voice input when the peripheral input is triggered.

 Value: 25

### TYPE_VOLUME_DOWN

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VOLUME_DOWN: Int
```

Action type: Volume down.

Specifies the action to decrease the current system volume level when the peripheral input is triggered.

 Value: 15

### TYPE_VOLUME_MUTE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VOLUME_MUTE: Int
```

Action type: Volume mute.

Specifies the action to toggle the system mute state or mute the current volume when the peripheral input is triggered.

 Value: 16

### TYPE_VOLUME_UP

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VOLUME_UP: Int
```

Action type: Volume up.

Specifies the action to increase the current system volume level when the peripheral input is triggered.

 Value: 17

## Public constructors

### SimpleCustomizationAction

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SimpleCustomizationAction(actionType: Int)
```

Creates a new `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#` with the specified action type.

| Parameters ||
|---|---|
| `actionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of action to be performed, such as `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SCREEN_CAPTURE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CALCULATOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DICTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_EMOJI_MENU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_NEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PLAY_PAUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PREVIOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PRINT_SCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SCREEN_CAPTURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SHOW_DESKTOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_MUTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DO_NOTHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CLOSE_WINDOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PARTIAL_SCREENSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_ASSIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_SEARCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_QUERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOICE_ASSIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SWITCH_INPUT_LANGUAGE:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provided action type does not match any defined android.hardware.input.SimpleCustomizationAction.Type. |

## Public methods

### equals

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getType

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the specific type of action to be performed.

The returned value corresponds to one of the action type constants, such as `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SCREEN_CAPTURE:kotlin.Int` which defines the behavior triggered by the peripheral customization.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the type of action. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_BRIGHTNESS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CALCULATOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DICTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_EMOJI_MENU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_NEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PLAY_PAUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_MEDIA_PREVIOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PRINT_SCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SCREEN_CAPTURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SHOW_DESKTOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_MUTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOLUME_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_DO_NOTHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CLOSE_WINDOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PARTIAL_SCREENSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_ASSIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_SEARCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CONTEXTUAL_QUERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_VOICE_ASSIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_COPY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_PASTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_CUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/SimpleCustomizationAction#TYPE_SWITCH_INPUT_LANGUAGE:kotlin.Int` |

### hashCode

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
