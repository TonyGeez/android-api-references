Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Properties

```
open class Properties : Hashtable<Any!, Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.Dictionary](Dictionary.md)\<K, V\> |||
| | ↳ | [java.util.Hashtable](Hashtable.md)\< [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)\> ||
| | | ↳ | [java.util.Properties](Properties.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [Provider](../java.security/Provider.md) [Provider](../java.security/Provider.md) This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security.
Known Indirect Subclasses [AuthProvider](../java.security/AuthProvider.md) [AuthProvider](../java.security/AuthProvider.md) Legacy security code; do not use.

The `Properties` class represents a persistent set of properties. The `Properties` can be saved to a stream or loaded from a stream. Each key and its corresponding value in the property list is a string.

A property list can contain another property list as its "defaults"; this second property list is searched if the property key is not found in the original property list.

Because `Properties` inherits from `Hashtable`, the `put` and `putAll` methods can be applied to a `Properties` object. Their use is strongly discouraged as they allow the caller to insert entries whose keys or values are not `Strings`. The `setProperty` method should be used instead. If the `store` or `save` method is called on a "compromised" `Properties` object that contains a non-`String` key or value, the call will fail. Similarly, the call to the `propertyNames` or `list` method will fail if it is called on a "compromised" `Properties` object that contains a non-`String` key.

The iterators returned by the `iterator` method of this class's "collection views" (that is, `entrySet()`, `keySet()`, and `values()`) may not fail-fast (unlike the Hashtable implementation). These iterators are guaranteed to traverse elements as they existed upon construction exactly once, and may (but are not guaranteed to) reflect any modifications subsequent to construction.

The load `/` store methods load and store properties from and to a character based stream in a simple line-oriented format specified below. The load `/` store methods work the same way as the load(Reader)/store(Writer, String) pair, except the input/output stream is encoded in ISO 8859-1 character encoding. Characters that cannot be directly represented in this encoding can be written using Unicode escapes as defined in section {@jls 3.3} of The Java Language Specification; only a single 'u' character is allowed in an escape sequence.

The loadFromXML and storeToXML methods load and store properties in a simple XML format. By default the UTF-8 character encoding is used, however a specific encoding may be specified if required. Implementations are required to support UTF-8 and UTF-16 and may support other encodings. An XML properties document has the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```
Note that the system URI (http://java.sun.com/dtd/properties.dtd) is *not* accessed when exporting or importing properties; it merely serves as a string to uniquely identify the DTD, which is:

```kotlin
<?xml version="1.0" encoding="UTF-8"?>
 
     <!-- DTD for properties -->
 
     <!ELEMENT properties ( comment?, entry* ) >
 
     <!ATTLIST properties version CDATA #FIXED "1.0">
 
     <!ELEMENT comment (#PCDATA) >
 
     <!ELEMENT entry (#PCDATA) >
 
     <!ATTLIST entry key CDATA #REQUIRED>
  
```

This class is thread-safe: multiple threads can share a single `Properties` object without the need for external synchronization.

## Summary

| Public constructors ||
|---|---|
| Properties Creates an empty property list with no default values. |
| Properties Creates an empty property list with no default values, and with an initial size accommodating the specified number of elements without the need to dynamically resize. |
| Properties Creates an empty property list with the specified defaults. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Clears this hashtable so that it contains no keys. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Creates a shallow copy of this hashtable. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | compute Attempts to compute a mapping for the specified key and its current mapped value, or `null` if there is no current mapping (optional operation). |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | computeIfAbsent If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null` (optional operation). |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | computeIfPresent If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Tests if some key maps into the specified value in this hashtable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsKey Tests if the specified object is a key in this hashtable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsValue Returns true if this hashtable maps one or more keys to this value. |
| open [Enumeration](Enumeration.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | elements Returns an enumeration of the values in this hashtable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares the specified Object with this Map for equality, as per the definition in the Map interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | forEach Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | get Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | getOrDefault Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getProperty Searches for the property with the specified key in this property list. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getProperty Searches for the property with the specified key in this property list. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns the hash code value for this Map as per the definition in the Map interface. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Tests if this hashtable maps no keys to values. |
| open [Enumeration](Enumeration.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | keys Returns an enumeration of the keys in this hashtable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | list Prints this property list out to the specified output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | list Prints this property list out to the specified output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | load Reads a property list (key and element pairs) from the input byte stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | load Reads a property list (key and element pairs) from the input character stream in a simple line-oriented format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | loadFromXML Loads all of the properties represented by the XML document on the specified input stream into this properties table. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | merge If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value (optional operation). |
| --- | --- |
| open [Enumeration](Enumeration.md)\<\*\>! | propertyNames Returns an enumeration of all the keys in this property list, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | put Maps the specified `key` to the specified `value` in this hashtable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putAll Copies all of the mappings from the specified map to this hashtable. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | putIfAbsent If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value (optional operation). |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | remove Removes the key (and its corresponding value) from this hashtable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | remove Removes the entry for the specified key only if it is currently mapped to the specified value (optional operation). |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | replace Replaces the entry for the specified key only if it is currently mapped to some value (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | replace Replaces the entry for the specified key only if currently mapped to the specified value (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | replaceAll Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | save Calls the `store(OutputStream out, String comments)` method and suppresses IOExceptions that were thrown. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | setProperty Calls the `Hashtable` method `put`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | store Writes this property list (key and element pairs) in this `Properties` table to the output stream in a format suitable for loading into a `Properties` table using the load method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | store Writes this property list (key and element pairs) in this `Properties` table to the output character stream in a format suitable for using the load method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | storeToXML Emits an XML document representing all of the properties contained in this table. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | storeToXML Emits an XML document representing all of the properties contained in this table, using the specified encoding. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | storeToXML Emits an XML document representing all of the properties contained in this table, using the specified encoding. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | stringPropertyNames Returns an unmodifiable set of keys from this property list where the key and its corresponding value are strings, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of this `Hashtable` object in the form of a set of entries, enclosed in braces and separated by the ASCII characters "` , `" (comma and space). |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | rehash Increases the capacity of and internally reorganizes this hashtable, in order to accommodate and access its entries more efficiently. |

| Properties ||
|---|---|
| [Properties](Properties.md)! | `https://developer.android.com/reference/kotlin/java/util/Properties#defaults:java.util.Properties` A property list that contains default values for any keys not found in this property list. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>\> | `https://developer.android.com/reference/kotlin/java/util/Properties#entries:kotlin.collections.MutableSet` Returns a Set view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Properties#keys:kotlin.collections.MutableSet` Returns a Set view of the keys contained in this map. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Properties#size:kotlin.Int` Returns the number of keys in this hashtable. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Properties#values:kotlin.collections.MutableCollection` Returns a Collection view of the values contained in this map. |

## Public constructors

### Properties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Properties()
```

Creates an empty property list with no default values.

### Properties

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Properties(initialCapacity: Int)
```

Creates an empty property list with no default values, and with an initial size accommodating the specified number of elements without the need to dynamically resize.

| Parameters ||
|---|---|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `Properties` will be sized to accommodate this many elements |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero. |

### Properties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Properties(defaults: Properties!)
```

Creates an empty property list with the specified defaults.

| Parameters ||
|---|---|
| `defaults` | [Properties](Properties.md)!: the defaults. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Clears this hashtable so that it contains no keys.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Creates a shallow copy of this hashtable. All the structure of the hashtable itself is copied, but the keys and values are not cloned. This is a relatively expensive operation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of the hashtable |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Any!, 
    remappingFunction: BiFunction<in Any!, in Any?, *>
): Any?
```

Attempts to compute a mapping for the specified key and its current mapped value, or `null` if there is no current mapping (optional operation). For example, to either create or append a `String` msg to a value mapping:

```kotlin
<code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code>
```
(Method merge is often simpler to use for such purposes.)

<br />

If the remapping function returns `null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a ConcurrentModificationException if the remapping function modified this map during computation.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, \*\>: the remapping function to compute a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `compute` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfAbsent(
    key: Any!, 
    mappingFunction: Function<in Any!, *>
): Any!
```

If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null` (optional operation).

If the mapping function returns `null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in:

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new Value(f(k)));
  </code>
```

Or to implement a multi-value map, `Map<K,Collection<V>>`, supporting multiple values per key:

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v);
  </code>
```

The mapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a ConcurrentModificationException if the mapping function modified this map during computation.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `mappingFunction` | [Function](../java.util.function/Function.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, \*\>: the mapping function to compute a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the mappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfAbsent` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the mapping function modified this map |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfPresent(
    key: Any!, 
    remappingFunction: BiFunction<in Any!, in Any, *>
): Any?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value (optional operation).

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a ConcurrentModificationException if the remapping function modified this map during computation.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), \*\>: the remapping function to compute a value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfPresent` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(value: Any!): Boolean
```

Tests if some key maps into the specified value in this hashtable. This operation is more expensive than the containsKey method.

Note that this method is identical in functionality to containsValue, (which is part of the Map interface in the collections framework).

| Parameters ||
|---|---|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: a value to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if some key maps to the `value` argument in this hashtable as determined by the `equals` method; `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the value is `null` |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: Any!): Boolean
```

Tests if the specified object is a key in this hashtable.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: possible key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the specified object is a key in this hashtable, as determined by the `equals` method; `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the key is `null` |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: Any!): Boolean
```

Returns true if this hashtable maps one or more keys to this value.

Note that this method is identical in functionality to contains (which predates the Map interface).

| Parameters ||
|---|---|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value whose presence in this hashtable is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map maps one or more keys to the specified value |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the value is `null` |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun elements(): Enumeration<Any!>!
```

Returns an enumeration of the values in this hashtable. Use the Enumeration methods on the returned object to fetch the elements sequentially. If the hashtable is structurally modified while enumerating over the values then the results of enumerating are undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | an enumeration of the values in this hashtable. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the specified Object with this Map for equality, as per the definition in the Map interface.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this hashtable |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the specified Object is equal to this Map |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: BiConsumer<in Any!, in Any!>): Unit
```

Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: The action to be performed for each entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: Any!): Any?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `(key.equals(k))`, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the key whose associated value is to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified key is null |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrDefault(
    key: Any!, 
    defaultValue: Any!
): Any!
```

Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the key whose associated value is to be returned |
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the default mapping of the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(key: String!): String!
```

Searches for the property with the specified key in this property list. If the key is not found in this property list, the default property list, and its defaults, recursively, are then checked. The method returns `null` if the property is not found.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the property key. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the value in this property list with the specified key value. |

**See Also**

- setProperty
- `https://developer.android.com/reference/kotlin/java/util/Properties#defaults:java.util.Properties`

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(
    key: String!, 
    defaultValue: String!
): String!
```

Searches for the property with the specified key in this property list. If the key is not found in this property list, the default property list, and its defaults, recursively, are then checked. The method returns the default value argument if the property is not found.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the hashtable key. |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the value in this property list with the specified key value. |

**See Also**

- setProperty
- `https://developer.android.com/reference/kotlin/java/util/Properties#defaults:java.util.Properties`

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the hash code value for this Map as per the definition in the Map interface.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this map |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Tests if this hashtable maps no keys to values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this hashtable maps no keys to values; `false` otherwise. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keys(): Enumeration<Any!>!
```

Returns an enumeration of the keys in this hashtable. Use the Enumeration methods on the returned object to fetch the keys sequentially. If the hashtable is structurally modified while enumerating over the keys then the results of enumerating are undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | an enumeration of the keys in this hashtable. |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun list(out: PrintStream!): Unit
```

Prints this property list out to the specified output stream. This method is useful for debugging.

| Parameters ||
|---|---|
| `out` | [PrintStream](../java.io/PrintStream.md)!: an output stream. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any key in this property list is not a string. |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun list(out: PrintWriter!): Unit
```

Prints this property list out to the specified output stream. This method is useful for debugging.

| Parameters ||
|---|---|
| `out` | [PrintWriter](../java.io/PrintWriter.md)!: an output stream. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any key in this property list is not a string. |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun load(inStream: InputStream!): Unit
```

Reads a property list (key and element pairs) from the input byte stream. The input stream is in a simple line-oriented format as specified in load and is assumed to use the ISO 8859-1 character encoding; that is each byte is one Latin1 character. Characters not in Latin1, and certain special characters, are represented in keys and elements using Unicode escapes as defined in section {@jls 3.3} of The Java Language Specification.

The specified stream remains open after this method returns.

| Parameters ||
|---|---|
| `inStream` | [InputStream](../java.io/InputStream.md)!: the input stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred when reading from the input stream. |
| `java.lang.IllegalArgumentException` | if the input stream contains a malformed Unicode escape sequence. |
| `java.lang.NullPointerException` | if `inStream` is null. |
| --- | --- |

### load

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun load(reader: Reader!): Unit
```

Reads a property list (key and element pairs) from the input character stream in a simple line-oriented format.

Properties are processed in terms of lines. There are two kinds of line, *natural lines* and *logical lines* . A natural line is defined as a line of characters that is terminated either by a set of line terminator characters (`\n` or `\r` or `\r\n`) or by the end of the stream. A natural line may be either a blank line, a comment line, or hold all or some of a key-element pair. A logical line holds all the data of a key-element pair, which may be spread out across several adjacent natural lines by escaping the line terminator sequence with a backslash character `\`. Note that a comment line cannot be extended in this manner; every natural line that is a comment must have its own comment indicator, as described below. Lines are read from input until the end of the stream is reached.

A natural line that contains only white space characters is considered blank and is ignored. A comment line has an ASCII `'#'` or `'!'` as its first non-white space character; comment lines are also ignored and do not encode key-element information. In addition to line terminators, this format considers the characters space (`' '`, `'\u005Cu0020'`), tab (`'\t'`, `'\u005Cu0009'`), and form feed (`'\f'`, `'\u005Cu000C'`) to be white space.

If a logical line is spread across several natural lines, the backslash escaping the line terminator sequence, the line terminator sequence, and any white space at the start of the following line have no affect on the key or element values. The remainder of the discussion of key and element parsing (when loading) will assume all the characters constituting the key and element appear on a single natural line after line continuation characters have been removed. Note that it is *not* sufficient to only examine the character preceding a line terminator sequence to decide if the line terminator is escaped; there must be an odd number of contiguous backslashes for the line terminator to be escaped. Since the input is processed from left to right, a non-zero even number of 2*n* contiguous backslashes before a line terminator (or elsewhere) encodes *n* backslashes after escape processing.

The key contains all of the characters in the line starting with the first non-white space character and up to, but not including, the first unescaped `'='`, `':'`, or white space character other than a line terminator. All of these key termination characters may be included in the key by escaping them with a preceding backslash character; for example,

`\:\=`

would be the two-character key `":="`. Line terminator characters can be included using `\r` and `\n` escape sequences. Any white space after the key is skipped; if the first non-white space character after the key is `'='` or `':'`, then it is ignored and any white space characters after it are also skipped. All remaining characters on the line become part of the associated element string; if there are no remaining characters, the element is the empty string `""`. Once the raw character sequences constituting the key and element are identified, escape processing is performed as described above.

As an example, each of the following three lines specifies the key `"Truth"` and the associated element value `"Beauty"`:

```kotlin
Truth = Beauty
   Truth:Beauty
  Truth                    :Beauty
  
```
As another example, the following three lines specify a single property:

```kotlin
fruits                           apple, banana, pear, \
                                   cantaloupe, watermelon, \
                                   kiwi, mango
  
```
The key is `"fruits"` and the associated element is:

```kotlin
"apple, banana, pear, cantaloupe, watermelon, kiwi, mango"
```
Note that a space appears before each `\` so that a space will appear after each comma in the final result; the `\`, line terminator, and leading white space on the continuation line are merely discarded and are *not* replaced by one or more other characters.

As a third example, the line:

```kotlin
cheeses
  
```
specifies that the key is `"cheeses"` and the associated element is the empty string `""`.

Characters in keys and elements can be represented in escape sequences similar to those used for character and string literals (see sections {@jls 3.3} and {@jls 3.10.6} of The Java Language Specification). The differences from the character escape sequences and Unicode escapes used for characters and strings are:

- Octal escapes are not recognized.
- The character sequence `\b` does *not* represent a backspace character.
- The method does not treat a backslash character, `\`, before a non-valid escape character as an error; the backslash is silently dropped. For example, in a Java string the sequence `"\z"` would cause a compile time error. In contrast, this method silently drops the backslash. Therefore, this method treats the two character sequence `"\b"` as equivalent to the single character `'b'`.
- Escapes are not necessary for single and double quotes; however, by the rule above, single and double quote characters preceded by a backslash still yield single and double quote characters, respectively.
- Only a single 'u' character is allowed in a Unicode escape sequence.

The specified stream remains open after this method returns.

| Parameters ||
|---|---|
| `reader` | [Reader](../java.io/Reader.md)!: the input character stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred when reading from the input stream. |
| `java.lang.IllegalArgumentException` | if a malformed Unicode escape appears in the input. |
| `java.lang.NullPointerException` | if `reader` is null. |
| --- | --- |

### loadFromXML

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadFromXML(in: InputStream!): Unit
```

Loads all of the properties represented by the XML document on the specified input stream into this properties table.

The XML document must have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```
Furthermore, the document must satisfy the properties DTD described above.

An implementation is required to read XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

The specified stream is closed after this method returns.

| Parameters ||
|---|---|
| `in` | [InputStream](../java.io/InputStream.md)!: the input stream from which to read the XML document. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if reading from the specified input stream results in an `IOException`. |
| `java.io.UnsupportedEncodingException` | if the document's encoding declaration can be read and it specifies an encoding that is not supported |
| `java.lang.NullPointerException` | if `in` is null. |
| --- | --- |
| `java.util.InvalidPropertiesFormatException` | Data on input stream does not constitute a valid XML document with the mandated document type. |

**See Also**

- storeToXML

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun merge(
    key: Any!, 
    value: Any, 
    remappingFunction: BiFunction<in Any, in Any, *>
): Any?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value (optional operation). Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is `null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a `String msg` to a value mapping:

```kotlin
<code>map.merge(key, msg, String::concat)
  </code>
```

<br />

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a ConcurrentModificationException if the remapping function modified this map during computation.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the resulting value is to be associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), \*\>: the remapping function to recompute a value if present |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the new value associated with the specified key, or null if no value is associated with the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys or the value or remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `merge` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### propertyNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun propertyNames(): Enumeration<*>!
```

Returns an enumeration of all the keys in this property list, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration<*>!` | an enumeration of all the keys in this property list, including the keys in the default property list. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any key in this property list is not a string. |

**See Also**

- Enumeration
- `https://developer.android.com/reference/kotlin/java/util/Properties#defaults:java.util.Properties`
- stringPropertyNames

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Any!, 
    value: Any!
): Any?
```

Maps the specified `key` to the specified `value` in this hashtable. Neither the key nor the value can be `null`.

The value can be retrieved by calling the `get` method with a key that is equal to the original key.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the hashtable key |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the previous value of the specified key in this hashtable, or `null` if it did not have one |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the key or value is `null` |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putAll(from: Map<*, *>): Unit
```

Copies all of the mappings from the specified map to this hashtable. These mappings will replace any mappings that this hashtable had for any of the keys currently in the specified map.

| Parameters ||
|---|---|
| `m` | mappings to be stored in this map |
| `t` | mappings to be stored in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putAll` operation is not supported by this map |

### putIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putIfAbsent(
    key: Any!, 
    value: Any!
): Any?
```

If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value (optional operation).

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value to be associated with the specified key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the previous value associated with the specified key, or `null` if there was no mapping for the key. (A `null` return can also indicate that the map previously associated `null` with the key, if the implementation supports null values.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putIfAbsent` operation is not supported by this map (java.util.Collection#) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: Any!): Any?
```

Removes the key (and its corresponding value) from this hashtable. This method does nothing if the key is not in the hashtable.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the key that needs to be removed |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the value to which the key had been mapped in this hashtable, or `null` if the key did not have a mapping |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the key is `null` |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(
    key: Any!, 
    value: Any!
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value (optional operation).

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value expected to be associated with the specified key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value was removed |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map (java.util.Collection#) |
| --- | --- |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: Any!, 
    value: Any!
): Any?
```

Replaces the entry for the specified key only if it is currently mapped to some value (optional operation).

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value to be associated with the specified key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the previous value associated with the specified key, or `null` if there was no mapping for the key. (A `null` return can also indicate that the map previously associated `null` with the key, if the implementation supports null values.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replace` operation is not supported by this map (java.util.Collection#) |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: Any!, 
    oldValue: Any!, 
    newValue: Any!
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value (optional operation).

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is associated |
| `oldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value expected to be associated with the specified key |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: value to be associated with the specified key |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value was replaced |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if oldValue is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replace` operation is not supported by this map (java.util.Collection#) |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(function: BiFunction<in Any!, in Any!, *>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). Exceptions thrown by the function are relayed to the caller.

| Parameters ||
|---|---|
| `function` | [BiFunction](../java.util.function/BiFunction.md)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, \*\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### save

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun save(
    out: OutputStream!, 
    comments: String!
): Unit
```

**Deprecated:** *This method does not throw an IOException if an I/O error occurs while saving the property list. The preferred way to save a properties list is via the `store(OutputStream out, String comments)` method or the `storeToXML(OutputStream os, String comment)` method.*

Calls the `store(OutputStream out, String comments)` method and suppresses IOExceptions that were thrown.

| Parameters ||
|---|---|
| `out` | [OutputStream](../java.io/OutputStream.md)!: an output stream. |
| `comments` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProperty(
    key: String!, 
    value: String!
): Any!
```

Calls the `Hashtable` method `put`. Provided for parallelism with the `getProperty` method. Enforces use of strings for property keys and values. The value returned is the result of the `Hashtable` call to `put`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key to be placed into this property list. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value corresponding to `key`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the previous value of the specified key in this property list, or `null` if it did not have one. |

**See Also**

### store

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun store(
    out: OutputStream!, 
    comments: String!
): Unit
```

Writes this property list (key and element pairs) in this `Properties` table to the output stream in a format suitable for loading into a `Properties` table using the load method.

Properties from the defaults table of this `Properties` table (if any) are *not* written out by this method.

This method outputs the comments, properties keys and values in the same format as specified in store, with the following differences:

- The stream is written using the ISO 8859-1 character encoding.
- Characters not in Latin-1 in the comments are written as `\u005Cu`*xxxx* for their appropriate unicode hexadecimal value *xxxx*.
- Characters less than `\u005Cu0020` and characters greater than `\u005Cu007E` in property keys or values are written as `\u005Cu`*xxxx* for the appropriate hexadecimal value *xxxx*.

After the entries have been written, the output stream is flushed. The output stream remains open after this method returns.

| Parameters ||
|---|---|
| `out` | [OutputStream](../java.io/OutputStream.md)!: an output stream. |
| `comments` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing this property list to the specified output stream throws an `IOException`. |
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |
| `java.lang.NullPointerException` | if `out` is null. |
| --- | --- |

### store

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun store(
    writer: Writer!, 
    comments: String!
): Unit
```

Writes this property list (key and element pairs) in this `Properties` table to the output character stream in a format suitable for using the load method.

Properties from the defaults table of this `Properties` table (if any) are *not* written out by this method.

If the comments argument is not null, then an ASCII character, the comments string, and a line separator are first written to the output stream. Thus, the `comments` can serve as an identifying comment. Any one of a line feed ('\\n'), a carriage return ('\\r'), or a carriage return followed immediately by a line feed in comments is replaced by a line separator generated by the `Writer` and if the next character in comments is not character or character `!` then an ASCII is written out after that line separator.

Next, a comment line is always written, consisting of an ASCII character, the current date and time (as if produced by the `toString` method of `Date` for the current time), and a line separator as generated by the `Writer`.

Then every entry in this `Properties` table is written out, one per line. For each entry the key string is written, then an ASCII `=`, then the associated element string. For the key, all space characters are written with a preceding `\` character. For the element, leading space characters, but not embedded or trailing space characters, are written with a preceding `\` character. The key and element characters , `!`, `=`, and `:` are written with a preceding backslash to ensure that they are properly loaded.

After the entries have been written, the output stream is flushed. The output stream remains open after this method returns.

| Parameters ||
|---|---|
| `writer` | [Writer](../java.io/Writer.md)!: an output character stream writer. |
| `comments` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing this property list to the specified output stream throws an `IOException`. |
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |
| `java.lang.NullPointerException` | if `writer` is null. |
| --- | --- |

### storeToXML

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun storeToXML(
    os: OutputStream!, 
    comment: String!
): Unit
```

Emits an XML document representing all of the properties contained in this table.

An invocation of this method of the form `props.storeToXML(os, comment)` behaves in exactly the same way as the invocation `props.storeToXML(os, comment, "UTF-8");`.

| Parameters ||
|---|---|
| `os` | [OutputStream](../java.io/OutputStream.md)!: the output stream on which to emit the XML document. |
| `comment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list, or `null` if no comment is desired. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing to the specified output stream results in an `IOException`. |
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |
| `java.lang.NullPointerException` | if `os` is null. |
| --- | --- |

**See Also**

- loadFromXML

### storeToXML

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun storeToXML(
    os: OutputStream!, 
    comment: String!, 
    encoding: String!
): Unit
```

Emits an XML document representing all of the properties contained in this table, using the specified encoding.

The XML document will have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```

If the specified comment is `null` then no comment will be stored in the document.

An implementation is required to support writing of XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

The specified stream remains open after this method returns.

This method behaves the same as [storeToXML(OutputStream,String,Charset)](Properties.md)) except that it will java.nio.charset.Charset#forName using the given encoding name.

| Parameters ||
|---|---|
| `os` | [OutputStream](../java.io/OutputStream.md)!: the output stream on which to emit the XML document. |
| `comment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list, or `null` if no comment is desired. |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of a supported [character encoding](../java.lang/_package.md) |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing to the specified output stream results in an `IOException`. |
| `java.io.UnsupportedEncodingException` | if the encoding is not supported by the implementation. |
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |
| --- | --- |
| `java.lang.NullPointerException` | if `os` is `null`, or if `encoding` is `null`. |

**See Also**

- loadFromXML

### storeToXML

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun storeToXML(
    os: OutputStream!, 
    comment: String!, 
    charset: Charset!
): Unit
```

Emits an XML document representing all of the properties contained in this table, using the specified encoding.

The XML document will have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```

If the specified comment is `null` then no comment will be stored in the document.

An implementation is required to support writing of XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

Unmappable characters for the specified charset will be encoded as numeric character references.

The specified stream remains open after this method returns.

| Parameters ||
|---|---|
| `os` | [OutputStream](../java.io/OutputStream.md)!: the output stream on which to emit the XML document. |
| `comment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the property list, or `null` if no comment is desired. |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: the charset |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if writing to the specified output stream results in an `IOException`. |
| `java.lang.ClassCastException` | if this `Properties` object contains any keys or values that are not `Strings`. |
| `java.lang.NullPointerException` | if `os` or `charset` is `null`. |
| --- | --- |

**See Also**

- loadFromXML

### stringPropertyNames

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stringPropertyNames(): MutableSet<String!>!
```

Returns an unmodifiable set of keys from this property list where the key and its corresponding value are strings, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list. Properties whose key or value is not of type `String` are omitted.

The returned set is not backed by this `Properties` object. Changes to this `Properties` object are not reflected in the returned set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an unmodifiable set of keys in this property list where the key and its corresponding value are strings, including the keys in the default property list. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Properties#defaults:java.util.Properties`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of this `Hashtable` object in the form of a set of entries, enclosed in braces and separated by the ASCII characters "` , `" (comma and space). Each entry is rendered as the key, an equals sign `=`, and the associated element, where the `toString` method is used to convert the key and element to strings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this hashtable |

## Protected methods

### rehash

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun rehash(): Unit
```

Increases the capacity of and internally reorganizes this hashtable, in order to accommodate and access its entries more efficiently. This method is called automatically when the number of keys in the hashtable exceeds this hashtable's capacity and load factor.

## Properties

### defaults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var defaults: Properties!
```

A property list that contains default values for any keys not found in this property list.

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val entries: MutableSet<MutableEntry<Any!, Any!>>
```

Returns a Set view of the mappings contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>>` | a set view of the mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val keys: MutableSet<Any!>
```

Returns a Set view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | a set view of the keys contained in this map |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of keys in this hashtable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of keys in this hashtable. |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val values: MutableCollection<Any!>
```

Returns a Collection view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | a collection view of the values contained in this map |
