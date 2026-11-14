Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteViews

```
open class RemoteViews : LayoutInflater.Filter, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.RemoteViews](RemoteViews.md) |

A class that describes a view hierarchy that can be displayed in another process. The hierarchy is inflated from a layout resource file, and this class provides some basic operations for modifying the content of the inflated hierarchy.

`RemoteViews` is limited to support for the following layouts:

- AdapterViewFlipper
- FrameLayout
- GridLayout
- GridView
- LinearLayout
- ListView
- RelativeLayout
- StackView
- ViewFlipper

And the following widgets:

- AnalogClock
- Button
- Chronometer
- ImageButton
- ImageView
- ProgressBar
- TextClock
- TextView

As of API 31, the following widgets and layouts may also be used:

- CheckBox
- RadioButton
- RadioGroup
- Switch

Descendants of these classes are not supported.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.ActionException` Exception to send when something goes wrong executing an action |
| | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` A data parcel that carries the instructions to draw the RemoteViews, as an alternative to XML layout. |
| | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteCollectionItems` Representation of a fixed list of items to be displayed in a RemoteViews collection. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` Class representing a response to an action performed on any element of a RemoteViews. |
| | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteView` This annotation indicates that a subclass of View is allowed to be used with the RemoteViews mechanism. |
| | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteViewOutlineProvider` OutlineProvider for a view with a radius set by setViewOutlinePreferredRadius. |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#EXTRA_CHECKED:kotlin.String` The intent extra for whether the view whose checked state changed is currently checked. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#EXTRA_SHARED_ELEMENT_BOUNDS:kotlin.String` The intent extra that contains the bounds for all shared elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_BOTTOM:kotlin.Int` The value will apply to the marginBottom. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` The value will apply to the marginEnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_LEFT:kotlin.Int` The value will apply to the marginLeft. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_RIGHT:kotlin.Int` The value will apply to the marginRight. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_START:kotlin.Int` The value will apply to the marginStart. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_TOP:kotlin.Int` The value will apply to the marginTop. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| RemoteViews Reads a RemoteViews object from a parcel. |
| RemoteViews Creates a copy of another RemoteViews. |
| RemoteViews Create a new RemoteViews object that will inflate as the specified landspace or portrait RemoteViews, depending on the current configuration. |
| RemoteViews Instantiates a RemoteViews object using `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions`, which serves as an alternative to XML layout. |
| RemoteViews Create a new RemoteViews object that will display the views contained in the specified layout file. |
| RemoteViews Create a new RemoteViews object that will display the views contained in the specified layout file and change the id of the root view to the specified one. |
| RemoteViews Create a new RemoteViews object that will inflate the layout with the closest size specification. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addStableView Equivalent to calling addView after inflating the given RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addView Equivalent to calling addView after inflating the given RemoteViews. |
| open [View](../android.view/View.md)! | apply Inflates the view hierarchy represented by this object and applies all of the actions. |
| --- | --- |
| open [RemoteViews](RemoteViews.md)! | clone Returns a deep copy of the RemoteViews object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [RemoteViews.DrawInstructions](../android/widget/RemoteViews.DrawInstructions.md)? | getDrawInstructions Returns the `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` associated with this RemoteViews, if any. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLayoutId Returns the layout id of the root layout associated with this RemoteViews. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getPackage <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getViewId Get the ID of the top-level view of the XML layout, if set using RemoteViews. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onLoadClass Used to restrict the views which can be inflated |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reapply Applies all of the actions to the provided view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeAllViews Equivalent to calling removeAllViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityTraversalAfter Equivalent to calling setAccessibilityTraversalAfter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAccessibilityTraversalBefore Equivalent to calling setAccessibilityTraversalBefore. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAppWidgetEventTag Set a view tag associating a View with an ID to be used for widget interaction usage events (`https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent.html#`). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBitmap Call a method taking one Bitmap on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBlendMode Call a method taking one BlendMode on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBoolean Call a method taking one boolean on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBundle Call a method taking one Bundle on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setByte Call a method taking one byte on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setChar Call a method taking one char on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCharSequence Call a method taking one CharSequence on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCharSequence Call a method taking one CharSequence on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCharSequenceAttr Call a method taking one CharSequence on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setChronometer Equivalent to calling setBase, setFormat, and start or stop. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setChronometerCountDown Equivalent to calling setCountDown on the chronometer with the given viewId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColor Call a method taking one int, a color, on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorAttr Call a method taking one int, a color, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorInt Call a method taking one int, a color, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorStateList Call a method taking one ColorStateList on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorStateList Call a method taking one ColorStateList on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorStateList Call a method taking one ColorStateList on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorStateListAttr Call a method taking one ColorStateList on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCompoundButtonChecked Equivalent to calling setChecked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setContentDescription Equivalent to calling View. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDisplayedChild Equivalent to calling setDisplayedChild |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDouble Call a method taking one double on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setEmptyView Equivalent to calling setEmptyView |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFloat Call a method taking one float on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFloatDimen Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFloatDimen Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFloatDimenAttr Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIcon Call a method taking one Icon on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIcon Call a method taking one Icon on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageViewBitmap Equivalent to calling setImageBitmap |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageViewIcon Equivalent to calling setImageIcon |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageViewResource Equivalent to calling setImageResource |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setImageViewUri Equivalent to calling setImageURI |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInt Call a method taking one int on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIntDimen Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIntDimen Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIntDimenAttr Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIntent Call a method taking one Intent on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLabelFor Equivalent to calling setLabelFor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLightBackgroundLayoutId Provides an alternate layout ID, which can be used to inflate this view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLong Call a method taking one long on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnCheckedChangeResponse Equivalent to calling setOnCheckedChangeListener to launch the provided `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnClickFillInIntent When using collections (eg. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnClickPendingIntent Equivalent to calling setOnClickListener to launch the provided `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnClickResponse Equivalent of calling setOnClickListener to launch the provided `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnStylusHandwritingPendingIntent Equivalent to calling setHandwritingDelegatorCallback to send the provided `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPendingIntentTemplate When using collections (eg. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setProgressBar Equivalent to calling setMax, android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRadioGroupChecked Equivalent to calling check. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRelativeScrollPosition Equivalent to calling smoothScrollByOffset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRemoteAdapter Equivalent to calling setRemoteViewsAdapter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRemoteAdapter Creates a simple Adapter for the viewId specified. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRemoteAdapter Equivalent to calling setRemoteViewsAdapter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setScrollPosition Equivalent to calling smoothScrollToPosition. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setShort Call a method taking one short on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setString Call a method taking one String on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextColor Equivalent to calling setTextColor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextViewCompoundDrawables Equivalent to calling setCompoundDrawablesWithIntrinsicBounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextViewCompoundDrawablesRelative Equivalent to calling setCompoundDrawablesRelativeWithIntrinsicBounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextViewText Equivalent to calling setText |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTextViewTextSize Equivalent to calling setTextSize |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setUri Call a method taking one Uri on a view in the layout for this RemoteViews. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutHeight Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` except that you may provide the value in any dimension units. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutHeightAttr Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` with the value of the given attribute in the current theme. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutHeightDimen Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` with the result of getDimensionPixelSize. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutMargin Equivalent to calling setMarginEnd. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutMarginAttr Equivalent to calling setMarginEnd. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutMarginDimen Equivalent to calling setMarginEnd. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutWidth Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` except that you may provide the value in any dimension units. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutWidthAttr Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` with the value of the given attribute in the current theme. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewLayoutWidthDimen Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` with the result of getDimensionPixelSize. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewOutlinePreferredRadius Sets an OutlineProvider on the view whose corner radius is a dimension calculated using applyDimension. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewOutlinePreferredRadiusAttr Sets an OutlineProvider on the view whose corner radius is a dimension attribute with `attrId`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewOutlinePreferredRadiusDimen Sets an OutlineProvider on the view whose corner radius is a dimension resource with `resId`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewPadding Equivalent to calling setPadding. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewPadding Equivalent to calling setPadding. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setViewVisibility Equivalent to calling setVisibility |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | showNext Equivalent to calling showNext |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | showPrevious Equivalent to calling showPrevious |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RemoteViews](RemoteViews.md)!\> | `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#CREATOR:android.os.Parcelable.Creator` Parcelable. |

## Constants

### EXTRA_CHECKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHECKED: String
```

The intent extra for whether the view whose checked state changed is currently checked.

 Value: "android.widget.extra.CHECKED"

### EXTRA_SHARED_ELEMENT_BOUNDS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SHARED_ELEMENT_BOUNDS: String
```

The intent extra that contains the bounds for all shared elements.

 Value: "android.widget.extra.SHARED_ELEMENT_BOUNDS"

### MARGIN_BOTTOM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_BOTTOM: Int
```

The value will apply to the marginBottom.

 Value: 3

### MARGIN_END

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_END: Int
```

The value will apply to the marginEnd.

 Value: 5

### MARGIN_LEFT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_LEFT: Int
```

The value will apply to the marginLeft.

 Value: 0

### MARGIN_RIGHT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_RIGHT: Int
```

The value will apply to the marginRight.

 Value: 2

### MARGIN_START

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_START: Int
```

The value will apply to the marginStart.

 Value: 4

### MARGIN_TOP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARGIN_TOP: Int
```

The value will apply to the marginTop.

 Value: 1

## Public constructors

### RemoteViews

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(parcel: Parcel!)
```

Reads a RemoteViews object from a parcel.

| Parameters ||
|---|---|
| `parcel` | [Parcel](../android.os/Parcel.md)!: the parcel object |

### RemoteViews

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(src: RemoteViews!)
```

Creates a copy of another RemoteViews.

### RemoteViews

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(
    landscape: RemoteViews!, 
    portrait: RemoteViews!)
```

Create a new RemoteViews object that will inflate as the specified landspace or portrait RemoteViews, depending on the current configuration.

| Parameters ||
|---|---|
| `landscape` | [RemoteViews](RemoteViews.md)!: The RemoteViews to inflate in landscape configuration |
| `portrait` | [RemoteViews](RemoteViews.md)!: The RemoteViews to inflate in portrait configuration |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if either landscape or portrait are null or if they are not from the same application |

### RemoteViews

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(drawInstructions: RemoteViews.DrawInstructions)
```

Instantiates a RemoteViews object using `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions`, which serves as an alternative to XML layout. `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` objects contains the instructions which can be interpreted and rendered accordingly in the host process.

**Size Limits \& Mixing Restrictions:**

- A `RemoteViews` created with `DrawInstructions` must not contain nested child `RemoteViews` (e.g. added via addView), and it cannot be added as a nested child of another classic XML-based `RemoteViews` using addView.
- It cannot be included as an item in remote collections (e.g., added to `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteCollectionItems`).
- Sized `RemoteViews` (RemoteViews) and landscape/portrait configurations (RemoteViews) are supported as long as they are not mixed; all individual configurations must either be classic XML-based `RemoteViews` or all must contain `DrawInstructions`.
- The total raw byte size of the `DrawInstructions` payload must not exceed the strict limit of 21MB (defined by `AppWidgetServiceImpl.MAX_REMOTE_COMPOSE_SIZE`). Exceeding this limit or violating the mixing rules will cause an `IllegalArgumentException` to be thrown at runtime.

| Parameters ||
|---|---|
| `drawInstructions` | [RemoteViews.DrawInstructions](../android/widget/RemoteViews.DrawInstructions.md): The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` object. This value cannot be `null`. |

### RemoteViews

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(
    packageName: String!, 
    layoutId: Int)
```

Create a new RemoteViews object that will display the views contained in the specified layout file.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the package that contains the layout resource |
| `layoutId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the layout resource |

### RemoteViews

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(
    packageName: String, 
    layoutId: Int, 
    viewId: Int)
```

Create a new RemoteViews object that will display the views contained in the specified layout file and change the id of the root view to the specified one.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package that contains the layout resource. This value cannot be `null`. |
| `layoutId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the layout resource |

### RemoteViews

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteViews(remoteViews: MutableMap<SizeF!, RemoteViews!>)
```

Create a new RemoteViews object that will inflate the layout with the closest size specification. The default remote views in that case is always the one with the smallest area. If the RemoteViews host provides the size of the view, the layout with the largest area that fits entirely in the provided size will be used (i.e. the width and height of the layout must be less than the size of the view, with a 1dp margin to account for rounding). If no layout fits in the view, the layout with the smallest area will be used.

| Parameters ||
|---|---|
| `remoteViews` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [SizeF](../android.util/SizeF.md)!, [RemoteViews](RemoteViews.md)!\>: Mapping of size to layout. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the map is empty, there are more than MAX_INIT_VIEW_COUNT layouts or the remote views are not all from the same application. |

## Public methods

### addStableView

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addStableView(
    viewId: Int, 
    nestedView: RemoteViews, 
    stableId: Int
): Unit
```

Equivalent to calling addView after inflating the given RemoteViews. If the RemoteViews may be re-inflated or updated, removeAllViews must be called on the same `viewId ` before the first call to this method for the behavior of this method to be predictable. The `stableId` will be used to identify a potential view to recycled when the remote view is inflated. Views can be re-used if inserted in the same order, potentially with some views appearing / disappearing. To be recycled the view must not change the layout used to inflate it or its view id (see RemoteViews). Note: if a view is re-used, all the actions will be re-applied on it. However, its properties are not reset, so what was applied in previous round will have an effect. As a view may be re-created at any time by the host, the RemoteViews should not rely on keeping information from previous applications and always re-set all the properties they need.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the parent `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` to add child into. |
| `nestedView` | [RemoteViews](RemoteViews.md): RemoteViews that describes the child. This value cannot be `null`. |
| `stableId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An id that is stable across different versions of RemoteViews. |
| --- | --- |

### addView

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addView(
    viewId: Int, 
    nestedView: RemoteViews!
): Unit
```

Equivalent to calling addView after inflating the given RemoteViews. This allows users to build "nested" RemoteViews. In cases where consumers of RemoteViews may recycle layouts, use removeAllViews to clear any existing children.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the parent `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` to add child into. |
| `nestedView` | [RemoteViews](RemoteViews.md)!: RemoteViews that describes the child. |

### apply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun apply(
    context: Context!, 
    parent: ViewGroup!
): View!
```

Inflates the view hierarchy represented by this object and applies all of the actions.

**Caller beware: this may throw**

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: Default context to use |
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!: Parent that the resulting view hierarchy will be attached to. This method does **not** attach the hierarchy. The caller should do so when appropriate. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | The inflated view hierarchy |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): RemoteViews!
```

**Deprecated:** *use RemoteViews instead.*

Returns a deep copy of the RemoteViews object. The RemoteView may not be attached to another RemoteView -- it must be the root of a hierarchy.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#!` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |
| `java.lang.IllegalStateException` | if this is not the root of a RemoteView hierarchy |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getDrawInstructions

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawInstructions(): RemoteViews.DrawInstructions?
```

Returns the `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` associated with this RemoteViews, if any.

If this `RemoteViews` is a container holding multiple responsive layouts (such as sized layouts created for different screen dimensions or landscape/portrait variants), this method returns the draw instructions of the smallest child view (for sized layouts) or the portrait child view (for orientation layouts).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions?` | The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.DrawInstructions` object, or `null` if this `RemoteViews` does not contain draw instructions. |

### getLayoutId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayoutId(): Int
```

Returns the layout id of the root layout associated with this RemoteViews. In the case that the RemoteViews has both a landscape and portrait root, this will return the layout id associated with the portrait layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the layout id. |

### getPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackage(): String!
```

### getViewId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getViewId(): Int
```

Get the ID of the top-level view of the XML layout, if set using RemoteViews.

### onLoadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLoadClass(clazz: Class<Any!>!): Boolean
```

**Deprecated:** *Used by system to enforce safe inflation of RemoteViews. Apps should not override this method. Changing of this method will NOT affect the process where RemoteViews is rendered.*

Used to restrict the views which can be inflated

| Parameters ||
|---|---|
| `clazz` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The class object for the View that is about to be inflated |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this class is allowed to be inflated, or false otherwise |

**See Also**

- onLoadClass

### reapply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reapply(
    context: Context!, 
    v: View!
): Unit
```

Applies all of the actions to the provided view.

**Caller beware: this may throw**

| Parameters ||
|---|---|
| `v` | [View](../android.view/View.md)!: The view to apply the actions to. This should be the result of the apply call. |

### removeAllViews

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAllViews(viewId: Int): Unit
```

Equivalent to calling removeAllViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the parent `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` to remove all children from. |

### setAccessibilityTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityTraversalAfter(
    viewId: Int, 
    nextId: Int
): Unit
```

Equivalent to calling setAccessibilityTraversalAfter.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose after view in accessibility traversal to set. |
| `nextId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the next in the accessibility traversal. |

### setAccessibilityTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityTraversalBefore(
    viewId: Int, 
    nextId: Int
): Unit
```

Equivalent to calling setAccessibilityTraversalBefore.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose before view in accessibility traversal to set. |
| `nextId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the next in the accessibility traversal. |

### setAppWidgetEventTag

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAppWidgetEventTag(
    viewId: Int, 
    tag: Int
): Unit
```

Set a view tag associating a View with an ID to be used for widget interaction usage events (`https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent.html#`). When this RemoteViews is applied to a bound widget, any clicks or scrolls on the tagged view will be reported to `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` using this tag.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID of the View whose tag will be set |
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The integer tag to use for the event |

**See Also**

- getClickedIds
- getScrolledIds
- queryAppWidgetEvents

### setBitmap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBitmap(
    viewId: Int, 
    methodName: String!, 
    value: Bitmap!
): Unit
```

Call a method taking one Bitmap on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Bitmap](../android.graphics/Bitmap.md)!: The value to pass to the method. |
| --- | --- |

### setBlendMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBlendMode(
    viewId: Int, 
    methodName: String, 
    value: BlendMode?
): Unit
```

Call a method taking one BlendMode on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `value` | [BlendMode](../android.graphics/BlendMode.md)?: The value to pass to the method. This value may be `null`. |
| --- | --- |

### setBoolean

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBoolean(
    viewId: Int, 
    methodName: String!, 
    value: Boolean
): Unit
```

Call a method taking one boolean on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The value to pass to the method. |
| --- | --- |

### setBundle

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBundle(
    viewId: Int, 
    methodName: String!, 
    value: Bundle!
): Unit
```

Call a method taking one Bundle on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Bundle](../android.os/Bundle.md)!: The value to pass to the method. |
| --- | --- |

### setByte

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setByte(
    viewId: Int, 
    methodName: String!, 
    value: Byte
): Unit
```

Call a method taking one byte on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): The value to pass to the method. |
| --- | --- |

### setChar

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChar(
    viewId: Int, 
    methodName: String!, 
    value: Char
): Unit
```

Call a method taking one char on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The value to pass to the method. |
| --- | --- |

### setCharSequence

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCharSequence(
    viewId: Int, 
    methodName: String, 
    stringResource: Int
): Unit
```

Call a method taking one CharSequence on a view in the layout for this RemoteViews. The CharSequence will be resolved from the resources at the time the RemoteViews is (re-)applied. Undefined resources will result in an exception, except 0 which will resolve to null.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `stringResource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource to resolve and pass as argument to the method. |
| --- | --- |

### setCharSequence

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCharSequence(
    viewId: Int, 
    methodName: String!, 
    value: CharSequence!
): Unit
```

Call a method taking one CharSequence on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The value to pass to the method. |
| --- | --- |

### setCharSequenceAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCharSequenceAttr(
    viewId: Int, 
    methodName: String, 
    stringAttribute: Int
): Unit
```

Call a method taking one CharSequence on a view in the layout for this RemoteViews. The CharSequence will be resolved from the theme attribute at the time the RemoteViews is (re-)applied. Unresolvable attributes will result in an exception, except 0 which will resolve to null.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `stringAttribute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The attribute to resolve and pass as argument to the method. |
| --- | --- |

### setChronometer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChronometer(
    viewId: Int, 
    base: Long, 
    format: String!, 
    started: Boolean
): Unit
```

Equivalent to calling setBase, setFormat, and start or stop.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the Chronometer to change |
| `base` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time at which the timer would have read 0:00. This time should be based off of elapsedRealtime. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The Chronometer format string, or null to simply display the timer value. |
| --- | --- |
| `started` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if you want the clock to be started, false if not. |

**See Also**

- setChronometerCountDown

### setChronometerCountDown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChronometerCountDown(
    viewId: Int, 
    isCountDown: Boolean
): Unit
```

Equivalent to calling setCountDown on the chronometer with the given viewId.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the Chronometer to change |
| `isCountDown` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if you want the chronometer to count down to base instead of counting up. |

### setColor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColor(
    viewId: Int, 
    methodName: String, 
    colorResource: Int
): Unit
```

Call a method taking one int, a color, on a view in the layout for this RemoteViews. The Color will be resolved from the resources at the time the RemoteViews is (re-) applied. Undefined resources will result in an exception, except 0 which will resolve to 0.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `colorResource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource to resolve and pass as argument to the method. |
| --- | --- |

### setColorAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorAttr(
    viewId: Int, 
    methodName: String, 
    colorAttribute: Int
): Unit
```

Call a method taking one int, a color, on a view in the layout for this RemoteViews. The Color will be resolved from the theme attribute at the time the RemoteViews is (re-)applied. Unresolvable attributes will result in an exception, except 0 which will resolve to 0.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `colorAttribute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The theme attribute to resolve and pass as argument to the method. |
| --- | --- |

### setColorInt

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorInt(
    viewId: Int, 
    methodName: String, 
    notNight: Int, 
    night: Int
): Unit
```

Call a method taking one int, a color, on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `notNight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_NO:kotlin.Int` |
| --- | --- |
| `night` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_YES:kotlin.Int` |

### setColorStateList

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorStateList(
    viewId: Int, 
    methodName: String, 
    value: ColorStateList?
): Unit
```

Call a method taking one ColorStateList on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `value` | [ColorStateList](../android.content.res/ColorStateList.md)?: The value to pass to the method. This value may be `null`. |
| --- | --- |

### setColorStateList

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorStateList(
    viewId: Int, 
    methodName: String, 
    notNight: ColorStateList?, 
    night: ColorStateList?
): Unit
```

Call a method taking one ColorStateList on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `notNight` | [ColorStateList](../android.content.res/ColorStateList.md)?: The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_NO:kotlin.Int` This value may be `null`. |
| --- | --- |
| `night` | [ColorStateList](../android.content.res/ColorStateList.md)?: The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_YES:kotlin.Int` This value may be `null`. |

### setColorStateList

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorStateList(
    viewId: Int, 
    methodName: String, 
    colorResource: Int
): Unit
```

Call a method taking one ColorStateList on a view in the layout for this RemoteViews. The ColorStateList will be resolved from the resources at the time the RemoteViews is (re-)applied. Undefined resources will result in an exception, except 0 which will resolve to null.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `colorResource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource to resolve and pass as argument to the method. |
| --- | --- |

### setColorStateListAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorStateListAttr(
    viewId: Int, 
    methodName: String, 
    colorAttr: Int
): Unit
```

Call a method taking one ColorStateList on a view in the layout for this RemoteViews. The ColorStateList will be resolved from the theme attribute at the time the RemoteViews is (re-)applied. Unresolvable attributes will result in an exception, except 0 which will resolve to null.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `colorAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The theme attribute to resolve and pass as argument to the method. |
| --- | --- |

### setCompoundButtonChecked

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCompoundButtonChecked(
    viewId: Int, 
    checked: Boolean
): Unit
```

Equivalent to calling setChecked.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose property to set. |
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to check the button, false to uncheck it. |

### setContentDescription

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentDescription(
    viewId: Int, 
    contentDescription: CharSequence!
): Unit
```

Equivalent to calling View.setContentDescription(CharSequence).

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose content description should change. |
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The new content description for the view. |

### setDisplayedChild

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDisplayedChild(
    viewId: Int, 
    childIndex: Int
): Unit
```

Equivalent to calling setDisplayedChild

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call setDisplayedChild |

### setDouble

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDouble(
    viewId: Int, 
    methodName: String!, 
    value: Double
): Unit
```

Call a method taking one double on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The value to pass to the method. |
| --- | --- |

### setEmptyView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEmptyView(
    viewId: Int, 
    emptyViewId: Int
): Unit
```

Equivalent to calling setEmptyView

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to set the empty view |
| `emptyViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The view id of the empty view |

### setFloat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloat(
    viewId: Int, 
    methodName: String!, 
    value: Float
): Unit
```

Call a method taking one float on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The value to pass to the method. |
| --- | --- |

### setFloatDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatDimen(
    viewId: Int, 
    methodName: String, 
    value: Float, 
    unit: Int
): Unit
```

Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the resources at the time the RemoteViews is (re-)applied.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The value of the dimension. |
| --- | --- |
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit in which the value is specified. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setFloatDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatDimen(
    viewId: Int, 
    methodName: String, 
    dimenResource: Int
): Unit
```

Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the resources at the time the RemoteViews is (re-)applied. Undefined resources will result in an exception, except 0 which will resolve to 0f.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `dimenResource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource to resolve and pass as argument to the method. |
| --- | --- |

### setFloatDimenAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatDimenAttr(
    viewId: Int, 
    methodName: String, 
    dimenAttr: Int
): Unit
```

Call a method taking one float, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the theme attribute at the time the RemoteViews is (re-)applied. Unresolvable attributes will result in an exception, except 0 which will resolve to 0f.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `dimenAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The attribute to resolve and pass as argument to the method. |
| --- | --- |

### setIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIcon(
    viewId: Int, 
    methodName: String!, 
    value: Icon!
): Unit
```

Call a method taking one Icon on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Icon](../android.graphics.drawable/Icon.md)!: The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` to pass the method. |
| --- | --- |

### setIcon

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIcon(
    viewId: Int, 
    methodName: String, 
    notNight: Icon?, 
    night: Icon?
): Unit
```

Call a method taking one Icon on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `notNight` | [Icon](../android.graphics.drawable/Icon.md)?: The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_NO:kotlin.Int` This value may be `null`. |
| --- | --- |
| `night` | [Icon](../android.graphics.drawable/Icon.md)?: The value to pass to the method when the view's configuration is set to `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_NIGHT_YES:kotlin.Int` This value may be `null`. |

### setImageViewBitmap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageViewBitmap(
    viewId: Int, 
    bitmap: Bitmap!
): Unit
```

Equivalent to calling setImageBitmap

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose bitmap should change |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: The new Bitmap for the drawable |

### setImageViewIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageViewIcon(
    viewId: Int, 
    icon: Icon!
): Unit
```

Equivalent to calling setImageIcon

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose bitmap should change |
| `icon` | [Icon](../android.graphics.drawable/Icon.md)!: The new Icon for the ImageView |

### setImageViewResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageViewResource(
    viewId: Int, 
    srcId: Int
): Unit
```

Equivalent to calling setImageResource

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose drawable should change |
| `srcId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new resource id for the drawable |

### setImageViewUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImageViewUri(
    viewId: Int, 
    uri: Uri!
): Unit
```

Equivalent to calling setImageURI

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose drawable should change |
| `uri` | [Uri](../android.net/Uri.md)!: The Uri for the image |

### setInt

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInt(
    viewId: Int, 
    methodName: String!, 
    value: Int
): Unit
```

Call a method taking one int on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The value to pass to the method. |
| --- | --- |

### setIntDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntDimen(
    viewId: Int, 
    methodName: String, 
    value: Float, 
    unit: Int
): Unit
```

Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the specified dimension at the time of inflation.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The value of the dimension. |
| --- | --- |
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit in which the value is specified. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setIntDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntDimen(
    viewId: Int, 
    methodName: String, 
    dimenResource: Int
): Unit
```

Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the resources at the time the RemoteViews is (re-)applied. Undefined resources will result in an exception, except 0 which will resolve to 0.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `dimenResource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource to resolve and pass as argument to the method. |
| --- | --- |

### setIntDimenAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntDimenAttr(
    viewId: Int, 
    methodName: String, 
    dimenAttr: Int
): Unit
```

Call a method taking one int, a size in pixels, on a view in the layout for this RemoteViews. The dimension will be resolved from the theme attribute at the time the RemoteViews is (re-)applied. Unresolvable attributes will result in an exception, except 0 which will resolve to 0.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the method to call. This value cannot be `null`. |
| `dimenAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The attribute to resolve and pass as argument to the method. |
| --- | --- |

### setIntent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntent(
    viewId: Int, 
    methodName: String!, 
    value: Intent!
): Unit
```

Call a method taking one Intent on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Intent](../android.content/Intent.md)!: The `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to pass the method. |
| --- | --- |

### setLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabelFor(
    viewId: Int, 
    labeledId: Int
): Unit
```

Equivalent to calling setLabelFor.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose property to set. |
| `labeledId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a view for which this view serves as a label. |

### setLightBackgroundLayoutId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLightBackgroundLayoutId(layoutId: Int): Unit
```

Provides an alternate layout ID, which can be used to inflate this view. This layout will be used by the host when the widgets displayed on a light-background where foreground elements and text can safely draw using a dark color without any additional background protection.

### setLong

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLong(
    viewId: Int, 
    methodName: String!, 
    value: Long
): Unit
```

Call a method taking one long on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The value to pass to the method. |
| --- | --- |

### setOnCheckedChangeResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnCheckedChangeResponse(
    viewId: Int, 
    response: RemoteViews.RemoteResponse
): Unit
```

Equivalent to calling setOnCheckedChangeListener to launch the provided `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse`. The intent will be filled with the current checked state of the view at the key `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#EXTRA_CHECKED:kotlin.String`. The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` will not be launched in response to check changes arising from setCompoundButtonChecked or setRadioGroupChecked usages. The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` must be created using fromFillInIntent in conjunction with setPendingIntentTemplate for items inside collections (eg. ListView, StackView etc.). Otherwise, create the `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` using fromPendingIntent.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view that will trigger the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` when checked state changes. |
| `response` | [RemoteViews.RemoteResponse](../android/widget/RemoteViews.RemoteResponse.md): The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` to send when the checked state changes. This value cannot be `null`. |

### setOnClickFillInIntent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnClickFillInIntent(
    viewId: Int, 
    fillInIntent: Intent!
): Unit
```

When using collections (eg. ListView, StackView etc.) in widgets, it is very costly to set PendingIntents on the individual items, and is hence not recommended. Instead a single PendingIntent template can be set on the collection, see setPendingIntentTemplate, and the individual on-click action of a given item can be distinguished by setting a fillInIntent on that item. The fillInIntent is then combined with the PendingIntent template in order to determine the final intent which will be executed when the item is clicked. This works as follows: any fields which are left blank in the PendingIntent template, but are provided by the fillInIntent will be overwritten, and the resulting PendingIntent will be used. The rest of the PendingIntent template will then be filled in with the associated fields that are set in fillInIntent. See fillIn for more details.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to set the fillInIntent |
| `fillInIntent` | [Intent](../android.content/Intent.md)!: The intent which will be combined with the parent's PendingIntent in order to determine the on-click behavior of the view specified by viewId |

### setOnClickPendingIntent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnClickPendingIntent(
    viewId: Int, 
    pendingIntent: PendingIntent!
): Unit
```

Equivalent to calling setOnClickListener to launch the provided `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`. The source bounds (getSourceBounds) of the intent will be set to the bounds of the clicked view in screen space. Note that any activity options associated with the mPendingIntent may get overridden before starting the intent. When setting the on-click action of items within collections (eg. ListView, StackView etc.), this method will not work. Instead, use setPendingIntentTemplate in conjunction with setOnClickFillInIntent.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view that will trigger the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` when clicked |
| `pendingIntent` | [PendingIntent](../android.app/PendingIntent.md)!: The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to send when user clicks |

### setOnClickResponse

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnClickResponse(
    viewId: Int, 
    response: RemoteViews.RemoteResponse
): Unit
```

Equivalent of calling setOnClickListener to launch the provided `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse`.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view that will trigger the `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` when clicked |
| `response` | [RemoteViews.RemoteResponse](../android/widget/RemoteViews.RemoteResponse.md): The `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteResponse` to send when user clicks. This value cannot be `null`. |

### setOnStylusHandwritingPendingIntent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnStylusHandwritingPendingIntent(
    viewId: Int, 
    pendingIntent: PendingIntent?
): Unit
```

Equivalent to calling setHandwritingDelegatorCallback to send the provided `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`.

A common use case is a remote view which looks like a text editor but does not actually support text editing itself, and clicking on the remote view launches an activity containing an EditText. To support handwriting initiation in this case, this method can be called on the remote view to configure it as a handwriting delegator, meaning that stylus movement on the remote view triggers a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` and starts handwriting mode for the delegate EditText. The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` is typically the same as the one passed to setOnClickPendingIntent which launches the activity containing the EditText. The EditText should call setIsHandwritingDelegate to set it as a delegate, and also use setAllowedHandwritingDelegatorPackage or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#HANDWRITING_DELEGATE_FLAG_HOME_DELEGATOR_ALLOWED:kotlin.Int` if necessary to support delegators from the package displaying the remote view.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): identifier of the view that will trigger the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` when a stylus `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` occurs within the view's bounds |
| `pendingIntent` | [PendingIntent](../android.app/PendingIntent.md)?: the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to send, or `null` to clear the handwriting delegation |

### setPendingIntentTemplate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPendingIntentTemplate(
    viewId: Int, 
    pendingIntentTemplate: PendingIntent!
): Unit
```

When using collections (eg. ListView, StackView etc.) in widgets, it is very costly to set PendingIntents on the individual items, and is hence not recommended. Instead this method should be used to set a single PendingIntent template on the collection, and individual items can differentiate their on-click behavior using setOnClickFillInIntent.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the collection who's children will use this PendingIntent template when clicked |
| `pendingIntentTemplate` | [PendingIntent](../android.app/PendingIntent.md)!: The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to be combined with extras specified by a child of viewId and executed when that child is clicked |

### setProgressBar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProgressBar(
    viewId: Int, 
    max: Int, 
    progress: Int, 
    indeterminate: Boolean
): Unit
```

Equivalent to calling setMax, android.widget.ProgressBar#setProgress, and setIndeterminate If indeterminate is true, then the values for max and progress are ignored.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the ProgressBar to change |
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The 100% value for the progress bar |
| `progress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The current value of the progress bar. |
| --- | --- |
| `indeterminate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the progress bar is indeterminate, false if not. |

### setRadioGroupChecked

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRadioGroupChecked(
    viewId: Int, 
    checkedId: Int
): Unit
```

Equivalent to calling check.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose property to set. |
| `checkedId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unique id of the radio button to select in the group. |

### setRelativeScrollPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRelativeScrollPosition(
    viewId: Int, 
    offset: Int
): Unit
```

Equivalent to calling smoothScrollByOffset.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Scroll by this adapter position offset |

### setRemoteAdapter

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRemoteAdapter(
    viewId: Int, 
    intent: Intent!
): Unit
```

**Deprecated:** *use setRemoteAdapter instead*

Equivalent to calling setRemoteViewsAdapter. Can only be used for App Widgets.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the AdapterView |
| `intent` | [Intent](../android.content/Intent.md)!: The intent of the service which will be providing data to the RemoteViewsAdapter |

### setRemoteAdapter

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRemoteAdapter(
    viewId: Int, 
    items: RemoteViews.RemoteCollectionItems
): Unit
```

Creates a simple Adapter for the viewId specified. The viewId must point to an AdapterView, ie. ListView, GridView, StackView or AdapterViewAnimator. This is a simpler but less flexible approach to populating collection widgets. Its use is encouraged for most scenarios, as long as the total memory within the list of RemoteViews is relatively small (ie. doesn't contain large or numerous Bitmaps, see setImageViewBitmap). In the case of numerous images, the use of API is still possible by setting image URIs instead of Bitmaps, see setImageViewUri. This API is supported in the compatibility library for previous API levels, see RemoteViewsCompat.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the AdapterView. |
| `items` | [RemoteViews.RemoteCollectionItems](../android/widget/RemoteViews.RemoteCollectionItems.md): The items to display in the AdapterView. This value cannot be `null`. |

### setRemoteAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRemoteAdapter(
    appWidgetId: Int, 
    viewId: Int, 
    intent: Intent!
): Unit
```

**Deprecated:** *This method has been deprecated. See setRemoteAdapter*

Equivalent to calling setRemoteViewsAdapter.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the app widget which contains the specified view. (This parameter is ignored in this deprecated method) |
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the AdapterView |
| `intent` | [Intent](../android.content/Intent.md)!: The intent of the service which will be providing data to the RemoteViewsAdapter |
| --- | --- |

### setScrollPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollPosition(
    viewId: Int, 
    position: Int
): Unit
```

Equivalent to calling smoothScrollToPosition.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Scroll to this adapter position |

### setShort

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShort(
    viewId: Int, 
    methodName: String!, 
    value: Short
): Unit
```

Call a method taking one short on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The value to pass to the method. |
| --- | --- |

### setString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setString(
    viewId: Int, 
    methodName: String!, 
    value: String!
): Unit
```

Call a method taking one String on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The value to pass to the method. |
| --- | --- |

### setTextColor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextColor(
    viewId: Int, 
    color: Int
): Unit
```

Equivalent to calling setTextColor.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose text color should change |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Sets the text color for all the states (normal, selected, focused) to be this color. |

### setTextViewCompoundDrawables

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextViewCompoundDrawables(
    viewId: Int, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Equivalent to calling setCompoundDrawablesWithIntrinsicBounds.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose text should change |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place to the left of the text, or 0 |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place above the text, or 0 |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place to the right of the text, or 0 |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place below the text, or 0 |

### setTextViewCompoundDrawablesRelative

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextViewCompoundDrawablesRelative(
    viewId: Int, 
    start: Int, 
    top: Int, 
    end: Int, 
    bottom: Int
): Unit
```

Equivalent to calling setCompoundDrawablesRelativeWithIntrinsicBounds.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose text should change |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place before the text (relative to the layout direction), or 0 |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place above the text, or 0 |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place after the text, or 0 |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a drawable to place below the text, or 0 |

### setTextViewText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextViewText(
    viewId: Int, 
    text: CharSequence!
): Unit
```

Equivalent to calling setText

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose text should change |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The new text for the view |

### setTextViewTextSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextViewTextSize(
    viewId: Int, 
    units: Int, 
    size: Float
): Unit
```

Equivalent to calling setTextSize

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose text size should change |
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The units of size (e.g. COMPLEX_UNIT_SP) |
| `size` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The size of the text |
| --- | --- |

### setUri

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUri(
    viewId: Int, 
    methodName: String!, 
    value: Uri!
): Unit
```

Call a method taking one Uri on a view in the layout for this RemoteViews.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call the method. |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the method to call. |
| `value` | [Uri](../android.net/Uri.md)!: The value to pass to the method. |
| --- | --- |

### setViewLayoutHeight

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutHeight(
    viewId: Int, 
    height: Float, 
    units: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` except that you may provide the value in any dimension units.

NOTE: It is recommended to use `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` only for 0, `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int`. Otherwise, prefer using scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.
.

| Parameters ||
|---|---|
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): height of the view in the given units |
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit type of the value e.g. `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setViewLayoutHeightAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutHeightAttr(
    viewId: Int, 
    heightAttr: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` with the value of the given attribute in the current theme.

| Parameters ||
|---|---|
| `heightAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a dimen attribute to read the height from. |

### setViewLayoutHeightDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutHeightDimen(
    viewId: Int, 
    heightDimen: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#height:kotlin.Int` with the result of getDimensionPixelSize.

| Parameters ||
|---|---|
| `heightDimen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a dimen resource to read the height from. |

### setViewLayoutMargin

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutMargin(
    viewId: Int, 
    type: Int, 
    value: Float, 
    units: Int
): Unit
```

Equivalent to calling setMarginEnd. Only works if the getLayoutParams supports margins.

NOTE: It is recommended to use `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` only for 0. Otherwise, prefer using scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.
.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The margin being set e.g. `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a value for the margin the given units. |
| --- | --- |
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit type of the value e.g. `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setViewLayoutMarginAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutMarginAttr(
    viewId: Int, 
    type: Int, 
    attr: Int
): Unit
```

Equivalent to calling setMarginEnd. Only works if the getLayoutParams supports margins.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The margin being set e.g. `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` |
| `attr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a dimension attribute to apply to the margin, or 0 to clear the margin. |
| --- | --- |

### setViewLayoutMarginDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutMarginDimen(
    viewId: Int, 
    type: Int, 
    dimen: Int
): Unit
```

Equivalent to calling setMarginEnd. Only works if the getLayoutParams supports margins.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The margin being set e.g. `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/RemoteViews#MARGIN_END:kotlin.Int` |
| `dimen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a dimension resource to apply to the margin, or 0 to clear the margin. |
| --- | --- |

### setViewLayoutWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutWidth(
    viewId: Int, 
    width: Float, 
    units: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` except that you may provide the value in any dimension units.

NOTE: It is recommended to use `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` only for 0, `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#WRAP_CONTENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#MATCH_PARENT:kotlin.Int`. Otherwise, prefer using scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.
.

| Parameters ||
|---|---|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Width of the view in the given units |
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit type of the value e.g. `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setViewLayoutWidthAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutWidthAttr(
    viewId: Int, 
    widthAttr: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` with the value of the given attribute in the current theme.

| Parameters ||
|---|---|
| `widthAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dimension attribute for the view's width |

### setViewLayoutWidthDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewLayoutWidthDimen(
    viewId: Int, 
    widthDimen: Int
): Unit
```

Equivalent to setting `https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#width:kotlin.Int` with the result of getDimensionPixelSize.

| Parameters ||
|---|---|
| `widthDimen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the dimension resource for the view's width |

### setViewOutlinePreferredRadius

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewOutlinePreferredRadius(
    viewId: Int, 
    radius: Float, 
    units: Int
): Unit
```

Sets an OutlineProvider on the view whose corner radius is a dimension calculated using applyDimension.

NOTE: It is recommended to use `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` only for 0. Otherwise, prefer using scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.
.

| Parameters ||
|---|---|
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |

### setViewOutlinePreferredRadiusAttr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewOutlinePreferredRadiusAttr(
    viewId: Int, 
    attrId: Int
): Unit
```

Sets an OutlineProvider on the view whose corner radius is a dimension attribute with `attrId`.

### setViewOutlinePreferredRadiusDimen

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewOutlinePreferredRadiusDimen(
    viewId: Int, 
    resId: Int
): Unit
```

Sets an OutlineProvider on the view whose corner radius is a dimension resource with `resId`.

### setViewPadding

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewPadding(
    viewId: Int, 
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    units: Int
): Unit
```

Equivalent to calling setPadding. This overload supports using values with complex units that are resolved when this RemoteViews is displayed.

Prefer using scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.
.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the left padding value in the given units |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the top padding value in the given units |
| --- | --- |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the right padding value in the given units |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the bottom padding value in the given units |
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The unit type of the value, e.g. `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int` |
| --- | --- |

### setViewPadding

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewPadding(
    viewId: Int, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Equivalent to calling setPadding.

Prefer using the setViewPadding overload that accepts scalable units like `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int`. As of Android 17, the pixel values set by this function will be automatically scaled when the RemoteViews is used on a display with a different density.

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view to change |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the left padding in pixels. The units of this value are pixels. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top padding in pixels. The units of this value are pixels. |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the right padding in pixels. The units of this value are pixels. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom padding in pixels. The units of this value are pixels. |

### setViewVisibility

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewVisibility(
    viewId: Int, 
    visibility: Int
): Unit
```

Equivalent to calling setVisibility

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view whose visibility should change |
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new visibility for the view. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int` |

### showNext

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showNext(viewId: Int): Unit
```

**Deprecated:** *As RemoteViews may be reapplied frequently, it is preferable to call setDisplayedChild to ensure that the adapter index does not change unexpectedly.*

Equivalent to calling showNext

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call showNext |

### showPrevious

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun showPrevious(viewId: Int): Unit
```

**Deprecated:** *As RemoteViews may be reapplied frequently, it is preferable to call setDisplayedChild to ensure that the adapter index does not change unexpectedly.*

Equivalent to calling showPrevious

| Parameters ||
|---|---|
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the view on which to call showPrevious |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RemoteViews!>
```

Parcelable.Creator that instantiates RemoteViews objects
