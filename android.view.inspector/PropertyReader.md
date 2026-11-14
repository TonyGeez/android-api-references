# PropertyReader

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyReader

Kotlin| [Java](../android/view/inspector/PropertyReader.md) 
| --- | --- |

```
interface PropertyReader
```

| [android.view.inspector.PropertyReader](../android/view/inspector/PropertyReader.md) |

An interface for reading the properties of an inspectable object.`PropertyReader`is defined as an interface that will be called by [InspectionCompanion.readProperties(Object, PropertyReader)](../android/view/inspector/InspectionCompanion.md)). This approach allows a client inspector to read the values of primitive properties without the overhead of instantiating a class to hold the property values for each inspection pass. If an inspectable remains unchanged between reading passes, it should be possible for a`PropertyReader`to avoid new allocations for subsequent reading passes. It has separate methods for all primitive types to avoid autoboxing overhead if a concrete implementation is able to work with primitives. Implementations should be prepared to accept {null} as the value of [PropertyReader.readObject(int, Object)](../android/view/inspector/PropertyReader.md)).

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PropertyTypeMismatchException](../android/view/inspector/PropertyReader.PropertyTypeMismatchException.md) Thrown if a client calls a typed read method for a property of a different type. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readBoolean](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Read a primitive boolean property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readByte](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Read a primitive byte property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readChar](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Read a primitive character property. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readColor](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Color](../android/graphics/Color.md)?`)` Read a [Color](../android/graphics/Color.md) object as a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readColor](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read a color packed into an int as a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readColor](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Read a color packed into a`ColorLong`as a property. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readDouble](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Read a read a primitive double property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFloat](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Read a primitive float property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readGravity](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read [android.view.Gravity](../android/view/Gravity.md) packed into an primitive`int`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readInt](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read a primitive integer property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readIntEnum](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read an enumeration packed into a primitive`int`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readIntFlag](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read a flag packed into a primitive`int`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readLong](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Read a primitive long property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readObject](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Read any object as a property. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readResourceId](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read an integer that contains a resource ID. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readShort](../android/view/inspector/PropertyReader.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Read a primitive short property. |

## Public methods

### readBoolean

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBoolean(
    id: Int, 
    value: Boolean
): Unit
```

Read a primitive boolean property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|------------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`boolean` |

### readByte

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readByte(
    id: Int, 
    value: Byte
): Unit
```

Read a primitive byte property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`byte` |

### readChar

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readChar(
    id: Int, 
    value: Char
): Unit
```

Read a primitive character property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`char` |

### readColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readColor(
    id: Int, 
    value: Color?
): Unit
```

Read a [Color](../android/graphics/Color.md) object as a property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Color](../android/graphics/Color.md)?:Value of the property This value may be`null`. |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a color |

### readColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readColor(
    id: Int, 
    value: Int
): Unit
```

Read a color packed into an int as a property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a color |

### readColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readColor(
    id: Int, 
    value: Long
): Unit
```

Read a color packed into a`ColorLong`as a property.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value of the property packed as a`ColorLong`. See the [Color](../android/graphics/Color.md) class for details of the packing. |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a color |

### readDouble

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readDouble(
    id: Int, 
    value: Double
): Unit
```

Read a read a primitive double property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|-----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`double` |

### readFloat

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readFloat(
    id: Int, 
    value: Float
): Unit
```

Read a primitive float property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`float` |

### readGravity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readGravity(
    id: Int, 
    value: Int
): Unit
```

Read [android.view.Gravity](../android/view/Gravity.md) packed into an primitive`int`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|--------------------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a gravity property |

### readInt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readInt(
    id: Int, 
    value: Int
): Unit
```

Read a primitive integer property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as an`int` |

### readIntEnum

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readIntEnum(
    id: Int, 
    value: Int
): Unit
```

Read an enumeration packed into a primitive`int`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|-----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as an object |

### readIntFlag

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readIntFlag(
    id: Int, 
    value: Int
): Unit
```

Read a flag packed into a primitive`int`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|-----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as an object |

### readLong

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readLong(
    id: Int, 
    value: Long
): Unit
```

Read a primitive long property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|---------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`long` |

### readObject

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readObject(
    id: Int, 
    value: Any?
): Unit
```

Read any object as a property. If value is null, the property is marked as empty.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:Value of the property This value may be`null`. |

| Exceptions ||
|-----------------------------------------------------------------------|-----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as an object |

### readResourceId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readResourceId(
    id: Int, 
    value: Int
): Unit
```

Read an integer that contains a resource ID.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|----------------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a resource ID. |

### readShort

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readShort(
    id: Int, 
    value: Short
): Unit
```

Read a primitive short property.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the property from a [PropertyMapper](../android/view/inspector/PropertyMapper.md) |
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):Value of the property |

| Exceptions ||
|-----------------------------------------------------------------------|----------------------------------------------|
| `android.view.inspector.PropertyReader.PropertyTypeMismatchException` | If the property ID is not mapped as a`short` |
