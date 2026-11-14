# InspectionCompanionProvider

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InspectionCompanionProvider

Kotlin| [Java](https://developer.android.com/reference/android/view/inspector/InspectionCompanionProvider "View this page in Java") 

```
interface InspectionCompanionProvider
```

| [android.view.inspector.InspectionCompanionProvider](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanionProvider#) |

| Known Direct Subclasses [StaticInspectionCompanionProvider](https://developer.android.com/reference/kotlin/android/view/inspector/StaticInspectionCompanionProvider) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [StaticInspectionCompanionProvider](https://developer.android.com/reference/kotlin/android/view/inspector/StaticInspectionCompanionProvider) | An inspection companion provider that finds companions as inner classes or generated code. | |

An interface for services that can provide inspection companions for a class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion)\<T\>? | [provide](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanionProvider#provide(java.lang.Class))`(`cls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Provide an [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion) for the supplied class. |

## Public methods

### provide

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> provide(cls: Class<T>): InspectionCompanion<T>?
```

Provide an [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion) for the supplied class. Implementing classes must not cache companion instances, and should instantiate a new one for each request.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>:A [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#) representing the inspectable type This value cannot be`null`. |
| `<T>` | The type to find the companion for |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion)<T>? | The inspection companion for the supplied type This value may be`null`. |
