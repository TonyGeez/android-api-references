# ViewStub.OnInflateListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInflateListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewStub.OnInflateListener "View this page in Java") 
| --- | --- |

```
interface OnInflateListener
```

| [android.view.ViewStub.OnInflateListener](https://developer.android.com/reference/kotlin/android/view/ViewStub.OnInflateListener#) |

Listener used to receive a notification after a ViewStub has successfully inflated its layout resource.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](https://developer.android.com/reference/kotlin/android/view/ViewStub.OnInflateListener#onInflate(android.view.ViewStub,%20android.view.View))`(`stub:` ` [ViewStub](https://developer.android.com/reference/kotlin/android/view/ViewStub)!`, `inflated:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Invoked after a ViewStub successfully inflated its layout resource. |

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
| `stub` | [ViewStub](https://developer.android.com/reference/kotlin/android/view/ViewStub)!:The ViewStub that initiated the inflation. |
| `inflated` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The inflated View. |
