# Attributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Attributes

```
open class Attributes : Cloneable, MutableMap<Any!, Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.jar.Attributes](../java/util/jar/Attributes.md) |

The Attributes class maps Manifest attribute names to associated string values. Valid attribute names are case-insensitive, are restricted to the ASCII characters in the set \[0-9a-zA-Z_-\], and cannot exceed 70 characters in length. There must be a colon and a SPACE after the name; the combined length will not exceed 72 characters. Attribute values can contain any characters and will be UTF8-encoded when written to the output stream. See the [JAR File Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/jar/jar.html) for more information about valid attribute names and values.

This map and its views have a predictable iteration order, namely the order that keys were inserted into the map, as with [LinkedHashMap](../java/util/LinkedHashMap.md).

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------|
| open | [Name](../java/util/jar/Attributes.Name.md) The Attributes. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Attributes](../java/util/jar/Attributes.md))`()` Constructs a new, empty Attributes object with default size. |
| [Attributes](../java/util/jar/Attributes.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new, empty Attributes object with the specified initial size. |
| [Attributes](../java/util/jar/Attributes.md))`(`attr:` ` [Attributes](../java/util/jar/Attributes.md)!`)` Constructs a new Attributes object with the same attribute name-value mappings as in the specified Attributes. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/jar/Attributes.md))`()` Removes all attributes from this Map. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/jar/Attributes.md))`()` Returns a copy of the Attributes, implemented as follows: ```kotlin public Object clone() { return new Attributes(this); } ``` Since the attribute names and values are themselves immutable, the Attributes returned can be safely modified without affecting the original. <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](../java/util/jar/Attributes.md))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this Map contains the specified attribute name (key). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](../java/util/jar/Attributes.md))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this Map maps one or more attribute names (keys) to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/jar/Attributes.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object to the underlying [map](../java/util/jar/Attributes.md) for equality. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [get](../java/util/jar/Attributes.md))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value of the specified attribute name, or null if the attribute name was not found. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../java/util/jar/Attributes.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of the specified attribute name, specified as a string, or null if the attribute was not found. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../java/util/jar/Attributes.md))`(`name:` ` [Attributes.Name](../java/util/jar/Attributes.Name.md)!`)` Returns the value of the specified Attributes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/jar/Attributes.md))`()` Returns the hash code value for this Map. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/jar/Attributes.md))`()` Returns true if this Map contains no attributes. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [put](../java/util/jar/Attributes.md))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Associates the specified value with the specified attribute name (key) in this Map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](../java/util/jar/Attributes.md))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<*,` `*>`)` Copies all of the attribute name-value mappings from the specified Attributes to this Map. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [putValue](../java/util/jar/Attributes.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Associates the specified value with the specified attribute name, specified as a String. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [remove](../java/util/jar/Attributes.md))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Removes the attribute with the specified name (key) from this Map. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>\> | [entries](../java/util/jar/Attributes.md) Returns a Collection view of the attribute name-value mappings contained in this Map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [keys](../java/util/jar/Attributes.md) Returns a Set view of the attribute names (keys) contained in this Map. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [map](../java/util/jar/Attributes.md) The attribute name-value mappings. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/jar/Attributes.md) Returns the number of attributes in this Map. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [values](../java/util/jar/Attributes.md) Returns a Collection view of the attribute values contained in this Map. |

## Public constructors

### Attributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Attributes()
```

Constructs a new, empty Attributes object with default size. 

### Attributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Attributes(size: Int)
```

Constructs a new, empty Attributes object with the specified initial size.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial number of attributes |

### Attributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Attributes(attr: Attributes!)
```

Constructs a new Attributes object with the same attribute name-value mappings as in the specified Attributes.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `attr` | [Attributes](../java/util/jar/Attributes.md)!:the specified Attributes |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all attributes from this Map.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a copy of the Attributes, implemented as follows: 

```kotlin
public Object clone() { return new Attributes(this); }
  
```
Since the attribute names and values are themselves immutable, the Attributes returned can be safely modified without affecting the original.

<br />

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: Any!): Boolean
```

Returns true if this Map contains the specified attribute name (key).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:key whose presence in this map is to be tested |
| `name` | the attribute name |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Map contains the specified attribute name |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: Any!): Boolean
```

Returns true if this Map maps one or more attribute names (keys) to the specified value.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the attribute value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Map maps one or more attribute names to the specified value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object to the underlying [map](../java/util/jar/Attributes.md) for equality. Returns true if the given object is also a Map and the two maps represent the same mappings.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the Object to be compared |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified Object is equal to this Map |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: Any!): Any?
```

Returns the value of the specified attribute name, or null if the attribute name was not found.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the key whose associated value is to be returned |
| `name` | the attribute name |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the value of the specified attribute name, or null if not found. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(name: String!): String!
```

Returns the value of the specified attribute name, specified as a string, or null if the attribute was not found. The attribute name is case-insensitive.

This method is defined as: 

```kotlin
return (String)get(new Attributes.Name((String)name));
  
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute name as a string |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the String value of the specified attribute name, or null if not found. |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if the attribute name is invalid |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(name: Attributes.Name!): String!
```

Returns the value of the specified Attributes.Name, or null if the attribute was not found.

This method is defined as: 

```kotlin
return (String)get(name);
  
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [Attributes.Name](../java/util/jar/Attributes.Name.md)!:the Attributes.Name object |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the String value of the specified Attribute.Name, or null if not found. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this Map.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this map |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns true if this Map contains no attributes.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map contains no key-value mappings |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: Any!, 
    value: Any!
): Any?
```

Associates the specified value with the specified attribute name (key) in this Map. If the Map previously contained a mapping for the attribute name, the old value is replaced.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:key with which the specified value is to be associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the attribute value |
| `name` | the attribute name |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the previous value of the attribute, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the name is not a Attributes.Name or the value is not a String |
| `java.lang.NullPointerException` | if the specified key or value is null and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<*, *>): Unit
```

Copies all of the attribute name-value mappings from the specified Attributes to this Map. Duplicate mappings will be replaced.

| Parameters ||
|--------|-----------------------------------------|
| `m` | mappings to be stored in this map |
| `attr` | the Attributes to be stored in this map |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if attr is not an Attributes |
| `java.lang.NullPointerException` | if the specified map is null, or if this map does not permit null keys or values, and the specified map contains null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### putValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putValue(
    name: String!, 
    value: String!
): String!
```

Associates the specified value with the specified attribute name, specified as a String. The attributes name is case-insensitive. If the Map previously contained a mapping for the attribute name, the old value is replaced.

This method is defined as: 

```kotlin
return (String)put(new Attributes.Name(name), value);
  
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute name as a string |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute value |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the previous value of the attribute, or null if none |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if the attribute name is invalid |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: Any!): Any?
```

Removes the attribute with the specified name (key) from this Map. Returns the previous attribute value, or null if none.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:key whose mapping is to be removed from the map |
| `name` | attribute name |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the previous value of the attribute, or null if none |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| --- | --- |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val entries: MutableSet<MutableEntry<Any!, Any!>>
```

Returns a Collection view of the attribute name-value mappings contained in this Map.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>> | a set view of the mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<Any!>
```

Returns a Set view of the attribute names (keys) contained in this Map.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | a set view of the keys contained in this map |

### map

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var map: MutableMap<Any!, Any!>!
```

The attribute name-value mappings. 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of attributes in this Map.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val values: MutableCollection<Any!>
```

Returns a Collection view of the attribute values contained in this Map.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | a collection view of the values contained in this map |
