# View.OnLayoutChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLayoutChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnLayoutChangeListener "View this page in Java") 
| --- | --- |

```
interface OnLayoutChangeListener
```

| [android.view.View.OnLayoutChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener#) |

Interface definition for a callback to be invoked when the layout bounds of a view changes due to layout processing.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLayoutChange](https://developer.android.com/reference/kotlin/android/view/View.OnLayoutChangeListener#onLayoutChange(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldLeft:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldTop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldRight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldBottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the layout bounds of a view changes due to layout processing. |

## Public methods

### onLayoutChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLayoutChange(
    v: View!, 
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int, 
    oldLeft: Int, 
    oldTop: Int, 
    oldRight: Int, 
    oldBottom: Int
): Unit
```

Called when the layout bounds of a view changes due to layout processing.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view whose bounds have changed. |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value of the view's left property. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value of the view's top property. |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value of the view's right property. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value of the view's bottom property. |
| `oldLeft` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value of the view's left property. |
| --- | --- |
| `oldTop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value of the view's top property. |
| `oldRight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value of the view's right property. |
| `oldBottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value of the view's bottom property. |
| --- | --- |
