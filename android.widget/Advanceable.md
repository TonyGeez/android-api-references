Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Advanceable

```
interface Advanceable
```

| [android.widget.Advanceable](Advanceable.md) |

| Known Direct Subclasses [AdapterViewAnimator](AdapterViewAnimator.md) |---|---| | [AdapterViewAnimator](AdapterViewAnimator.md) | Base class for a `https://developer.android.com/reference/kotlin/android/widget/AdapterView` that will perform animations when switching between its views. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AdapterViewFlipper](AdapterViewFlipper.md), [StackView](StackView.md) |---|---| | [AdapterViewFlipper](AdapterViewFlipper.md) | Simple `https://developer.android.com/reference/kotlin/android/widget/ViewAnimator` that will animate between two or more views that have been added to it. | | [StackView](StackView.md) | A view that displays its children in a stack and allows users to discretely swipe through the children. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface can be implemented by any collection-type view which has a notion of progressing through its set of children. The interface exists to give AppWidgetHosts a way of taking responsibility for automatically advancing such collections.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/Advanceable#advance()()` Advances this collection, eg. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/Advanceable#fyiWillBeAdvancedByHostKThx()()` Called by the AppWidgetHost once before it begins to call advance(), allowing the collection to do any required setup. |

## Public methods

### advance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun advance(): Unit
```

Advances this collection, eg. shows the next view.

### fyiWillBeAdvancedByHostKThx

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun fyiWillBeAdvancedByHostKThx(): Unit
```

Called by the AppWidgetHost once before it begins to call advance(), allowing the collection to do any required setup.
