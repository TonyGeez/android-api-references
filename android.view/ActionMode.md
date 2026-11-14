Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActionMode

```
abstract class ActionMode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ActionMode](../android/view/ActionMode.md) |

Represents a contextual mode of the user interface. Action modes can be used to provide alternative interaction modes and replace parts of the normal UI until finished. Examples of good action modes include text selection and contextual actions.

> [!NOTE]
>
> ### Developer Guides
>
> For information about how to provide contextual actions with `ActionMode`, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html#context-menu) developer guide.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback` Callback interface for action modes. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback2` Extension of `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback` to provide content rect information. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#DEFAULT_HIDE_DURATION:kotlin.Int` Default value to hide the action mode for `https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getDefaultActionModeHideDuration()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int` The action mode is treated as a Floating Toolbar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int` The action mode is treated as a Primary mode. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionMode#ActionMode()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#clearTextSelection()()` Clear the text selection. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#finish()()` Finish and close this action mode. |
| abstract [View](../android/view/View.md)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getCustomView()()` Returns the current custom view for this action mode. |
| --- | --- |
| abstract [Menu](../android/view/Menu.md)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getMenu()()` Returns the menu of actions that this action mode presents. |
| abstract [MenuInflater](../android/view/MenuInflater.md)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getMenuInflater()()` Returns a `https://developer.android.com/reference/kotlin/android/view/MenuInflater` with the ActionMode's context. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getSubtitle()()` Returns the current subtitle of this action mode. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getTag()()` Retrieve the tag object associated with this ActionMode. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getTitle()()` Returns the current title of this action mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getTitleOptionalHint()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#getType()()` Returns the type for this action mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#hide(kotlin.Long)(duration: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Hide the action mode view from obstructing the content below for a short duration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#invalidate()()` Invalidate the action mode and refresh menu content. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#invalidateContentRect()()` Invalidate the content rect associated to this ActionMode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#isTitleOptional()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#onWindowFocusChanged(kotlin.Boolean)(hasWindowFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the window containing the view that started this action mode gains or loses focus. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setCustomView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View!)` Set a custom view for this action mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setSubtitle(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the subtitle of the action mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setSubtitle(kotlin.CharSequence)(subtitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Set the subtitle of the action mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTag(kotlin.Any)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Set a tag object associated with this ActionMode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTextSelection(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.os.LocaleList)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locales: https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)` Forward text selection data for ActionMode to process. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitle(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the title of the action mode. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Set the title of the action mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitleOptionalHint(kotlin.Boolean)(titleOptional: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether or not the title/subtitle display for this action mode is optional. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionMode#setType(kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a type for this action mode. |
| --- | --- |

## Constants

### DEFAULT_HIDE_DURATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_HIDE_DURATION: Int
```

Default value to hide the action mode for `https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getDefaultActionModeHideDuration()`.

 Value: -1

### TYPE_FLOATING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FLOATING: Int
```

The action mode is treated as a Floating Toolbar. Use with `https://developer.android.com/reference/kotlin/android/view/ActionMode#setType(kotlin.Int)`.

 Value: 1

### TYPE_PRIMARY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PRIMARY: Int
```

The action mode is treated as a Primary mode. This is the default. Use with `https://developer.android.com/reference/kotlin/android/view/ActionMode#setType(kotlin.Int)`.

 Value: 0

## Public constructors

### ActionMode

```
ActionMode()
```

## Public methods

### clearTextSelection

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearTextSelection(): Unit
```

Clear the text selection. The method is called when the previous text selection needs to be cleared. Calling it will also clear the actions resulted from previous text selection set by setTextSelection.

### finish

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun finish(): Unit
```

Finish and close this action mode. The action mode's `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback` will have its `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onDestroyActionMode(android.view.ActionMode)` method called.

### getCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCustomView(): View!
```

Returns the current custom view for this action mode.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View!` | The current custom view |

### getMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMenu(): Menu!
```

Returns the menu of actions that this action mode presents.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Menu!` | The action mode's menu. |

### getMenuInflater

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMenuInflater(): MenuInflater!
```

Returns a `https://developer.android.com/reference/kotlin/android/view/MenuInflater` with the ActionMode's context.

### getSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSubtitle(): CharSequence!
```

Returns the current subtitle of this action mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | Subtitle text |

### getTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTag(): Any!
```

Retrieve the tag object associated with this ActionMode.

Like the tag available to views, this allows applications to associate arbitrary data with an ActionMode for later reference.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | Tag associated with this ActionMode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTag(kotlin.Any)`

### getTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTitle(): CharSequence!
```

Returns the current title of this action mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | Title text |

### getTitleOptionalHint

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTitleOptionalHint(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this action mode has been given a hint to consider the title/subtitle display to be optional. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitleOptionalHint(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#isTitleOptional()`

### getType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): Int
```

Returns the type for this action mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int`. |

### hide

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hide(duration: Long): Unit
```

Hide the action mode view from obstructing the content below for a short duration. This only makes sense for action modes that support dynamic positioning on the screen. If this method is called again before the hide duration expires, the later hide call will cancel the former and then take effect. NOTE that there is an internal limit to how long the mode can be hidden for. It's typically about a few seconds.

| Parameters ||
|---|---|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of milliseconds to hide for. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#DEFAULT_HIDE_DURATION:kotlin.Int`

### invalidate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun invalidate(): Unit
```

Invalidate the action mode and refresh menu content. The mode's `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback` will have its `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback#onPrepareActionMode(android.view.ActionMode,%20android.view.Menu)` method called. If it returns true the menu will be scanned for updated content and any relevant changes will be reflected to the user.

### invalidateContentRect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateContentRect(): Unit
```

Invalidate the content rect associated to this ActionMode. This only makes sense for action modes that support dynamic positioning on the screen, and provides a more efficient way to reposition it without invalidating the whole action mode.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode.Callback2#onGetContentRect(android.view.ActionMode,%20android.view.View,%20android.graphics.Rect)`

### isTitleOptional

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTitleOptional(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this action mode considers the title and subtitle fields as optional. Optional titles may not be displayed to the user. |

### onWindowFocusChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWindowFocusChanged(hasWindowFocus: Boolean): Unit
```

Called when the window containing the view that started this action mode gains or loses focus.

| Parameters ||
|---|---|
| `hasWindowFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the window containing the view that started this action mode now has focus, false otherwise. |

### setCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCustomView(view: View!): Unit
```

Set a custom view for this action mode. The custom view will take the place of the title and subtitle. Useful for things like search boxes.

| Parameters ||
|---|---|
| `view` | [View](../android/view/View.md)!: Custom view to use in place of the title/subtitle. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setSubtitle(kotlin.CharSequence)`

### setSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSubtitle(resId: Int): Unit
```

Set the subtitle of the action mode. This method will have no visible effect if a custom view has been set.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a string to set as the subtitle |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setSubtitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setCustomView(android.view.View)`

### setSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSubtitle(subtitle: CharSequence!): Unit
```

Set the subtitle of the action mode. This method will have no visible effect if a custom view has been set.

| Parameters ||
|---|---|
| `subtitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Subtitle string to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setSubtitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setCustomView(android.view.View)`

### setTag

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTag(tag: Any!): Unit
```

Set a tag object associated with this ActionMode.

Like the tag available to views, this allows applications to associate arbitrary data with an ActionMode for later reference.

| Parameters ||
|---|---|
| `tag` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Tag to associate with this ActionMode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#getTag()`

### setTextSelection

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextSelection(
    text: CharSequence?, 
    start: Int, 
    end: Int, 
    locales: LocaleList
): Unit
```

Forward text selection data for ActionMode to process. The method is called when text selection changes. An implementation of this API processes the text selection data such as running the text classification task and handles the resulting actions, rendering them in the action bar.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The text of the text view. If the text is empty or null, it clears the previous text selection and its action classification results, equivalent to calling clearTextSelection(). |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The start of the selection. If this parameter is \< 0 or \> end, it throws an IllegalArgumentException. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The end of the selection. If this parameter is \< 0 or \< start, it throws an IllegalArgumentException. |
| --- | --- |
| `locales` | [LocaleList](../android/os/LocaleList.md): The locales of the texts/view/selection. If it is empty, a default/unknown locale will be used. This value cannot be `null`. |

### setTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitle(resId: Int): Unit
```

Set the title of the action mode. This method will have no visible effect if a custom view has been set.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a string to set as the title |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setCustomView(android.view.View)`

### setTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitle(title: CharSequence!): Unit
```

Set the title of the action mode. This method will have no visible effect if a custom view has been set.

| Parameters ||
|---|---|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Title string to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setTitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/ActionMode#setCustomView(android.view.View)`

### setTitleOptionalHint

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTitleOptionalHint(titleOptional: Boolean): Unit
```

Set whether or not the title/subtitle display for this action mode is optional.

In many cases the supplied title for an action mode is merely meant to add context and is not strictly required for the action mode to be useful. If the title is optional, the system may choose to hide the title entirely rather than truncate it due to a lack of available space.

Note that this is merely a hint; the underlying implementation may choose to ignore this setting under some circumstances.

| Parameters ||
|---|---|
| `titleOptional` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the title only presents optional information. |

### setType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setType(type: Int): Unit
```

Set a type for this action mode. This will affect how the system renders the action mode if it has to.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_PRIMARY:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/ActionMode#TYPE_FLOATING:kotlin.Int`. |
