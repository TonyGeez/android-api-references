# TextClassificationManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationManager

Kotlin| [Java](../android/view/textclassifier/TextClassificationManager.md) 
| --- | --- |

```
class TextClassificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextClassificationManager](../android/view/textclassifier/TextClassificationManager.md) |

Interface to the text classification service.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TextClassifier](../android/view/textclassifier/TextClassifier.md) | [createTextClassificationSession](../android/view/textclassifier/TextClassificationManager.md))`(`classificationContext:` ` [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md)`)` Call this method to start a text classification session with the given context. |
| [TextClassifier](../android/view/textclassifier/TextClassifier.md) | [getTextClassifier](../android/view/textclassifier/TextClassificationManager.md))`()` Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](../android/view/textclassifier/TextClassificationManager.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassificationSessionFactory](../android/view/textclassifier/TextClassificationManager.md))`(`factory:` ` [TextClassificationSessionFactory](../android/view/textclassifier/TextClassificationSessionFactory.md)?`)` Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassifier](../android/view/textclassifier/TextClassificationManager.md))`(`textClassifier:` ` [TextClassifier](../android/view/textclassifier/TextClassifier.md)?`)` Sets the text classifier. |

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
| `classificationContext` | [TextClassificationContext](../android/view/textclassifier/TextClassificationContext.md):The context in which classification would occur This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [TextClassifier](../android/view/textclassifier/TextClassifier.md) | An instance to perform classification in the given context This value cannot be`null`. |

### getTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextClassifier(): TextClassifier
```

Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](../android/view/textclassifier/TextClassificationManager.md)). If this is null, this method returns a default text classifier (i.e. either the system text classifier if one exists, or a local text classifier running in this process.)

Note that requests to the TextClassifier may be handled in an OEM-provided process rather than in the calling app's process. 
**See Also**

- [#setTextClassifier(TextClassifier)](../android/view/textclassifier/TextClassificationManager.md)) 

### setTextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassificationSessionFactory(factory: TextClassificationSessionFactory?): Unit
```

Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factory` | [TextClassificationSessionFactory](../android/view/textclassifier/TextClassificationSessionFactory.md)?:the textClassification session factory. If this is null, the default factory will be used. |

### setTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassifier(textClassifier: TextClassifier?): Unit
```

Sets the text classifier. Set to null to use the system default text classifier. Set to [TextClassifier.NO_OP](../android/view/textclassifier/TextClassifier.md) to disable text classifier features.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `textClassifier` | [TextClassifier](../android/view/textclassifier/TextClassifier.md)?:This value may be`null`. |
