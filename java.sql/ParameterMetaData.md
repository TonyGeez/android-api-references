# ParameterMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParameterMetaData

```
interface ParameterMetaData : Wrapper
```

| [java.sql.ParameterMetaData](../java/sql/ParameterMetaData.md) |

An object that can be used to get information about the types and properties for each parameter marker in a`PreparedStatement`object. For some queries and driver implementations, the data that would be returned by a`ParameterMetaData`object may not be available until the`PreparedStatement`has been executed.

Some driver implementations may not be able to provide information about the types and properties for each parameter marker in a`CallableStatement`object.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterModeIn](../java/sql/ParameterMetaData.md) The constant indicating that the parameter's mode is IN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterModeInOut](../java/sql/ParameterMetaData.md) The constant indicating that the parameter's mode is INOUT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterModeOut](../java/sql/ParameterMetaData.md) The constant indicating that the parameter's mode is OUT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterModeUnknown](../java/sql/ParameterMetaData.md) The constant indicating that the mode of the parameter is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterNoNulls](../java/sql/ParameterMetaData.md) The constant indicating that a parameter will not allow`NULL`values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterNullable](../java/sql/ParameterMetaData.md) The constant indicating that a parameter will allow`NULL`values. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterNullableUnknown](../java/sql/ParameterMetaData.md) The constant indicating that the nullability of a parameter is unknown. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParameterClassName](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the fully-qualified name of the Java class whose instances should be passed to the method`PreparedStatement.setObject`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterCount](../java/sql/ParameterMetaData.md))`()` Retrieves the number of parameters in the`PreparedStatement`object for which this`ParameterMetaData`object contains information. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterMode](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated parameter's mode. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterType](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated parameter's SQL type. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getParameterTypeName](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated parameter's database-specific type name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated parameter's specified column size. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScale](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated parameter's number of digits to right of the decimal point. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [isNullable](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether null values are allowed in the designated parameter. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSigned](../java/sql/ParameterMetaData.md))`(`param:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether values for the designated parameter can be signed numbers. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Wrapper](../java/sql/Wrapper.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](../java/sql/Wrapper.md))`(`iface:` ` [Class](../java/lang/Class.md)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](../java/sql/Wrapper.md))`(`iface:` ` [Class](../java/lang/Class.md)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Constants

### parameterModeIn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterModeIn: Int
```

The constant indicating that the parameter's mode is IN. 

 Value: 1

### parameterModeInOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterModeInOut: Int
```

The constant indicating that the parameter's mode is INOUT. 

 Value: 2

### parameterModeOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterModeOut: Int
```

The constant indicating that the parameter's mode is OUT. 

 Value: 4

### parameterModeUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterModeUnknown: Int
```

The constant indicating that the mode of the parameter is unknown. 

 Value: 0

### parameterNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterNoNulls: Int
```

The constant indicating that a parameter will not allow`NULL`values. 

 Value: 0

### parameterNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterNullable: Int
```

The constant indicating that a parameter will allow`NULL`values. 

 Value: 1

### parameterNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val parameterNullableUnknown: Int
```

The constant indicating that the nullability of a parameter is unknown. 

 Value: 2

## Public methods

### getParameterClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterClassName(param: Int): String!
```

Retrieves the fully-qualified name of the Java class whose instances should be passed to the method`PreparedStatement.setObject`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully-qualified name of the class in the Java programming language that would be used by the method`PreparedStatement.setObject`to set the value in the specified parameter. This is the class name used for custom mapping. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getParameterCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterCount(): Int
```

Retrieves the number of parameters in the`PreparedStatement`object for which this`ParameterMetaData`object contains information.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of parameters |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getParameterMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterMode(param: Int): Int
```

Retrieves the designated parameter's mode.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mode of the parameter; one of`ParameterMetaData.parameterModeIn`,`ParameterMetaData.parameterModeOut`, or`ParameterMetaData.parameterModeInOut``ParameterMetaData.parameterModeUnknown`. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getParameterType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterType(param: Int): Int
```

Retrieves the designated parameter's SQL type.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | SQL type from`java.sql.Types` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Types](../java/sql/Types.md) 

### getParameterTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterTypeName(param: Int): String!
```

Retrieves the designated parameter's database-specific type name.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | type the name used by the database. If the parameter type is a user-defined type, then a fully-qualified type name is returned. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrecision(param: Int): Int
```

Retrieves the designated parameter's specified column size.

The returned value represents the maximum column size for the given parameter. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. 0 is returned for data types where the column size is not applicable.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | precision |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getScale(param: Int): Int
```

Retrieves the designated parameter's number of digits to right of the decimal point. 0 is returned for data types where the scale is not applicable.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | scale |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNullable(param: Int): Int
```

Retrieves whether null values are allowed in the designated parameter.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the nullability status of the given parameter; one of`ParameterMetaData.parameterNoNulls`,`ParameterMetaData.parameterNullable`, or`ParameterMetaData.parameterNullableUnknown` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isSigned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSigned(param: Int): Boolean
```

Retrieves whether values for the designated parameter can be signed numbers.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
