Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActionBar

Kotlin | [Java](https://developer.android.com/reference/android/app/ActionBar "View this page in Java")

```
abstract class ActionBar
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar#) |

A primary toolbar within the activity that may display the activity title, application-level navigation affordances, and other interactive items.

Beginning with Android 3.0 (API level 11), the action bar appears at the top of an activity's window when the activity uses the system's `https://developer.android.com/reference/kotlin/android/R.style.html#Theme_Holo:kotlin.Int` theme (or one of its descendant themes), which is the default. You may otherwise add the action bar by calling `https://developer.android.com/reference/kotlin/android/view/Window.html#requestFeature(kotlin.Int)` or by declaring it in a custom theme with the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_windowActionBar:kotlin.Int` property.

Beginning with Android L (API level 21), the action bar may be represented by any Toolbar widget within the application layout. The application may signal to the Activity which Toolbar should be treated as the Activity's action bar. Activities that use this feature should use one of the supplied `.NoActionBar` themes, set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_windowActionBar:kotlin.Int` attribute to `false` or otherwise not request the window feature.

By adjusting the window features requested by the theme and the layouts used for an Activity's content view, an app can use the standard system action bar on older platform releases and the newer inline toolbars on newer platform releases. The `ActionBar` object obtained from the Activity can be used to control either configuration transparently.

When using the Holo themes the action bar shows the application icon on the left, followed by the activity title. If your activity has an options menu, you can make select items accessible directly from the action bar as "action items". You can also modify various characteristics of the action bar or remove it completely.

When using the Material themes (default in API 21 or newer) the navigation button (formerly "Home") takes over the space previously occupied by the application icon. Apps wishing to express a stronger branding should use their brand colors heavily in the action bar and other application chrome or use a `https://developer.android.com/reference/kotlin/android/app/ActionBar#setLogo(kotlin.Int)` in place of their standard title text.

From your activity, you can retrieve an instance of `https://developer.android.com/reference/kotlin/android/app/ActionBar#` by calling `https://developer.android.com/reference/kotlin/android/app/Activity#getActionBar()`.

In some cases, the action bar may be overlayed by another bar that enables contextual actions, using an `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#`. For example, when the user selects one or more items in your activity, you can enable an action mode that offers actions specific to the selected items, with a UI that temporarily replaces the action bar. Although the UI may occupy the same space, the `https://developer.android.com/reference/kotlin/android/view/ActionMode.html#` APIs are distinct and independent from those for `https://developer.android.com/reference/kotlin/android/app/ActionBar#`.

> [!NOTE]
>
> ### Developer Guides
>
> For information about how to use the action bar, including how to add action items, navigation modes and more, read the [Action Bar](https://developer.android.com/guide/topics/ui/actionbar.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/ActionBar.LayoutParams` Per-child layout information associated with action bar custom views. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener` Listener for receiving events when action bar menus are shown or hidden. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/ActionBar.OnNavigationListener` Listener interface for ActionBar navigation events. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab` A tab in the action bar. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/ActionBar.TabListener` Callback interface invoked when a tab is focused, unfocused, added, or removed. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` Display the 'home' element such that it appears as an 'up' affordance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` Show the custom view if one has been set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` Show 'home' elements in this action bar, leaving more space for other navigation elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` Show the activity title and subtitle, if present. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int` Use logo instead of icon if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_LIST:kotlin.Int` List navigation mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int` Standard navigation mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_TABS:kotlin.Int` Tab navigation mode. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActionBar#ActionBar()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#addOnMenuVisibilityListener(android.app.ActionBar.OnMenuVisibilityListener)(listener: https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener!)` Add a listener that will respond to menu visibility change events. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#addTab(android.app.ActionBar.Tab)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!)` Add a tab for use in tabbed navigation mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#addTab(android.app.ActionBar.Tab,%20kotlin.Boolean)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!, setSelected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Add a tab for use in tabbed navigation mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#addTab(android.app.ActionBar.Tab,%20kotlin.Int)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!, position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Add a tab for use in tabbed navigation mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#addTab(android.app.ActionBar.Tab,%20kotlin.Int,%20kotlin.Boolean)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!, position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, setSelected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Add a tab for use in tabbed navigation mode. |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getCustomView()()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getDisplayOptions()()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getElevation()()` Get the Z-axis elevation of the action bar in pixels. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getHeight()()` Retrieve the current height of the ActionBar. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getHideOffset()()` Return the current vertical offset of the action bar. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getNavigationItemCount()()` Get the number of navigation items present in the current navigation mode. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getNavigationMode()()` Returns the current navigation mode. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getSelectedNavigationIndex()()` Get the position of the selected navigation item in list or tabbed navigation modes. |
| abstract [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getSelectedTab()()` Returns the currently selected tab if in tabbed navigation mode and there is at least one tab present. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getSubtitle()()` Returns the current ActionBar subtitle in standard mode. |
| abstract [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getTabAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the tab at the specified index. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getTabCount()()` Returns the number of tabs currently registered with the action bar. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getThemedContext()()` Returns a `https://developer.android.com/reference/kotlin/android/content/Context.html#` with an appropriate theme for creating views that will appear in the action bar. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#getTitle()()` Returns the current ActionBar title in standard mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#hide()()` Hide the ActionBar if it is currently showing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#isHideOnContentScrollEnabled()()` Return whether the action bar is configured to scroll out of sight along with a `https://developer.android.com/reference/kotlin/android/view/View.html#setNestedScrollingEnabled(kotlin.Boolean)`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#isShowing()()` <br /> |
| abstract [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)! | `https://developer.android.com/reference/kotlin/android/app/ActionBar#newTab()()` Create and return a new `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#removeAllTabs()()` Remove all tabs from the action bar and deselect the current tab. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#removeOnMenuVisibilityListener(android.app.ActionBar.OnMenuVisibilityListener)(listener: https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener!)` Remove a menu visibility listener. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#removeTab(android.app.ActionBar.Tab)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!)` Remove a tab from the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#removeTabAt(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove a tab from the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#selectTab(android.app.ActionBar.Tab)(tab: https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!)` Select the specified tab. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setBackgroundDrawable(android.graphics.drawable.Drawable)(d: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?)` Set the ActionBar's background. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setCustomView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Set the action bar into custom navigation mode, supplying a view for custom navigation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setCustomView(android.view.View,%20android.app.ActionBar.LayoutParams)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, layoutParams: https://developer.android.com/reference/kotlin/android/app/ActionBar.LayoutParams!)` Set the action bar into custom navigation mode, supplying a view for custom navigation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setCustomView(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the action bar into custom navigation mode, supplying a view for custom navigation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayHomeAsUpEnabled(kotlin.Boolean)(showHomeAsUp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether home should be displayed as an "up" affordance. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)(options: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set display options. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)(options: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set selected display options. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowCustomEnabled(kotlin.Boolean)(showCustom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether a custom view should be displayed, if set. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowHomeEnabled(kotlin.Boolean)(showHome: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether to include the application home affordance in the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowTitleEnabled(kotlin.Boolean)(showTitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether an activity title/subtitle should be displayed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayUseLogoEnabled(kotlin.Boolean)(useLogo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether to display the activity logo rather than the activity icon. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setElevation(kotlin.Float)(elevation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the Z-axis elevation of the action bar in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHideOffset(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the current hide offset of the action bar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHideOnContentScrollEnabled(kotlin.Boolean)(hideOnContentScroll: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable hiding the action bar on content scroll. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set an alternate description for the Home/Up action, when enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.CharSequence)(description: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Set an alternate description for the Home/Up action, when enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(android.graphics.drawable.Drawable)(indicator: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set an alternate drawable to display next to the icon/logo/title when `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set an alternate drawable to display next to the icon/logo/title when `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeButtonEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable the "home" button in the corner of the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setIcon(android.graphics.drawable.Drawable)(icon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set the icon to display in the 'home' section of the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setIcon(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the icon to display in the 'home' section of the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setListNavigationCallbacks(android.widget.SpinnerAdapter,%20android.app.ActionBar.OnNavigationListener)(adapter: https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter.html#!, callback: https://developer.android.com/reference/kotlin/android/app/ActionBar.OnNavigationListener!)` Set the adapter and navigation callback for list navigation mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setLogo(android.graphics.drawable.Drawable)(logo: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set the logo to display in the 'home' section of the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setLogo(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the logo to display in the 'home' section of the action bar. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setNavigationMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the current navigation mode. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSelectedNavigationItem(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the selected navigation item in list or tabbed navigation modes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSplitBackgroundDrawable(android.graphics.drawable.Drawable)(d: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set the ActionBar's split background. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setStackedBackgroundDrawable(android.graphics.drawable.Drawable)(d: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Set the ActionBar's stacked background. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the action bar's subtitle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.CharSequence)(subtitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Set the action bar's subtitle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the action bar's title. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Set the action bar's title. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActionBar#show()()` Show the ActionBar if it is not currently showing. |

## Constants

### DISPLAY_HOME_AS_UP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_HOME_AS_UP: Int
```

Display the 'home' element such that it appears as an 'up' affordance. e.g. show an arrow to the left indicating the action that will be taken. Set this flag if selecting the 'home' button in the action bar to return up by a single level in your UI rather than back to the top level or front page.

Setting this option will implicitly enable interaction with the home/up button. See `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeButtonEnabled(kotlin.Boolean)`.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### DISPLAY_SHOW_CUSTOM

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_SHOW_CUSTOM: Int
```

Show the custom view if one has been set.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setCustomView(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### DISPLAY_SHOW_HOME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_SHOW_HOME: Int
```

Show 'home' elements in this action bar, leaving more space for other navigation elements. This includes logo and icon.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### DISPLAY_SHOW_TITLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_SHOW_TITLE: Int
```

Show the activity title and subtitle, if present.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### DISPLAY_USE_LOGO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_USE_LOGO: Int
```

Use logo instead of icon if available. This flag will cause appropriate navigation modes to use a wider logo in place of the standard icon.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### NAVIGATION_MODE_LIST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAVIGATION_MODE_LIST: Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

List navigation mode. Instead of static title text this mode presents a list menu for navigation within the activity. e.g. this might be presented to the user as a dropdown list.

 Value: 1

### NAVIGATION_MODE_STANDARD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAVIGATION_MODE_STANDARD: Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Standard navigation mode. Consists of either a logo or icon and title text with an optional subtitle. Clicking any of these elements will dispatch onOptionsItemSelected to the host Activity with a MenuItem with item ID android.R.id.home.

 Value: 0

### NAVIGATION_MODE_TABS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAVIGATION_MODE_TABS: Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Tab navigation mode. Instead of static title text this mode presents a series of tabs for navigation within the activity.

 Value: 2

## Public constructors

### ActionBar

```
ActionBar()
```

## Public methods

### addOnMenuVisibilityListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addOnMenuVisibilityListener(listener: ActionBar.OnMenuVisibilityListener!): Unit
```

Add a listener that will respond to menu visibility change events.

| Parameters ||
|---|---|
| `listener` | [ActionBar.OnMenuVisibilityListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener)!: The new listener to add |

### addTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addTab(tab: ActionBar.Tab!): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Add a tab for use in tabbed navigation mode. The tab will be added at the end of the list. If this is the first tab to be added it will become the selected tab.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: Tab to add |

### addTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addTab(
    tab: ActionBar.Tab!, 
    setSelected: Boolean
): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Add a tab for use in tabbed navigation mode. The tab will be added at the end of the list.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: Tab to add |
| `setSelected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the added tab should become the selected tab. |

### addTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addTab(
    tab: ActionBar.Tab!, 
    position: Int
): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Add a tab for use in tabbed navigation mode. The tab will be inserted at `position`. If this is the first tab to be added it will become the selected tab.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: The tab to add |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new position of the tab |

### addTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addTab(
    tab: ActionBar.Tab!, 
    position: Int, 
    setSelected: Boolean
): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Add a tab for use in tabbed navigation mode. The tab will be insterted at `position`.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: The tab to add |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new position of the tab |
| `setSelected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the added tab should become the selected tab. |

### getCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCustomView(): View!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | The current custom view. |

### getDisplayOptions

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDisplayOptions(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current set of display options. |

### getElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getElevation(): Float
```

Get the Z-axis elevation of the action bar in pixels.

The action bar's elevation is the distance it is placed from its parent surface. Higher values are closer to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Elevation value in pixels |

### getHeight

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getHeight(): Int
```

Retrieve the current height of the ActionBar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ActionBar's height |

### getHideOffset

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHideOffset(): Int
```

Return the current vertical offset of the action bar.

The action bar's current hide offset is the distance that the action bar is currently scrolled offscreen in pixels. The valid range is 0 (fully visible) to the action bar's current measured `https://developer.android.com/reference/kotlin/android/app/ActionBar#getHeight()` (fully invisible).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The action bar's offset toward its fully hidden state in pixels |

### getNavigationItemCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNavigationItemCount(): Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Get the number of navigation items present in the current navigation mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Number of navigation items. |

### getNavigationMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNavigationMode(): Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Returns the current navigation mode. The result will be one of:

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_LIST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_TABS:kotlin.Int`

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current navigation mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_LIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_TABS:kotlin.Int` |

### getSelectedNavigationIndex

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSelectedNavigationIndex(): Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Get the position of the selected navigation item in list or tabbed navigation modes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Position of the selected item. |

### getSelectedTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSelectedTab(): ActionBar.Tab!
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Returns the currently selected tab if in tabbed navigation mode and there is at least one tab present.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!` | The currently selected tab or null |

### getSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSubtitle(): CharSequence!
```

Returns the current ActionBar subtitle in standard mode. Returns null if `https://developer.android.com/reference/kotlin/android/app/ActionBar#getNavigationMode()` would not return `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The current ActionBar subtitle or null. |

### getTabAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTabAt(index: Int): ActionBar.Tab!
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Returns the tab at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index value in the range 0-get |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!` | |

### getTabCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTabCount(): Int
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Returns the number of tabs currently registered with the action bar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Tab count |

### getThemedContext

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThemedContext(): Context!
```

Returns a `https://developer.android.com/reference/kotlin/android/content/Context.html#` with an appropriate theme for creating views that will appear in the action bar. If you are inflating or instantiating custom views that will appear in an action bar, you should use the Context returned by this method. (This includes adapters used for list navigation mode.) This will ensure that views contrast properly against the action bar.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | A themed Context for creating views |

### getTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTitle(): CharSequence!
```

Returns the current ActionBar title in standard mode. Returns null if `https://developer.android.com/reference/kotlin/android/app/ActionBar#getNavigationMode()` would not return `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The current ActionBar title or null. |

### hide

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hide(): Unit
```

Hide the ActionBar if it is currently showing. If the window hosting the ActionBar does not have the feature `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int` it will resize application content to fit the new space available.

Instead of calling this function directly, you can also cause an ActionBar using the overlay feature to hide through `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`. Hiding the ActionBar through this system UI flag allows you to more seamlessly hide it in conjunction with other screen decorations.

### isHideOnContentScrollEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHideOnContentScrollEnabled(): Boolean
```

Return whether the action bar is configured to scroll out of sight along with a `https://developer.android.com/reference/kotlin/android/view/View.html#setNestedScrollingEnabled(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if hide-on-content-scroll is enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHideOnContentScrollEnabled(kotlin.Boolean)`

### isShowing

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isShowing(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the ActionBar is showing, `false` otherwise. |

### newTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun newTab(): ActionBar.Tab!
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Create and return a new `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab`. This tab will not be included in the action bar until it is added.

Very often tabs will be used to switch between `https://developer.android.com/reference/kotlin/android/app/Fragment` objects. Here is a typical implementation of such tabs:

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab!` | A new Tab |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#addTab(android.app.ActionBar.Tab)`

### removeAllTabs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeAllTabs(): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Remove all tabs from the action bar and deselect the current tab.

### removeOnMenuVisibilityListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeOnMenuVisibilityListener(listener: ActionBar.OnMenuVisibilityListener!): Unit
```

Remove a menu visibility listener. This listener will no longer receive menu visibility change events.

| Parameters ||
|---|---|
| `listener` | [ActionBar.OnMenuVisibilityListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener)!: A listener to remove that was previously added |

### removeTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeTab(tab: ActionBar.Tab!): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Remove a tab from the action bar. If the removed tab was selected it will be deselected and another tab will be selected if present.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: The tab to remove |

### removeTabAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeTabAt(position: Int): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Remove a tab from the action bar. If the removed tab was selected it will be deselected and another tab will be selected if present.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Position of the tab to remove |

### selectTab

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun selectTab(tab: ActionBar.Tab!): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Select the specified tab. If it is not a child of this action bar it will be added.

Note: If you want to select by index, use `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSelectedNavigationItem(kotlin.Int)`.

| Parameters ||
|---|---|
| `tab` | [ActionBar.Tab](https://developer.android.com/reference/kotlin/android/app/ActionBar.Tab)!: Tab to select |

### setBackgroundDrawable

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setBackgroundDrawable(d: Drawable?): Unit
```

Set the ActionBar's background. This will be used for the primary action bar.

| Parameters ||
|---|---|
| `d` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?: Background drawable. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setStackedBackgroundDrawable(android.graphics.drawable.Drawable)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSplitBackgroundDrawable(android.graphics.drawable.Drawable)`

### setCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCustomView(view: View!): Unit
```

Set the action bar into custom navigation mode, supplying a view for custom navigation. Custom navigation views appear between the application icon and any action buttons and may use any space available there. Common use cases for custom navigation views might include an auto-suggesting address bar for a browser or other navigation mechanisms that do not translate well to provided navigation modes.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: Custom navigation view to place in the ActionBar. |

### setCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCustomView(
    view: View!, 
    layoutParams: ActionBar.LayoutParams!
): Unit
```

Set the action bar into custom navigation mode, supplying a view for custom navigation.

Custom navigation views appear between the application icon and any action buttons and may use any space available there. Common use cases for custom navigation views might include an auto-suggesting address bar for a browser or other navigation mechanisms that do not translate well to provided navigation modes.

The display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` must be set for the custom view to be displayed.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: Custom navigation view to place in the ActionBar. |
| `layoutParams` | [ActionBar.LayoutParams](https://developer.android.com/reference/kotlin/android/app/ActionBar.LayoutParams)!: How this custom view should layout in the bar. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setCustomView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCustomView(resId: Int): Unit
```

Set the action bar into custom navigation mode, supplying a view for custom navigation.

Custom navigation views appear between the application icon and any action buttons and may use any space available there. Common use cases for custom navigation views might include an auto-suggesting address bar for a browser or other navigation mechanisms that do not translate well to provided navigation modes.

The display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` must be set for the custom view to be displayed.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a layout to inflate into the ActionBar. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setDisplayHomeAsUpEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayHomeAsUpEnabled(showHomeAsUp: Boolean): Unit
```

Set whether home should be displayed as an "up" affordance. Set this to true if selecting "home" returns up by a single level in your UI rather than back to the top level or front page.

To set several display options at once, see the setDisplayOptions methods.

| Parameters ||
|---|---|
| `showHomeAsUp` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to show the user that selecting home will return one level up rather than to the top level of the app. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setDisplayOptions

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayOptions(options: Int): Unit
```

Set display options. This changes all display option bits at once. To change a limited subset of display options, see `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A combination of the bits defined by the DISPLAY_ constants defined in ActionBar. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` |

### setDisplayOptions

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayOptions(
    options: Int, 
    mask: Int
): Unit
```

Set selected display options. Only the options specified by mask will be changed. To change all display option bits at once, see `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`.

Example: setDisplayOptions(0, DISPLAY_SHOW_HOME) will disable the `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` option. setDisplayOptions(DISPLAY_SHOW_HOME, DISPLAY_SHOW_HOME | DISPLAY_USE_LOGO) will enable `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` and disable `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int`.

| Parameters ||
|---|---|
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A combination of the bits defined by the DISPLAY_ constants defined in ActionBar. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bit mask declaring which display options should be changed. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_CUSTOM:kotlin.Int` |

### setDisplayShowCustomEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayShowCustomEnabled(showCustom: Boolean): Unit
```

Set whether a custom view should be displayed, if set.

To set several display options at once, see the setDisplayOptions methods.

| Parameters ||
|---|---|
| `showCustom` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the currently set custom view should be displayed, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setDisplayShowHomeEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayShowHomeEnabled(showHome: Boolean): Unit
```

Set whether to include the application home affordance in the action bar. Home is presented as either an activity icon or logo.

To set several display options at once, see the setDisplayOptions methods.

| Parameters ||
|---|---|
| `showHome` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to show home, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setDisplayShowTitleEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayShowTitleEnabled(showTitle: Boolean): Unit
```

Set whether an activity title/subtitle should be displayed.

To set several display options at once, see the setDisplayOptions methods.

| Parameters ||
|---|---|
| `showTitle` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to display a title/subtitle if present. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setDisplayUseLogoEnabled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDisplayUseLogoEnabled(useLogo: Boolean): Unit
```

Set whether to display the activity logo rather than the activity icon. A logo is often a wider, more detailed image.

To set several display options at once, see the setDisplayOptions methods.

| Parameters ||
|---|---|
| `useLogo` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to use the activity logo, false to use the activity icon. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setElevation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setElevation(elevation: Float): Unit
```

Set the Z-axis elevation of the action bar in pixels.

The action bar's elevation is the distance it is placed from its parent surface. Higher values are closer to the user.

| Parameters ||
|---|---|
| `elevation` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Elevation value in pixels |

### setHideOffset

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHideOffset(offset: Int): Unit
```

Set the current hide offset of the action bar.

The action bar's current hide offset is the distance that the action bar is currently scrolled offscreen in pixels. The valid range is 0 (fully visible) to the action bar's current measured `https://developer.android.com/reference/kotlin/android/app/ActionBar#getHeight()` (fully invisible).

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action bar's offset toward its fully hidden state in pixels. |

### setHideOnContentScrollEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHideOnContentScrollEnabled(hideOnContentScroll: Boolean): Unit
```

Enable hiding the action bar on content scroll.

If enabled, the action bar will scroll out of sight along with a `https://developer.android.com/reference/kotlin/android/view/View.html#setNestedScrollingEnabled(kotlin.Boolean)` view's content. The action bar must be in `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int` to enable hiding on content scroll.

When partially scrolled off screen the action bar is considered `https://developer.android.com/reference/kotlin/android/app/ActionBar#hide()`. A call to `https://developer.android.com/reference/kotlin/android/app/ActionBar#show()` will cause it to return to full view.

| Parameters ||
|---|---|
| `hideOnContentScroll` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable hiding on content scroll. |

### setHomeActionContentDescription

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHomeActionContentDescription(resId: Int): Unit
```

Set an alternate description for the Home/Up action, when enabled.

This description is commonly used for accessibility/screen readers when the Home action is enabled. (See `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayHomeAsUpEnabled(kotlin.Boolean)`.) Examples of this are, "Navigate Home" or "Navigate Up" depending on the `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` display option. If you have changed the home-as-up indicator using `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(kotlin.Int)` to indicate more specific functionality such as a sliding drawer, you should also set this to accurately describe the action.

Setting this to `0` will use the system default description.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a string to use as the new description for the Home action when enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(android.graphics.drawable.Drawable)`

### setHomeActionContentDescription

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHomeActionContentDescription(description: CharSequence!): Unit
```

Set an alternate description for the Home/Up action, when enabled.

This description is commonly used for accessibility/screen readers when the Home action is enabled. (See `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayHomeAsUpEnabled(kotlin.Boolean)`.) Examples of this are, "Navigate Home" or "Navigate Up" depending on the `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` display option. If you have changed the home-as-up indicator using `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(kotlin.Int)` to indicate more specific functionality such as a sliding drawer, you should also set this to accurately describe the action.

Setting this to `null` will use the system default description.

| Parameters ||
|---|---|
| `description` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: New description for the Home action when enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeAsUpIndicator(android.graphics.drawable.Drawable)`

### setHomeAsUpIndicator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHomeAsUpIndicator(indicator: Drawable!): Unit
```

Set an alternate drawable to display next to the icon/logo/title when `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` is enabled. This can be useful if you are using this mode to display an alternate selection for up navigation, such as a sliding drawer.

If you pass `null` to this method, the default drawable from the theme will be used.

If you implement alternate or intermediate behavior around Up, you should also call `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.Int)` to provide a correct description of the action for accessibility support.

| Parameters ||
|---|---|
| `indicator` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!: A drawable to use for the up indicator, or null to use the theme's default |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayHomeAsUpEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.Int)`

### setHomeAsUpIndicator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHomeAsUpIndicator(resId: Int): Unit
```

Set an alternate drawable to display next to the icon/logo/title when `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` is enabled. This can be useful if you are using this mode to display an alternate selection for up navigation, such as a sliding drawer.

If you pass `0` to this method, the default drawable from the theme will be used.

If you implement alternate or intermediate behavior around Up, you should also call `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.Int)` to provide a correct description of the action for accessibility support.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a drawable to use for the up indicator, or null to use the theme's default |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayHomeAsUpEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setHomeActionContentDescription(kotlin.Int)`

### setHomeButtonEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHomeButtonEnabled(enabled: Boolean): Unit
```

Enable or disable the "home" button in the corner of the action bar. (Note that this is the application home/up affordance on the action bar, not the systemwide home button.)

This defaults to true for packages targeting \< API 14. For packages targeting API 14 or greater, the application should call this method to enable interaction with the home/up affordance.

Setting the `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_HOME_AS_UP:kotlin.Int` display option will automatically enable the home button.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable the home button, false to disable the home button. |

### setIcon

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setIcon(icon: Drawable!): Unit
```

Set the icon to display in the 'home' section of the action bar. The action bar will use an icon specified by its style or the activity icon by default. Whether the home section shows an icon or logo is controlled by the display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int`.

| Parameters ||
|---|---|
| `icon` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!: Drawable to show as an icon. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayUseLogoEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowHomeEnabled(kotlin.Boolean)`

### setIcon

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setIcon(resId: Int): Unit
```

Set the icon to display in the 'home' section of the action bar. The action bar will use an icon specified by its style or the activity icon by default. Whether the home section shows an icon or logo is controlled by the display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int`.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a drawable to show as an icon. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayUseLogoEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowHomeEnabled(kotlin.Boolean)`

### setListNavigationCallbacks

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setListNavigationCallbacks(
    adapter: SpinnerAdapter!, 
    callback: ActionBar.OnNavigationListener!
): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Set the adapter and navigation callback for list navigation mode. The supplied adapter will provide views for the expanded list as well as the currently selected item. (These may be displayed differently.) The supplied OnNavigationListener will alert the application when the user changes the current list selection.

| Parameters ||
|---|---|
| `adapter` | [SpinnerAdapter](https://developer.android.com/reference/kotlin/android/widget/SpinnerAdapter.html#)!: An adapter that will provide views both to display the current navigation selection and populate views within the dropdown navigation menu. |
| `callback` | [ActionBar.OnNavigationListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnNavigationListener)!: An OnNavigationListener that will receive events when the user selects a navigation item. |

### setLogo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setLogo(logo: Drawable!): Unit
```

Set the logo to display in the 'home' section of the action bar. The action bar will use a logo specified by its style or the activity logo by default. Whether the home section shows an icon or logo is controlled by the display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int`.

| Parameters ||
|---|---|
| `logo` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!: Drawable to show as a logo. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayUseLogoEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowHomeEnabled(kotlin.Boolean)`

### setLogo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setLogo(resId: Int): Unit
```

Set the logo to display in the 'home' section of the action bar. The action bar will use a logo specified by its style or the activity logo by default. Whether the home section shows an icon or logo is controlled by the display option `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_USE_LOGO:kotlin.Int`.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of a drawable to show as a logo. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayUseLogoEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayShowHomeEnabled(kotlin.Boolean)`

### setNavigationMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setNavigationMode(mode: Int): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Set the current navigation mode.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new mode to set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_LIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_TABS:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_STANDARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_LIST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#NAVIGATION_MODE_TABS:kotlin.Int`

### setSelectedNavigationItem

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSelectedNavigationItem(position: Int): Unit
```

**Deprecated:** *Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.*

Set the selected navigation item in list or tabbed navigation modes.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Position of the item to select. |

### setSplitBackgroundDrawable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSplitBackgroundDrawable(d: Drawable!): Unit
```

Set the ActionBar's split background. This will appear in the split action bar containing menu-provided action buttons on some devices and configurations.

You can enable split action bar with `https://developer.android.com/reference/kotlin/android/R.attr.html#uiOptions:kotlin.Int`

| Parameters ||
|---|---|
| `d` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!: Background drawable for the split bar |

### setStackedBackgroundDrawable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStackedBackgroundDrawable(d: Drawable!): Unit
```

Set the ActionBar's stacked background. This will appear in the second row/stacked bar on some devices and configurations.

| Parameters ||
|---|---|
| `d` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!: Background drawable for the stacked row |

### setSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSubtitle(resId: Int): Unit
```

Set the action bar's subtitle. This will only be displayed if `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` is set.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of subtitle string to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setSubtitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSubtitle(subtitle: CharSequence!): Unit
```

Set the action bar's subtitle. This will only be displayed if `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` is set. Set to null to disable the subtitle entirely.

| Parameters ||
|---|---|
| `subtitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Subtitle to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setSubtitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitle(resId: Int): Unit
```

Set the action bar's title. This will only be displayed if `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` is set.

| Parameters ||
|---|---|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Resource ID of title string to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### setTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTitle(title: CharSequence!): Unit
```

Set the action bar's title. This will only be displayed if `https://developer.android.com/reference/kotlin/android/app/ActionBar#DISPLAY_SHOW_TITLE:kotlin.Int` is set.

| Parameters ||
|---|---|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Title to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setTitle(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/ActionBar#setDisplayOptions(kotlin.Int,%20kotlin.Int)`

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun show(): Unit
```

Show the ActionBar if it is not currently showing. If the window hosting the ActionBar does not have the feature `https://developer.android.com/reference/kotlin/android/view/Window.html#FEATURE_ACTION_BAR_OVERLAY:kotlin.Int` it will resize application content to fit the new space available.

If you are hiding the ActionBar through `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int`, you should not call this function directly.
