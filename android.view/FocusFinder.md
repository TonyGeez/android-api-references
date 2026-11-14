Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FocusFinder

```
open class FocusFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.FocusFinder](FocusFinder.md) |

The algorithm used for finding the next focusable view in a given direction from a view that currently has focus.

## Summary

| Public methods ||
|---|---|
| open [View](View.md)! | `https://developer.android.com/reference/kotlin/android/view/FocusFinder#findNearestTouchable(android.view.ViewGroup,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)(root: https://developer.android.com/reference/kotlin/android/view/ViewGroup!, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, deltas: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Find the nearest touchable view to the specified view. |
| [View](View.md)! | `https://developer.android.com/reference/kotlin/android/view/FocusFinder#findNextFocus(android.view.ViewGroup,%20android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/ViewGroup!, focused: https://developer.android.com/reference/kotlin/android/view/View!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find the next view to take focus in root's descendants, starting from the view that currently is focused. |
| open [View](View.md)! | `https://developer.android.com/reference/kotlin/android/view/FocusFinder#findNextFocusFromRect(android.view.ViewGroup,%20android.graphics.Rect,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/ViewGroup!, focusedRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find the next view to take focus in root's descendants, searching from a particular rectangle in root's coordinates. |
| --- | --- |
| open [View](View.md)! | `https://developer.android.com/reference/kotlin/android/view/FocusFinder#findNextKeyboardNavigationCluster(android.view.View,%20android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View, currentCluster: https://developer.android.com/reference/kotlin/android/view/View?, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find the root of the next keyboard navigation cluster after the current one. |
| open static [FocusFinder](FocusFinder.md)! | `https://developer.android.com/reference/kotlin/android/view/FocusFinder#getInstance()()` Get the focus finder for this thread. |

## Public methods

### findNearestTouchable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findNearestTouchable(
    root: ViewGroup!, 
    x: Int, 
    y: Int, 
    direction: Int, 
    deltas: IntArray!
): View!
```

Find the nearest touchable view to the specified view.

| Parameters ||
|---|---|
| `root` | [ViewGroup](ViewGroup.md)!: The root of the tree in which to search |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X coordinate from which to start the search |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y coordinate from which to start the search |
| --- | --- |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look |
| `deltas` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Offset from the to the edge of the nearest view. Note that this array may already be populated with values. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The nearest touchable view, or null if none exists. |

### findNextFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findNextFocus(
    root: ViewGroup!, 
    focused: View!, 
    direction: Int
): View!
```

Find the next view to take focus in root's descendants, starting from the view that currently is focused.

If `focused` is not part of the active focusable sequence (for example, if it is an accessibility focus node that is not capable of taking input focus), this method falls back to a generic entry behavior for relative focus navigation (`https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int`), returning the first or last focusable view in the hierarchy respectively.

For absolute directional navigation (`https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int`), this method always uses the `focused` view's bounding rectangle as the geometric starting point for the spatial search, regardless of whether the view is included in the focusable sequence.

| Parameters ||
|---|---|
| `root` | [ViewGroup](ViewGroup.md)!: Contains focused. Cannot be null. |
| `focused` | [View](View.md)!: Has focus now. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The next focusable view, or null if none exists. |

### findNextFocusFromRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findNextFocusFromRect(
    root: ViewGroup!, 
    focusedRect: Rect!, 
    direction: Int
): View!
```

Find the next view to take focus in root's descendants, searching from a particular rectangle in root's coordinates.

| Parameters ||
|---|---|
| `root` | [ViewGroup](ViewGroup.md)!: Contains focusedRect. Cannot be null. |
| `focusedRect` | [Rect](../android.graphics/Rect.md)!: The starting point of the search. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The next focusable view, or null if none exists. |

### findNextKeyboardNavigationCluster

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findNextKeyboardNavigationCluster(
    root: View, 
    currentCluster: View?, 
    direction: Int
): View!
```

Find the root of the next keyboard navigation cluster after the current one.

| Parameters ||
|---|---|
| `root` | [View](View.md): The view tree to look inside. Cannot be null |
| `currentCluster` | [View](View.md)?: The starting point of the search. Null means the default cluster. This value may be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Direction to look. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The next cluster, or null if none exists |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): FocusFinder!
```

Get the focus finder for this thread.
