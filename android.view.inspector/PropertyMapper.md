# PropertyMapper

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyMapper

Kotlin| [Java](https://developer.android.com/reference/android/view/inspector/PropertyMapper "View this page in Java") 
| --- | --- |

```
interface PropertyMapper
```

| [android.view.inspector.PropertyMapper](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#) |

An interface for mapping the string names of inspectable properties to integer identifiers. This interface is consumed by [InspectionCompanion.mapProperties(PropertyMapper)](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion#mapProperties(android.view.inspector.PropertyMapper)). Mapping properties to IDs enables quick comparisons against shadow copies of inspectable objects without performing a large number of string comparisons. Properties that derive their value from an XML attribute should provide the attribute resource ID (e.g.:`R.attr.color`). For runtime or generated properties properties without attribute IDs, supply [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) for`attributeId`.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PropertyConflictException](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper.PropertyConflictException) Thrown from a map method if a property name is already mapped as different type. |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapBoolean](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapBoolean(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive boolean property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapByte](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapByte(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive byte property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapChar](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapChar(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive char property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapColor](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapColor(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a color property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapDouble](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapDouble(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive double property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapFloat](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapFloat(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive float property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapGravity](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapGravity(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a gravity property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapInt](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapInt(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive int property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapIntEnum](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapIntEnum(kotlin.String,%20kotlin.Int,%20java.util.function.IntFunction))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mapping:` ` [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Map a string name to an integer ID for an enumeration packed into an int property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapIntFlag](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapIntFlag(kotlin.String,%20kotlin.Int,%20java.util.function.IntFunction))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mapping:` ` [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>`)` Map a string name to an integer ID for a flag set packed into an int property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapLong](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapLong(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive long property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapObject](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapObject(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for an object property. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapResourceId](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapResourceId(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for an attribute that contains resource IDs. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mapShort](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper#mapShort(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributeId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map a string name to an integer ID for a primitive short property. |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

**See Also**

- [android.graphics.Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#) 

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |

**See Also**

- [android.view.Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity.html#) 

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |
| `mapping` | [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:A mapping from int to String This value cannot be`null`. |
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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |
| `mapping` | [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>:A mapping from int to a set of strings This value cannot be`null`. |
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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

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
| `attributeId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The attribute resource ID of this property, or [Resources.ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An integer ID for the property |

| Exceptions ||
|-------------------------------------------------------------------|---------------------------------------------------------|
| `android.view.inspector.PropertyMapper.PropertyConflictException` | If the property name is already mapped as another type. |
