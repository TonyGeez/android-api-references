# AutoCompleteTextView.OnDismissListener

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDismissListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/AutoCompleteTextView.OnDismissListener "View this page in Java") 
| --- | --- |

```
interface OnDismissListener
```

| [android.widget.AutoCompleteTextView.OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.OnDismissListener#) |

Listener to respond to the AutoCompleteTextView's completion list being dismissed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.OnDismissListener#onDismiss())`()` This method will be invoked whenever the AutoCompleteTextView's list of completion options has been dismissed and is no longer available for user interaction. |

## Public methods

### onDismiss

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDismiss(): Unit
```

This method will be invoked whenever the AutoCompleteTextView's list of completion options has been dismissed and is no longer available for user interaction.
