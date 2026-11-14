# Struct

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Struct

```
interface Struct
```

| [java.sql.Struct](Struct.md) |

The standard mapping in the Java programming language for an SQL structured type. A `Struct` object contains a value for each attribute of the SQL structured type that it represents. By default, an instance of`Struct` is valid as long as the application has a reference to it.

All methods on the `Struct` interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getAttributes](Struct.md))`()` Produces the ordered values of the attributes of the SQL structured type that this `Struct` object represents. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getAttributes](Struct.md))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Produces the ordered values of the attributes of the SQL structured type that this `Struct` object represents. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLTypeName](Struct.md))`()` Retrieves the SQL type name of the SQL structured type that this `Struct` object represents. |
| --- | --- |

## Public methods

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributes(): Array<Any!>!
```

Produces the ordered values of the attributes of the SQL structured type that this `Struct` object represents. As individual attributes are processed, this method uses the type map associated with the connection for customizations of the type mappings. If there is no entry in the connection's type map that matches the structured type that an attribute represents, the driver uses the standard mapping.

Conceptually, this method calls the method `getObject` on each attribute of the structured type and returns a Java array containing the result.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array containing the ordered attribute values |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributes(map: MutableMap<String!, Class<*>!>!): Array<Any!>!
```

Produces the ordered values of the attributes of the SQL structured type that this `Struct` object represents. As individual attrbutes are proccessed, this method uses the given type map for customizations of the type mappings. If there is no entry in the given type map that matches the structured type that an attribute represents, the driver uses the standard mapping. This method never uses the type map associated with the connection.

Conceptually, this method calls the method `getObject` on each attribute of the structured type and returns a Java array containing the result.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!: a mapping of SQL type names to Java classes |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array containing the ordered attribute values |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getSQLTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSQLTypeName(): String!
```

Retrieves the SQL type name of the SQL structured type that this `Struct` object represents.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully-qualified type name of the SQL structured type for which this `Struct` object is the generic representation |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
