# TextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationSessionFactory

Kotlin| [Java](https://developer.android.com/reference/android/view/textclassifier/TextClassificationSessionFactory "View this page in Java") 

```
interface TextClassificationSessionFactory
```

| [android.view.textclassifier.TextClassificationSessionFactory](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationSessionFactory#) |

An interface for creating a session-aware TextClassifier.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) | [createTextClassificationSession](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationSessionFactory#createTextClassificationSession(android.view.textclassifier.TextClassificationContext))`(`classificationContext:` ` [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext)`)` Creates and returns a session-aware TextClassifier. |

## Public methods

### createTextClassificationSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createTextClassificationSession(classificationContext: TextClassificationContext): TextClassifier
```

Creates and returns a session-aware TextClassifier.

| Parameters ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classificationContext` | [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext):the classification context This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) | This value cannot be`null`. |
