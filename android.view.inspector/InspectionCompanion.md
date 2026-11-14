# InspectionCompanion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InspectionCompanion

Kotlin| [Java](../android/view/inspector/InspectionCompanion.md) 
| --- | --- |

```
interface InspectionCompanion<T : Any!>
```

| [android.view.inspector.InspectionCompanion](../android/view/inspector/InspectionCompanion.md) |

An interface for companion objects used to inspect views. Inspection companions only need to handle the properties and node name of the specific class they are defined for, not anything from a parent class. At runtime, the inspector instantiates one instance of each inspection companion, and handles visiting them in the correct inheritance order for each type it inspects. Properties are read from the top of the type tree to the bottom, so that classes that override a property in their parent class can overwrite it in the reader. In general, properties will cleanly inherit through their getters, and the inspector runtime will read the properties of a parent class via the parent's inspection companion, and the child companion will only read properties added or changed since the parent was defined.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [UninitializedPropertyMapException](../android/view/inspector/InspectionCompanion.UninitializedPropertyMapException.md) Thrown by [readProperties(java.lang.Object,android.view.inspector.PropertyReader)](../android/view/inspector/InspectionCompanion.md))if called before [mapProperties(android.view.inspector.PropertyMapper)](../android/view/inspector/InspectionCompanion.md)). |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapProperties](../android/view/inspector/InspectionCompanion.md))`(`propertyMapper:` ` [PropertyMapper](../android/view/inspector/PropertyMapper.md)`)` Map the string names of the properties this companion knows about to integer IDs. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readProperties](../android/view/inspector/InspectionCompanion.md))`(`inspectable:` `T`, `propertyReader:` ` [PropertyReader](../android/view/inspector/PropertyReader.md)`)` Read the values of an instance of this companion's type into a [PropertyReader](../android/view/inspector/PropertyReader.md). |

## Public methods

### mapProperties

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapProperties(propertyMapper: PropertyMapper): Unit
```

Map the string names of the properties this companion knows about to integer IDs. Each companion is responsible for storing the integer IDs of all its properties. This is the only method that is allowed to modify the stored IDs. Calling [readProperties(T,android.view.inspector.PropertyReader)](../android/view/inspector/InspectionCompanion.md))before calling this results in undefined behavior.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyMapper` | [PropertyMapper](../android/view/inspector/PropertyMapper.md):A [PropertyMapper](../android/view/inspector/PropertyMapper.md) maps string names to IDs. This value cannot be`null`. |

### readProperties

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readProperties(
    inspectable: T, 
    propertyReader: PropertyReader
): Unit
```

Read the values of an instance of this companion's type into a [PropertyReader](../android/view/inspector/PropertyReader.md). This method needs to return the property IDs stored by [mapProperties(android.view.inspector.PropertyMapper)](../android/view/inspector/InspectionCompanion.md)). Implementations should track if their properties have been mapped and throw a [UninitializedPropertyMapException](../android/view/inspector/InspectionCompanion.UninitializedPropertyMapException.md) if this method is called before {mapProperties}.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inspectable` | T:A object of type {T} to read the properties of. This value cannot be`null`. |
| `propertyReader` | [PropertyReader](../android/view/inspector/PropertyReader.md):An object which receives the property IDs and values. This value cannot be`null`. |
