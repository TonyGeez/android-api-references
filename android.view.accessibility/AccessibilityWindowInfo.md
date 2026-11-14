Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityWindowInfo

```
class AccessibilityWindowInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md) |

This class represents a state snapshot of a window for accessibility purposes. The screen content contains one or more windows where some windows can be descendants of other windows, which is the windows are hierarchically ordered. Note that there is no root window. Hence, the screen content can be seen as a collection of window trees.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_ACCESSIBILITY_OVERLAY:kotlin.Int` Window type: Windows that are overlaid *only* by an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` for interception of user interactions without changing the windows an accessibility service can introspect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_APPLICATION:kotlin.Int` Window type: This is an application window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_INPUT_METHOD:kotlin.Int` Window type: This is an input method window. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_MAGNIFICATION_OVERLAY:kotlin.Int` Window type: A system window used to show the UI for the interaction with window-based magnification, which includes the magnified content and the option menu. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_SPLIT_SCREEN_DIVIDER:kotlin.Int` Window type: A system window used to divide the screen in split-screen mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_SYSTEM:kotlin.Int` Window type: This is a system window. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_WINDOW_CONTROL:kotlin.Int` Window type: A system window that has the function to control an associated window. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#AccessibilityWindowInfo()()` Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#`. |
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#AccessibilityWindowInfo(android.view.accessibility.AccessibilityWindowInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#)` Copy constructor. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getAnchor()()` Gets the node that anchors this window to another. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getBoundsInScreen(android.graphics.Rect)(outBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Gets the bounds of this window in the screen. |
| [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getChild(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the child window at a given index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getChildCount()()` Gets the number of child windows. |
| --- | --- |
| [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControlledWindow(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the controlled window at the given index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControlledWindowsCount()()` Gets the number of windows which are controlled by this window, if there are any. |
| [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControllingWindow()()` Gets the system window which has the functionality to control this window. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getDisplayId()()` Returns the ID of the display this window is on, for use with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getId()()` Gets the unique window id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getLayer()()` Gets the layer which determines the Z-order of the window. |
| --- | --- |
| [LocaleList](../android/os/LocaleList.md) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getLocales()()` Return the `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` of the window. |
| [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getParent()()` Gets the parent window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getRegionInScreen(android.graphics.Region)(outRegion: https://developer.android.com/reference/kotlin/android/graphics/Region.html#)` Gets the touchable region of this window in the screen. |
| --- | --- |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getRoot()()` Gets the root node in the window's hierarchy. |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getRoot(kotlin.Int)(prefetchingStrategy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the root node in the window's hierarchy. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getTitle()()` Gets the title of the window. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getTransitionTimeMillis()()` Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` at which the last transition happens. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getType()()` Gets the type of the window. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isAccessibilityFocused()()` Gets if this window has accessibility focus. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isActive()()` Gets if this window is active. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isFocused()()` Gets if this window has input focus. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isInPictureInPictureMode()()` Check if the window is in picture-in-picture mode. |
| static [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#obtain()()` Returns a cached instance if such is available or a new one is created. |
| static [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#obtain(android.view.accessibility.AccessibilityWindowInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#!)` Returns a cached instance if such is available or a new one is created. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#recycle()()` Return an instance back to be reused. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#refresh()()` Refreshes this window with the latest state of the window it represents. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_ACCESSIBILITY_OVERLAY

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ACCESSIBILITY_OVERLAY: Int
```

Window type: Windows that are overlaid *only* by an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` for interception of user interactions without changing the windows an accessibility service can introspect. In particular, an accessibility service can introspect only windows that a sighted user can interact with which they can touch these windows or can type into these windows. For example, if there is a full screen accessibility overlay that is touchable, the windows below it will be introspectable by an accessibility service regardless they are covered by a touchable window.

 Value: 4

### TYPE_APPLICATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_APPLICATION: Int
```

Window type: This is an application window. Such a window shows UI for interacting with an application.

 Value: 1

### TYPE_INPUT_METHOD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_INPUT_METHOD: Int
```

Window type: This is an input method window. Such a window shows UI for inputting text such as keyboard, suggestions, etc.

 Value: 2

### TYPE_MAGNIFICATION_OVERLAY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MAGNIFICATION_OVERLAY: Int
```

Window type: A system window used to show the UI for the interaction with window-based magnification, which includes the magnified content and the option menu.

 Value: 6

### TYPE_SPLIT_SCREEN_DIVIDER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SPLIT_SCREEN_DIVIDER: Int
```

Window type: A system window used to divide the screen in split-screen mode. This type of window is present only in split-screen mode.

 Value: 5

### TYPE_SYSTEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SYSTEM: Int
```

Window type: This is a system window. Such a window shows UI for interacting with the system.

 Value: 3

### TYPE_WINDOW_CONTROL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WINDOW_CONTROL: Int
```

Window type: A system window that has the function to control an associated window.

Window associations can be determined using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControllingWindow()`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControlledWindowsCount()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getControlledWindow(kotlin.Int)`.

 Value: 7

## Public constructors

### AccessibilityWindowInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityWindowInfo()
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#`.

### AccessibilityWindowInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityWindowInfo(info: AccessibilityWindowInfo)
```

Copy constructor. Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#`, and this new instance is initialized from given `info`.

| Parameters ||
|---|---|
| `info` | [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md): The other info. This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAnchor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAnchor(): AccessibilityNodeInfo!
```

Gets the node that anchors this window to another.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo!` | The anchor node, or `null` if none exists. |

### getBoundsInScreen

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBoundsInScreen(outBounds: Rect!): Unit
```

Gets the bounds of this window in the screen. This is equivalent to get the bounds of the Region from `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getRegionInScreen(android.graphics.Region)`.

| Parameters ||
|---|---|
| `outBounds` | [Rect](../android/graphics/Rect.md)!: The out window bounds. |

### getChild

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChild(index: Int): AccessibilityWindowInfo!
```

Gets the child window at a given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#!` | The child. |

### getChildCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChildCount(): Int
```

Gets the number of child windows.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The child count. |

### getControlledWindow

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getControlledWindow(index: Int): AccessibilityWindowInfo?
```

Gets the controlled window at the given index.

Clients should not depend on the order of the controlled windows. If the controlled windows change, clients will receive a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int`.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#?` | The `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#` controlled by this window at the given `index`, or `null` if the connection is invalid or the window is no longer available. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If the index is out of range. |

### getControlledWindowsCount

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getControlledWindowsCount(): Int
```

Gets the number of windows which are controlled by this window, if there are any. If this window is not of type `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_WINDOW_CONTROL:kotlin.Int` then this will always return 0.

The returned list will not include children of the top level controlled windows. If the number of controlled windows changes, clients will receive a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The count of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#` controlled by this window, or 0 if this window does not control other windows. |

### getControllingWindow

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getControllingWindow(): AccessibilityWindowInfo?
```

Gets the system window which has the functionality to control this window.

If this window is the child of another window it may not be controlled directly. In that case, to find the window control, check those of its ancestor windows.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#?` | The window of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_WINDOW_CONTROL:kotlin.Int` that controls this window if one exists, or `null` otherwise. |

### getDisplayId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayId(): Int
```

Returns the ID of the display this window is on, for use with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The logical display id. |

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

Gets the unique window id.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | windowId The window id. |

### getLayer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLayer(): Int
```

Gets the layer which determines the Z-order of the window. Windows with greater layer appear on top of windows with lesser layer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The window layer. |

### getLocales

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocales(): LocaleList
```

Return the `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` of the window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` | the locales of the window. This value cannot be `null`. |

### getParent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParent(): AccessibilityWindowInfo!
```

Gets the parent window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#!` | The parent window, or `null` if none exists. |

### getRegionInScreen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRegionInScreen(outRegion: Region): Unit
```

Gets the touchable region of this window in the screen.

| Parameters ||
|---|---|
| `outRegion` | [Region](../android/graphics/Region.md): The out window region. This value cannot be `null`. |

### getRoot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRoot(): AccessibilityNodeInfo!
```

Gets the root node in the window's hierarchy.

Returns `null` if connection is invalid. Otherwise, always returns a node, even if the root is considered unimportant for accessibility. In this case, calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isImportantForAccessibility()` on the returned node will return `false`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo!` | The root node. |

### getRoot

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRoot(prefetchingStrategy: Int): AccessibilityNodeInfo?
```

Gets the root node in the window's hierarchy.

Returns `null` if connection is invalid. Otherwise, always returns a node, even if the root is considered unimportant for accessibility. In this case, calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isImportantForAccessibility()` on the returned node will return `false`.

| Parameters ||
|---|---|
| `prefetchingStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the prefetching strategy. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo?` | The root node. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent(kotlin.Int)`

### getTitle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTitle(): CharSequence?
```

Gets the title of the window.

This is taken from the `https://developer.android.com/reference/kotlin/android/view/Window.html#`'s title, or its `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` if that is unset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The title of the window, or `null` if none is available. |

### getTransitionTimeMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransitionTimeMillis(): Long
```

Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` at which the last transition happens. A transition happens when `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getBoundsInScreen(android.graphics.Rect)` is changed. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The transition timestamp. Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. |

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Gets the type of the window.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The type. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_APPLICATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_INPUT_METHOD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_SYSTEM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#TYPE_ACCESSIBILITY_OVERLAY:kotlin.Int`

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isAccessibilityFocused

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAccessibilityFocused(): Boolean
```

Gets if this window has accessibility focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether has accessibility focus. |

### isActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActive(): Boolean
```

Gets if this window is active. An active window is the one the user is currently touching or the window has input focus and the user is not touching any window.

This is defined as the window that most recently fired one of the following events: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int`. In other words, the last window shown that also has input focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this is the active window. |

### isFocused

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFocused(): Boolean
```

Gets if this window has input focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether has input focus. |

### isInPictureInPictureMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInPictureInPictureMode(): Boolean
```

Check if the window is in picture-in-picture mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the window is in picture-in-picture mode, `false` otherwise. |

### obtain

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun obtain(): AccessibilityWindowInfo!
```

Returns a cached instance if such is available or a new one is created.

In most situations object pooling is not beneficial. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#AccessibilityWindowInfo()` instead.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#!` | An instance. |

### obtain

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun obtain(info: AccessibilityWindowInfo!): AccessibilityWindowInfo!
```

Returns a cached instance if such is available or a new one is created. The returned instance is initialized from the given `info`.

In most situations object pooling is not beneficial. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#AccessibilityWindowInfo(android.view.accessibility.AccessibilityWindowInfo)` instead.

| Parameters ||
|---|---|
| `info` | [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md)!: The other info. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#!` | An instance. |

### recycle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun recycle(): Unit
```

Return an instance back to be reused.

**Note:** You must not touch the object after calling this function.

In most situations object pooling is not beneficial, and recycling is not necessary.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If the info is already recycled. |

### refresh

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun refresh(): Boolean
```

Refreshes this window with the latest state of the window it represents.

**Note:** If this method returns false this info is obsolete since it represents a window that is no longer exist.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the refresh succeeded. `false` if this window is no longer in the window tree (and thus it has become stale). |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AccessibilityWindowInfo!>
```
