# Dictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dictionary

```
abstract class Dictionary<K : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Dictionary](https://developer.android.com/reference/kotlin/java/util/Dictionary#) |

| Known Direct Subclasses [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable) |---------------------------------------------------------------------------------|----------------------------------------------------------------| | [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable) | This class implements a hash table, which maps keys to values. | |

| Known Indirect Subclasses [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider.html#), [Properties](https://developer.android.com/reference/kotlin/java/util/Properties), [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider.html#) | Legacy security code; do not use. | | [Properties](https://developer.android.com/reference/kotlin/java/util/Properties) | The`Properties`class represents a persistent set of properties. | | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) | This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. | |

The`Dictionary`class is the abstract parent of any class, such as`Hashtable`, which maps keys to values. Every key and every value is an object. In any one`Dictionary`object, every key is associated with at most one value. Given a`Dictionary`and a key, the associated element can be looked up. Any non-`null`object can be used as a key and as a value.

As a rule, the`equals`method should be used by implementations of this class to decide if two keys are the same.

**NOTE: This class is obsolete. New implementations should implement the Map interface, rather than extending this class.**

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------|---|
| [Dictionary](https://developer.android.com/reference/kotlin/java/util/Dictionary#Dictionary())`()` Sole constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<V\>! | [elements](https://developer.android.com/reference/kotlin/java/util/Dictionary#elements())`()` Returns an enumeration of the values in this dictionary. |
| abstractV | [get](https://developer.android.com/reference/kotlin/java/util/Dictionary#get(kotlin.Any))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value to which the key is mapped in this dictionary. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/Dictionary#isEmpty())`()` Tests if this dictionary maps no keys to value. |
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<K\>! | [keys](https://developer.android.com/reference/kotlin/java/util/Dictionary#keys())`()` Returns an enumeration of the keys in this dictionary. |
| abstractV | [put](https://developer.android.com/reference/kotlin/java/util/Dictionary#put(java.util.Dictionary.K,%20java.util.Dictionary.V))`(`key:` `K`, `value:` `V`)` Maps the specified`key`to the specified`value`in this dictionary. |
| abstractV | [remove](https://developer.android.com/reference/kotlin/java/util/Dictionary#remove(kotlin.Any))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Removes the`key`(and its corresponding`value`) from this dictionary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/Dictionary#size())`()` Returns the number of entries (distinct keys) in this dictionary. |

## Public constructors

### Dictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Dictionary()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun elements(): Enumeration<V>!
```

Returns an enumeration of the values in this dictionary. The general contract for the`elements`method is that an`Enumeration`is returned that will generate all the elements contained in entries in this dictionary.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<V>! | an enumeration of the values in this dictionary. |

**See Also**

- [java.util.Dictionary#keys()](https://developer.android.com/reference/kotlin/java/util/Dictionary#keys())
- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration) 

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(key: Any!): V
```

Returns the value to which the key is mapped in this dictionary. The general contract for the`isEmpty`method is that if this dictionary contains an entry for the specified key, the associated value is returned; otherwise,`null`is returned.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a key in this dictionary.`null`if the key is not mapped to any value in this dictionary. |

| Return ||
|---|----------------------------------------------------------|
| V | the value to which the key is mapped in this dictionary; |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if the`key`is`null`. |

**See Also**

- [java.util.Dictionary#put(java.lang.Object, java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/Dictionary#put(java.util.Dictionary.K,%20java.util.Dictionary.V)) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
```

Tests if this dictionary maps no keys to value. The general contract for the`isEmpty`method is that the result is true if and only if this dictionary contains no entries.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this dictionary maps no keys to values;`false`otherwise. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keys(): Enumeration<K>!
```

Returns an enumeration of the keys in this dictionary. The general contract for the keys method is that an`Enumeration`object is returned that will generate all the keys for which this dictionary contains entries.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<K>! | an enumeration of the keys in this dictionary. |

**See Also**

- [java.util.Dictionary#elements()](https://developer.android.com/reference/kotlin/java/util/Dictionary#elements())
- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration) 

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    key: K, 
    value: V
): V
```

Maps the specified`key`to the specified`value`in this dictionary. Neither the key nor the value can be`null`.

If this dictionary already contains an entry for the specified`key`, the value already in this dictionary for that`key`is returned, after modifying the entry to contain the new element.

If this dictionary does not already have an entry for the specified`key`, an entry is created for the specified`key`and`value`, and`null`is returned.

The`value`can be retrieved by calling the`get`method with a`key`that is equal to the original`key`.

| Parameters ||
|---------|----------------------|
| `key` | K:the hashtable key. |
| `value` | V:the value. |

| Return ||
|---|------------------------------------------------------------------------------------------------------------------------|
| V | the previous value to which the`key`was mapped in this dictionary, or`null`if the key did not have a previous mapping. |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if the`key`or`value`is`null`. |

**See Also**

- [java.lang.Object#equals(java.lang.Object)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))
- [java.util.Dictionary#get(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/Dictionary#get(kotlin.Any)) 

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(key: Any!): V
```

Removes the`key`(and its corresponding`value`) from this dictionary. This method does nothing if the`key`is not in this dictionary.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the key that needs to be removed. |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------|
| V | the value to which the`key`had been mapped in this dictionary, or`null`if the key did not have a mapping. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`key`is`null`. |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Int
```

Returns the number of entries (distinct keys) in this dictionary.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of keys in this dictionary. |
