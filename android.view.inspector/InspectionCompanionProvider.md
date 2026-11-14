# InspectionCompanionProvider

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InspectionCompanionProvider

Kotlin| [Java](InspectionCompanionProvider.md) 
| --- | --- |

```
interface InspectionCompanionProvider
```

| [android.view.inspector.InspectionCompanionProvider](InspectionCompanionProvider.md) |

| Known Direct Subclasses [StaticInspectionCompanionProvider](StaticInspectionCompanionProvider.md) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [StaticInspectionCompanionProvider](StaticInspectionCompanionProvider.md) | An inspection companion provider that finds companions as inner classes or generated code. | |
| --- | --- | --- | --- | --- | --- | --- |

An interface for services that can provide inspection companions for a class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [InspectionCompanion](InspectionCompanion.md)\<T\>? | [provide](InspectionCompanionProvider.md))`(`cls:` ` [Class](../java.lang/Class.md)<T>`)` Provide an [InspectionCompanion](InspectionCompanion.md) for the supplied class. |

## Public methods

### provide

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> provide(cls: Class<T>): InspectionCompanion<T>?
```

Provide an [InspectionCompanion](InspectionCompanion.md) for the supplied class. Implementing classes must not cache companion instances, and should instantiate a new one for each request.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](../java.lang/Class.md)\<T\>:A [Class](../java.lang/Class.md) representing the inspectable type This value cannot be`null`. |
| `<T>` | The type to find the companion for |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [InspectionCompanion](InspectionCompanion.md)<T>? | The inspection companion for the supplied type This value may be`null`. |
