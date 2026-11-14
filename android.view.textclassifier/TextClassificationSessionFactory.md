# TextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationSessionFactory

Kotlin| [Java](TextClassificationSessionFactory.md) 
| --- | --- |

```
interface TextClassificationSessionFactory
```

| [android.view.textclassifier.TextClassificationSessionFactory](TextClassificationSessionFactory.md) |

An interface for creating a session-aware TextClassifier.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TextClassifier](TextClassifier.md) | [createTextClassificationSession](TextClassificationSessionFactory.md))`(`classificationContext:` ` [TextClassificationContext](TextClassificationContext.md)`)` Creates and returns a session-aware TextClassifier. |

## Public methods

### createTextClassificationSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createTextClassificationSession(classificationContext: TextClassificationContext): TextClassifier
```

Creates and returns a session-aware TextClassifier.

| Parameters ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classificationContext` | [TextClassificationContext](TextClassificationContext.md):the classification context This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TextClassifier](TextClassifier.md) | This value cannot be`null`. |
