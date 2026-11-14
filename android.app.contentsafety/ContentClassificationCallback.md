Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentClassificationCallback

```
interface ContentClassificationCallback
```

| [android.app.contentsafety.ContentClassificationCallback](../android/app/contentsafety/ContentClassificationCallback.md) |

Callback for receiving content classification results.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationCallback#onContentClassification(android.app.contentsafety.ContentClassificationResult)(result: https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult)` Called when the content has been classified. |

## Public methods

### onContentClassification

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onContentClassification(result: ContentClassificationResult): Unit
```

Called when the content has been classified.

| Parameters ||
|---|---|
| `result` | [ContentClassificationResult](../android/app/contentsafety/ContentClassificationResult.md): the result of the classification. This value cannot be `null`. |
