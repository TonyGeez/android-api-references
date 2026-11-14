Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpParams

```
interface HttpParams
```

| [org.apache.http.params.HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#) |

> [!CAUTION]
> **This interface was deprecated in API level 22.**
>
> Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Represents a collection of HTTP protocol and framework parameters.

## Summary

| Public methods ||
|---|---|
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#copy()()` Creates a copy of these parameters. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#getBooleanParameter(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` parameter value with the given name. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#getDoubleParameter(kotlin.String,%20kotlin.Double)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns a `https://developer.android.com/reference/kotlin/java/lang/Double.html#` parameter value with the given name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#getIntParameter(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` parameter value with the given name. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#getLongParameter(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a `https://developer.android.com/reference/kotlin/java/lang/Long.html#` parameter value with the given name. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#getParameter(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Obtains the value of the given parameter. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#isParameterFalse(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Checks if a boolean parameter is not set or `false`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#isParameterTrue(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Checks if a boolean parameter is set to `true`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#removeParameter(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes the parameter with the specified name. |
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setBooleanParameter(kotlin.String,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Assigns a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` to the parameter with the given name |
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setDoubleParameter(kotlin.String,%20kotlin.Double)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Assigns a `https://developer.android.com/reference/kotlin/java/lang/Double.html#` to the parameter with the given name |
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setIntParameter(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Assigns an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` to the parameter with the given name |
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setLongParameter(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Assigns a `https://developer.android.com/reference/kotlin/java/lang/Long.html#` to the parameter with the given name |
| abstract [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#)! | `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setParameter(kotlin.String,%20kotlin.Any)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Assigns the value to the parameter with the given name. |

## Public methods

### copy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun copy(): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Creates a copy of these parameters.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#!` | a new set of parameters holding the same values as this one |

### getBooleanParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBooleanParameter(
    name: String!, 
    defaultValue: Boolean
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` parameter value with the given name. If the parameter is not explicitly set, the default value is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent name. |
| `defaultValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` that represents the value of the parameter. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setBooleanParameter(kotlin.String,%20kotlin.Boolean)`

### getDoubleParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDoubleParameter(
    name: String!, 
    defaultValue: Double
): Double
```

**Deprecated:** *Deprecated in Java.*

Returns a `https://developer.android.com/reference/kotlin/java/lang/Double.html#` parameter value with the given name. If the parameter is not explicitly set, the default value is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent name. |
| `defaultValue` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | a `https://developer.android.com/reference/kotlin/java/lang/Double.html#` that represents the value of the parameter. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setDoubleParameter(kotlin.String,%20kotlin.Double)`

### getIntParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIntParameter(
    name: String!, 
    defaultValue: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Returns an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` parameter value with the given name. If the parameter is not explicitly set, the default value is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent name. |
| `defaultValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` that represents the value of the parameter. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setIntParameter(kotlin.String,%20kotlin.Int)`

### getLongParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLongParameter(
    name: String!, 
    defaultValue: Long
): Long
```

**Deprecated:** *Deprecated in Java.*

Returns a `https://developer.android.com/reference/kotlin/java/lang/Long.html#` parameter value with the given name. If the parameter is not explicitly set, the default value is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent name. |
| `defaultValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a `https://developer.android.com/reference/kotlin/java/lang/Long.html#` that represents the value of the parameter. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setLongParameter(kotlin.String,%20kotlin.Long)`

### getParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getParameter(name: String!): Any!
```

**Deprecated:** *Deprecated in Java.*

Obtains the value of the given parameter.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the parent name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | an object that represents the value of the parameter, `null` if the parameter is not set or if it is explicitly set to `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams#setParameter(kotlin.String,%20kotlin.Any)`

### isParameterFalse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isParameterFalse(name: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if a boolean parameter is not set or `false`.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the parameter is either not set or set to value false, false if it is set to `true` |

### isParameterTrue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isParameterTrue(name: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if a boolean parameter is set to `true`.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the parameter is set to value true, false if it is not set or set to `false` |

### removeParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeParameter(name: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes the parameter with the specified name.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the parameter existed and has been removed, false else. |

### setBooleanParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setBooleanParameter(
    name: String!, 
    value: Boolean
): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Assigns a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` to the parameter with the given name

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): parameter value |

### setDoubleParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDoubleParameter(
    name: String!, 
    value: Double
): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Assigns a `https://developer.android.com/reference/kotlin/java/lang/Double.html#` to the parameter with the given name

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): parameter value |

### setIntParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setIntParameter(
    name: String!, 
    value: Int
): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Assigns an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` to the parameter with the given name

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): parameter value |

### setLongParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setLongParameter(
    name: String!, 
    value: Long
): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Assigns a `https://developer.android.com/reference/kotlin/java/lang/Long.html#` to the parameter with the given name

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): parameter value |

### setParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setParameter(
    name: String!, 
    value: Any!
): HttpParams!
```

**Deprecated:** *Deprecated in Java.*

Assigns the value to the parameter with the given name.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: parameter name |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: parameter value |
