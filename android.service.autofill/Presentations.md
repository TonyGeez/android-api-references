Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Presentations

```
class Presentations
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.Presentations](https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#) |

Holds presentations used to visualize autofill suggestions for each available UI type.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations.Builder` A builder for `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#` |

| Public methods ||
|---|---|
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)? | `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#getDialogPresentation()()` The presentation used to visualize this field in the [fill dialog UI](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset#FillDialogUI) |
| [InlinePresentation](https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation)? | `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#getInlinePresentation()()` The `https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation` used to visualize this dataset as inline suggestions. |
| [InlinePresentation](https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation)? | `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#getInlineTooltipPresentation()()` The `https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation` used to show the tooltip for the `mInlinePresentation`. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)? | `https://developer.android.com/reference/kotlin/android/service/autofill/Presentations#getMenuPresentation()()` The presentation used to visualize this field in fill UI. |

## Public methods

### getDialogPresentation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDialogPresentation(): RemoteViews?
```

The presentation used to visualize this field in the [fill dialog UI](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset#FillDialogUI)

Theme does not work with RemoteViews layout. Avoid hardcoded text color or background color: Autofill on different platforms may have different themes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#?` | This value may be `null`. |

### getInlinePresentation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInlinePresentation(): InlinePresentation?
```

The `https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation` used to visualize this dataset as inline suggestions. If the dataset supports inline suggestions, this should not be null.

### getInlineTooltipPresentation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInlineTooltipPresentation(): InlinePresentation?
```

The `https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation` used to show the tooltip for the `mInlinePresentation`. If the set this field, the `mInlinePresentation` should not be null.

### getMenuPresentation

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMenuPresentation(): RemoteViews?
```

The presentation used to visualize this field in fill UI.

Note: Before Android 13, this was referred to simply as "presentation" in the SDK.

Theme does not work with RemoteViews layout. Avoid hardcoded text color or background color: Autofill on different platforms may have different themes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#?` | This value may be `null`. |
