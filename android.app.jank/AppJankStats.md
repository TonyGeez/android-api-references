# AppJankStats

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppJankStats

Kotlin| [Java](AppJankStats.md) 
| --- | --- |

```
class AppJankStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.jank.AppJankStats](AppJankStats.md) |

This class stores detailed jank statistics for an individual UI widget. These statistics provide performance insights for specific UI widget states by correlating the number of "Janky frames" with the total frames rendered while the widget is in that state. This class can be used by library widgets to provide the system with more detailed information about where jank is happening for diagnostic purposes.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_ANIMATION](AppJankStats.md) UI elements that facilitate playing animations. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_KEYBOARD](AppJankStats.md) UI elements that facilitate displaying, hiding or interacting with keyboard. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_MEDIA](AppJankStats.md) UI elements that facilitate media playback. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_NAVIGATION](AppJankStats.md) UI elements that facilitate in-app navigation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_OTHER](AppJankStats.md) UI elements that don't fall in one or any of the other categories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_SCROLL](AppJankStats.md) UI elements that facilitate scrolling. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_CATEGORY_UNSPECIFIED](AppJankStats.md) Used to indicate no widget category has been set. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_ANIMATING](AppJankStats.md) Used to indicate the UI element is currently animating. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_DRAGGING](AppJankStats.md) Used to indicate the UI element is currently being dragged. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_FLINGING](AppJankStats.md) Used to indicate the UI element is currently being flung. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_NONE](AppJankStats.md) Used to indicate the UI element currently has no state and is idle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_PLAYBACK](AppJankStats.md) Used to indicate the UI element is currently playing media. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_PREDICTIVE_BACK](AppJankStats.md) Used to indicate predictive back navigation is currently being used |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_SCROLLING](AppJankStats.md) Used to indicate the UI element is currently scrolling. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_SWIPING](AppJankStats.md) Used to indicate the UI element is currently being swiped. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_TAPPING](AppJankStats.md) Used to indicate the UI element is currently being tapped on, for example on a keyboard. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_UNSPECIFIED](AppJankStats.md) Used to indicate no widget state has been set. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WIDGET_STATE_ZOOMING](AppJankStats.md) Used to indicate the UI element is currently zooming. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppJankStats](AppJankStats.md))`(`appUid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `widgetId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `navigationComponent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `widgetCategory:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `widgetState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `totalFrames:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `jankyFrames:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `relativeFrameTimeHistogram:` ` [RelativeFrameTimeHistogram](RelativeFrameTimeHistogram.md)`)` Creates a new AppJankStats object. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getJankyFrameCount](AppJankStats.md))`()` Returns the number of frames that were determined to be janky for this stat. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getNavigationComponent](AppJankStats.md))`()` Returns the navigation component if it exists that this stat applies to. |
| [RelativeFrameTimeHistogram](RelativeFrameTimeHistogram.md) | [getRelativeFrameTimeHistogram](AppJankStats.md))`()` Returns a Histogram containing relative frame times in millis grouped into predefined buckets. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalFrameCount](AppJankStats.md))`()` Returns the total number of frames counted for this stat. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUid](AppJankStats.md))`()` Returns the app uid. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getWidgetCategory](AppJankStats.md))`()` Returns the category that the widget's functionality generally falls into, or [WIDGET_CATEGORY_UNSPECIFIED](AppJankStats.md) if no value was passed in. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getWidgetId](AppJankStats.md))`()` Returns the id of the widget that reported state changes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getWidgetState](AppJankStats.md))`()` Returns the widget's state that was reported for this stat, or [WIDGET_STATE_UNSPECIFIED](AppJankStats.md) if no value was passed in. |

## Constants

### WIDGET_CATEGORY_ANIMATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_ANIMATION: String
```

UI elements that facilitate playing animations. 

 Value: "animation"

### WIDGET_CATEGORY_KEYBOARD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_KEYBOARD: String
```

UI elements that facilitate displaying, hiding or interacting with keyboard. 

 Value: "keyboard"

### WIDGET_CATEGORY_MEDIA

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_MEDIA: String
```

UI elements that facilitate media playback. 

 Value: "media"

### WIDGET_CATEGORY_NAVIGATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_NAVIGATION: String
```

UI elements that facilitate in-app navigation. 

 Value: "navigation"

### WIDGET_CATEGORY_OTHER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_OTHER: String
```

UI elements that don't fall in one or any of the other categories. 

 Value: "other"

### WIDGET_CATEGORY_SCROLL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_SCROLL: String
```

UI elements that facilitate scrolling. 

 Value: "scroll"

### WIDGET_CATEGORY_UNSPECIFIED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_CATEGORY_UNSPECIFIED: String
```

Used to indicate no widget category has been set. 

 Value: "unspecified"

### WIDGET_STATE_ANIMATING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_ANIMATING: String
```

Used to indicate the UI element is currently animating. 

 Value: "animating"

### WIDGET_STATE_DRAGGING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_DRAGGING: String
```

Used to indicate the UI element is currently being dragged. 

 Value: "dragging"

### WIDGET_STATE_FLINGING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_FLINGING: String
```

Used to indicate the UI element is currently being flung. 

 Value: "flinging"

### WIDGET_STATE_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_NONE: String
```

Used to indicate the UI element currently has no state and is idle. 

 Value: "none"

### WIDGET_STATE_PLAYBACK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_PLAYBACK: String
```

Used to indicate the UI element is currently playing media. 

 Value: "playback"

### WIDGET_STATE_PREDICTIVE_BACK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_PREDICTIVE_BACK: String
```

Used to indicate predictive back navigation is currently being used 

 Value: "predictive_back"

### WIDGET_STATE_SCROLLING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_SCROLLING: String
```

Used to indicate the UI element is currently scrolling. 

 Value: "scrolling"

### WIDGET_STATE_SWIPING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_SWIPING: String
```

Used to indicate the UI element is currently being swiped. 

 Value: "swiping"

### WIDGET_STATE_TAPPING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_TAPPING: String
```

Used to indicate the UI element is currently being tapped on, for example on a keyboard. 

 Value: "tapping"

### WIDGET_STATE_UNSPECIFIED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_UNSPECIFIED: String
```

Used to indicate no widget state has been set. 

 Value: "unspecified"

### WIDGET_STATE_ZOOMING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDGET_STATE_ZOOMING: String
```

Used to indicate the UI element is currently zooming. 

 Value: "zooming"

## Public constructors

### AppJankStats

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppJankStats(
    appUid: Int, 
    widgetId: String, 
    navigationComponent: String?, 
    widgetCategory: String?, 
    widgetState: String?, 
    totalFrames: Long, 
    jankyFrames: Long, 
    relativeFrameTimeHistogram: RelativeFrameTimeHistogram)
```

Creates a new AppJankStats object.

| Parameters ||
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appUid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Uid of the App that is collecting jank stats. |
| `widgetId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the widget id that frames will be associated to. This value cannot be`null`. |
| `navigationComponent` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the intended navigation target within the activity, this could be a navigation destination, screen and/or pane. This value may be`null`. |
| --- | --- |
| `widgetCategory` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a category used to organize widgets in a structured way that indicates they serve a similar purpose or perform related functions. Must be prefixed with WIDGET_CATEGORY_ and have a suffix of one of the following:SCROLL, ANIMATION, MEDIA, NAVIGATION, KEYBOARD, OTHER or will be set to UNSPECIFIED if no value is passed. This value may be`null`. Value is [android.app.jank.AppJankStats#WIDGET_CATEGORY_UNSPECIFIED](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_SCROLL](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_ANIMATION](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_MEDIA](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_NAVIGATION](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_KEYBOARD](AppJankStats.md), or [android.app.jank.AppJankStats#WIDGET_CATEGORY_OTHER](AppJankStats.md) |
| `widgetState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the state the widget was in while frames were counted. Must be prefixed with WIDGET_STATE_ and have a suffix of one of the following: NONE, SCROLLING, FLINGING, SWIPING, DRAGGING, ZOOMING, ANIMATING, PLAYBACK, TAPPING, PREDICTIVE_BACK or will be set to WIDGET_STATE_UNSPECIFIED if no value is passed. This value may be`null`. Value is [android.app.jank.AppJankStats#WIDGET_STATE_UNSPECIFIED](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_NONE](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_SCROLLING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_FLINGING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_SWIPING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_DRAGGING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_ZOOMING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_ANIMATING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_PLAYBACK](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_TAPPING](AppJankStats.md), or [android.app.jank.AppJankStats#WIDGET_STATE_PREDICTIVE_BACK](AppJankStats.md) |
| `totalFrames` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the total number of frames that were counted for this stat. |
| --- | --- |
| `jankyFrames` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the total number of janky frames that were counted for this stat. |
| `relativeFrameTimeHistogram` | [RelativeFrameTimeHistogram](RelativeFrameTimeHistogram.md):the histogram with predefined buckets. See [getRelativeFrameTimeHistogram()](AppJankStats.md))for details. This value cannot be`null`. |

## Public methods

### getJankyFrameCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getJankyFrameCount(): Long
```

Returns the number of frames that were determined to be janky for this stat.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of frames that were determined to be janky for this stat. |

### getNavigationComponent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNavigationComponent(): String?
```

Returns the navigation component if it exists that this stat applies to.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the navigation component if it exists that this stat applies to. This value may be`null`. |

### getRelativeFrameTimeHistogram

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRelativeFrameTimeHistogram(): RelativeFrameTimeHistogram
```

Returns a Histogram containing relative frame times in millis grouped into predefined buckets. See [RelativeFrameTimeHistogram](RelativeFrameTimeHistogram.md) for more information.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [RelativeFrameTimeHistogram](RelativeFrameTimeHistogram.md) | Histogram containing relative frame times in predefined buckets. This value cannot be null. |

### getTotalFrameCount

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTotalFrameCount(): Long
```

Returns the total number of frames counted for this stat.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total number of frames counted for this stat. |

### getUid

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUid(): Int
```

Returns the app uid.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the app uid. |

### getWidgetCategory

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidgetCategory(): String
```

Returns the category that the widget's functionality generally falls into, or [WIDGET_CATEGORY_UNSPECIFIED](AppJankStats.md) if no value was passed in.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the category that the widget's functionality generally falls into, this value cannot be null. Value is [android.app.jank.AppJankStats#WIDGET_CATEGORY_UNSPECIFIED](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_SCROLL](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_ANIMATION](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_MEDIA](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_NAVIGATION](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_CATEGORY_KEYBOARD](AppJankStats.md), or [android.app.jank.AppJankStats#WIDGET_CATEGORY_OTHER](AppJankStats.md) |

### getWidgetId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidgetId(): String
```

Returns the id of the widget that reported state changes.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the id of the widget that reported state changes. This value cannot be null. |

### getWidgetState

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidgetState(): String
```

Returns the widget's state that was reported for this stat, or [WIDGET_STATE_UNSPECIFIED](AppJankStats.md) if no value was passed in.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the widget's state that was reported for this stat. This value cannot be null. Value is [android.app.jank.AppJankStats#WIDGET_STATE_UNSPECIFIED](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_NONE](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_SCROLLING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_FLINGING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_SWIPING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_DRAGGING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_ZOOMING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_ANIMATING](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_PLAYBACK](AppJankStats.md), [android.app.jank.AppJankStats#WIDGET_STATE_TAPPING](AppJankStats.md), or [android.app.jank.AppJankStats#WIDGET_STATE_PREDICTIVE_BACK](AppJankStats.md) |
