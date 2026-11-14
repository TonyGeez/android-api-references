# ViewGroup.OnHierarchyChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHierarchyChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewGroup.OnHierarchyChangeListener "View this page in Java") 

```
interface OnHierarchyChangeListener
```

| [android.view.ViewGroup.OnHierarchyChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener#) |

| Known Direct Subclasses [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) |----------------------------------------------------------------------------------------|---------------------------------| | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) | A View that displays web pages. | |

Interface definition for a callback to be invoked when the hierarchy within this view changed. The hierarchy changes whenever a child is added to or removed from this view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChildViewAdded](https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener#onChildViewAdded(android.view.View,%20android.view.View))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a new child is added to a parent view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChildViewRemoved](https://developer.android.com/reference/kotlin/android/view/ViewGroup.OnHierarchyChangeListener#onChildViewRemoved(android.view.View,%20android.view.View))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a child is removed from a parent view. |

## Public methods

### onChildViewAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChildViewAdded(
    parent: View!, 
    child: View!
): Unit
```

Called when a new child is added to a parent view.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the view in which a child was added |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the new child view added in the hierarchy |

### onChildViewRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChildViewRemoved(
    parent: View!, 
    child: View!
): Unit
```

Called when a child is removed from a parent view.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the view from which the child was removed |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:the child removed from the hierarchy |
