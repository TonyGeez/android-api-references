# IntFlagMapping

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntFlagMapping

Kotlin| [Java](IntFlagMapping.md) 
| --- | --- |

```
class IntFlagMapping
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inspector.IntFlagMapping](IntFlagMapping.md) |

Maps the values of an`int`property to sets of string for properties that encode flags. An [InspectionCompanion](InspectionCompanion.md) may provide an instance of this class to a [PropertyMapper](PropertyMapper.md) for flag values packed into primitive`int`properties. Each flag has a mask and a target value, for non-exclusive flags, the target can also be used as the mask. A given integer value is compared against each flag to find what flags are active for it by bitwise anding it with the mask and comparing the result against the target, that is,`(value & mask) == target`.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [IntFlagMapping](IntFlagMapping.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](IntFlagMapping.md))`(`mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Add a mutually exclusive flag to the map. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [get](IntFlagMapping.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a set of the names of enabled flags for a given property value. |

## Public constructors

### IntFlagMapping

```
IntFlagMapping()
```

## Public methods

### add

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(
    mask: Int, 
    target: Int, 
    name: String
): Unit
```

Add a mutually exclusive flag to the map.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bit mask to compare to and with a value |
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target value to compare the masked value with |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the flag to include if enabled This value cannot be`null`. |
| --- | --- |

### get

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(value: Int): MutableSet<String!>
```

Get a set of the names of enabled flags for a given property value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value of the property |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The names of the enabled flags, empty if no flags enabled This value cannot be`null`. |
