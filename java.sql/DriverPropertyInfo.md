# DriverPropertyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DriverPropertyInfo

```
open class DriverPropertyInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.sql.DriverPropertyInfo](DriverPropertyInfo.md) |

Driver properties for making a connection. The`DriverPropertyInfo`class is of interest only to advanced programmers who need to interact with a Driver via the method`getDriverProperties`to discover and supply properties for connections.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DriverPropertyInfo](DriverPropertyInfo.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`DriverPropertyInfo`object with a given name and value. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [choices](DriverPropertyInfo.md) An array of possible values if the value for the field`DriverPropertyInfo.value`may be selected from a particular set of values; otherwise null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [description](DriverPropertyInfo.md) A brief description of the property, which may be null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](DriverPropertyInfo.md) The name of the property. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [required](DriverPropertyInfo.md) The`required`field is`true`if a value must be supplied for this property during`Driver.connect`and`false`otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [value](DriverPropertyInfo.md) The`value`field specifies the current value of the property, based on a combination of the information supplied to the method`getPropertyInfo`, the Java environment, and the driver-supplied default values. |

## Public constructors

### DriverPropertyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DriverPropertyInfo(
    name: String!, 
    value: String!)
```

Constructs a`DriverPropertyInfo`object with a given name and value. The`description`and`choices`are intialized to`null`and`required`is initialized to`false`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the property |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the current value, which may be null |

## Properties

### choices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var choices: Array<String!>!
```

An array of possible values if the value for the field`DriverPropertyInfo.value`may be selected from a particular set of values; otherwise null. 

### description

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var description: String!
```

A brief description of the property, which may be null. 

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var name: String!
```

The name of the property. 

### required

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var required: Boolean
```

The`required`field is`true`if a value must be supplied for this property during`Driver.connect`and`false`otherwise. 

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var value: String!
```

The`value`field specifies the current value of the property, based on a combination of the information supplied to the method`getPropertyInfo`, the Java environment, and the driver-supplied default values. This field may be null if no value is known.
