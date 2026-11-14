# View.OnScrollChangeListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScrollChangeListener

Kotlin| [Java](../android/view/View.OnScrollChangeListener.md) 
| --- | --- |

```
interface OnScrollChangeListener
```

| [android.view.View.OnScrollChangeListener](../android/view/View.OnScrollChangeListener.md) |

Interface definition for a callback to be invoked when the scroll X or Y positions of a view change.

**Note:** Some views handle scrolling independently from View and may have their own separate listeners for scroll-type events. For example, [ListView](../android/widget/ListView.md) allows clients to register an [AbsListView.OnScrollListener](../android/widget/AbsListView.md))to listen for changes in list scroll position.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollChange](../android/view/View.OnScrollChangeListener.md))`(`v:` ` [View](../android/view/View.md)!`, `scrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldScrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldScrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the scroll position of a view changes. |

## Public methods

### onScrollChange

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollChange(
    v: View!, 
    scrollX: Int, 
    scrollY: Int, 
    oldScrollX: Int, 
    oldScrollY: Int
): Unit
```

Called when the scroll position of a view changes.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `v` | [View](../android/view/View.md)!:The view whose scroll position has changed. |
| `scrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Current horizontal scroll origin. |
| `scrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Current vertical scroll origin. |
| --- | --- |
| `oldScrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Previous horizontal scroll origin. |
| `oldScrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Previous vertical scroll origin. |
