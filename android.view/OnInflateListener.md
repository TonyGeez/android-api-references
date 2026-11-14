# ViewStub.OnInflateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInflateListener

Kotlin| [Java](../android/view/ViewStub.OnInflateListener.md) 
| --- | --- |

```
interface OnInflateListener
```

| [android.view.ViewStub.OnInflateListener](../android/view/ViewStub.OnInflateListener.md) |

Listener used to receive a notification after a ViewStub has successfully inflated its layout resource.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](../android/view/ViewStub.OnInflateListener.md))`(`stub:` ` [ViewStub](../android/view/ViewStub.md)!`, `inflated:` ` [View](../android/view/View.md)!`)` Invoked after a ViewStub successfully inflated its layout resource. |

## Public methods

### onInflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInflate(
    stub: ViewStub!, 
    inflated: View!
): Unit
```

Invoked after a ViewStub successfully inflated its layout resource. This method is invoked after the inflated view was added to the hierarchy but before the layout pass.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `stub` | [ViewStub](../android/view/ViewStub.md)!:The ViewStub that initiated the inflation. |
| `inflated` | [View](../android/view/View.md)!:The inflated View. |
