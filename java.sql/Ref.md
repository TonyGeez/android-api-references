# Ref

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ref

```
interface Ref
```

| [java.sql.Ref](https://developer.android.com/reference/kotlin/java/sql/Ref#) |

The mapping in the Java programming language of an SQL`REF`value, which is a reference to an SQL structured type value in the database.

SQL`REF`values are stored in a table that contains instances of a referenceable SQL structured type, and each`REF`value is a unique identifier for one instance in that table. An SQL`REF`value may be used in place of the SQL structured type it references, either as a column value in a table or an attribute value in a structured type.

Because an SQL`REF`value is a logical pointer to an SQL structured type, a`Ref`object is by default also a logical pointer. Thus, retrieving an SQL`REF`value as a`Ref`object does not materialize the attributes of the structured type on the client.

A`Ref`object can be stored in the database using the`PreparedStatement.setRef`method.

All methods on the`Ref`interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseTypeName](https://developer.android.com/reference/kotlin/java/sql/Ref#getBaseTypeName())`()` Retrieves the fully-qualified SQL name of the SQL structured type that this`Ref`object references. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/Ref#getObject())`()` Retrieves the SQL structured type instance referenced by this`Ref`object. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/Ref#getObject(kotlin.collections.MutableMap))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!>!`)` Retrieves the referenced object and maps it to a Java type using the given type map. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/Ref#setObject(kotlin.Any))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the structured type value that this`Ref`object references to the given instance of`Object`. |

## Public methods

### getBaseTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseTypeName(): String!
```

Retrieves the fully-qualified SQL name of the SQL structured type that this`Ref`object references.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully-qualified SQL name of the referenced SQL structured type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(): Any!
```

Retrieves the SQL structured type instance referenced by this`Ref`object. If the connection's type map has an entry for the structured type, the instance will be custom mapped to the Java class indicated in the type map. Otherwise, the structured type instance will be mapped to a`Struct`object.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a Java`Object`that is the mapping for the SQL structured type to which this`Ref`object refers |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setObject](https://developer.android.com/reference/kotlin/java/sql/Ref#setObject(kotlin.Any)) 

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(map: MutableMap<String!, Class<*>!>!): Any!
```

Retrieves the referenced object and maps it to a Java type using the given type map.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!\>!:a`java.util.Map`object that contains the mapping to use (the fully-qualified name of the SQL structured type being referenced and the class object for`SQLData`implementation to which the SQL structured type will be mapped) |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a Java`Object`that is the custom mapping for the SQL structured type to which this`Ref`object refers |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setObject](https://developer.android.com/reference/kotlin/java/sql/Ref#setObject(kotlin.Any)) 

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(value: Any!): Unit
```

Sets the structured type value that this`Ref`object references to the given instance of`Object`. The driver converts this to an SQL structured type when it sends it to the database.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:an`Object`representing the SQL structured type instance that this`Ref`object will reference |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- <https://developer.android.com/reference/kotlin/java/sql/Ref#getObject()>
- [java.sql.PreparedStatement#setObject(int, Object)](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any))
- [java.sql.CallableStatement#setObject(String, Object)](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setObject(kotlin.String,%20kotlin.Any))
