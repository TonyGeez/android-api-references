# Manifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Manifest

```
open class Manifest : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.jar.Manifest](Manifest.md) |

The Manifest class is used to maintain Manifest entry names and their associated Attributes. There are main Manifest Attributes as well as per-entry Attributes. For information on the Manifest format, please see the [Manifest format specification](https://docs.oracle.com/en/java/javase/17/docs/specs/jar/jar.html).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Manifest](Manifest.md))`()` Constructs a new, empty Manifest. |
| [Manifest](Manifest.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` Constructs a new Manifest from the specified input stream. |
| [Manifest](Manifest.md))`(`man:` ` [Manifest](Manifest.md)!`)` Constructs a new Manifest that is a copy of the specified Manifest. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](Manifest.md))`()` Clears the main Attributes as well as the entries in this Manifest. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](Manifest.md))`()` Returns a shallow copy of this Manifest. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Manifest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified Object is also a Manifest and has the same main Attributes and entries. |
| --- | --- |
| open [Attributes](Attributes.md)! | [getAttributes](Manifest.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the Attributes for the specified entry name. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Attributes](Attributes.md)!\>! | [getEntries](Manifest.md))`()` Returns a Map of the entries contained in this Manifest. |
| open [Attributes](Attributes.md)! | [getMainAttributes](Manifest.md))`()` Returns the main Attributes for the Manifest. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Manifest.md))`()` Returns the hash code for this Manifest. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [read](Manifest.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` Reads the Manifest from the specified InputStream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Manifest.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` Writes the Manifest to the specified OutputStream. |
| --- | --- |

## Public constructors

### Manifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Manifest()
```

Constructs a new, empty Manifest. 

### Manifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Manifest(is: InputStream!)
```

Constructs a new Manifest from the specified input stream.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](../java.io/InputStream.md)!:the input stream containing manifest data |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### Manifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Manifest(man: Manifest!)
```

Constructs a new Manifest that is a copy of the specified Manifest.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `man` | [Manifest](Manifest.md)!:the Manifest to copy |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Clears the main Attributes as well as the entries in this Manifest. 

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a shallow copy of this Manifest. The shallow copy is implemented as follows: 

```kotlin
public Object clone() { return new Manifest(this); }
  
```

<br />

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this Manifest |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Returns true if the specified Object is also a Manifest and has the same main Attributes and entries.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified Object is also a Manifest and has the same main Attributes and entries |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributes(name: String!): Attributes!
```

Returns the Attributes for the specified entry name. This method is defined as: 

```kotlin
return (Attributes)getEntries().get(name)
  
```
Though`null`is a valid`name`, when`getAttributes(null)`is invoked on a`Manifest`obtained from a jar file,`null`will be returned. While jar files themselves do not allow`null`-named attributes, it is possible to invoke [getEntries](Manifest.md))on a`Manifest`, and on that result, invoke`put`with a null key and an arbitrary value. Subsequent invocations of`getAttributes(null)`will return the just-`put`value.

<br />

Note that this method does not return the manifest's main attributes; see [getMainAttributes](Manifest.md)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:entry name |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------|
| [Attributes](Attributes.md)! | the Attributes for the specified entry name |

### getEntries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntries(): MutableMap<String!, Attributes!>!
```

Returns a Map of the entries contained in this Manifest. Each entry is represented by a String name (key) and associated Attributes (value). The Map permits the`null`key, but no entry with a null key is created by [read](Manifest.md)), nor is such an entry written by using [write](Manifest.md)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Attributes](Attributes.md)!>! | a Map of the entries contained in this Manifest |

### getMainAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMainAttributes(): Attributes!
```

Returns the main Attributes for the Manifest.

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------|
| [Attributes](Attributes.md)! | the main Attributes for the Manifest |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code for this Manifest.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(is: InputStream!): Unit
```

Reads the Manifest from the specified InputStream. The entry names and attributes read will be merged in with the current manifest entries.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](../java.io/InputStream.md)!:the input stream |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(out: OutputStream!): Unit
```

Writes the Manifest to the specified OutputStream. Attributes.Name.MANIFEST_VERSION must be set in MainAttributes prior to invoking this method.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java.io/OutputStream.md)!:the output stream |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

**See Also**

- [#getMainAttributes](Manifest.md))
