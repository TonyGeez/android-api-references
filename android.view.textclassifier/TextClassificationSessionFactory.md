# TextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationSessionFactory

Kotlin| [Java](../android/view/textclassifier/TextClassificationSessionFactory.md) 
| --- | --- |

```
interface TextClassificationSessionFactory
```

| [android.view.textclassifier.TextClassificationSessionFactory](../android/view/textclassifier/TextClassificationSessionFactory.md) |

An interface for creating a session-aware TextClassifier.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TextClassifier](../android/view/textclassifier/TextClassifier.md) | [createTextClassificationSession](../android/view/textclassifier/TextClassificationSessionFactory.md))`(`classificationContext:` ` [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md)`)` Creates and returns a session-aware TextClassifier. |

## Public methods

### createTextClassificationSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createTextClassificationSession(classificationContext: TextClassificationContext): TextClassifier
```

Creates and returns a session-aware TextClassifier.

| Parameters ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classificationContext` | [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md):the classification context This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TextClassifier](../android/view/textclassifier/TextClassifier.md) | This value cannot be`null`. |
