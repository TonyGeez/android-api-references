Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyEvent

```
open class KeyEvent : InputEvent, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent) ||
| | ↳ | [android.view.KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#) |

Object used to report key and button events.

Each key press is described by a sequence of key events. A key press starts with a key event with `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int`. If the key is held sufficiently long that it repeats, then the initial down is followed additional key events with `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` and a non-zero value for `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getRepeatCount()`. The last key event is a `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` for the key up. If the key press is canceled, the key up event will have the `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int` flag set.

Key events are generally accompanied by a key code (`https://developer.android.com/reference/kotlin/android/view/KeyEvent#getKeyCode()`), scan code (`https://developer.android.com/reference/kotlin/android/view/KeyEvent#getScanCode()`) and meta state (`https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`). Key code constants are defined in this class. Scan code constants are raw device-specific codes obtained from the OS and so are not generally meaningful to applications unless interpreted using the `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap`. Meta states describe the pressed state of key modifiers such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`.

Key codes typically correspond one-to-one with individual keys on an input device. Many keys and key combinations serve quite different functions on different input devices so care must be taken when interpreting them. Always use the `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap` associated with the input device when mapping keys to characters. Be aware that there may be multiple key input devices active at the same time and each will have its own key character map.

As soft input methods can use multiple and inventive ways of inputting text, there is no guarantee that any key press on a soft keyboard will generate a key event: this is left to the IME's discretion, and in fact sending such events is discouraged. You should never rely on receiving KeyEvents for any key on a soft input method. In particular, the default software keyboard will never send any key event to any application targetting Jelly Bean or later, and will only send events for some presses of the delete and return keys to applications targetting Ice Cream Sandwich or earlier. Be aware that other software input methods may never send key events regardless of the version. Consider using editor actions like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_DONE:kotlin.Int` if you need specific interaction with the software keyboard, as it gives more visibility to the user as to how your application will react to key presses.

In general, the framework cannot guarantee that the key events it delivers to a view always constitute complete key sequences since some events may be dropped or modified by containing views before they are delivered. The view implementation should be prepared to handle `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int` and should tolerate anomalous situations such as receiving a new `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` without first having received an `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` for the prior key press.

Refer to `https://developer.android.com/reference/kotlin/android/view/InputDevice` for more information about how different kinds of input devices and sources represent keys and buttons.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback` <br /> |
| open | `https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState` Use with `https://developer.android.com/reference/kotlin/android/view/KeyEvent#dispatch(android.view.KeyEvent.Callback,%20android.view.KeyEvent.DispatcherState,%20kotlin.Any)` for more advanced key dispatching, such as long presses. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()` value: the key has been pressed down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()` value: the key has been released. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int` When associated with up key events, this indicates that the key press has been canceled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED_LONG_PRESS:kotlin.Int` Set when a key event has `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int` set because a long press action was executed while it was down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_EDITOR_ACTION:kotlin.Int` This mask is used for compatibility, to identify enter keys that are coming from an IME whose enter key has been auto-labelled "next" or "done". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_FALLBACK:kotlin.Int` Set when a key event has been synthesized to implement default behavior for an event that the application did not handle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_FROM_SYSTEM:kotlin.Int` This mask is set if an event was known to come from a trusted part of the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_KEEP_TOUCH_MODE:kotlin.Int` This mask is set if we don't want the key event to cause us to leave touch mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_LONG_PRESS:kotlin.Int` This flag is set for the first key repeat that occurs after the long press timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_SOFT_KEYBOARD:kotlin.Int` This mask is set if the key event was generated by a software keyboard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_TRACKING:kotlin.Int` Set for `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` when this event's key code is still being tracked from its initial down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_VIRTUAL_HARD_KEY:kotlin.Int` This key event was generated by a virtual (on-screen) hard key area. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_WOKE_HERE:kotlin.Int` This mask is set if the device woke because of this key event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_0:kotlin.Int` Key code constant: '0' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_1:kotlin.Int` Key code constant: '1' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_11:kotlin.Int` Key code constant: '11' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_12:kotlin.Int` Key code constant: '12' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_2:kotlin.Int` Key code constant: '2' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_3:kotlin.Int` Key code constant: '3' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_3D_MODE:kotlin.Int` Key code constant: 3D Mode key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_4:kotlin.Int` Key code constant: '4' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_5:kotlin.Int` Key code constant: '5' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_6:kotlin.Int` Key code constant: '6' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_7:kotlin.Int` Key code constant: '7' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_8:kotlin.Int` Key code constant: '8' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_9:kotlin.Int` Key code constant: '9' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_A:kotlin.Int` Key code constant: 'A' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ACCESSIBILITY:kotlin.Int` Key code constant: System Accessibility key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALL_APPS:kotlin.Int` Key code constant: Show all apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int` Key code constant: Left Alt modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_RIGHT:kotlin.Int` Key code constant: Right Alt modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_APOSTROPHE:kotlin.Int` Key code constant: ''' (apostrophe) key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_APP_SWITCH:kotlin.Int` Key code constant: App switch key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ASSIST:kotlin.Int` Key code constant: Assist key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_AT:kotlin.Int` Key code constant: '@' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_AVR_INPUT:kotlin.Int` Key code constant: A/V Receiver input key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_AVR_POWER:kotlin.Int` Key code constant: A/V Receiver power key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_B:kotlin.Int` Key code constant: 'B' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BACK:kotlin.Int` Key code constant: Back key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BACKSLASH:kotlin.Int` Key code constant: '\\' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BOOKMARK:kotlin.Int` Key code constant: Bookmark key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BREAK:kotlin.Int` Key code constant: Break / Pause key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BRIGHTNESS_DOWN:kotlin.Int` Key code constant: Brightness Down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BRIGHTNESS_UP:kotlin.Int` Key code constant: Brightness Up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_1:kotlin.Int` Key code constant: Generic Game Pad Button #1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_10:kotlin.Int` Key code constant: Generic Game Pad Button #10. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_11:kotlin.Int` Key code constant: Generic Game Pad Button #11. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_12:kotlin.Int` Key code constant: Generic Game Pad Button #12. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_13:kotlin.Int` Key code constant: Generic Game Pad Button #13. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_14:kotlin.Int` Key code constant: Generic Game Pad Button #14. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_15:kotlin.Int` Key code constant: Generic Game Pad Button #15. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_16:kotlin.Int` Key code constant: Generic Game Pad Button #16. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_2:kotlin.Int` Key code constant: Generic Game Pad Button #2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_3:kotlin.Int` Key code constant: Generic Game Pad Button #3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_4:kotlin.Int` Key code constant: Generic Game Pad Button #4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_5:kotlin.Int` Key code constant: Generic Game Pad Button #5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_6:kotlin.Int` Key code constant: Generic Game Pad Button #6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_7:kotlin.Int` Key code constant: Generic Game Pad Button #7. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_8:kotlin.Int` Key code constant: Generic Game Pad Button #8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_9:kotlin.Int` Key code constant: Generic Game Pad Button #9. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_A:kotlin.Int` Key code constant: A Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_B:kotlin.Int` Key code constant: B Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_C:kotlin.Int` Key code constant: C Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_L1:kotlin.Int` Key code constant: L1 Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_L2:kotlin.Int` Key code constant: L2 Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_MODE:kotlin.Int` Key code constant: Mode Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_R1:kotlin.Int` Key code constant: R1 Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_R2:kotlin.Int` Key code constant: R2 Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_SELECT:kotlin.Int` Key code constant: Select Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_START:kotlin.Int` Key code constant: Start Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_THUMBL:kotlin.Int` Key code constant: Left Thumb Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_THUMBR:kotlin.Int` Key code constant: Right Thumb Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_X:kotlin.Int` Key code constant: X Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_Y:kotlin.Int` Key code constant: Y Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_Z:kotlin.Int` Key code constant: Z Button key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_C:kotlin.Int` Key code constant: 'C' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CALCULATOR:kotlin.Int` Key code constant: Calculator special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CALENDAR:kotlin.Int` Key code constant: Calendar special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CALL:kotlin.Int` Key code constant: Call key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAMERA:kotlin.Int` Key code constant: Camera key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int` Key code constant: Caps Lock key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPTIONS:kotlin.Int` Key code constant: Toggle captions key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CHANNEL_DOWN:kotlin.Int` Key code constant: Channel down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CHANNEL_UP:kotlin.Int` Key code constant: Channel up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CLEAR:kotlin.Int` Key code constant: Clear key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CLOSE:kotlin.Int` Key code constant: AC Close. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_COMMA:kotlin.Int` Key code constant: ',' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CONTACTS:kotlin.Int` Key code constant: Contacts special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CONTEXTUAL_INSERT:kotlin.Int` Key code constant: Contextual Insert key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CONTEXTUAL_QUERY:kotlin.Int` Key code constant: Contextual Query key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CONTEXTUAL_SEARCH:kotlin.Int` Key code constant: Contextual Search key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_COPY:kotlin.Int` Key code constant: Copy key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_LEFT:kotlin.Int` Key code constant: Left Control modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_RIGHT:kotlin.Int` Key code constant: Right Control modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CUT:kotlin.Int` Key code constant: Cut key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_D:kotlin.Int` Key code constant: 'D' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEL:kotlin.Int` Key code constant: Backspace key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEMO_APP_1:kotlin.Int` Key code constant: Demo Application key #1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEMO_APP_2:kotlin.Int` Key code constant: Demo Application key #2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEMO_APP_3:kotlin.Int` Key code constant: Demo Application key #3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEMO_APP_4:kotlin.Int` Key code constant: Demo Application key #4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DICTATE:kotlin.Int` Key code constant: To start dictate to an input field |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DO_NOT_DISTURB:kotlin.Int` Key code constant: To toggle 'Do Not Disturb' mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_CENTER:kotlin.Int` Key code constant: Directional Pad Center key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_DOWN:kotlin.Int` Key code constant: Directional Pad Down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_DOWN_LEFT:kotlin.Int` Key code constant: Directional Pad Down-Left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_DOWN_RIGHT:kotlin.Int` Key code constant: Directional Pad Down-Right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_LEFT:kotlin.Int` Key code constant: Directional Pad Left key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_RIGHT:kotlin.Int` Key code constant: Directional Pad Right key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_UP:kotlin.Int` Key code constant: Directional Pad Up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_UP_LEFT:kotlin.Int` Key code constant: Directional Pad Up-Left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DPAD_UP_RIGHT:kotlin.Int` Key code constant: Directional Pad Up-Right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DVR:kotlin.Int` Key code constant: DVR key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_E:kotlin.Int` Key code constant: 'E' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_EISU:kotlin.Int` Key code constant: Japanese alphanumeric key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_EMOJI_PICKER:kotlin.Int` Key code constant: To open emoji picker. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENDCALL:kotlin.Int` Key code constant: End Call key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENTER:kotlin.Int` Key code constant: Enter key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ENVELOPE:kotlin.Int` Key code constant: Envelope special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_EQUALS:kotlin.Int` Key code constant: '=' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ESCAPE:kotlin.Int` Key code constant: Escape key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_EXPLORER:kotlin.Int` Key code constant: Explorer special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F:kotlin.Int` Key code constant: 'F' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F1:kotlin.Int` Key code constant: F1 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F10:kotlin.Int` Key code constant: F10 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F11:kotlin.Int` Key code constant: F11 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F12:kotlin.Int` Key code constant: F12 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F13:kotlin.Int` Key code constant: F13 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F14:kotlin.Int` Key code constant: F14 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F15:kotlin.Int` Key code constant: F15 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F16:kotlin.Int` Key code constant: F16 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F17:kotlin.Int` Key code constant: F17 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F18:kotlin.Int` Key code constant: F18 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F19:kotlin.Int` Key code constant: F19 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F2:kotlin.Int` Key code constant: F2 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F20:kotlin.Int` Key code constant: F20 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F21:kotlin.Int` Key code constant: F21 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F22:kotlin.Int` Key code constant: F22 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F23:kotlin.Int` Key code constant: F23 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F24:kotlin.Int` Key code constant: F24 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F3:kotlin.Int` Key code constant: F3 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F4:kotlin.Int` Key code constant: F4 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F5:kotlin.Int` Key code constant: F5 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F6:kotlin.Int` Key code constant: F6 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F7:kotlin.Int` Key code constant: F7 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F8:kotlin.Int` Key code constant: F8 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_F9:kotlin.Int` Key code constant: F9 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FEATURED_APP_1:kotlin.Int` Key code constant: Featured Application key #1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FEATURED_APP_2:kotlin.Int` Key code constant: Featured Application key #2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FEATURED_APP_3:kotlin.Int` Key code constant: Featured Application key #3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FEATURED_APP_4:kotlin.Int` Key code constant: Featured Application key #4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FOCUS:kotlin.Int` Key code constant: Camera Focus key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FORWARD:kotlin.Int` Key code constant: Forward key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FORWARD_DEL:kotlin.Int` Key code constant: Forward Delete key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FULLSCREEN:kotlin.Int` Key code constant: To toggle fullscreen mode (on the current application). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FUNCTION:kotlin.Int` Key code constant: Function modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_G:kotlin.Int` Key code constant: 'G' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_GRAVE:kotlin.Int` Key code constant: '\`' (backtick) key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_GUIDE:kotlin.Int` Key code constant: Guide key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_H:kotlin.Int` Key code constant: 'H' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_HEADSETHOOK:kotlin.Int` Key code constant: Headset Hook key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_HELP:kotlin.Int` Key code constant: Help key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_HENKAN:kotlin.Int` Key code constant: Japanese conversion key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_HOME:kotlin.Int` Key code constant: Home key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_I:kotlin.Int` Key code constant: 'I' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_INFO:kotlin.Int` Key code constant: Info key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_INSERT:kotlin.Int` Key code constant: Insert key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_J:kotlin.Int` Key code constant: 'J' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_K:kotlin.Int` Key code constant: 'K' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_KANA:kotlin.Int` Key code constant: Japanese kana key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_KATAKANA_HIRAGANA:kotlin.Int` Key code constant: Japanese katakana / hiragana key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_KEYBOARD_BACKLIGHT_DOWN:kotlin.Int` Key code constant: Keyboard backlight down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_KEYBOARD_BACKLIGHT_TOGGLE:kotlin.Int` Key code constant: Keyboard backlight toggle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_KEYBOARD_BACKLIGHT_UP:kotlin.Int` Key code constant: Keyboard backlight up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_L:kotlin.Int` Key code constant: 'L' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_LANGUAGE_SWITCH:kotlin.Int` Key code constant: Language Switch key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_LAST_CHANNEL:kotlin.Int` Key code constant: Last Channel key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_LEFT_BRACKET:kotlin.Int` Key code constant: '\[' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_LOCK:kotlin.Int` Key code constant: To lock the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_M:kotlin.Int` Key code constant: 'M' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MACRO_1:kotlin.Int` Key code constant: A button whose usage can be customized by the user through the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MACRO_2:kotlin.Int` Key code constant: A button whose usage can be customized by the user through the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MACRO_3:kotlin.Int` Key code constant: A button whose usage can be customized by the user through the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MACRO_4:kotlin.Int` Key code constant: A button whose usage can be customized by the user through the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MANNER_MODE:kotlin.Int` Key code constant: Manner Mode key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_AUDIO_TRACK:kotlin.Int` Key code constant: Audio Track key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_CLOSE:kotlin.Int` Key code constant: Close media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_EJECT:kotlin.Int` Key code constant: Eject media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_FAST_FORWARD:kotlin.Int` Key code constant: Fast Forward media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_NEXT:kotlin.Int` Key code constant: Play Next media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PAUSE:kotlin.Int` Key code constant: Pause media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PLAY:kotlin.Int` Key code constant: Play media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PLAY_PAUSE:kotlin.Int` Key code constant: Play/Pause media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PREVIOUS:kotlin.Int` Key code constant: Play Previous media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_RECORD:kotlin.Int` Key code constant: Record media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_REWIND:kotlin.Int` Key code constant: Rewind media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_SKIP_BACKWARD:kotlin.Int` Key code constant: Skip backward media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_SKIP_FORWARD:kotlin.Int` Key code constant: Skip forward media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_STEP_BACKWARD:kotlin.Int` Key code constant: Step backward media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_STEP_FORWARD:kotlin.Int` Key code constant: Step forward media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_STOP:kotlin.Int` Key code constant: Stop media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_TOP_MENU:kotlin.Int` Key code constant: Media Top Menu key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MENU:kotlin.Int` Key code constant: Menu key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_LEFT:kotlin.Int` Key code constant: Left Meta modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_RIGHT:kotlin.Int` Key code constant: Right Meta modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MINUS:kotlin.Int` Key code constant: '-'. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MOVE_END:kotlin.Int` Key code constant: End Movement key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MOVE_HOME:kotlin.Int` Key code constant: Home Movement key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MUHENKAN:kotlin.Int` Key code constant: Japanese non-conversion key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MUSIC:kotlin.Int` Key code constant: Music special function key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MUTE:kotlin.Int` Key code constant: Mute key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_N:kotlin.Int` Key code constant: 'N' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NAVIGATE_IN:kotlin.Int` Key code constant: Navigate in key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NAVIGATE_NEXT:kotlin.Int` Key code constant: Navigate to next key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NAVIGATE_OUT:kotlin.Int` Key code constant: Navigate out key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NAVIGATE_PREVIOUS:kotlin.Int` Key code constant: Navigate to previous key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NEW:kotlin.Int` Key code constant: AC New. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NOTIFICATION:kotlin.Int` Key code constant: Notification key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM:kotlin.Int` Key code constant: Number modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_0:kotlin.Int` Key code constant: Numeric keypad '0' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_1:kotlin.Int` Key code constant: Numeric keypad '1' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_2:kotlin.Int` Key code constant: Numeric keypad '2' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_3:kotlin.Int` Key code constant: Numeric keypad '3' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_4:kotlin.Int` Key code constant: Numeric keypad '4' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_5:kotlin.Int` Key code constant: Numeric keypad '5' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_6:kotlin.Int` Key code constant: Numeric keypad '6' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_7:kotlin.Int` Key code constant: Numeric keypad '7' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_8:kotlin.Int` Key code constant: Numeric keypad '8' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_9:kotlin.Int` Key code constant: Numeric keypad '9' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_ADD:kotlin.Int` Key code constant: Numeric keypad '+' key (for addition). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_COMMA:kotlin.Int` Key code constant: Numeric keypad ',' key (for decimals or digit grouping). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_DIVIDE:kotlin.Int` Key code constant: Numeric keypad '/' key (for division). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_DOT:kotlin.Int` Key code constant: Numeric keypad '. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_ENTER:kotlin.Int` Key code constant: Numeric keypad Enter key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_EQUALS:kotlin.Int` Key code constant: Numeric keypad '=' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_LEFT_PAREN:kotlin.Int` Key code constant: Numeric keypad '(' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_MULTIPLY:kotlin.Int` Key code constant: Numeric keypad '\*' key (for multiplication). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_RIGHT_PAREN:kotlin.Int` Key code constant: Numeric keypad ')' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUMPAD_SUBTRACT:kotlin.Int` Key code constant: Numeric keypad '-' key (for subtraction). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` Key code constant: Num Lock key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_O:kotlin.Int` Key code constant: 'O' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_P:kotlin.Int` Key code constant: 'P' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PAGE_DOWN:kotlin.Int` Key code constant: Page Down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PAGE_UP:kotlin.Int` Key code constant: Page Up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PAIRING:kotlin.Int` Key code constant: Pairing key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PASTE:kotlin.Int` Key code constant: Paste key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PERIOD:kotlin.Int` Key code constant: '. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PICTSYMBOLS:kotlin.Int` Key code constant: Picture Symbols modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PLUS:kotlin.Int` Key code constant: '+' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_POUND:kotlin.Int` Key code constant: '#' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_POWER:kotlin.Int` Key code constant: Power key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PRINT:kotlin.Int` Key code constant: To print. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PROFILE_SWITCH:kotlin.Int` Key code constant: Used to switch current `https://developer.android.com/reference/kotlin/android/accounts/Account.html#` that is consuming content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PROG_BLUE:kotlin.Int` Key code constant: Blue "programmable" key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PROG_GREEN:kotlin.Int` Key code constant: Green "programmable" key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PROG_RED:kotlin.Int` Key code constant: Red "programmable" key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_PROG_YELLOW:kotlin.Int` Key code constant: Yellow "programmable" key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_Q:kotlin.Int` Key code constant: 'Q' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_R:kotlin.Int` Key code constant: 'R' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_RECENT_APPS:kotlin.Int` Key code constant: To open recent apps view (a.k.a. Overview). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_REFRESH:kotlin.Int` Key code constant: Refresh key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_RIGHT_BRACKET:kotlin.Int` Key code constant: '\]' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_RO:kotlin.Int` Key code constant: Japanese Ro key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_S:kotlin.Int` Key code constant: 'S' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCREENSHOT:kotlin.Int` Key code constant: To take a screenshot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int` Key code constant: Scroll Lock key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SEARCH:kotlin.Int` Key code constant: Search key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SEMICOLON:kotlin.Int` Key code constant: ';' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SETTINGS:kotlin.Int` Key code constant: Settings key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_LEFT:kotlin.Int` Key code constant: Left Shift modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_RIGHT:kotlin.Int` Key code constant: Right Shift modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SLASH:kotlin.Int` Key code constant: '/' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SLEEP:kotlin.Int` Key code constant: Sleep key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SOFT_LEFT:kotlin.Int` Key code constant: Soft Left key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SOFT_RIGHT:kotlin.Int` Key code constant: Soft Right key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SOFT_SLEEP:kotlin.Int` Key code constant: Put device to sleep unless a wakelock is held. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SPACE:kotlin.Int` Key code constant: Space key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STAR:kotlin.Int` Key code constant: '\*' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STB_INPUT:kotlin.Int` Key code constant: Set-top-box input key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STB_POWER:kotlin.Int` Key code constant: Set-top-box power key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STEM_1:kotlin.Int` Key code constant: Generic stem key 1 for Wear. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STEM_2:kotlin.Int` Key code constant: Generic stem key 2 for Wear. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STEM_3:kotlin.Int` Key code constant: Generic stem key 3 for Wear. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STEM_PRIMARY:kotlin.Int` Key code constant: Primary stem key for Wear. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STYLUS_BUTTON_PRIMARY:kotlin.Int` Key code constant: The primary button on the barrel of a stylus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STYLUS_BUTTON_SECONDARY:kotlin.Int` Key code constant: The secondary button on the barrel of a stylus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STYLUS_BUTTON_TAIL:kotlin.Int` Key code constant: A button on the tail end of a stylus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_STYLUS_BUTTON_TERTIARY:kotlin.Int` Key code constant: The tertiary button on the barrel of a stylus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SWITCH_CHARSET:kotlin.Int` Key code constant: Switch Charset modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYM:kotlin.Int` Key code constant: Symbol modifier key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSRQ:kotlin.Int` Key code constant: System Request / Print Screen key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSTEM_NAVIGATION_DOWN:kotlin.Int` Key code constant: Consumed by the system for navigation down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSTEM_NAVIGATION_LEFT:kotlin.Int` Key code constant: Consumed by the system for navigation left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSTEM_NAVIGATION_RIGHT:kotlin.Int` Key code constant: Consumed by the system for navigation right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSTEM_NAVIGATION_UP:kotlin.Int` Key code constant: Consumed by the system for navigation up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_T:kotlin.Int` Key code constant: 'T' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TAB:kotlin.Int` Key code constant: Tab key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_THUMBS_DOWN:kotlin.Int` Key code constant: Thumbs down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_THUMBS_UP:kotlin.Int` Key code constant: Thumbs up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV:kotlin.Int` Key code constant: TV key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_ANTENNA_CABLE:kotlin.Int` Key code constant: Antenna/Cable key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_AUDIO_DESCRIPTION:kotlin.Int` Key code constant: Audio description key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_AUDIO_DESCRIPTION_MIX_DOWN:kotlin.Int` Key code constant: Audio description mixing volume down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_AUDIO_DESCRIPTION_MIX_UP:kotlin.Int` Key code constant: Audio description mixing volume up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_CONTENTS_MENU:kotlin.Int` Key code constant: Contents menu key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_DATA_SERVICE:kotlin.Int` Key code constant: TV data service key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT:kotlin.Int` Key code constant: TV input key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_COMPONENT_1:kotlin.Int` Key code constant: Component #1 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_COMPONENT_2:kotlin.Int` Key code constant: Component #2 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_COMPOSITE_1:kotlin.Int` Key code constant: Composite #1 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_COMPOSITE_2:kotlin.Int` Key code constant: Composite #2 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_HDMI_1:kotlin.Int` Key code constant: HDMI #1 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_HDMI_2:kotlin.Int` Key code constant: HDMI #2 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_HDMI_3:kotlin.Int` Key code constant: HDMI #3 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_HDMI_4:kotlin.Int` Key code constant: HDMI #4 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_INPUT_VGA_1:kotlin.Int` Key code constant: VGA #1 key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_MEDIA_CONTEXT_MENU:kotlin.Int` Key code constant: Media context menu key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_NETWORK:kotlin.Int` Key code constant: Toggle Network key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_NUMBER_ENTRY:kotlin.Int` Key code constant: Number entry key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_POWER:kotlin.Int` Key code constant: TV power key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_RADIO_SERVICE:kotlin.Int` Key code constant: Radio key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_SATELLITE:kotlin.Int` Key code constant: Satellite key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_SATELLITE_BS:kotlin.Int` Key code constant: BS key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_SATELLITE_CS:kotlin.Int` Key code constant: CS key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_SATELLITE_SERVICE:kotlin.Int` Key code constant: BS/CS key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_TELETEXT:kotlin.Int` Key code constant: Teletext key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_TERRESTRIAL_ANALOG:kotlin.Int` Key code constant: Analog Terrestrial key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_TERRESTRIAL_DIGITAL:kotlin.Int` Key code constant: Digital Terrestrial key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_TIMER_PROGRAMMING:kotlin.Int` Key code constant: Timer programming key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_TV_ZOOM_MODE:kotlin.Int` Key code constant: Zoom mode key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_U:kotlin.Int` Key code constant: 'U' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int` Key code constant: Unknown key code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_V:kotlin.Int` Key code constant: 'V' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_1:kotlin.Int` Key code constant: Video Application key #1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_2:kotlin.Int` Key code constant: Video Application key #2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_3:kotlin.Int` Key code constant: Video Application key #3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_4:kotlin.Int` Key code constant: Video Application key #4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_5:kotlin.Int` Key code constant: Video Application key #5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_6:kotlin.Int` Key code constant: Video Application key #6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_7:kotlin.Int` Key code constant: Video Application key #7. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VIDEO_APP_8:kotlin.Int` Key code constant: Video Application key #8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VOICE_ASSIST:kotlin.Int` Key code constant: Voice Assist key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VOLUME_DOWN:kotlin.Int` Key code constant: Volume Down key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VOLUME_MUTE:kotlin.Int` Key code constant: Volume Mute key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VOLUME_UP:kotlin.Int` Key code constant: Volume Up key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_W:kotlin.Int` Key code constant: 'W' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_WAKEUP:kotlin.Int` Key code constant: Wakeup key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_WINDOW:kotlin.Int` Key code constant: Window key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_X:kotlin.Int` Key code constant: 'X' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_Y:kotlin.Int` Key code constant: 'Y' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_YEN:kotlin.Int` Key code constant: Japanese Yen key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_Z:kotlin.Int` Key code constant: 'Z' key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ZENKAKU_HANKAKU:kotlin.Int` Key code constant: Japanese full-width / half-width key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ZOOM_IN:kotlin.Int` Key code constant: Zoom in key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ZOOM_OUT:kotlin.Int` Key code constant: Zoom out key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#MAX_KEYCODE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int` This mask is used to check whether the left ALT meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_MASK:kotlin.Int` This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_RIGHT_ON:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int` This mask is used to check whether one of the ALT meta keys is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_RIGHT_ON:kotlin.Int` This mask is used to check whether the right the ALT meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int` This mask is used to check whether the CAPS LOCK meta key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_LEFT_ON:kotlin.Int` This mask is used to check whether the left CTRL meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_MASK:kotlin.Int` This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_RIGHT_ON:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int` This mask is used to check whether one of the CTRL meta keys is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_RIGHT_ON:kotlin.Int` This mask is used to check whether the right CTRL meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int` This mask is used to check whether the FUNCTION meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_LEFT_ON:kotlin.Int` This mask is used to check whether the left META meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_MASK:kotlin.Int` This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_RIGHT_ON:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int` This mask is used to check whether one of the META meta keys is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_RIGHT_ON:kotlin.Int` This mask is used to check whether the right META meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int` This mask is used to check whether the NUM LOCK meta key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` This mask is used to check whether the SCROLL LOCK meta key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int` This mask is used to check whether the left SHIFT meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_MASK:kotlin.Int` This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_RIGHT_ON:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int` This mask is used to check whether one of the SHIFT meta keys is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_RIGHT_ON:kotlin.Int` This mask is used to check whether the right SHIFT meta key is pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int` This mask is used to check whether the SYM meta key is pressed. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(android.view.KeyEvent)(origEvent: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!)` Make an exact copy of an existing key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(android.view.KeyEvent,%20kotlin.Long,%20kotlin.Int)(origEvent: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newRepeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy an existing key event, modifying its time and repeat count. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Int,%20kotlin.Int)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)(time: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, characters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event for a string of characters. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(downTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(downTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(downTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scancode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(downTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scancode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |
| `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(downTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, repeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scancode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event. |

| Public methods ||
|---|---|
| open static [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#changeAction(android.view.KeyEvent,%20kotlin.Int)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event that is the same as the given one, but whose action is replaced with the given value. |
| open static [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#changeFlags(android.view.KeyEvent,%20kotlin.Int)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event that is the same as the given one, but whose flags are replaced with the given value. |
| open static [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#changeTimeRepeat(android.view.KeyEvent,%20kotlin.Long,%20kotlin.Int)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newRepeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event that is the same as the given one, but whose event time and repeat count are replaced with the given value. |
| open static [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#changeTimeRepeat(android.view.KeyEvent,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent#!, eventTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newRepeat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new key event that is the same as the given one, but whose event time and repeat count are replaced with the given value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#dispatch(android.view.KeyEvent.Callback)(receiver: https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback!)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#dispatch(android.view.KeyEvent.Callback,%20android.view.KeyEvent.DispatcherState,%20kotlin.Any)(receiver: https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback!, state: https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState!, target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Deliver this key event to a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback` interface. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()()` Retrieve the action of this key event. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getCharacters()()` For the special case of a `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int` event with key code of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int`, this is a raw string of characters associated with the event. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDeadChar(kotlin.Int,%20kotlin.Int)(accent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the character that is produced by putting accent on the character c. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDeviceId()()` Gets the id for the device that this event came from. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDisplayLabel()()` Gets the primary character for this key. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDownTime()()` Retrieve the time of the most recent key down event, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getEventTime()()` Retrieve the time this event occurred, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getFlags()()` Returns the flags for this key event. |
| [KeyCharacterMap](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getKeyCharacterMap()()` Gets the `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap` associated with the keyboard device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getKeyCode()()` Retrieve the key code of the key event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getKeyData(android.view.KeyCharacterMap.KeyData)(results: https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.KeyData!)` Get the character conversion data for a given key code. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMatch(kotlin.CharArray)(chars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Gets the first character in the character array that can be generated by the specified key code. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMatch(kotlin.CharArray,%20kotlin.Int)(chars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the first character in the character array that can be generated by the specified key code. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMaxKeyCode()()` Returns the maximum keycode. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()()` Returns the state of the meta keys. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifierMetaStateMask()()` Gets a mask that includes all valid modifier key meta state bits. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifiers()()` Returns the state of the modifier keys. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getNumber()()` Gets the number or symbol associated with the key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getRepeatCount()()` Retrieve the repeat count of the event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getScanCode()()` Retrieve the hardware key id of this key event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getSource()()` Gets the source of the event. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getUnicodeChar()()` Gets the Unicode character generated by the specified key and meta key state combination. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getUnicodeChar(kotlin.Int)(metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the Unicode character generated by the specified key and meta key state combination. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#hasModifiers(kotlin.Int)(modifiers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if only the specified modifiers keys are pressed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#hasNoModifiers()()` Returns true if no modifier keys are pressed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isAltPressed()()` Returns the pressed state of the ALT meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCanceled()()` For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` events, indicates that the event has been canceled as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCapsLockOn()()` Returns the locked state of the CAPS LOCK meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCtrlPressed()()` Returns the pressed state of the CTRL meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isFunctionPressed()()` Returns the pressed state of the FUNCTION meta key. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isGamepadButton(kotlin.Int)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the specified keycode is a gamepad button. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isLongPress()()` For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` events, indicates that the event has been canceled as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_LONG_PRESS:kotlin.Int`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMediaSessionKey(kotlin.Int)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether this key will be sent to the `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback.html#` if not handled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMetaPressed()()` Returns the pressed state of the META meta key. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isModifierKey(kotlin.Int)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if this key code is a modifier key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isNumLockOn()()` Returns the locked state of the NUM LOCK meta key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isPrintingKey()()` Returns true if this key produces a glyph. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isScrollLockOn()()` Returns the locked state of the SCROLL LOCK meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isShiftPressed()()` Returns the pressed state of the SHIFT meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isSymPressed()()` Returns the pressed state of the SYM meta key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isSystem()()` Is this a system key? System keys can not be used for menu shortcuts. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isTracking()()` For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` events, indicates that the event is still being tracked from its initial down event as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_TRACKING:kotlin.Int`. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#keyCodeFromString(kotlin.String)(symbolicName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets a keycode by its symbolic name such as "KEYCODE_A" or an equivalent numeric constant such as "29". |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#keyCodeToString(kotlin.Int)(keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string that represents the symbolic name of the specified keycode such as "KEYCODE_A", "KEYCODE_DPAD_UP", or an equivalent numeric constant such as "1001" if unknown. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#metaStateHasModifiers(kotlin.Int,%20kotlin.Int)(metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modifiers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if only the specified modifier keys are pressed according to the specified meta state. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#metaStateHasNoModifiers(kotlin.Int)(metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if no modifiers keys are pressed according to the specified meta state. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#normalizeMetaState(kotlin.Int)(metaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Normalizes the specified meta state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#setSource(kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#startTracking()()` Call this during `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` to have the system track the key through its final up (possibly including a long press). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/view/InputEvent` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/InputEvent#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit. <br /> | | `https://developer.android.com/reference/kotlin/android/view/InputDevice!` | `https://developer.android.com/reference/kotlin/android/view/InputEvent#getDevice()()` Gets the device that this event came from. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/view/InputEvent#isFromSource(kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines whether the event is from the given source. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!\> | `https://developer.android.com/reference/kotlin/android/view/KeyEvent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACTION_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DOWN: Int
```

`https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()` value: the key has been pressed down.

 Value: 0

### ACTION_MULTIPLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MULTIPLE: Int
```

**Deprecated:** *No longer used by the input system. `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()` value: multiple duplicate key events have occurred in a row, or a complex string is being delivered. If the key code is not `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int` then the `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getRepeatCount()` method returns the number of times the given key code should be executed. Otherwise, if the key code is `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int`, then this is a sequence of characters as returned by `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getCharacters()`.*

 Value: 2

### ACTION_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_UP: Int
```

`https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()` value: the key has been released.

 Value: 1

### FLAG_CANCELED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CANCELED: Int
```

When associated with up key events, this indicates that the key press has been canceled. Typically this is used with virtual touch screen keys, where the user can slide from the virtual key area on to the display: in that case, the application will receive a canceled up event and should not perform the action normally associated with the key. Note that for this to work, the application can not perform an action for a key until it receives an up or the long press timeout has expired.

 Value: 32

### FLAG_CANCELED_LONG_PRESS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CANCELED_LONG_PRESS: Int
```

Set when a key event has `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int` set because a long press action was executed while it was down.

 Value: 256

### FLAG_EDITOR_ACTION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_EDITOR_ACTION: Int
```

This mask is used for compatibility, to identify enter keys that are coming from an IME whose enter key has been auto-labelled "next" or "done". This allows TextView to dispatch these as normal enter keys for old applications, but still do the appropriate action when receiving them.

 Value: 16

### FLAG_FALLBACK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FALLBACK: Int
```

Set when a key event has been synthesized to implement default behavior for an event that the application did not handle. Fallback key events are generated by unhandled trackball motions (to emulate a directional keypad) and by certain unhandled key presses that are declared in the key map (such as special function numeric keypad keys when numlock is off).

 Value: 1024

### FLAG_FROM_SYSTEM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FROM_SYSTEM: Int
```

This mask is set if an event was known to come from a trusted part of the system. That is, the event is known to come from the user, and could not have been spoofed by a third party component.

 Value: 8

### FLAG_KEEP_TOUCH_MODE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_KEEP_TOUCH_MODE: Int
```

This mask is set if we don't want the key event to cause us to leave touch mode.

 Value: 4

### FLAG_LONG_PRESS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LONG_PRESS: Int
```

This flag is set for the first key repeat that occurs after the long press timeout.

 Value: 128

### FLAG_SOFT_KEYBOARD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SOFT_KEYBOARD: Int
```

This mask is set if the key event was generated by a software keyboard.

 Value: 2

### FLAG_TRACKING

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_TRACKING: Int
```

Set for `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` when this event's key code is still being tracked from its initial down. That is, somebody requested that tracking started on the key down and a long press has not caused the tracking to be canceled.

 Value: 512

### FLAG_VIRTUAL_HARD_KEY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_VIRTUAL_HARD_KEY: Int
```

This key event was generated by a virtual (on-screen) hard key area. Typically this is an area of the touchscreen, outside of the regular display, dedicated to "hardware" buttons.

 Value: 64

### FLAG_WOKE_HERE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_WOKE_HERE: Int
```

**Deprecated:** *This flag will never be set by the system since the system consumes all wake keys itself.*

This mask is set if the device woke because of this key event.

 Value: 1

### KEYCODE_0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_0: Int
```

Key code constant: '0' key.

 Value: 7

### KEYCODE_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_1: Int
```

Key code constant: '1' key.

 Value: 8

### KEYCODE_11

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_11: Int
```

Key code constant: '11' key.

 Value: 227

### KEYCODE_12

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_12: Int
```

Key code constant: '12' key.

 Value: 228

### KEYCODE_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_2: Int
```

Key code constant: '2' key.

 Value: 9

### KEYCODE_3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_3: Int
```

Key code constant: '3' key.

 Value: 10

### KEYCODE_3D_MODE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_3D_MODE: Int
```

Key code constant: 3D Mode key.

Toggles the display between 2D and 3D mode.

 Value: 206

### KEYCODE_4

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_4: Int
```

Key code constant: '4' key.

 Value: 11

### KEYCODE_5

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_5: Int
```

Key code constant: '5' key.

 Value: 12

### KEYCODE_6

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_6: Int
```

Key code constant: '6' key.

 Value: 13

### KEYCODE_7

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_7: Int
```

Key code constant: '7' key.

 Value: 14

### KEYCODE_8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_8: Int
```

Key code constant: '8' key.

 Value: 15

### KEYCODE_9

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_9: Int
```

Key code constant: '9' key.

 Value: 16

### KEYCODE_A

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_A: Int
```

Key code constant: 'A' key.

 Value: 29

### KEYCODE_ACCESSIBILITY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ACCESSIBILITY: Int
```

Key code constant: System Accessibility key.

Introduced by HUTRR116, toggles the system bound accessibility UI/command (i.e. invoke system-specific accessibility UI or user-customized accessibility feature). Some example usages could be to toggle Talkback or toggle display color inversion. Applications will not receive this keycode.

 Value: 338

### KEYCODE_ALL_APPS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ALL_APPS: Int
```

Key code constant: Show all apps.

 Value: 284

### KEYCODE_ALT_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ALT_LEFT: Int
```

Key code constant: Left Alt modifier key.

 Value: 57

### KEYCODE_ALT_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ALT_RIGHT: Int
```

Key code constant: Right Alt modifier key.

 Value: 58

### KEYCODE_APOSTROPHE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_APOSTROPHE: Int
```

Key code constant: ''' (apostrophe) key.

 Value: 75

### KEYCODE_APP_SWITCH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_APP_SWITCH: Int
```

Key code constant: App switch key.

Should bring up the application switcher dialog.

 Value: 187

### KEYCODE_ASSIST

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ASSIST: Int
```

Key code constant: Assist key.

Launches the global assist activity. Not delivered to applications.

 Value: 219

### KEYCODE_AT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_AT: Int
```

Key code constant: '@' key.

 Value: 77

### KEYCODE_AVR_INPUT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_AVR_INPUT: Int
```

Key code constant: A/V Receiver input key.

On TV remotes, switches the input mode on an external A/V Receiver.

 Value: 182

### KEYCODE_AVR_POWER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_AVR_POWER: Int
```

Key code constant: A/V Receiver power key.

On TV remotes, toggles the power on an external A/V Receiver.

 Value: 181

### KEYCODE_B

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_B: Int
```

Key code constant: 'B' key.

 Value: 30

### KEYCODE_BACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BACK: Int
```

Key code constant: Back key.

 Value: 4

### KEYCODE_BACKSLASH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BACKSLASH: Int
```

Key code constant: '\\' key.

 Value: 73

### KEYCODE_BOOKMARK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BOOKMARK: Int
```

Key code constant: Bookmark key.

On some TV remotes, bookmarks content or web pages.

 Value: 174

### KEYCODE_BREAK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BREAK: Int
```

Key code constant: Break / Pause key.

 Value: 121

### KEYCODE_BRIGHTNESS_DOWN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BRIGHTNESS_DOWN: Int
```

Key code constant: Brightness Down key.

Adjusts the screen brightness down.

 Value: 220

### KEYCODE_BRIGHTNESS_UP

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BRIGHTNESS_UP: Int
```

Key code constant: Brightness Up key.

Adjusts the screen brightness up.

 Value: 221

### KEYCODE_BUTTON_1

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_1: Int
```

Key code constant: Generic Game Pad Button #1.

 Value: 188

### KEYCODE_BUTTON_10

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_10: Int
```

Key code constant: Generic Game Pad Button #10.

 Value: 197

### KEYCODE_BUTTON_11

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_11: Int
```

Key code constant: Generic Game Pad Button #11.

 Value: 198

### KEYCODE_BUTTON_12

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_12: Int
```

Key code constant: Generic Game Pad Button #12.

 Value: 199

### KEYCODE_BUTTON_13

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_13: Int
```

Key code constant: Generic Game Pad Button #13.

 Value: 200

### KEYCODE_BUTTON_14

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_14: Int
```

Key code constant: Generic Game Pad Button #14.

 Value: 201

### KEYCODE_BUTTON_15

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_15: Int
```

Key code constant: Generic Game Pad Button #15.

 Value: 202

### KEYCODE_BUTTON_16

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_16: Int
```

Key code constant: Generic Game Pad Button #16.

 Value: 203

### KEYCODE_BUTTON_2

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_2: Int
```

Key code constant: Generic Game Pad Button #2.

 Value: 189

### KEYCODE_BUTTON_3

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_3: Int
```

Key code constant: Generic Game Pad Button #3.

 Value: 190

### KEYCODE_BUTTON_4

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_4: Int
```

Key code constant: Generic Game Pad Button #4.

 Value: 191

### KEYCODE_BUTTON_5

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_5: Int
```

Key code constant: Generic Game Pad Button #5.

 Value: 192

### KEYCODE_BUTTON_6

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_6: Int
```

Key code constant: Generic Game Pad Button #6.

 Value: 193

### KEYCODE_BUTTON_7

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_7: Int
```

Key code constant: Generic Game Pad Button #7.

 Value: 194

### KEYCODE_BUTTON_8

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_8: Int
```

Key code constant: Generic Game Pad Button #8.

 Value: 195

### KEYCODE_BUTTON_9

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_9: Int
```

Key code constant: Generic Game Pad Button #9.

 Value: 196

### KEYCODE_BUTTON_A

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_A: Int
```

Key code constant: A Button key.

On a game controller, the A button should be either the button labeled A or the first button on the bottom row of controller buttons.

 Value: 96

### KEYCODE_BUTTON_B

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_B: Int
```

Key code constant: B Button key.

On a game controller, the B button should be either the button labeled B or the second button on the bottom row of controller buttons.

 Value: 97

### KEYCODE_BUTTON_C

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_C: Int
```

Key code constant: C Button key.

On a game controller, the C button should be either the button labeled C or the third button on the bottom row of controller buttons.

 Value: 98

### KEYCODE_BUTTON_L1

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_L1: Int
```

Key code constant: L1 Button key.

On a game controller, the L1 button should be either the button labeled L1 (or L) or the top left trigger button.

 Value: 102

### KEYCODE_BUTTON_L2

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_L2: Int
```

Key code constant: L2 Button key.

On a game controller, the L2 button should be either the button labeled L2 or the bottom left trigger button.

 Value: 104

### KEYCODE_BUTTON_MODE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_MODE: Int
```

Key code constant: Mode Button key.

On a game controller, the button labeled Mode.

 Value: 110

### KEYCODE_BUTTON_R1

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_R1: Int
```

Key code constant: R1 Button key.

On a game controller, the R1 button should be either the button labeled R1 (or R) or the top right trigger button.

 Value: 103

### KEYCODE_BUTTON_R2

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_R2: Int
```

Key code constant: R2 Button key.

On a game controller, the R2 button should be either the button labeled R2 or the bottom right trigger button.

 Value: 105

### KEYCODE_BUTTON_SELECT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_SELECT: Int
```

Key code constant: Select Button key.

On a game controller, the button labeled Select.

 Value: 109

### KEYCODE_BUTTON_START

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_START: Int
```

Key code constant: Start Button key.

On a game controller, the button labeled Start.

 Value: 108

### KEYCODE_BUTTON_THUMBL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_THUMBL: Int
```

Key code constant: Left Thumb Button key.

On a game controller, the left thumb button indicates that the left (or only) joystick is pressed.

 Value: 106

### KEYCODE_BUTTON_THUMBR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_THUMBR: Int
```

Key code constant: Right Thumb Button key.

On a game controller, the right thumb button indicates that the right joystick is pressed.

 Value: 107

### KEYCODE_BUTTON_X

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_X: Int
```

Key code constant: X Button key.

On a game controller, the X button should be either the button labeled X or the first button on the upper row of controller buttons.

 Value: 99

### KEYCODE_BUTTON_Y

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_Y: Int
```

Key code constant: Y Button key.

On a game controller, the Y button should be either the button labeled Y or the second button on the upper row of controller buttons.

 Value: 100

### KEYCODE_BUTTON_Z

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_BUTTON_Z: Int
```

Key code constant: Z Button key.

On a game controller, the Z button should be either the button labeled Z or the third button on the upper row of controller buttons.

 Value: 101

### KEYCODE_C

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_C: Int
```

Key code constant: 'C' key.

 Value: 31

### KEYCODE_CALCULATOR

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CALCULATOR: Int
```

Key code constant: Calculator special function key.

Used to launch a calculator application.

 Value: 210

### KEYCODE_CALENDAR

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CALENDAR: Int
```

Key code constant: Calendar special function key.

Used to launch a calendar application.

 Value: 208

### KEYCODE_CALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CALL: Int
```

Key code constant: Call key.

 Value: 5

### KEYCODE_CAMERA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CAMERA: Int
```

Key code constant: Camera key.

Used to launch a camera application or take pictures.

 Value: 27

### KEYCODE_CAPS_LOCK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CAPS_LOCK: Int
```

Key code constant: Caps Lock key.

 Value: 115

### KEYCODE_CAPTIONS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CAPTIONS: Int
```

Key code constant: Toggle captions key.

Switches the mode for closed-captioning text, for example during television shows.

 Value: 175

### KEYCODE_CHANNEL_DOWN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CHANNEL_DOWN: Int
```

Key code constant: Channel down key.

On TV remotes, decrements the television channel.

 Value: 167

### KEYCODE_CHANNEL_UP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CHANNEL_UP: Int
```

Key code constant: Channel up key.

On TV remotes, increments the television channel.

 Value: 166

### KEYCODE_CLEAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CLEAR: Int
```

Key code constant: Clear key.

 Value: 28

### KEYCODE_CLOSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CLOSE: Int
```

Key code constant: AC Close.

e.g. To close current instance of the application window, close the current tab, etc.

 Value: 321

### KEYCODE_COMMA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_COMMA: Int
```

Key code constant: ',' key.

 Value: 55

### KEYCODE_CONTACTS

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CONTACTS: Int
```

Key code constant: Contacts special function key.

Used to launch an address book application.

 Value: 207

### KEYCODE_CONTEXTUAL_INSERT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CONTEXTUAL_INSERT: Int
```

Key code constant: Contextual Insert key.

Introduced by HUTRR119, triggers a contextual overlay that enables the user to search, retrieve, and generate content for immediate insertion into the active focused element.

 Value: 340

### KEYCODE_CONTEXTUAL_QUERY

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CONTEXTUAL_QUERY: Int
```

Key code constant: Contextual Query key.

Introduced by HUTRR119, triggers contextual suggestions on active or hovered screen elements (e.g. an image or a paragraph) to discover available actions.

 Value: 341

### KEYCODE_CONTEXTUAL_SEARCH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CONTEXTUAL_SEARCH: Int
```

Key code constant: Contextual Search key.

Introduced by HUTRR119, invokes an AI agent to perform an action on the content currently selected by the user (e.g., highlighted text, active image, or selected file) or invoke a selection experience. Often referred to as "Select to Search" or "Summarize Selection." This key is fully handled by the framework and will not be sent to the foreground app.

 Value: 339

### KEYCODE_COPY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_COPY: Int
```

Key code constant: Copy key.

 Value: 278

### KEYCODE_CTRL_LEFT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CTRL_LEFT: Int
```

Key code constant: Left Control modifier key.

 Value: 113

### KEYCODE_CTRL_RIGHT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CTRL_RIGHT: Int
```

Key code constant: Right Control modifier key.

 Value: 114

### KEYCODE_CUT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_CUT: Int
```

Key code constant: Cut key.

 Value: 277

### KEYCODE_D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_D: Int
```

Key code constant: 'D' key.

 Value: 32

### KEYCODE_DEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DEL: Int
```

Key code constant: Backspace key.

Deletes characters before the insertion point, unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FORWARD_DEL:kotlin.Int`.

 Value: 67

### KEYCODE_DEMO_APP_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DEMO_APP_1: Int
```

Key code constant: Demo Application key #1.

 Value: 301

### KEYCODE_DEMO_APP_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DEMO_APP_2: Int
```

Key code constant: Demo Application key #2.

 Value: 302

### KEYCODE_DEMO_APP_3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DEMO_APP_3: Int
```

Key code constant: Demo Application key #3.

 Value: 303

### KEYCODE_DEMO_APP_4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DEMO_APP_4: Int
```

Key code constant: Demo Application key #4.

 Value: 304

### KEYCODE_DICTATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DICTATE: Int
```

Key code constant: To start dictate to an input field

 Value: 319

### KEYCODE_DO_NOT_DISTURB

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DO_NOT_DISTURB: Int
```

Key code constant: To toggle 'Do Not Disturb' mode.

 Value: 322

### KEYCODE_DPAD_CENTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_CENTER: Int
```

Key code constant: Directional Pad Center key.

May also be synthesized from trackball motions.

 Value: 23

### KEYCODE_DPAD_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_DOWN: Int
```

Key code constant: Directional Pad Down key.

May also be synthesized from trackball motions.

 Value: 20

### KEYCODE_DPAD_DOWN_LEFT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_DOWN_LEFT: Int
```

Key code constant: Directional Pad Down-Left.

 Value: 269

### KEYCODE_DPAD_DOWN_RIGHT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_DOWN_RIGHT: Int
```

Key code constant: Directional Pad Down-Right.

 Value: 271

### KEYCODE_DPAD_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_LEFT: Int
```

Key code constant: Directional Pad Left key.

May also be synthesized from trackball motions.

 Value: 21

### KEYCODE_DPAD_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_RIGHT: Int
```

Key code constant: Directional Pad Right key.

May also be synthesized from trackball motions.

 Value: 22

### KEYCODE_DPAD_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_UP: Int
```

Key code constant: Directional Pad Up key.

May also be synthesized from trackball motions.

 Value: 19

### KEYCODE_DPAD_UP_LEFT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_UP_LEFT: Int
```

Key code constant: Directional Pad Up-Left.

 Value: 268

### KEYCODE_DPAD_UP_RIGHT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DPAD_UP_RIGHT: Int
```

Key code constant: Directional Pad Up-Right.

 Value: 270

### KEYCODE_DVR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_DVR: Int
```

Key code constant: DVR key.

On some TV remotes, switches to a DVR mode for recorded shows.

 Value: 173

### KEYCODE_E

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_E: Int
```

Key code constant: 'E' key.

 Value: 33

### KEYCODE_EISU

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_EISU: Int
```

Key code constant: Japanese alphanumeric key.

 Value: 212

### KEYCODE_EMOJI_PICKER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_EMOJI_PICKER: Int
```

Key code constant: To open emoji picker.

 Value: 317

### KEYCODE_ENDCALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ENDCALL: Int
```

Key code constant: End Call key.

 Value: 6

### KEYCODE_ENTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ENTER: Int
```

Key code constant: Enter key.

 Value: 66

### KEYCODE_ENVELOPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ENVELOPE: Int
```

Key code constant: Envelope special function key.

Used to launch a mail application.

 Value: 65

### KEYCODE_EQUALS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_EQUALS: Int
```

Key code constant: '=' key.

 Value: 70

### KEYCODE_ESCAPE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ESCAPE: Int
```

Key code constant: Escape key.

 Value: 111

### KEYCODE_EXPLORER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_EXPLORER: Int
```

Key code constant: Explorer special function key.

Used to launch a browser application.

 Value: 64

### KEYCODE_F

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F: Int
```

Key code constant: 'F' key.

 Value: 34

### KEYCODE_F1

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F1: Int
```

Key code constant: F1 key.

 Value: 131

### KEYCODE_F10

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F10: Int
```

Key code constant: F10 key.

 Value: 140

### KEYCODE_F11

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F11: Int
```

Key code constant: F11 key.

 Value: 141

### KEYCODE_F12

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F12: Int
```

Key code constant: F12 key.

 Value: 142

### KEYCODE_F13

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F13: Int
```

Key code constant: F13 key.

 Value: 326

### KEYCODE_F14

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F14: Int
```

Key code constant: F14 key.

 Value: 327

### KEYCODE_F15

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F15: Int
```

Key code constant: F15 key.

 Value: 328

### KEYCODE_F16

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F16: Int
```

Key code constant: F16 key.

 Value: 329

### KEYCODE_F17

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F17: Int
```

Key code constant: F17 key.

 Value: 330

### KEYCODE_F18

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F18: Int
```

Key code constant: F18 key.

 Value: 331

### KEYCODE_F19

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F19: Int
```

Key code constant: F19 key.

 Value: 332

### KEYCODE_F2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F2: Int
```

Key code constant: F2 key.

 Value: 132

### KEYCODE_F20

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F20: Int
```

Key code constant: F20 key.

 Value: 333

### KEYCODE_F21

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F21: Int
```

Key code constant: F21 key.

 Value: 334

### KEYCODE_F22

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F22: Int
```

Key code constant: F22 key.

 Value: 335

### KEYCODE_F23

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F23: Int
```

Key code constant: F23 key.

 Value: 336

### KEYCODE_F24

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F24: Int
```

Key code constant: F24 key.

 Value: 337

### KEYCODE_F3

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F3: Int
```

Key code constant: F3 key.

 Value: 133

### KEYCODE_F4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F4: Int
```

Key code constant: F4 key.

 Value: 134

### KEYCODE_F5

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F5: Int
```

Key code constant: F5 key.

 Value: 135

### KEYCODE_F6

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F6: Int
```

Key code constant: F6 key.

 Value: 136

### KEYCODE_F7

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F7: Int
```

Key code constant: F7 key.

 Value: 137

### KEYCODE_F8

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F8: Int
```

Key code constant: F8 key.

 Value: 138

### KEYCODE_F9

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_F9: Int
```

Key code constant: F9 key.

 Value: 139

### KEYCODE_FEATURED_APP_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FEATURED_APP_1: Int
```

Key code constant: Featured Application key #1.

 Value: 297

### KEYCODE_FEATURED_APP_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FEATURED_APP_2: Int
```

Key code constant: Featured Application key #2.

 Value: 298

### KEYCODE_FEATURED_APP_3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FEATURED_APP_3: Int
```

Key code constant: Featured Application key #3.

 Value: 299

### KEYCODE_FEATURED_APP_4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FEATURED_APP_4: Int
```

Key code constant: Featured Application key #4.

 Value: 300

### KEYCODE_FOCUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FOCUS: Int
```

Key code constant: Camera Focus key.

Used to focus the camera.

 Value: 80

### KEYCODE_FORWARD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FORWARD: Int
```

Key code constant: Forward key.

Navigates forward in the history stack. Complement of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BACK:kotlin.Int`.

 Value: 125

### KEYCODE_FORWARD_DEL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FORWARD_DEL: Int
```

Key code constant: Forward Delete key.

Deletes characters ahead of the insertion point, unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_DEL:kotlin.Int`.

 Value: 112

### KEYCODE_FULLSCREEN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FULLSCREEN: Int
```

Key code constant: To toggle fullscreen mode (on the current application).

 Value: 325

### KEYCODE_FUNCTION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_FUNCTION: Int
```

Key code constant: Function modifier key.

 Value: 119

### KEYCODE_G

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_G: Int
```

Key code constant: 'G' key.

 Value: 35

### KEYCODE_GRAVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_GRAVE: Int
```

Key code constant: '\`' (backtick) key.

 Value: 68

### KEYCODE_GUIDE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_GUIDE: Int
```

Key code constant: Guide key.

On TV remotes, shows a programming guide.

 Value: 172

### KEYCODE_H

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_H: Int
```

Key code constant: 'H' key.

 Value: 36

### KEYCODE_HEADSETHOOK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_HEADSETHOOK: Int
```

Key code constant: Headset Hook key.

Used to hang up calls and stop media.

 Value: 79

### KEYCODE_HELP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_HELP: Int
```

Key code constant: Help key.

 Value: 259

### KEYCODE_HENKAN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_HENKAN: Int
```

Key code constant: Japanese conversion key.

 Value: 214

### KEYCODE_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_HOME: Int
```

Key code constant: Home key.

This key is handled by the framework and is never delivered to applications.

 Value: 3

### KEYCODE_I

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_I: Int
```

Key code constant: 'I' key.

 Value: 37

### KEYCODE_INFO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_INFO: Int
```

Key code constant: Info key.

Common on TV remotes to show additional information related to what is currently being viewed.

 Value: 165

### KEYCODE_INSERT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_INSERT: Int
```

Key code constant: Insert key.

Toggles insert / overwrite edit mode.

 Value: 124

### KEYCODE_J

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_J: Int
```

Key code constant: 'J' key.

 Value: 38

### KEYCODE_K

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_K: Int
```

Key code constant: 'K' key.

 Value: 39

### KEYCODE_KANA

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_KANA: Int
```

Key code constant: Japanese kana key.

 Value: 218

### KEYCODE_KATAKANA_HIRAGANA

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_KATAKANA_HIRAGANA: Int
```

Key code constant: Japanese katakana / hiragana key.

 Value: 215

### KEYCODE_KEYBOARD_BACKLIGHT_DOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_KEYBOARD_BACKLIGHT_DOWN: Int
```

Key code constant: Keyboard backlight down.

 Value: 305

### KEYCODE_KEYBOARD_BACKLIGHT_TOGGLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_KEYBOARD_BACKLIGHT_TOGGLE: Int
```

Key code constant: Keyboard backlight toggle.

 Value: 307

### KEYCODE_KEYBOARD_BACKLIGHT_UP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_KEYBOARD_BACKLIGHT_UP: Int
```

Key code constant: Keyboard backlight up.

 Value: 306

### KEYCODE_L

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_L: Int
```

Key code constant: 'L' key.

 Value: 40

### KEYCODE_LANGUAGE_SWITCH

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_LANGUAGE_SWITCH: Int
```

Key code constant: Language Switch key.

Toggles the current input language such as switching between English and Japanese on a QWERTY keyboard. On some devices, the same function may be performed by pressing Shift + Spacebar.

 Value: 204

### KEYCODE_LAST_CHANNEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_LAST_CHANNEL: Int
```

Key code constant: Last Channel key.

Goes to the last viewed channel.

 Value: 229

### KEYCODE_LEFT_BRACKET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_LEFT_BRACKET: Int
```

Key code constant: '\[' key.

 Value: 71

### KEYCODE_LOCK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_LOCK: Int
```

Key code constant: To lock the screen.

 Value: 324

### KEYCODE_M

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_M: Int
```

Key code constant: 'M' key.

 Value: 41

### KEYCODE_MACRO_1

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MACRO_1: Int
```

Key code constant: A button whose usage can be customized by the user through the system.

User customizable key #1.

 Value: 313

### KEYCODE_MACRO_2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MACRO_2: Int
```

Key code constant: A button whose usage can be customized by the user through the system.

User customizable key #2.

 Value: 314

### KEYCODE_MACRO_3

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MACRO_3: Int
```

Key code constant: A button whose usage can be customized by the user through the system.

User customizable key #3.

 Value: 315

### KEYCODE_MACRO_4

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MACRO_4: Int
```

Key code constant: A button whose usage can be customized by the user through the system.

User customizable key #4.

 Value: 316

### KEYCODE_MANNER_MODE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MANNER_MODE: Int
```

Key code constant: Manner Mode key.

Toggles silent or vibrate mode on and off to make the device behave more politely in certain settings such as on a crowded train. On some devices, the key may only operate when long-pressed.

 Value: 205

### KEYCODE_MEDIA_AUDIO_TRACK

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_AUDIO_TRACK: Int
```

Key code constant: Audio Track key.

Switches the audio tracks.

 Value: 222

### KEYCODE_MEDIA_CLOSE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_CLOSE: Int
```

Key code constant: Close media key.

May be used to close a CD tray, for example.

 Value: 128

### KEYCODE_MEDIA_EJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_EJECT: Int
```

Key code constant: Eject media key.

May be used to eject a CD tray, for example.

 Value: 129

### KEYCODE_MEDIA_FAST_FORWARD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_FAST_FORWARD: Int
```

Key code constant: Fast Forward media key.

 Value: 90

### KEYCODE_MEDIA_NEXT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_NEXT: Int
```

Key code constant: Play Next media key.

 Value: 87

### KEYCODE_MEDIA_PAUSE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_PAUSE: Int
```

Key code constant: Pause media key.

 Value: 127

### KEYCODE_MEDIA_PLAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_PLAY: Int
```

Key code constant: Play media key.

 Value: 126

### KEYCODE_MEDIA_PLAY_PAUSE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_PLAY_PAUSE: Int
```

Key code constant: Play/Pause media key.

 Value: 85

### KEYCODE_MEDIA_PREVIOUS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_PREVIOUS: Int
```

Key code constant: Play Previous media key.

 Value: 88

### KEYCODE_MEDIA_RECORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_RECORD: Int
```

Key code constant: Record media key.

 Value: 130

### KEYCODE_MEDIA_REWIND

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_REWIND: Int
```

Key code constant: Rewind media key.

 Value: 89

### KEYCODE_MEDIA_SKIP_BACKWARD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_SKIP_BACKWARD: Int
```

Key code constant: Skip backward media key.

 Value: 273

### KEYCODE_MEDIA_SKIP_FORWARD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_SKIP_FORWARD: Int
```

Key code constant: Skip forward media key.

 Value: 272

### KEYCODE_MEDIA_STEP_BACKWARD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_STEP_BACKWARD: Int
```

Key code constant: Step backward media key.

Steps media backward, one frame at a time.

 Value: 275

### KEYCODE_MEDIA_STEP_FORWARD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_STEP_FORWARD: Int
```

Key code constant: Step forward media key.

Steps media forward, one frame at a time.

 Value: 274

### KEYCODE_MEDIA_STOP

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_STOP: Int
```

Key code constant: Stop media key.

 Value: 86

### KEYCODE_MEDIA_TOP_MENU

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MEDIA_TOP_MENU: Int
```

Key code constant: Media Top Menu key.

Goes to the top of media menu.

 Value: 226

### KEYCODE_MENU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MENU: Int
```

Key code constant: Menu key.

 Value: 82

### KEYCODE_META_LEFT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_META_LEFT: Int
```

Key code constant: Left Meta modifier key.

 Value: 117

### KEYCODE_META_RIGHT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_META_RIGHT: Int
```

Key code constant: Right Meta modifier key.

 Value: 118

### KEYCODE_MINUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MINUS: Int
```

Key code constant: '-'.

 Value: 69

### KEYCODE_MOVE_END

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MOVE_END: Int
```

Key code constant: End Movement key.

Used for scrolling or moving the cursor around to the end of a line or to the bottom of a list.

 Value: 123

### KEYCODE_MOVE_HOME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MOVE_HOME: Int
```

Key code constant: Home Movement key.

Used for scrolling or moving the cursor around to the start of a line or to the top of a list.

 Value: 122

### KEYCODE_MUHENKAN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MUHENKAN: Int
```

Key code constant: Japanese non-conversion key.

 Value: 213

### KEYCODE_MUSIC

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MUSIC: Int
```

Key code constant: Music special function key.

Used to launch a music player application.

 Value: 209

### KEYCODE_MUTE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_MUTE: Int
```

Key code constant: Mute key.

Mute key for the microphone (unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_VOLUME_MUTE:kotlin.Int`, which is the speaker mute key).

 Value: 91

### KEYCODE_N

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_N: Int
```

Key code constant: 'N' key.

 Value: 42

### KEYCODE_NAVIGATE_IN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NAVIGATE_IN: Int
```

Key code constant: Navigate in key.

Activates the item that currently has focus or expands to the next level of a navigation hierarchy.

 Value: 262

### KEYCODE_NAVIGATE_NEXT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NAVIGATE_NEXT: Int
```

Key code constant: Navigate to next key.

Advances to the next item in an ordered collection of items.

 Value: 261

### KEYCODE_NAVIGATE_OUT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NAVIGATE_OUT: Int
```

Key code constant: Navigate out key.

Backs out one level of a navigation hierarchy or collapses the item that currently has focus.

 Value: 263

### KEYCODE_NAVIGATE_PREVIOUS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NAVIGATE_PREVIOUS: Int
```

Key code constant: Navigate to previous key.

Goes backward by one item in an ordered collection of items.

 Value: 260

### KEYCODE_NEW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NEW: Int
```

Key code constant: AC New.

e.g. To create a new instance of a window, open a new tab, etc.

 Value: 320

### KEYCODE_NOTIFICATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NOTIFICATION: Int
```

Key code constant: Notification key.

 Value: 83

### KEYCODE_NUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUM: Int
```

Key code constant: Number modifier key.

Used to enter numeric symbols. This key is not Num Lock; it is more like `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int` and is interpreted as an ALT key by `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#`.

 Value: 78

### KEYCODE_NUMPAD_0

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_0: Int
```

Key code constant: Numeric keypad '0' key.

 Value: 144

### KEYCODE_NUMPAD_1

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_1: Int
```

Key code constant: Numeric keypad '1' key.

 Value: 145

### KEYCODE_NUMPAD_2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_2: Int
```

Key code constant: Numeric keypad '2' key.

 Value: 146

### KEYCODE_NUMPAD_3

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_3: Int
```

Key code constant: Numeric keypad '3' key.

 Value: 147

### KEYCODE_NUMPAD_4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_4: Int
```

Key code constant: Numeric keypad '4' key.

 Value: 148

### KEYCODE_NUMPAD_5

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_5: Int
```

Key code constant: Numeric keypad '5' key.

 Value: 149

### KEYCODE_NUMPAD_6

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_6: Int
```

Key code constant: Numeric keypad '6' key.

 Value: 150

### KEYCODE_NUMPAD_7

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_7: Int
```

Key code constant: Numeric keypad '7' key.

 Value: 151

### KEYCODE_NUMPAD_8

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_8: Int
```

Key code constant: Numeric keypad '8' key.

 Value: 152

### KEYCODE_NUMPAD_9

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_9: Int
```

Key code constant: Numeric keypad '9' key.

 Value: 153

### KEYCODE_NUMPAD_ADD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_ADD: Int
```

Key code constant: Numeric keypad '+' key (for addition).

 Value: 157

### KEYCODE_NUMPAD_COMMA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_COMMA: Int
```

Key code constant: Numeric keypad ',' key (for decimals or digit grouping).

 Value: 159

### KEYCODE_NUMPAD_DIVIDE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_DIVIDE: Int
```

Key code constant: Numeric keypad '/' key (for division).

 Value: 154

### KEYCODE_NUMPAD_DOT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_DOT: Int
```

Key code constant: Numeric keypad '.' key (for decimals or digit grouping).

 Value: 158

### KEYCODE_NUMPAD_ENTER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_ENTER: Int
```

Key code constant: Numeric keypad Enter key.

 Value: 160

### KEYCODE_NUMPAD_EQUALS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_EQUALS: Int
```

Key code constant: Numeric keypad '=' key.

 Value: 161

### KEYCODE_NUMPAD_LEFT_PAREN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_LEFT_PAREN: Int
```

Key code constant: Numeric keypad '(' key.

 Value: 162

### KEYCODE_NUMPAD_MULTIPLY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_MULTIPLY: Int
```

Key code constant: Numeric keypad '\*' key (for multiplication).

 Value: 155

### KEYCODE_NUMPAD_RIGHT_PAREN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_RIGHT_PAREN: Int
```

Key code constant: Numeric keypad ')' key.

 Value: 163

### KEYCODE_NUMPAD_SUBTRACT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUMPAD_SUBTRACT: Int
```

Key code constant: Numeric keypad '-' key (for subtraction).

 Value: 156

### KEYCODE_NUM_LOCK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_NUM_LOCK: Int
```

Key code constant: Num Lock key.

This is the Num Lock key; it is different from `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM:kotlin.Int`. This key alters the behavior of other keys on the numeric keypad.

 Value: 143

### KEYCODE_O

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_O: Int
```

Key code constant: 'O' key.

 Value: 43

### KEYCODE_P

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_P: Int
```

Key code constant: 'P' key.

 Value: 44

### KEYCODE_PAGE_DOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PAGE_DOWN: Int
```

Key code constant: Page Down key.

 Value: 93

### KEYCODE_PAGE_UP

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PAGE_UP: Int
```

Key code constant: Page Up key.

 Value: 92

### KEYCODE_PAIRING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PAIRING: Int
```

Key code constant: Pairing key.

Initiates peripheral pairing mode. Useful for pairing remote control devices or game controllers, especially if no other input mode is available.

 Value: 225

### KEYCODE_PASTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PASTE: Int
```

Key code constant: Paste key.

 Value: 279

### KEYCODE_PERIOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PERIOD: Int
```

Key code constant: '.' key.

 Value: 56

### KEYCODE_PICTSYMBOLS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PICTSYMBOLS: Int
```

Key code constant: Picture Symbols modifier key.

Used to switch symbol sets (Emoji, Kao-moji).

 Value: 94

### KEYCODE_PLUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PLUS: Int
```

Key code constant: '+' key.

 Value: 81

### KEYCODE_POUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_POUND: Int
```

Key code constant: '#' key.

 Value: 18

### KEYCODE_POWER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_POWER: Int
```

Key code constant: Power key.

 Value: 26

### KEYCODE_PRINT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PRINT: Int
```

Key code constant: To print.

 Value: 323

### KEYCODE_PROFILE_SWITCH

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PROFILE_SWITCH: Int
```

Key code constant: Used to switch current `https://developer.android.com/reference/kotlin/android/accounts/Account.html#` that is consuming content.

May be consumed by system to set account globally.

 Value: 288

### KEYCODE_PROG_BLUE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PROG_BLUE: Int
```

Key code constant: Blue "programmable" key.

On TV remotes, acts as a contextual/programmable key.

 Value: 186

### KEYCODE_PROG_GREEN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PROG_GREEN: Int
```

Key code constant: Green "programmable" key.

On TV remotes, acts as a contextual/programmable key.

 Value: 184

### KEYCODE_PROG_RED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PROG_RED: Int
```

Key code constant: Red "programmable" key.

On TV remotes, acts as a contextual/programmable key.

 Value: 183

### KEYCODE_PROG_YELLOW

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_PROG_YELLOW: Int
```

Key code constant: Yellow "programmable" key.

On TV remotes, acts as a contextual/programmable key.

 Value: 185

### KEYCODE_Q

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_Q: Int
```

Key code constant: 'Q' key.

 Value: 45

### KEYCODE_R

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_R: Int
```

Key code constant: 'R' key.

 Value: 46

### KEYCODE_RECENT_APPS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_RECENT_APPS: Int
```

Key code constant: To open recent apps view (a.k.a. Overview).

This key is handled by the framework and is never delivered to applications.

 Value: 312

### KEYCODE_REFRESH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_REFRESH: Int
```

Key code constant: Refresh key.

 Value: 285

### KEYCODE_RIGHT_BRACKET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_RIGHT_BRACKET: Int
```

Key code constant: '\]' key.

 Value: 72

### KEYCODE_RO

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_RO: Int
```

Key code constant: Japanese Ro key.

 Value: 217

### KEYCODE_S

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_S: Int
```

Key code constant: 'S' key.

 Value: 47

### KEYCODE_SCREENSHOT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SCREENSHOT: Int
```

Key code constant: To take a screenshot.

This key is fully handled by the framework and will not be sent to the foreground app, unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYSRQ:kotlin.Int` which is sent to the app first and only if the app doesn't handle it, the framework handles it (to take a screenshot).

 Value: 318

### KEYCODE_SCROLL_LOCK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SCROLL_LOCK: Int
```

Key code constant: Scroll Lock key.

 Value: 116

### KEYCODE_SEARCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SEARCH: Int
```

Key code constant: Search key.

 Value: 84

### KEYCODE_SEMICOLON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SEMICOLON: Int
```

Key code constant: ';' key.

 Value: 74

### KEYCODE_SETTINGS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SETTINGS: Int
```

Key code constant: Settings key.

Starts the system settings activity.

 Value: 176

### KEYCODE_SHIFT_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SHIFT_LEFT: Int
```

Key code constant: Left Shift modifier key.

 Value: 59

### KEYCODE_SHIFT_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SHIFT_RIGHT: Int
```

Key code constant: Right Shift modifier key.

 Value: 60

### KEYCODE_SLASH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SLASH: Int
```

Key code constant: '/' key.

 Value: 76

### KEYCODE_SLEEP

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SLEEP: Int
```

Key code constant: Sleep key.

Puts the device to sleep. Behaves somewhat like `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_POWER:kotlin.Int` but it has no effect if the device is already asleep.

 Value: 223

### KEYCODE_SOFT_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SOFT_LEFT: Int
```

Key code constant: Soft Left key.

Usually situated below the display on phones and used as a multi-function feature key for selecting a software defined function shown on the bottom left of the display.

 Value: 1

### KEYCODE_SOFT_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SOFT_RIGHT: Int
```

Key code constant: Soft Right key.

Usually situated below the display on phones and used as a multi-function feature key for selecting a software defined function shown on the bottom right of the display.

 Value: 2

### KEYCODE_SOFT_SLEEP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SOFT_SLEEP: Int
```

Key code constant: Put device to sleep unless a wakelock is held.

 Value: 276

### KEYCODE_SPACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SPACE: Int
```

Key code constant: Space key.

 Value: 62

### KEYCODE_STAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STAR: Int
```

Key code constant: '\*' key.

 Value: 17

### KEYCODE_STB_INPUT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STB_INPUT: Int
```

Key code constant: Set-top-box input key.

On TV remotes, switches the input mode on an external Set-top-box.

 Value: 180

### KEYCODE_STB_POWER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STB_POWER: Int
```

Key code constant: Set-top-box power key.

On TV remotes, toggles the power on an external Set-top-box.

 Value: 179

### KEYCODE_STEM_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STEM_1: Int
```

Key code constant: Generic stem key 1 for Wear.

 Value: 265

### KEYCODE_STEM_2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STEM_2: Int
```

Key code constant: Generic stem key 2 for Wear.

 Value: 266

### KEYCODE_STEM_3

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STEM_3: Int
```

Key code constant: Generic stem key 3 for Wear.

 Value: 267

### KEYCODE_STEM_PRIMARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STEM_PRIMARY: Int
```

Key code constant: Primary stem key for Wear.

Main power/reset button on watch.

 Value: 264

### KEYCODE_STYLUS_BUTTON_PRIMARY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STYLUS_BUTTON_PRIMARY: Int
```

Key code constant: The primary button on the barrel of a stylus.

This is usually the button closest to the tip of the stylus.

 Value: 308

### KEYCODE_STYLUS_BUTTON_SECONDARY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STYLUS_BUTTON_SECONDARY: Int
```

Key code constant: The secondary button on the barrel of a stylus.

This is usually the second button from the tip of the stylus.

 Value: 309

### KEYCODE_STYLUS_BUTTON_TAIL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STYLUS_BUTTON_TAIL: Int
```

Key code constant: A button on the tail end of a stylus.

The use of this button does not usually correspond to the function of an eraser.

 Value: 311

### KEYCODE_STYLUS_BUTTON_TERTIARY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_STYLUS_BUTTON_TERTIARY: Int
```

Key code constant: The tertiary button on the barrel of a stylus.

This is usually the third button from the tip of the stylus.

 Value: 310

### KEYCODE_SWITCH_CHARSET

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SWITCH_CHARSET: Int
```

Key code constant: Switch Charset modifier key.

Used to switch character sets (Kanji, Katakana).

 Value: 95

### KEYCODE_SYM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYM: Int
```

Key code constant: Symbol modifier key.

Used to enter alternate symbols.

 Value: 63

### KEYCODE_SYSRQ

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYSRQ: Int
```

Key code constant: System Request / Print Screen key.

This key is sent to the app first and only if the app doesn't handle it, the framework handles it (to take a screenshot), unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCREENSHOT:kotlin.Int` which is fully handled by the framework.

 Value: 120

### KEYCODE_SYSTEM_NAVIGATION_DOWN

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYSTEM_NAVIGATION_DOWN: Int
```

Key code constant: Consumed by the system for navigation down.

 Value: 281

### KEYCODE_SYSTEM_NAVIGATION_LEFT

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYSTEM_NAVIGATION_LEFT: Int
```

Key code constant: Consumed by the system for navigation left.

 Value: 282

### KEYCODE_SYSTEM_NAVIGATION_RIGHT

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYSTEM_NAVIGATION_RIGHT: Int
```

Key code constant: Consumed by the system for navigation right.

 Value: 283

### KEYCODE_SYSTEM_NAVIGATION_UP

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_SYSTEM_NAVIGATION_UP: Int
```

Key code constant: Consumed by the system for navigation up.

 Value: 280

### KEYCODE_T

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_T: Int
```

Key code constant: 'T' key.

 Value: 48

### KEYCODE_TAB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TAB: Int
```

Key code constant: Tab key.

 Value: 61

### KEYCODE_THUMBS_DOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_THUMBS_DOWN: Int
```

Key code constant: Thumbs down key.

Apps can use this to let user downvote content.

 Value: 287

### KEYCODE_THUMBS_UP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_THUMBS_UP: Int
```

Key code constant: Thumbs up key.

Apps can use this to let user upvote content.

 Value: 286

### KEYCODE_TV

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV: Int
```

Key code constant: TV key.

On TV remotes, switches to viewing live TV.

 Value: 170

### KEYCODE_TV_ANTENNA_CABLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_ANTENNA_CABLE: Int
```

Key code constant: Antenna/Cable key.

Toggles broadcast input source between antenna and cable.

 Value: 242

### KEYCODE_TV_AUDIO_DESCRIPTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_AUDIO_DESCRIPTION: Int
```

Key code constant: Audio description key.

Toggles audio description off / on.

 Value: 252

### KEYCODE_TV_AUDIO_DESCRIPTION_MIX_DOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_AUDIO_DESCRIPTION_MIX_DOWN: Int
```

Key code constant: Audio description mixing volume down key.

Lessen audio description volume as compared with normal audio volume.

 Value: 254

### KEYCODE_TV_AUDIO_DESCRIPTION_MIX_UP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_AUDIO_DESCRIPTION_MIX_UP: Int
```

Key code constant: Audio description mixing volume up key.

Louden audio description volume as compared with normal audio volume.

 Value: 253

### KEYCODE_TV_CONTENTS_MENU

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_CONTENTS_MENU: Int
```

Key code constant: Contents menu key.

Goes to the title list. Corresponds to Contents Menu (0x0B) of CEC User Control Code.

 Value: 256

### KEYCODE_TV_DATA_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_DATA_SERVICE: Int
```

Key code constant: TV data service key.

Displays data services like weather, sports.

 Value: 230

### KEYCODE_TV_INPUT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT: Int
```

Key code constant: TV input key.

On TV remotes, switches the input on a television screen.

 Value: 178

### KEYCODE_TV_INPUT_COMPONENT_1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_COMPONENT_1: Int
```

Key code constant: Component #1 key.

Switches to component video input #1.

 Value: 249

### KEYCODE_TV_INPUT_COMPONENT_2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_COMPONENT_2: Int
```

Key code constant: Component #2 key.

Switches to component video input #2.

 Value: 250

### KEYCODE_TV_INPUT_COMPOSITE_1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_COMPOSITE_1: Int
```

Key code constant: Composite #1 key.

Switches to composite video input #1.

 Value: 247

### KEYCODE_TV_INPUT_COMPOSITE_2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_COMPOSITE_2: Int
```

Key code constant: Composite #2 key.

Switches to composite video input #2.

 Value: 248

### KEYCODE_TV_INPUT_HDMI_1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_HDMI_1: Int
```

Key code constant: HDMI #1 key.

Switches to HDMI input #1.

 Value: 243

### KEYCODE_TV_INPUT_HDMI_2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_HDMI_2: Int
```

Key code constant: HDMI #2 key.

Switches to HDMI input #2.

 Value: 244

### KEYCODE_TV_INPUT_HDMI_3

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_HDMI_3: Int
```

Key code constant: HDMI #3 key.

Switches to HDMI input #3.

 Value: 245

### KEYCODE_TV_INPUT_HDMI_4

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_HDMI_4: Int
```

Key code constant: HDMI #4 key.

Switches to HDMI input #4.

 Value: 246

### KEYCODE_TV_INPUT_VGA_1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_INPUT_VGA_1: Int
```

Key code constant: VGA #1 key.

Switches to VGA (analog RGB) input #1.

 Value: 251

### KEYCODE_TV_MEDIA_CONTEXT_MENU

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_MEDIA_CONTEXT_MENU: Int
```

Key code constant: Media context menu key.

Goes to the context menu of media contents. Corresponds to Media Context-sensitive Menu (0x11) of CEC User Control Code.

 Value: 257

### KEYCODE_TV_NETWORK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_NETWORK: Int
```

Key code constant: Toggle Network key.

Toggles selecting broadcast services.

 Value: 241

### KEYCODE_TV_NUMBER_ENTRY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_NUMBER_ENTRY: Int
```

Key code constant: Number entry key.

Initiates to enter multi-digit channel number when each digit key is assigned for selecting a separate channel. Corresponds to Number Entry Mode (0x1D) of CEC User Control Code.

 Value: 234

### KEYCODE_TV_POWER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_POWER: Int
```

Key code constant: TV power key.

On HDMI TV panel devices and Android TV devices that don't support HDMI, toggles the power state of the device. On HDMI source devices, toggles the power state of the HDMI-connected TV via HDMI-CEC and makes the source device follow this power state.

 Value: 177

### KEYCODE_TV_RADIO_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_RADIO_SERVICE: Int
```

Key code constant: Radio key.

Toggles TV service / Radio service.

 Value: 232

### KEYCODE_TV_SATELLITE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_SATELLITE: Int
```

Key code constant: Satellite key.

Switches to digital satellite broadcast service.

 Value: 237

### KEYCODE_TV_SATELLITE_BS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_SATELLITE_BS: Int
```

Key code constant: BS key.

Switches to BS digital satellite broadcasting service available in Japan.

 Value: 238

### KEYCODE_TV_SATELLITE_CS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_SATELLITE_CS: Int
```

Key code constant: CS key.

Switches to CS digital satellite broadcasting service available in Japan.

 Value: 239

### KEYCODE_TV_SATELLITE_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_SATELLITE_SERVICE: Int
```

Key code constant: BS/CS key.

Toggles between BS and CS digital satellite services.

 Value: 240

### KEYCODE_TV_TELETEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_TELETEXT: Int
```

Key code constant: Teletext key.

Displays Teletext service.

 Value: 233

### KEYCODE_TV_TERRESTRIAL_ANALOG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_TERRESTRIAL_ANALOG: Int
```

Key code constant: Analog Terrestrial key.

Switches to analog terrestrial broadcast service.

 Value: 235

### KEYCODE_TV_TERRESTRIAL_DIGITAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_TERRESTRIAL_DIGITAL: Int
```

Key code constant: Digital Terrestrial key.

Switches to digital terrestrial broadcast service.

 Value: 236

### KEYCODE_TV_TIMER_PROGRAMMING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_TIMER_PROGRAMMING: Int
```

Key code constant: Timer programming key.

Goes to the timer recording menu. Corresponds to Timer Programming (0x54) of CEC User Control Code.

 Value: 258

### KEYCODE_TV_ZOOM_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_TV_ZOOM_MODE: Int
```

Key code constant: Zoom mode key.

Changes Zoom mode (Normal, Full, Zoom, Wide-zoom, etc.).

 Value: 255

### KEYCODE_U

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_U: Int
```

Key code constant: 'U' key.

 Value: 49

### KEYCODE_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_UNKNOWN: Int
```

Key code constant: Unknown key code.

 Value: 0

### KEYCODE_V

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_V: Int
```

Key code constant: 'V' key.

 Value: 50

### KEYCODE_VIDEO_APP_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_1: Int
```

Key code constant: Video Application key #1.

 Value: 289

### KEYCODE_VIDEO_APP_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_2: Int
```

Key code constant: Video Application key #2.

 Value: 290

### KEYCODE_VIDEO_APP_3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_3: Int
```

Key code constant: Video Application key #3.

 Value: 291

### KEYCODE_VIDEO_APP_4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_4: Int
```

Key code constant: Video Application key #4.

 Value: 292

### KEYCODE_VIDEO_APP_5

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_5: Int
```

Key code constant: Video Application key #5.

 Value: 293

### KEYCODE_VIDEO_APP_6

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_6: Int
```

Key code constant: Video Application key #6.

 Value: 294

### KEYCODE_VIDEO_APP_7

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_7: Int
```

Key code constant: Video Application key #7.

 Value: 295

### KEYCODE_VIDEO_APP_8

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VIDEO_APP_8: Int
```

Key code constant: Video Application key #8.

 Value: 296

### KEYCODE_VOICE_ASSIST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VOICE_ASSIST: Int
```

Key code constant: Voice Assist key.

Launches the global voice assist activity. Not delivered to applications.

 Value: 231

### KEYCODE_VOLUME_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VOLUME_DOWN: Int
```

Key code constant: Volume Down key.

Adjusts the speaker volume down.

 Value: 25

### KEYCODE_VOLUME_MUTE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VOLUME_MUTE: Int
```

Key code constant: Volume Mute key.

Mute key for speaker (unlike `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MUTE:kotlin.Int`, which is the mute key for the microphone). This key should normally be implemented as a toggle such that the first press mutes the speaker and the second press restores the original volume.

 Value: 164

### KEYCODE_VOLUME_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_VOLUME_UP: Int
```

Key code constant: Volume Up key.

Adjusts the speaker volume up.

 Value: 24

### KEYCODE_W

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_W: Int
```

Key code constant: 'W' key.

 Value: 51

### KEYCODE_WAKEUP

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_WAKEUP: Int
```

Key code constant: Wakeup key.

Wakes up the device. Behaves somewhat like `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_POWER:kotlin.Int` but it has no effect if the device is already awake.

 Value: 224

### KEYCODE_WINDOW

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_WINDOW: Int
```

Key code constant: Window key.

On TV remotes, toggles picture-in-picture mode or other windowing functions. On Android Wear devices, triggers a display offset.

 Value: 171

### KEYCODE_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_X: Int
```

Key code constant: 'X' key.

 Value: 52

### KEYCODE_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_Y: Int
```

Key code constant: 'Y' key.

 Value: 53

### KEYCODE_YEN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_YEN: Int
```

Key code constant: Japanese Yen key.

 Value: 216

### KEYCODE_Z

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_Z: Int
```

Key code constant: 'Z' key.

 Value: 54

### KEYCODE_ZENKAKU_HANKAKU

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ZENKAKU_HANKAKU: Int
```

Key code constant: Japanese full-width / half-width key.

 Value: 211

### KEYCODE_ZOOM_IN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ZOOM_IN: Int
```

Key code constant: Zoom in key.

 Value: 168

### KEYCODE_ZOOM_OUT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYCODE_ZOOM_OUT: Int
```

Key code constant: Zoom out key.

 Value: 169

### MAX_KEYCODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_KEYCODE: Int
```

**Deprecated:** *There are now more than MAX_KEYCODE keycodes. Use `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMaxKeyCode()` instead.*

 Value: 84

### META_ALT_LEFT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_ALT_LEFT_ON: Int
```

This mask is used to check whether the left ALT meta key is pressed.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isAltPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int`

### META_ALT_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_ALT_MASK: Int
```

This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_RIGHT_ON:kotlin.Int`.

 Value: 50

### META_ALT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_ALT_ON: Int
```

This mask is used to check whether one of the ALT meta keys is pressed.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isAltPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_RIGHT:kotlin.Int`

### META_ALT_RIGHT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_ALT_RIGHT_ON: Int
```

This mask is used to check whether the right the ALT meta key is pressed.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isAltPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_RIGHT:kotlin.Int`

### META_CAPS_LOCK_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_CAPS_LOCK_ON: Int
```

This mask is used to check whether the CAPS LOCK meta key is on.

 Value: 1048576

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCapsLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`

### META_CTRL_LEFT_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_CTRL_LEFT_ON: Int
```

This mask is used to check whether the left CTRL meta key is pressed.

 Value: 8192

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCtrlPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_LEFT:kotlin.Int`

### META_CTRL_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_CTRL_MASK: Int
```

This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_RIGHT_ON:kotlin.Int`.

 Value: 28672

### META_CTRL_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_CTRL_ON: Int
```

This mask is used to check whether one of the CTRL meta keys is pressed.

 Value: 4096

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCtrlPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_RIGHT:kotlin.Int`

### META_CTRL_RIGHT_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_CTRL_RIGHT_ON: Int
```

This mask is used to check whether the right CTRL meta key is pressed.

 Value: 16384

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCtrlPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_RIGHT:kotlin.Int`

### META_FUNCTION_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_FUNCTION_ON: Int
```

This mask is used to check whether the FUNCTION meta key is pressed.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isFunctionPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`

### META_META_LEFT_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_META_LEFT_ON: Int
```

This mask is used to check whether the left META meta key is pressed.

 Value: 131072

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMetaPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_LEFT:kotlin.Int`

### META_META_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_META_MASK: Int
```

This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_RIGHT_ON:kotlin.Int`.

 Value: 458752

### META_META_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_META_ON: Int
```

This mask is used to check whether one of the META meta keys is pressed.

 Value: 65536

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMetaPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_RIGHT:kotlin.Int`

### META_META_RIGHT_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_META_RIGHT_ON: Int
```

This mask is used to check whether the right META meta key is pressed.

 Value: 262144

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMetaPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_RIGHT:kotlin.Int`

### META_NUM_LOCK_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_NUM_LOCK_ON: Int
```

This mask is used to check whether the NUM LOCK meta key is on.

 Value: 2097152

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isNumLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int`

### META_SCROLL_LOCK_ON

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SCROLL_LOCK_ON: Int
```

This mask is used to check whether the SCROLL LOCK meta key is on.

 Value: 4194304

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isScrollLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`

### META_SHIFT_LEFT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SHIFT_LEFT_ON: Int
```

This mask is used to check whether the left SHIFT meta key is pressed.

 Value: 64

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isShiftPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_LEFT:kotlin.Int`

### META_SHIFT_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SHIFT_MASK: Int
```

This mask is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_RIGHT_ON:kotlin.Int`.

 Value: 193

### META_SHIFT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SHIFT_ON: Int
```

This mask is used to check whether one of the SHIFT meta keys is pressed.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isShiftPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_RIGHT:kotlin.Int`

### META_SHIFT_RIGHT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SHIFT_RIGHT_ON: Int
```

This mask is used to check whether the right SHIFT meta key is pressed.

 Value: 128

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isShiftPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_RIGHT:kotlin.Int`

### META_SYM_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_SYM_ON: Int
```

This mask is used to check whether the SYM meta key is pressed.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isSymPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`

## Public constructors

### KeyEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(origEvent: KeyEvent!)
```

Make an exact copy of an existing key event.

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    origEvent: KeyEvent!, 
    eventTime: Long, 
    newRepeat: Int)
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/KeyEvent#changeTimeRepeat(android.view.KeyEvent,%20kotlin.Long,%20kotlin.Int)` instead.*

Copy an existing key event, modifying its time and repeat count.

| Parameters ||
|---|---|
| `origEvent` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!: The existing event to be copied. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new event time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) of the event. |
| `newRepeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new repeat count of the event. |

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    action: Int, 
    code: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |

### KeyEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    time: Long, 
    characters: String!, 
    deviceId: Int, 
    flags: Int)
```

Create a new key event for a string of characters. The key code, action, repeat count and source will automatically be set to `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int`, 0, and `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_KEYBOARD:kotlin.Int` for you.

| Parameters ||
|---|---|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event occured. |
| `characters` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The string of characters. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device ID that generated the key event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags for this key event |

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    code: Int, 
    repeat: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this key code originally went down. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event happened. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A repeat count for down events (\> 0 if this is after the initial down) or event count for multiple events. |

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    code: Int, 
    repeat: Int, 
    metaState: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this key code originally went down. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event happened. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A repeat count for down events (\> 0 if this is after the initial down) or event count for multiple events. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which meta keys are currently pressed. |

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    code: Int, 
    repeat: Int, 
    metaState: Int, 
    deviceId: Int, 
    scancode: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this key code originally went down. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event happened. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A repeat count for down events (\> 0 if this is after the initial down) or event count for multiple events. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which meta keys are currently pressed. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device ID that generated the key event. |
| `scancode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Raw device scan code of the event. |

### KeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    code: Int, 
    repeat: Int, 
    metaState: Int, 
    deviceId: Int, 
    scancode: Int, 
    flags: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this key code originally went down. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event happened. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A repeat count for down events (\> 0 if this is after the initial down) or event count for multiple events. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which meta keys are currently pressed. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device ID that generated the key event. |
| `scancode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Raw device scan code of the event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags for this key event |

### KeyEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
KeyEvent(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    code: Int, 
    repeat: Int, 
    metaState: Int, 
    deviceId: Int, 
    scancode: Int, 
    flags: Int, 
    source: Int)
```

Create a new key event.

| Parameters ||
|---|---|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this key code originally went down. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) at which this event happened. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Action code: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `repeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A repeat count for down events (\> 0 if this is after the initial down) or event count for multiple events. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which meta keys are currently pressed. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device ID that generated the key event. |
| `scancode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Raw device scan code of the event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags for this key event |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The input source such as `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_KEYBOARD:kotlin.Int`. |

## Public methods

### changeAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun changeAction(
    event: KeyEvent!, 
    action: Int
): KeyEvent!
```

Create a new key event that is the same as the given one, but whose action is replaced with the given value.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!: The existing event to be copied. This is not modified. |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new action code of the event. |

### changeFlags

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun changeFlags(
    event: KeyEvent!, 
    flags: Int
): KeyEvent!
```

Create a new key event that is the same as the given one, but whose flags are replaced with the given value.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!: The existing event to be copied. This is not modified. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new flags constant. |

### changeTimeRepeat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun changeTimeRepeat(
    event: KeyEvent!, 
    eventTime: Long, 
    newRepeat: Int
): KeyEvent!
```

Create a new key event that is the same as the given one, but whose event time and repeat count are replaced with the given value.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!: The existing event to be copied. This is not modified. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new event time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) of the event. |
| `newRepeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new repeat count of the event. |

### changeTimeRepeat

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun changeTimeRepeat(
    event: KeyEvent!, 
    eventTime: Long, 
    newRepeat: Int, 
    newFlags: Int
): KeyEvent!
```

Create a new key event that is the same as the given one, but whose event time and repeat count are replaced with the given value.

| Parameters ||
|---|---|
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent#)!: The existing event to be copied. This is not modified. |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new event time (in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`) of the event. |
| `newRepeat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new repeat count of the event. |
| `newFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): New flags for the event, replacing the entire value in the original event. |

### dispatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatch(receiver: KeyEvent.Callback!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/KeyEvent#dispatch(android.view.KeyEvent.Callback,%20android.view.KeyEvent.DispatcherState,%20kotlin.Any)` instead.*

### dispatch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatch(
    receiver: KeyEvent.Callback!, 
    state: KeyEvent.DispatcherState!, 
    target: Any!
): Boolean
```

Deliver this key event to a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback` interface. If this is an `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int` event and it is not handled, then an attempt will be made to deliver a single normal event.

| Parameters ||
|---|---|
| `receiver` | [KeyEvent.Callback](https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback)!: The Callback that will be given the event. |
| `state` | [KeyEvent.DispatcherState](https://developer.android.com/reference/kotlin/android/view/KeyEvent.DispatcherState)!: State information retained across events. |
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The target of the dispatch, for use in tracking. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The return value from the Callback method that was called. |

### getAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAction(): Int
```

Retrieve the action of this key event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the event action: either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int`. |

### getCharacters

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharacters(): String!
```

**Deprecated:** *no longer used by the input system.*

For the special case of a `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_MULTIPLE:kotlin.Int` event with key code of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int`, this is a raw string of characters associated with the event. In all other cases it is null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Returns a String of 1 or more characters associated with the event. |

### getDeadChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDeadChar(
    accent: Int, 
    c: Int
): Int
```

Get the character that is produced by putting accent on the character c. For example, getDeadChar('\`', 'e') returns è.

### getDeviceId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceId(): Int
```

Gets the id for the device that this event came from. An id of zero indicates that the event didn't come from a physical device and maps to the default keymap. The other numbers are arbitrary and you shouldn't depend on the values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The device id. |

### getDisplayLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayLabel(): Char
```

Gets the primary character for this key. In other words, the label that is physically printed on it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The display label character, or 0 if none (eg. for non-printing keys). |

### getDownTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDownTime(): Long
```

Retrieve the time of the most recent key down event, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. If this is a down event, this will be the same as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getEventTime()`. Note that when chording keys, this value is the down time of the most recently pressed key, which may *not* be the same physical key of this event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Returns the most recent key down time, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base |

### getEventTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEventTime(): Long
```

Retrieve the time this event occurred, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Returns the time this event occurred, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. |

### getFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFlags(): Int
```

Returns the flags for this key event.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_WOKE_HERE:kotlin.Int`

### getKeyCharacterMap

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyCharacterMap(): KeyCharacterMap!
```

Gets the `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap` associated with the keyboard device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap!` | The associated key character map. |

| Exceptions ||
|---|---|
| `android.view.KeyCharacterMap.UnavailableException` | if the key character map could not be loaded because it was malformed or the default key character map is missing from the system. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#load(kotlin.Int)`

### getKeyCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyCode(): Int
```

Retrieve the key code of the key event. This is the physical key that was pressed, *not* the Unicode character.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The key code of the event. |

### getKeyData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeyData(results: KeyCharacterMap.KeyData!): Boolean
```

**Deprecated:** *instead use `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDisplayLabel()`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getNumber()` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getUnicodeChar(kotlin.Int)`.*

Get the character conversion data for a given key code.

| Parameters ||
|---|---|
| `results` | [KeyCharacterMap.KeyData](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.KeyData)!: A `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.KeyData` instance that will be filled with the results. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the key was mapped. If the key was not mapped, results is not modified. |

### getMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatch(chars: CharArray!): Char
```

Gets the first character in the character array that can be generated by the specified key code.

This is a convenience function that returns the same value as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMatch(kotlin.CharArray,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The array of matching characters to consider. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The matching associated character, or 0 if none. |

### getMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatch(
    chars: CharArray!, 
    metaState: Int
): Char
```

Gets the first character in the character array that can be generated by the specified key code. If there are multiple choices, prefers the one that would be generated with the specified meta key modifier state.

| Parameters ||
|---|---|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The array of matching characters to consider. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The preferred meta key modifier state. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The matching associated character, or 0 if none. |

### getMaxKeyCode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaxKeyCode(): Int
```

Returns the maximum keycode.

### getMetaState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetaState(): Int
```

Returns the state of the meta keys.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer in which each bit set to 1 represents a pressed meta key |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isAltPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isShiftPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isSymPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCtrlPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isMetaPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isFunctionPressed()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isCapsLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isNumLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#isScrollLockOn()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_RIGHT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_RIGHT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_LEFT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_RIGHT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_LEFT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_RIGHT_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifiers()`

### getModifierMetaStateMask

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getModifierMetaStateMask(): Int
```

Gets a mask that includes all valid modifier key meta state bits.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, the mask specifically excludes `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The modifier meta state mask which is a combination of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_RIGHT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_RIGHT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_LEFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_RIGHT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_LEFT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_RIGHT_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int`. |

### getModifiers

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getModifiers(): Int
```

Returns the state of the modifier keys.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function specifically masks out `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

The value returned consists of the meta state (from `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`) normalized using `https://developer.android.com/reference/kotlin/android/view/KeyEvent#normalizeMetaState(kotlin.Int)` and then masked with `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifierMetaStateMask()` so that only valid modifier bits are retained.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer in which each bit set to 1 represents a pressed modifier key. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`

### getNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumber(): Char
```

Gets the number or symbol associated with the key.

The character value is returned, not the numeric value. If the key is not a number, but is a symbol, the symbol is retuned.

This method is intended to to support dial pads and other numeric or symbolic entry on keyboards where certain keys serve dual function as alphabetic and symbolic keys. This method returns the number or symbol associated with the key independent of whether the user has pressed the required modifier.

For example, on one particular keyboard the keys on the top QWERTY row generate numbers when ALT is pressed such that ALT-Q maps to '1'. So for that keyboard when `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getNumber()` is called with `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_Q:kotlin.Int` it returns '1' so that the user can type numbers without pressing ALT when it makes sense.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | The associated numeric or symbolic character, or 0 if none. |

### getRepeatCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRepeatCount(): Int
```

Retrieve the repeat count of the event. For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` events, this is the number of times the key has repeated with the first down starting at 0 and counting up from there. For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` events, this is always 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of times the key has repeated. |

### getScanCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScanCode(): Int
```

Retrieve the hardware key id of this key event. These values are not reliable and vary from device to device. {@more} Mostly this is here for debugging purposes.

### getSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSource(): Int
```

Gets the source of the event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The event source or `https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_UNKNOWN:kotlin.Int` if unknown. |

### getUnicodeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUnicodeChar(): Int
```

Gets the Unicode character generated by the specified key and meta key state combination.

Returns the Unicode character that the specified key would produce when the specified meta bits (see `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#`) were active.

Returns 0 if the key is not one that is used to type Unicode characters.

If the return value has bit `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#COMBINING_ACCENT:kotlin.Int` set, the key is a "dead key" that should be combined with another to actually produce a character -- see `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#getDeadChar(kotlin.Int,%20kotlin.Int)` -- after masking with `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#COMBINING_ACCENT_MASK:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The associated character or combining accent, or 0 if none. |

### getUnicodeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUnicodeChar(metaState: Int): Int
```

Gets the Unicode character generated by the specified key and meta key state combination.

Returns the Unicode character that the specified key would produce when the specified meta bits (see `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#`) were active.

Returns 0 if the key is not one that is used to type Unicode characters.

If the return value has bit `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#COMBINING_ACCENT:kotlin.Int` set, the key is a "dead key" that should be combined with another to actually produce a character -- see `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#getDeadChar(kotlin.Int,%20kotlin.Int)` -- after masking with `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#COMBINING_ACCENT_MASK:kotlin.Int`.

| Parameters ||
|---|---|
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta key modifier state. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The associated character or combining accent, or 0 if none. |

### hasModifiers

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasModifiers(modifiers: Int): Boolean
```

Returns true if only the specified modifiers keys are pressed. Returns false if a different combination of modifier keys are pressed.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function ignores `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

If the specified modifier mask includes directional modifiers, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`, then this method ensures that the modifier is pressed on that side. If the specified modifier mask includes non-directional modifiers, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`, then this method ensures that the modifier is pressed on either side. If the specified modifier mask includes both directional and non-directional modifiers for the same type of key, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`, then this method throws an illegal argument exception.

| Parameters ||
|---|---|
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta state of the modifier keys to check. May be a combination of modifier meta states as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifierMetaStateMask()`. May be 0 to ensure that no modifier keys are pressed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if only the specified modifier keys are pressed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the modifiers parameter contains invalid modifiers |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#metaStateHasModifiers(kotlin.Int,%20kotlin.Int)`

### hasNoModifiers

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNoModifiers(): Boolean
```

Returns true if no modifier keys are pressed.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function ignores `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

The meta state is normalized prior to comparison using `https://developer.android.com/reference/kotlin/android/view/KeyEvent#normalizeMetaState(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if no modifier keys are pressed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#metaStateHasNoModifiers(kotlin.Int)`

### isAltPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAltPressed(): Boolean
```

Returns the pressed state of the ALT meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the ALT key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`

### isCanceled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCanceled(): Boolean
```

For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` events, indicates that the event has been canceled as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int`.

### isCapsLockOn

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCapsLockOn(): Boolean
```

Returns the locked state of the CAPS LOCK meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the CAPS LOCK key is on, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`

### isCtrlPressed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCtrlPressed(): Boolean
```

Returns the pressed state of the CTRL meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the CTRL key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int`

### isFunctionPressed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFunctionPressed(): Boolean
```

Returns the pressed state of the FUNCTION meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the FUNCTION key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FUNCTION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int`

### isGamepadButton

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isGamepadButton(keyCode: Int): Boolean
```

Returns true if the specified keycode is a gamepad button.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the keycode is a gamepad button, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BUTTON_A:kotlin.Int`. |

### isLongPress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLongPress(): Boolean
```

For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` events, indicates that the event has been canceled as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_LONG_PRESS:kotlin.Int`.

### isMediaSessionKey

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isMediaSessionKey(keyCode: Int): Boolean
```

Returns whether this key will be sent to the `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback.html#` if not handled.

The following key codes are considered `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.html#` keys:

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PLAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PAUSE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PLAY_PAUSE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_HEADSETHOOK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_STOP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_NEXT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_PREVIOUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_REWIND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_MEDIA_FAST_FORWARD:kotlin.Int`

### isMetaPressed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMetaPressed(): Boolean
```

Returns the pressed state of the META meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the META key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int`

### isModifierKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isModifierKey(keyCode: Int): Boolean
```

Returns true if this key code is a modifier key.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function return false for those keys.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the key code is one of `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_LEFT:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_ALT_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CTRL_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_LEFT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_META_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FUNCTION:kotlin.Int`. |

### isNumLockOn

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNumLockOn(): Boolean
```

Returns the locked state of the NUM LOCK meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the NUM LOCK key is on, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`

### isPrintingKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPrintingKey(): Boolean
```

Returns true if this key produces a glyph.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the key is a printing key. |

### isScrollLockOn

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isScrollLockOn(): Boolean
```

Returns the locked state of the SCROLL LOCK meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the SCROLL LOCK key is on, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int`

### isShiftPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isShiftPressed(): Boolean
```

Returns the pressed state of the SHIFT meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the SHIFT key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SHIFT_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`

### isSymPressed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSymPressed(): Boolean
```

Returns the pressed state of the SYM meta key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the SYM key is pressed, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SYM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int`

### isSystem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSystem(): Boolean
```

Is this a system key? System keys can not be used for menu shortcuts.

### isTracking

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTracking(): Boolean
```

For `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` events, indicates that the event is still being tracked from its initial down event as per `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_TRACKING:kotlin.Int`.

### keyCodeFromString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun keyCodeFromString(symbolicName: String): Int
```

Gets a keycode by its symbolic name such as "KEYCODE_A" or an equivalent numeric constant such as "29". For symbolic names, starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` the prefix "KEYCODE_" is optional.

| Parameters ||
|---|---|
| `symbolicName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The symbolic name of the keycode. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The keycode or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int` if not found. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#keyCodeToString(kotlin.Int)`

### keyCodeToString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun keyCodeToString(keyCode: Int): String!
```

Returns a string that represents the symbolic name of the specified keycode such as "KEYCODE_A", "KEYCODE_DPAD_UP", or an equivalent numeric constant such as "1001" if unknown. This function is intended to be used mostly for debugging, logging, and testing. It is not locale-specific and is not intended to be used in a user-facing manner.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The symbolic name of the specified keycode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#getDisplayLabel(kotlin.Int)`

### metaStateHasModifiers

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun metaStateHasModifiers(
    metaState: Int, 
    modifiers: Int
): Boolean
```

Returns true if only the specified modifier keys are pressed according to the specified meta state. Returns false if a different combination of modifier keys are pressed.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function ignores `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

If the specified modifier mask includes directional modifiers, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`, then this method ensures that the modifier is pressed on that side. If the specified modifier mask includes non-directional modifiers, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int`, then this method ensures that the modifier is pressed on either side. If the specified modifier mask includes both directional and non-directional modifiers for the same type of key, such as `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_LEFT_ON:kotlin.Int`, then this method throws an illegal argument exception.

| Parameters ||
|---|---|
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta state to consider. |
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta state of the modifier keys to check. May be a combination of modifier meta states as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getModifierMetaStateMask()`. May be 0 to ensure that no modifier keys are pressed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if only the specified modifier keys are pressed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the modifiers parameter contains invalid modifiers |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#hasModifiers(kotlin.Int)`

### metaStateHasNoModifiers

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun metaStateHasNoModifiers(metaState: Int): Boolean
```

Returns true if no modifiers keys are pressed according to the specified meta state.

For the purposes of this function, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_CAPS_LOCK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_SCROLL_LOCK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_NUM_LOCK:kotlin.Int` are not considered modifier keys. Consequently, this function ignores `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SCROLL_LOCK_ON:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_NUM_LOCK_ON:kotlin.Int`.

The meta state is normalized prior to comparison using `https://developer.android.com/reference/kotlin/android/view/KeyEvent#normalizeMetaState(kotlin.Int)`.

| Parameters ||
|---|---|
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta state to consider. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if no modifier keys are pressed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#hasNoModifiers()`

### normalizeMetaState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun normalizeMetaState(metaState: Int): Int
```

Normalizes the specified meta state.

The meta state is normalized such that if either the left or right modifier meta state bits are set then the result will also include the universal bit for that modifier.

If the specified meta state contains `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int` then the result will also contain `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int` in addition to `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_LEFT_ON:kotlin.Int` and the other bits that were specified in the input. The same is process is performed for shift, control and meta.

If the specified meta state contains synthetic meta states defined by `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#`, then those states are translated here and the original synthetic meta states are removed from the result. `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#META_CAP_LOCKED:kotlin.Int` is translated to `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CAPS_LOCK_ON:kotlin.Int`. `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#META_ALT_LOCKED:kotlin.Int` is translated to `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int`. `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener.html#META_SYM_LOCKED:kotlin.Int` is translated to `https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int`.

Undefined meta state bits are removed.

| Parameters ||
|---|---|
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta state. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The normalized meta state. |

### setSource

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSource(source: Int): Unit
```

### startTracking

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startTracking(): Unit
```

Call this during `https://developer.android.com/reference/kotlin/android/view/KeyEvent.Callback#onKeyDown(kotlin.Int,%20android.view.KeyEvent)` to have the system track the key through its final up (possibly including a long press). Note that only one key can be tracked at a time -- if another key down event is received while a previous one is being tracked, tracking is stopped on the previous event.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<KeyEvent!>
```
