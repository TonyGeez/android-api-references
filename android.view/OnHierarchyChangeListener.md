# ViewGroup.OnHierarchyChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHierarchyChangeListener

Kotlin| [Java](../android/view/ViewGroup.OnHierarchyChangeListener.md) 
| --- | --- |

```
interface OnHierarchyChangeListener
```

| [android.view.ViewGroup.OnHierarchyChangeListener](../android/view/ViewGroup.OnHierarchyChangeListener.md) |

| Known Direct Subclasses [WebView](../android/webkit/WebView.md) |----------------------------------------------------------------------------------------|---------------------------------| | [WebView](../android/webkit/WebView.md) | A View that displays web pages. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the hierarchy within this view changed. The hierarchy changes whenever a child is added to or removed from this view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChildViewAdded](../android/view/ViewGroup.OnHierarchyChangeListener.md))`(`parent:` ` [View](../android/view/View.md)!`, `child:` ` [View](../android/view/View.md)!`)` Called when a new child is added to a parent view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChildViewRemoved](../android/view/ViewGroup.OnHierarchyChangeListener.md))`(`parent:` ` [View](../android/view/View.md)!`, `child:` ` [View](../android/view/View.md)!`)` Called when a child is removed from a parent view. |

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
| `parent` | [View](../android/view/View.md)!:the view in which a child was added |
| `child` | [View](../android/view/View.md)!:the new child view added in the hierarchy |

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
| `parent` | [View](../android/view/View.md)!:the view from which the child was removed |
| `child` | [View](../android/view/View.md)!:the child removed from the hierarchy |
