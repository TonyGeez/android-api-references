# TextClassificationManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationManager

Kotlin| [Java](TextClassificationManager.md) 
| --- | --- |

```
class TextClassificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextClassificationManager](TextClassificationManager.md) |

Interface to the text classification service.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TextClassifier](TextClassifier.md) | [createTextClassificationSession](TextClassificationManager.md))`(`classificationContext:` ` [TextClassificationContext](TextClassificationContext.md)`)` Call this method to start a text classification session with the given context. |
| [TextClassifier](TextClassifier.md) | [getTextClassifier](TextClassificationManager.md))`()` Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](TextClassificationManager.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassificationSessionFactory](TextClassificationManager.md))`(`factory:` ` [TextClassificationSessionFactory](TextClassificationSessionFactory.md)?`)` Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassifier](TextClassificationManager.md))`(`textClassifier:` ` [TextClassifier](TextClassifier.md)?`)` Sets the text classifier. |

## Public methods

### createTextClassificationSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createTextClassificationSession(classificationContext: TextClassificationContext): TextClassifier
```

Call this method to start a text classification session with the given context. A session is created with a context helping the classifier better understand what the user needs and consists of queries and feedback events. The queries are directly related to providing useful functionality to the user and the events are a feedback loop back to the classifier helping it learn and better serve future queries.

All interactions with the returned classifier are considered part of a single session and are logically grouped. For example, when a text widget is focused all user interactions around text editing (selection, editing, etc) can be grouped together to allow the classifier get better.

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classificationContext` | [TextClassificationContext](TextClassificationContext.md):The context in which classification would occur This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [TextClassifier](TextClassifier.md) | An instance to perform classification in the given context This value cannot be`null`. |

### getTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextClassifier(): TextClassifier
```

Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](TextClassificationManager.md)). If this is null, this method returns a default text classifier (i.e. either the system text classifier if one exists, or a local text classifier running in this process.)

Note that requests to the TextClassifier may be handled in an OEM-provided process rather than in the calling app's process. 
**See Also**

- [#setTextClassifier(TextClassifier)](TextClassificationManager.md)) 

### setTextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassificationSessionFactory(factory: TextClassificationSessionFactory?): Unit
```

Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factory` | [TextClassificationSessionFactory](TextClassificationSessionFactory.md)?:the textClassification session factory. If this is null, the default factory will be used. |

### setTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassifier(textClassifier: TextClassifier?): Unit
```

Sets the text classifier. Set to null to use the system default text classifier. Set to [TextClassifier.NO_OP](TextClassifier.md) to disable text classifier features.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `textClassifier` | [TextClassifier](TextClassifier.md)?:This value may be`null`. |
