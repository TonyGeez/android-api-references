# ShareActionProvider.OnShareTargetSelectedListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnShareTargetSelectedListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/ShareActionProvider.OnShareTargetSelectedListener "View this page in Java") 

```
interface OnShareTargetSelectedListener
```

| [android.widget.ShareActionProvider.OnShareTargetSelectedListener](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider.OnShareTargetSelectedListener#) |

Listener for the event of selecting a share target.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onShareTargetSelected](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider.OnShareTargetSelectedListener#onShareTargetSelected(android.widget.ShareActionProvider,%20android.content.Intent))`(`source:` ` [ShareActionProvider](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Called when a share target has been selected. |

## Public methods

### onShareTargetSelected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShareTargetSelected(
    source: ShareActionProvider!, 
    intent: Intent!
): Boolean
```

Called when a share target has been selected. The client can decide whether to perform some action before the sharing is actually performed.

**Note:**Modifying the intent is not permitted and any changes to the latter will be ignored.

**Note:** You should**not**handle the intent here. This callback aims to notify the client that a sharing is being performed, so the client can update the UI if necessary.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [ShareActionProvider](https://developer.android.com/reference/kotlin/android/widget/ShareActionProvider)!:The source of the notification. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent for launching the chosen share target. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The return result is ignored. Always return false for consistency. |
