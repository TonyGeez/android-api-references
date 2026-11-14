# PropertyMapper

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyMapper

Kotlin| [Java](../android/view/inspector/PropertyMapper.md) 
| --- | --- |

```
interface PropertyMapper
```

| [android.view.inspector.PropertyMapper](../android/view/inspector/PropertyMapper.md) |

An interface for mapping the string names of inspectable properties to integer identifiers. This interface is consumed by [InspectionCompanion.mapProperties(PropertyMapper)](../android/view/inspector/InspectionCompanion.md)). Mapping properties to IDs enables quick comparisons against shadow copies of inspectable objects without performing a large number of string comparisons. Properties that derive their value from an XML attribute should provide the attribute resource ID (e.g.:`R.attr.color`). For runtime or generated properties properties without attribute IDs, supply [Resources.ID_NULL](../android/content/res/Resources.md) for`attributeId`.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PropertyConflictException](../android/view/inspector/PropertyMapper.PropertyConflictException.md) Thrown from a map method if a property name is already mapped as different type. |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapBoolean](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive boolean property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapByte](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive byte property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapChar](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive char property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapColor](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a color property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapDouble](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive double property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapFloat](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive float property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapGravity](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a gravity property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapInt](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive int property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapIntEnum](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mapping:` ` [IntFunction](../java/util/function/IntFunction.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Map a string name to an integer ID for an enumeration packed into an int property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapIntFlag](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mapping:` ` [IntFunction](../java/util/function/IntFunction.md)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>`)` Map a string name to an integer ID for a flag set packed into an int property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapLong](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive long property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapObject](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for an object property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapResourceId](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for an attribute that contains resource IDs. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapShort](../android/view/inspector/PropertyMapper.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive short property. |

## Public methods

### mapBoolean

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapBoolean(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive boolean property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapByte

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapByte(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive byte property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapChar

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapChar(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive char property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapColor(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a color property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

**See Also**

- [android.graphics.Color](../android/graphics/Color.md) 

### mapDouble

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapDouble(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive double property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapFloat

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapFloat(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive float property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapGravity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapGravity(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a gravity property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

**See Also**

- [android.view.Gravity](../android/view/Gravity.md) 

### mapInt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapInt(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive int property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapIntEnum

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapIntEnum(
    name: String, 
    attributeId: Int, 
    mapping: IntFunction<String!>
): Int
```

Map a string name to an integer ID for an enumeration packed into an int property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |
| `mapping` | [IntFunction](../java/util/function/IntFunction.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A mapping from int to String This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapIntFlag

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapIntFlag(
    name: String, 
    attributeId: Int, 
    mapping: IntFunction<MutableSet<String!>!>
): Int
```

Map a string name to an integer ID for a flag set packed into an int property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |
| `mapping` | [IntFunction](../java/util/function/IntFunction.md)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>:A mapping from int to a set of strings This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapLong

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapLong(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive long property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapObject

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapObject(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for an object property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapResourceId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapResourceId(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for an attribute that contains resource IDs.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

### mapShort

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapShort(
    name: String, 
    attributeId: Int
): Int
```

Map a string name to an integer ID for a primitive short property.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property This value cannot be`null`. |
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](../android/content/res/Resources.md) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |
