Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Provider

```
abstract class Provider : Properties
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.util.Dictionary](https://developer.android.com/reference/kotlin/java/util/Dictionary.html#)\<K, V\> ||||
| | ↳ | [java.util.Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable.html#)\< [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)\> |||
| | | ↳ | [java.util.Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider#) |

Known Direct Subclasses [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider) [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider) Legacy security code; do not use.

This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. Services that a provider may implement include:

- Algorithms (such as DSA, RSA, MD5 or SHA-1).
- Key generation, conversion, and management facilities (such as for algorithm-specific keys).

<br />

Each provider has a name and a version number, and is configured in each runtime it is installed in.

See [The Provider Class](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#Provider) in the "Java Cryptography Architecture API Specification \& Reference" for information about how a particular type of provider, the cryptographic service provider, works and is installed. However, please note that a provider can be used to implement any security service in Java that uses a pluggable architecture with a choice of implementations that fit underneath.

Some provider implementations may encounter unrecoverable internal errors during their operation, for example a failure to communicate with a security token. A `https://developer.android.com/reference/kotlin/java/security/ProviderException` should be used to indicate such errors.

The service type `Provider` is reserved for use by the security framework. Services of this type cannot be added, removed, or modified by applications. The following attributes are automatically placed in each Provider object:
**Attributes Automatically Placed in a Provider Object**

| Name | Value |
|---|---|
| `Provider.id name` | `String.valueOf(provider.getName())` |
| `Provider.id version` | `String.valueOf(provider.getVersion())` |
| `Provider.id info` | `String.valueOf(provider.getInfo())` |
| --- | --- |
| `Provider.id className` | `provider.getClass().getName()` |

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/security/Provider.Service` The description of a security service. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider#Provider(kotlin.String,%20kotlin.Double,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, info: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a provider with the specified name, version number, and information. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#clear()()` Clears this provider so that it no longer contains the properties used to look up facilities implemented by the provider. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#compute(kotlin.Any,%20java.util.function.BiFunction)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, *>)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Provider#computeIfAbsent(kotlin.Any,%20java.util.function.Function)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, mappingFunction: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, *>)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#computeIfPresent(kotlin.Any,%20java.util.function.BiFunction)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, *>)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/Provider#elements()()` Returns an enumeration of the values in this hashtable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>)` <br /> |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#get(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Provider#getInfo()()` Returns a human-readable description of the provider and its services. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Provider#getName()()` Returns the name of this provider. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Provider#getOrDefault(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Provider#getProperty(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Searches for the property with the specified key in this property list. |
| open [Provider.Service](https://developer.android.com/reference/kotlin/java/security/Provider.Service)! | `https://developer.android.com/reference/kotlin/java/security/Provider#getService(kotlin.String,%20kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Get the service describing this Provider's implementation of the specified type of this algorithm or alias. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Provider.Service](https://developer.android.com/reference/kotlin/java/security/Provider.Service)!\>! | `https://developer.android.com/reference/kotlin/java/security/Provider#getServices()()` Get an unmodifiable Set of all services supported by this Provider. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#getVersion()()` Returns the version number for this provider. |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/Provider#keys()()` Returns an enumeration of the keys in this hashtable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#load(java.io.InputStream)(inStream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Reads a property list (key and element pairs) from the input stream. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#merge(kotlin.Any,%20kotlin.Any,%20java.util.function.BiFunction)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html, *>)` If the specified key is not already associated with a value or is associated with null, associates it with the given value. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#put(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Sets the `key` property to have the specified `value`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<*, *>)` Copies all of the mappings from the specified Map to this provider. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#putIfAbsent(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#remove(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Removes the `key` property (and its corresponding `value`). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#remove(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Removes the entry for the specified key only if it is currently mapped to the specified value. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/java/security/Provider#replace(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Replaces the entry for the specified key only if it is currently mapped to some value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#replace(kotlin.Any,%20kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, oldValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Replaces the entry for the specified key only if currently mapped to the specified value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, *>)` Replaces each entry's value with the result of invoking the given function on that entry, in the order entries are returned by an entry set iterator, until all entries have been processed or the function throws an exception. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#toString()()` Returns a string with the name and the version number of this provider. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)(s: https://developer.android.com/reference/kotlin/java/security/Provider.Service!)` Add a service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Provider#removeService(java.security.Provider.Service)(s: https://developer.android.com/reference/kotlin/java/security/Provider.Service!)` Remove a service previously added using `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)`. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/util/Properties.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#clone()()`

Creates a shallow copy of this hashtable. All the structure of the hashtable itself is copied, but the keys and values are not cloned. This is a relatively expensive operation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#contains(kotlin.Any)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Tests if some key maps into the specified value in this hashtable. This operation is more expensive than the `https://developer.android.com/reference/kotlin/java/util/Hashtable.html#containsKey(java.util.Hashtable.K)` method.

Note that this method is identical in functionality to `https://developer.android.com/reference/kotlin/java/util/Hashtable.html#containsValue(java.util.Hashtable.V)`, (which is part of the `https://developer.android.com/reference/kotlin/java/util/Map.html#` interface in the collections framework).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#containsKey(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Tests if the specified object is a key in this hashtable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#containsValue(kotlin.Any)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Returns true if this hashtable maps one or more keys to this value.

Note that this method is identical in functionality to `https://developer.android.com/reference/kotlin/java/util/Hashtable.html#contains(kotlin.Any)` (which predates the `https://developer.android.com/reference/kotlin/java/util/Map.html#` interface).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)`

Compares the specified Object with this Map for equality, as per the definition in the Map interface.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/java/util/Properties.html#getProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Searches for the property with the specified key in this property list. If the key is not found in this property list, the default property list, and its defaults, recursively, are then checked. The method returns the default value argument if the property is not found.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#hashCode()()`

Returns the hash code value for this Map as per the definition in the Map interface.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#isEmpty()()`

Tests if this hashtable maps no keys to values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#list(java.io.PrintStream)(out: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#!)`

Prints this property list out to the specified output stream. This method is useful for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#list(java.io.PrintWriter)(out: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!)`

Prints this property list out to the specified output stream. This method is useful for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#load(java.io.Reader)(reader: https://developer.android.com/reference/kotlin/java/io/Reader.html#!)`

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#loadFromXML(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)`

Loads all of the properties represented by the XML document on the specified input stream into this properties table.

The XML document must have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```
Furthermore, the document must satisfy the properties DTD described above.

An implementation is required to read XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

The specified stream is closed after this method returns.

<br />

`https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<*>!` `https://developer.android.com/reference/kotlin/java/util/Properties.html#propertyNames()()`

Returns an enumeration of all the keys in this property list, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#rehash()()`

Increases the capacity of and internally reorganizes this hashtable, in order to accommodate and access its entries more efficiently. This method is called automatically when the number of keys in the hashtable exceeds this hashtable's capacity and load factor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#save(java.io.OutputStream,%20kotlin.String)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, comments: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Calls the `store(OutputStream out, String comments)` method and suppresses IOExceptions that were thrown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` `https://developer.android.com/reference/kotlin/java/util/Properties.html#setProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Calls the `Hashtable` method `put`. Provided for parallelism with the `getProperty` method. Enforces use of strings for property keys and values. The value returned is the result of the `Hashtable` call to `put`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#store(java.io.OutputStream,%20kotlin.String)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, comments: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Writes this property list (key and element pairs) in this `Properties` table to the output stream in a format suitable for loading into a `Properties` table using the `https://developer.android.com/reference/kotlin/java/util/Properties.html#load(java.io.InputStream)` method.

Properties from the defaults table of this `Properties` table (if any) are *not* written out by this method.

This method outputs the comments, properties keys and values in the same format as specified in `https://developer.android.com/reference/kotlin/java/util/Properties.html#store(java.io.Writer,%20kotlin.String)`, with the following differences:

- The stream is written using the ISO 8859-1 character encoding.
- Characters not in Latin-1 in the comments are written as `\u005Cu`*xxxx* for their appropriate unicode hexadecimal value *xxxx*.
- Characters less than `\u005Cu0020` and characters greater than `\u005Cu007E` in property keys or values are written as `\u005Cu`*xxxx* for the appropriate hexadecimal value *xxxx*.

After the entries have been written, the output stream is flushed. The output stream remains open after this method returns.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#store(java.io.Writer,%20kotlin.String)(writer: https://developer.android.com/reference/kotlin/java/io/Writer.html#!, comments: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Writes this property list (key and element pairs) in this `Properties` table to the output character stream in a format suitable for using the `https://developer.android.com/reference/kotlin/java/util/Properties.html#load(java.io.Reader)` method.

Properties from the defaults table of this `Properties` table (if any) are *not* written out by this method.

If the comments argument is not null, then an ASCII character, the comments string, and a line separator are first written to the output stream. Thus, the `comments` can serve as an identifying comment. Any one of a line feed ('\\n'), a carriage return ('\\r'), or a carriage return followed immediately by a line feed in comments is replaced by a line separator generated by the `Writer` and if the next character in comments is not character or character `!` then an ASCII is written out after that line separator.

Next, a comment line is always written, consisting of an ASCII character, the current date and time (as if produced by the `toString` method of `Date` for the current time), and a line separator as generated by the `Writer`.

Then every entry in this `Properties` table is written out, one per line. For each entry the key string is written, then an ASCII `=`, then the associated element string. For the key, all space characters are written with a preceding `\` character. For the element, leading space characters, but not embedded or trailing space characters, are written with a preceding `\` character. The key and element characters , `!`, `=`, and `:` are written with a preceding backslash to ensure that they are properly loaded.

After the entries have been written, the output stream is flushed. The output stream remains open after this method returns.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#storeToXML(java.io.OutputStream,%20kotlin.String)(os: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, comment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Emits an XML document representing all of the properties contained in this table.

An invocation of this method of the form `props.storeToXML(os, comment)` behaves in exactly the same way as the invocation `props.storeToXML(os, comment, "UTF-8");`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#storeToXML(java.io.OutputStream,%20kotlin.String,%20kotlin.String)(os: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, comment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, encoding: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Emits an XML document representing all of the properties contained in this table, using the specified encoding.

The XML document will have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```

If the specified comment is `null` then no comment will be stored in the document.

An implementation is required to support writing of XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

The specified stream remains open after this method returns.

This method behaves the same as [storeToXML(OutputStream,String,Charset)](https://developer.android.com/reference/kotlin/java/util/Properties.html#storeToXML(java.io.OutputStream,%20kotlin.String,%20java.nio.charset.Charset)) except that it will java.nio.charset.Charset#forName using the given encoding name.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#storeToXML(java.io.OutputStream,%20kotlin.String,%20java.nio.charset.Charset)(os: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, comment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, charset: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#!)`

Emits an XML document representing all of the properties contained in this table, using the specified encoding.

The XML document will have the following DOCTYPE declaration:

```kotlin
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
  
```

If the specified comment is `null` then no comment will be stored in the document.

An implementation is required to support writing of XML documents that use the "`UTF-8`" or "`UTF-16`" encoding. An implementation may support additional encodings.

Unmappable characters for the specified charset will be encoded as numeric character references.

The specified stream remains open after this method returns.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/java/util/Properties.html#stringPropertyNames()()`

Returns an unmodifiable set of keys from this property list where the key and its corresponding value are strings, including distinct keys in the default property list if a key of the same name has not already been found from the main properties list. Properties whose key or value is not of type `String` are omitted.

The returned set is not backed by this `Properties` object. Changes to this `Properties` object are not reflected in the returned set.

<br />

| Properties ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>\> | `https://developer.android.com/reference/kotlin/java/security/Provider#entries:kotlin.collections.MutableSet` Returns an unmodifiable Set view of the property entries contained in this Provider. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/security/Provider#keys:kotlin.collections.MutableSet` Returns an unmodifiable Set view of the property keys contained in this provider. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/security/Provider#values:kotlin.collections.MutableCollection` Returns an unmodifiable Collection view of the property values contained in this provider. |
| --- | --- |

Inherited properties From class `https://developer.android.com/reference/kotlin/java/util/Properties.html#` `https://developer.android.com/reference/kotlin/java/util/Properties.html#!` `https://developer.android.com/reference/kotlin/java/util/Properties.html#defaults:java.util.Properties`

A property list that contains default values for any keys not found in this property list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/util/Properties.html#size:kotlin.Int`

Returns the number of keys in this hashtable.

<br />

## Protected constructors

### Provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Provider(
    name: String!, 
    version: Double, 
    info: String!)
```

Constructs a provider with the specified name, version number, and information.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the provider name. |
| `version` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the provider version number. |
| `info` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the provider and its services. |
| --- | --- |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Clears this provider so that it no longer contains the properties used to look up facilities implemented by the provider.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"clearProviderProperties."+name` (where `name` is the provider name) to see if it's ok to clear this provider.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to clear this provider |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Any!, 
    remappingFunction: BiFunction<in Any!, in Any?, *>
): Any?
```

Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping).

If a security manager is enabled, its `checkSecurityAccess` method is called with the strings `"putProviderProperty."+name` and `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values and remove this provider's properties.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, \*\>: the remapping function to compute a value |

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values or remove properties. |
| --- | --- |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfAbsent(
    key: Any!, 
    mappingFunction: Function<in Any!, *>
): Any!
```

If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`.

If a security manager is enabled, its `checkSecurityAccess` method is called with the strings `"putProviderProperty."+name` and `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values and remove this provider's properties.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `mappingFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, \*\>: the mapping function to compute a value |

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values and remove properties. |
| --- | --- |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfPresent(
    key: Any!, 
    remappingFunction: BiFunction<in Any!, in Any, *>
): Any?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value.

If a security manager is enabled, its `checkSecurityAccess` method is called with the strings `"putProviderProperty."+name` and `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values and remove this provider's properties.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), \*\>: the remapping function to compute a value |

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values or remove properties. |
| --- | --- |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun elements(): Enumeration<Any!>!
```

Returns an enumeration of the values in this hashtable. Use the Enumeration methods on the returned object to fetch the elements sequentially. If the hashtable is structurally modified while enumerating over the values then the results of enumerating are undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | an enumeration of the values in this hashtable. |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: BiConsumer<in Any!, in Any!>): Unit
```

| Parameters ||
|---|---|
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: The action to be performed for each entry |

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

### getInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInfo(): String!
```

Returns a human-readable description of the provider and its services. This may return an HTML page, with relevant links.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a description of the provider and its services. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

Returns the name of this provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of this provider. |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrDefault(
    key: Any!, 
    defaultValue: Any!
): Any!
```

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

### getService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getService(
    type: String!, 
    algorithm: String!
): Provider.Service!
```

Get the service describing this Provider's implementation of the specified type of this algorithm or alias. If no such implementation exists, this method returns null. If there are two matching services, one added to this provider using `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)` and one added via #put, the service added via `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)` is returned.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of `https://developer.android.com/reference/kotlin/java/security/Provider.Service` requested (for example, `MessageDigest`) |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the case insensitive algorithm name (or alternate alias) of the service requested (for example, `SHA-1`) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider.Service!` | the service describing this Provider's matching service or null if no such service exists |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if type or algorithm is null |

### getServices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServices(): MutableSet<Provider.Service!>!
```

Get an unmodifiable Set of all services supported by this Provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/Provider.Service!>!` | an unmodifiable Set of all services supported by this Provider |

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVersion(): Double
```

Returns the version number for this provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the version number for this provider. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keys(): Enumeration<Any!>!
```

Returns an enumeration of the keys in this hashtable. Use the Enumeration methods on the returned object to fetch the keys sequentially. If the hashtable is structurally modified while enumerating over the keys then the results of enumerating are undefined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | an enumeration of the keys in this hashtable. |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun load(inStream: InputStream!): Unit
```

Reads a property list (key and element pairs) from the input stream.

| Parameters ||
|---|---|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the input stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred when reading from the input stream. |
| `java.lang.IllegalArgumentException` | if the input stream contains a malformed Unicode escape sequence. |
| `java.lang.NullPointerException` | if `inStream` is null. |
| --- | --- |

**See Also**

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun merge(
    key: Any!, 
    value: Any, 
    remappingFunction: BiFunction<in Any, in Any, *>
): Any?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given value. Otherwise, replaces the value with the results of the given remapping function, or removes if the result is null. This method may be of use when combining multiple mapped values for a key.

If a security manager is enabled, its `checkSecurityAccess` method is called with the strings `"putProviderProperty."+name` and `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values and remove this provider's properties.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: key with which the resulting value is to be associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html), \*\>: the remapping function to recompute a value if present |
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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values or remove properties. |
| --- | --- |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Any!, 
    value: Any!
): Any?
```

Sets the `key` property to have the specified `value`.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putAll(from: Map<*, *>): Unit
```

Copies all of the mappings from the specified Map to this provider. These mappings will replace any properties that this provider had for any of the keys currently in the specified Map.

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

If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: Any!): Any?
```

Removes the `key` property (and its corresponding `value`).

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to remove this provider's properties.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to remove this provider's properties. |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(
    key: Any!, 
    value: Any!
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to remove this provider's properties.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to remove this provider's properties. |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: Any!, 
    value: Any!
): Any?
```

Replaces the entry for the specified key only if it is currently mapped to some value.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: Any!, 
    oldValue: Any!, 
    newValue: Any!
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values.

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
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(function: BiFunction<in Any!, in Any!, *>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry, in the order entries are returned by an entry set iterator, until all entries have been processed or the function throws an exception.

If a security manager is enabled, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values.

| Parameters ||
|---|---|
| `function` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, in [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, \*\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |
| --- | --- |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string with the name and the version number of this provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string with the name and the version number for this provider. |

## Protected methods

### putService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun putService(s: Provider.Service!): Unit
```

Add a service. If a service of the same type with the same algorithm name exists and it was added using `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)`, it is replaced by the new service. This method also places information about this service in the provider's Hashtable values in the format described in the [Java Cryptography Architecture API Specification \& Reference](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html).

Also, if there is a security manager, its `checkSecurityAccess` method is called with the string `"putProviderProperty."+name`, where `name` is the provider name, to see if it's ok to set this provider's property values. If the default implementation of `checkSecurityAccess` is used (that is, that method is not overriden), then this results in a call to the security manager's `checkPermission` method with a `SecurityPermission("putProviderProperty."+name)` permission.

| Parameters ||
|---|---|
| `s` | [Provider.Service](https://developer.android.com/reference/kotlin/java/security/Provider.Service)!: the Service to add |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if s is null |
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to set property values. |

### removeService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun removeService(s: Provider.Service!): Unit
```

Remove a service previously added using `https://developer.android.com/reference/kotlin/java/security/Provider#putService(java.security.Provider.Service)`. The specified service is removed from this provider. It will no longer be returned by `https://developer.android.com/reference/kotlin/java/security/Provider#getService(kotlin.String,%20kotlin.String)` and its information will be removed from this provider's Hashtable.

Also, if there is a security manager, its `checkSecurityAccess` method is called with the string `"removeProviderProperty."+name`, where `name` is the provider name, to see if it's ok to remove this provider's properties. If the default implementation of `checkSecurityAccess` is used (that is, that method is not overriden), then this results in a call to the security manager's `checkPermission` method with a `SecurityPermission("removeProviderProperty."+name)` permission.

| Parameters ||
|---|---|
| `s` | [Provider.Service](https://developer.android.com/reference/kotlin/java/security/Provider.Service)!: the Service to be removed |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if s is null |
| `java.lang.SecurityException` | if a security manager exists and its `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String)` method denies access to remove this provider's properties. |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val entries: MutableSet<MutableEntry<Any!, Any!>>
```

Returns an unmodifiable Set view of the property entries contained in this Provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>>` | a set view of the mappings contained in this map |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Map.Entry.html#`

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val keys: MutableSet<Any!>
```

Returns an unmodifiable Set view of the property keys contained in this provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | a set view of the keys contained in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val values: MutableCollection<Any!>
```

Returns an unmodifiable Collection view of the property values contained in this provider.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | a collection view of the values contained in this map |
