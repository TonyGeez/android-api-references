# AbsListView.SelectionBoundsAdjuster

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectionBoundsAdjuster

Kotlin| [Java](https://developer.android.com/reference/android/widget/AbsListView.SelectionBoundsAdjuster "View this page in Java") 

```
interface SelectionBoundsAdjuster
```

| [android.widget.AbsListView.SelectionBoundsAdjuster](https://developer.android.com/reference/kotlin/android/widget/AbsListView.SelectionBoundsAdjuster#) |

The top-level view of a list item can implement this interface to allow itself to modify the bounds of the selection shown for that item.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustListItemSelectionBounds](https://developer.android.com/reference/kotlin/android/widget/AbsListView.SelectionBoundsAdjuster#adjustListItemSelectionBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Called to allow the list item to adjust the bounds shown for its selection. |

## Public methods

### adjustListItemSelectionBounds

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun adjustListItemSelectionBounds(bounds: Rect!): Unit
```

Called to allow the list item to adjust the bounds shown for its selection.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:On call, this contains the bounds the list has selected for the item (that is the bounds of the entire view). The values can be modified as desired. |
