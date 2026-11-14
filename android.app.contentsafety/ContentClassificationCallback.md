Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentClassificationCallback

```
interface ContentClassificationCallback
```

| [android.app.contentsafety.ContentClassificationCallback](ContentClassificationCallback.md) |

Callback for receiving content classification results.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onContentClassification Called when the content has been classified. |

## Public methods

### onContentClassification

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onContentClassification(result: ContentClassificationResult): Unit
```

Called when the content has been classified.

| Parameters ||
|---|---|
| `result` | [ContentClassificationResult](ContentClassificationResult.md): the result of the classification. This value cannot be `null`. |
