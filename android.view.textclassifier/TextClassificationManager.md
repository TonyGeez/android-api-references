# TextClassificationManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassificationManager

Kotlin| [Java](https://developer.android.com/reference/android/view/textclassifier/TextClassificationManager "View this page in Java") 

```
class TextClassificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.textclassifier.TextClassificationManager](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#) |

Interface to the text classification service.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) | [createTextClassificationSession](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#createTextClassificationSession(android.view.textclassifier.TextClassificationContext))`(`classificationContext:` ` [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext)`)` Call this method to start a text classification session with the given context. |
| [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) | [getTextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#getTextClassifier())`()` Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#setTextClassifier(android.view.textclassifier.TextClassifier)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassificationSessionFactory](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#setTextClassificationSessionFactory(android.view.textclassifier.TextClassificationSessionFactory))`(`factory:` ` [TextClassificationSessionFactory](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationSessionFactory)?`)` Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#setTextClassifier(android.view.textclassifier.TextClassifier))`(`textClassifier:` ` [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier)?`)` Sets the text classifier. |

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
| `classificationContext` | [TextClassificationContext](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationContext):The context in which classification would occur This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier) | An instance to perform classification in the given context This value cannot be`null`. |

### getTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextClassifier(): TextClassifier
```

Returns the text classifier that was set via [setTextClassifier(android.view.textclassifier.TextClassifier)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#setTextClassifier(android.view.textclassifier.TextClassifier)). If this is null, this method returns a default text classifier (i.e. either the system text classifier if one exists, or a local text classifier running in this process.)

Note that requests to the TextClassifier may be handled in an OEM-provided process rather than in the calling app's process. 
**See Also**

- [#setTextClassifier(TextClassifier)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager#setTextClassifier(android.view.textclassifier.TextClassifier)) 

### setTextClassificationSessionFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassificationSessionFactory(factory: TextClassificationSessionFactory?): Unit
```

Sets a TextClassificationSessionFactory to be used to create session-aware TextClassifiers.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factory` | [TextClassificationSessionFactory](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationSessionFactory)?:the textClassification session factory. If this is null, the default factory will be used. |

### setTextClassifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTextClassifier(textClassifier: TextClassifier?): Unit
```

Sets the text classifier. Set to null to use the system default text classifier. Set to [TextClassifier.NO_OP](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#NO_OP:android.view.textclassifier.TextClassifier) to disable text classifier features.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `textClassifier` | [TextClassifier](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier)?:This value may be`null`. |
