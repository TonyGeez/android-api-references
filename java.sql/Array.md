# Array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Array

```
interface Array
```

| [java.sql.Array](Array.md) |

The mapping in the Java programming language for the SQL type `ARRAY`. By default, an `Array` value is a transaction-duration reference to an SQL `ARRAY` value. By default, an `Array` object is implemented using an SQL LOCATOR(array) internally, which means that an `Array` object contains a logical pointer to the data in the SQL `ARRAY` value rather than containing the `ARRAY` value's data.

The `Array` interface provides methods for bringing an SQL `ARRAY` value's data to the client as either an array or a `ResultSet` object. If the elements of the SQL `ARRAY` are a UDT, they may be custom mapped. To create a custom mapping, a programmer must do two things:

- create a class that implements the [SQLData](SQLData.md) interface for the UDT to be custom mapped.
- make an entry in a type map that contains
 - the fully-qualified SQL type name of the UDT
 - the `Class` object for the class implementing `SQLData`

When a type map with an entry for the base type is supplied to the methods `getArray` and `getResultSet`, the mapping it contains will be used to map the elements of the `ARRAY` value. If no type map is supplied, which would typically be the case, the connection's type map is used by default. If the connection's type map or a type map supplied to a method has no entry for the base type, the elements are mapped according to the standard mapping.

All methods on the `Array` interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [free](Array.md))`()` This method frees the `Array` object and releases the resources that it holds. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getArray](Array.md))`()` Retrieves the contents of the SQL `ARRAY` value designated by this `Array` object in the form of an array in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getArray](Array.md))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Retrieves the contents of the SQL `ARRAY` value designated by this `Array` object. |
| --- | --- |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getArray](Array.md))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves a slice of the SQL `ARRAY` value designated by this `Array` object, beginning with the specified `index` and containing up to `count` successive elements of the SQL array. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getArray](Array.md))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Retreives a slice of the SQL `ARRAY` value designated by this `Array` object, beginning with the specified `index` and containing up to `count` successive elements of the SQL array. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseType](Array.md))`()` Retrieves the JDBC type of the elements in the array designated by this `Array` object. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseTypeName](Array.md))`()` Retrieves the SQL type name of the elements in the array designated by this `Array` object. |
| abstract [ResultSet](ResultSet.md)! | [getResultSet](Array.md))`()` Retrieves a result set that contains the elements of the SQL `ARRAY` value designated by this `Array` object. |
| abstract [ResultSet](ResultSet.md)! | [getResultSet](Array.md))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Retrieves a result set that contains the elements of the SQL `ARRAY` value designated by this `Array` object. |
| --- | --- |
| abstract [ResultSet](ResultSet.md)! | [getResultSet](Array.md))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves a result set holding the elements of the subarray that starts at index `index` and contains up to `count` successive elements. |
| abstract [ResultSet](ResultSet.md)! | [getResultSet](Array.md))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Retrieves a result set holding the elements of the subarray that starts at index `index` and contains up to `count` successive elements. |

## Public methods

### free

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun free(): Unit
```

This method frees the `Array` object and releases the resources that it holds. The object is invalid once the `free` method is called.

After `free` has been called, any attempt to invoke a method other than `free` will result in a `SQLException` being thrown. If `free` is called multiple times, the subsequent calls to `free` are treated as a no-op.

<br />

| Exceptions ||
|--------------------------------------------|----------------------------------------------------|
| `java.sql.SQLException` | if an error occurs releasing the Array's resources |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(): Any!
```

Retrieves the contents of the SQL `ARRAY` value designated by this `Array` object in the form of an array in the Java programming language. This version of the method `getArray` uses the type map associated with the connection for customizations of the type mappings.

**Note:** When `getArray` is used to materialize a base type that maps to a primitive data type, then it is implementation-defined whether the array returned is an array of that primitive data type or an array of `Object`.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | an array in the Java programming language that contains the ordered elements of the SQL `ARRAY` value designated by this `Array` object |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(map: MutableMap<String!, Class<*>!>!): Any!
```

Retrieves the contents of the SQL `ARRAY` value designated by this `Array` object. This method uses the specified `map` for type map customizations unless the base type of the array does not match a user-defined type in `map`, in which case it uses the standard mapping. This version of the method `getArray` uses either the given type map or the standard mapping; it never uses the type map associated with the connection.

**Note:** When `getArray` is used to materialize a base type that maps to a primitive data type, then it is implementation-defined whether the array returned is an array of that primitive data type or an array of `Object`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!: a `java.util.Map` object that contains mappings of SQL type names to classes in the Java programming language |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | an array in the Java programming language that contains the ordered elements of the SQL array designated by this object |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(
    index: Long, 
    count: Int
): Any!
```

Retrieves a slice of the SQL `ARRAY` value designated by this `Array` object, beginning with the specified `index` and containing up to `count` successive elements of the SQL array. This method uses the type map associated with the connection for customizations of the type mappings.

**Note:** When `getArray` is used to materialize a base type that maps to a primitive data type, then it is implementation-defined whether the array returned is an array of that primitive data type or an array of `Object`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the array index of the first element to retrieve; the first element is at index 1 |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of successive SQL array elements to retrieve |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | an array containing up to `count` consecutive elements of the SQL array, beginning with element `index` |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(
    index: Long, 
    count: Int, 
    map: MutableMap<String!, Class<*>!>!
): Any!
```

Retreives a slice of the SQL `ARRAY` value designated by this `Array` object, beginning with the specified `index` and containing up to `count` successive elements of the SQL array.

This method uses the specified `map` for type map customizations unless the base type of the array does not match a user-defined type in `map`, in which case it uses the standard mapping. This version of the method `getArray` uses either the given type map or the standard mapping; it never uses the type map associated with the connection.

**Note:** When `getArray` is used to materialize a base type that maps to a primitive data type, then it is implementation-defined whether the array returned is an array of that primitive data type or an array of `Object`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the array index of the first element to retrieve; the first element is at index 1 |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of successive SQL array elements to retrieve |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!: a `java.util.Map` object that contains SQL type names and the classes in the Java programming language to which they are mapped |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | an array containing up to `count` consecutive elements of the SQL `ARRAY` value designated by this `Array` object, beginning with element `index` |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBaseType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseType(): Int
```

Retrieves the JDBC type of the elements in the array designated by this `Array` object.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a constant from the class [java.sql.Types](Types.md) that is the type code for the elements in the array designated by this `Array` object |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the base type |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBaseTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseTypeName(): String!
```

Retrieves the SQL type name of the elements in the array designated by this `Array` object. If the elements are a built-in type, it returns the database-specific type name of the elements. If the elements are a user-defined type (UDT), this method returns the fully-qualified SQL type name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a `String` that is the database-specific name for a built-in base type; or the fully-qualified SQL type name for a base type that is a UDT |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the type name |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getResultSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResultSet(): ResultSet!
```

Retrieves a result set that contains the elements of the SQL `ARRAY` value designated by this `Array` object. If appropriate, the elements of the array are mapped using the connection's type map; otherwise, the standard mapping is used.

The result set contains one row for each array element, with two columns in each row. The second column stores the element value; the first column stores the index into the array for that element (with the first array element being at index 1). The rows are in ascending order corresponding to the order of the indices.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ResultSet](ResultSet.md)! | a [ResultSet](ResultSet.md) object containing one row for each of the elements in the array designated by this `Array` object, with the rows in ascending order based on the indices. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getResultSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResultSet(map: MutableMap<String!, Class<*>!>!): ResultSet!
```

Retrieves a result set that contains the elements of the SQL `ARRAY` value designated by this `Array` object. This method uses the specified `map` for type map customizations unless the base type of the array does not match a user-defined type in `map`, in which case it uses the standard mapping. This version of the method `getResultSet` uses either the given type map or the standard mapping; it never uses the type map associated with the connection.

The result set contains one row for each array element, with two columns in each row. The second column stores the element value; the first column stores the index into the array for that element (with the first array element being at index 1). The rows are in ascending order corresponding to the order of the indices.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!: contains the mapping of SQL user-defined types to classes in the Java programming language |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ResultSet](ResultSet.md)! | a `ResultSet` object containing one row for each of the elements in the array designated by this `Array` object, with the rows in ascending order based on the indices. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getResultSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResultSet(
    index: Long, 
    count: Int
): ResultSet!
```

Retrieves a result set holding the elements of the subarray that starts at index `index` and contains up to `count` successive elements. This method uses the connection's type map to map the elements of the array if the map contains an entry for the base type. Otherwise, the standard mapping is used.

The result set has one row for each element of the SQL array designated by this object, with the first row containing the element at index `index`. The result set has up to `count` rows in ascending order based on the indices. Each row has two columns: The second column stores the element value; the first column stores the index into the array for that element.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the array index of the first element to retrieve; the first element is at index 1 |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of successive SQL array elements to retrieve |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [ResultSet](ResultSet.md)! | a `ResultSet` object containing up to `count` consecutive elements of the SQL array designated by this `Array` object, starting at index `index`. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getResultSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResultSet(
    index: Long, 
    count: Int, 
    map: MutableMap<String!, Class<*>!>!
): ResultSet!
```

Retrieves a result set holding the elements of the subarray that starts at index `index` and contains up to `count` successive elements. This method uses the specified `map` for type map customizations unless the base type of the array does not match a user-defined type in `map`, in which case it uses the standard mapping. This version of the method `getResultSet` uses either the given type map or the standard mapping; it never uses the type map associated with the connection.

The result set has one row for each element of the SQL array designated by this object, with the first row containing the element at index `index`. The result set has up to `count` rows in ascending order based on the indices. Each row has two columns: The second column stores the element value; the first column stroes the index into the array for that element.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the array index of the first element to retrieve; the first element is at index 1 |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of successive SQL array elements to retrieve |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!: the `Map` object that contains the mapping of SQL type names to classes in the Java(tm) programming language |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [ResultSet](ResultSet.md)! | a `ResultSet` object containing up to `count` consecutive elements of the SQL array designated by this `Array` object, starting at index `index`. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------|
| `java.sql.SQLException` | if an error occurs while attempting to access the array |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
