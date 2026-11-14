# StaticInspectionCompanionProvider

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StaticInspectionCompanionProvider

Kotlin| [Java](StaticInspectionCompanionProvider.md) 
| --- | --- |

```
open class StaticInspectionCompanionProvider : InspectionCompanionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inspector.StaticInspectionCompanionProvider](StaticInspectionCompanionProvider.md) |

An inspection companion provider that finds companions as inner classes or generated code.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StaticInspectionCompanionProvider](StaticInspectionCompanionProvider.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InspectionCompanion](InspectionCompanion.md)\<T\>? | [provide](StaticInspectionCompanionProvider.md))`(`cls:` ` [Class](../java.lang/Class.md)<T>`)` Provide an [InspectionCompanion](InspectionCompanion.md) for the supplied class. |

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

Provide an [InspectionCompanion](InspectionCompanion.md) for the supplied class. Implementing classes must not cache companion instances, and should instantiate a new one for each request.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](../java.lang/Class.md)\<T\>:This value cannot be`null`. |
| `<T>` | The type to find the companion for |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------|
| [InspectionCompanion](InspectionCompanion.md)<T>? | This value may be`null`. |
