# StaticInspectionCompanionProvider

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StaticInspectionCompanionProvider

Kotlin| [Java](https://developer.android.com/reference/android/view/inspector/StaticInspectionCompanionProvider "View this page in Java") 
| --- | --- |

```
open class StaticInspectionCompanionProvider : InspectionCompanionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inspector.StaticInspectionCompanionProvider](https://developer.android.com/reference/kotlin/android/view/inspector/StaticInspectionCompanionProvider#) |

An inspection companion provider that finds companions as inner classes or generated code.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StaticInspectionCompanionProvider](https://developer.android.com/reference/kotlin/android/view/inspector/StaticInspectionCompanionProvider#StaticInspectionCompanionProvider())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion)\<T\>? | [provide](https://developer.android.com/reference/kotlin/android/view/inspector/StaticInspectionCompanionProvider#provide(java.lang.Class))`(`cls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Provide an [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion) for the supplied class. |

## Public constructors

### StaticInspectionCompanionProvider

```
StaticInspectionCompanionProvider()
```

## Public methods

### provide

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> provide(cls: Class<T>): InspectionCompanion<T>?
```

Provide an [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion) for the supplied class. Implementing classes must not cache companion instances, and should instantiate a new one for each request.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>:This value cannot be`null`. |
| `<T>` | The type to find the companion for |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------|
| [InspectionCompanion](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion)<T>? | This value may be`null`. |
