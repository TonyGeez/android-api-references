# Enum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Enum

```
abstract class Enum<E : Enum<E>!> : Comparable<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Enum](https://developer.android.com/reference/kotlin/java/lang/Enum#) |

This is the common base class of all Java language enumeration classes. More information about enums, including descriptions of the implicitly declared methods synthesized by the compiler, can be found in section {@jls 8.9} of The Java Language Specification. Enumeration classes are all serializable and receive special handling by the serialization mechanism. The serialized representation used for enum constants cannot be customized. Declarations of methods and fields that would otherwise interact with serialization are ignored, including`serialVersionUID`; see the Java Object Serialization Specification for details.

Note that when using an enumeration type as the type of a set or as the type of the keys in a map, specialized and efficient [set](https://developer.android.com/reference/kotlin/java/util/EnumSet.html#) and implementations are available.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Enum](https://developer.android.com/reference/kotlin/java/lang/Enum#Enum(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `ordinal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sole constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/lang/Enum#compareTo(java.lang.Enum.E))`(`other:` `E`)` Compares this enum with the specified object for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/lang/Enum#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified object is equal to this enum constant. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<E\> | [getDeclaringClass](https://developer.android.com/reference/kotlin/java/lang/Enum#getDeclaringClass())`()` Returns the Class object corresponding to this enum constant's enum type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/Enum#hashCode())`()` Returns a hash code for this enum constant. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [name](https://developer.android.com/reference/kotlin/java/lang/Enum#name())`()` Returns the name of this enum constant, exactly as declared in its enum declaration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ordinal](https://developer.android.com/reference/kotlin/java/lang/Enum#ordinal())`()` Returns the ordinal of this enumeration constant (its position in its enum declaration, where the initial constant is assigned an ordinal of zero). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Enum#toString())`()` Returns the name of this enum constant, as contained in the declaration. |
| openstaticT | [valueOf](https://developer.android.com/reference/kotlin/java/lang/Enum#valueOf(java.lang.Class,%20kotlin.String))`(`enumClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<T>`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the enum constant of the specified enum class with the specified name. |

| Protected methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/lang/Enum#clone())`()` Throws CloneNotSupportedException. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/java/lang/Enum#finalize())`()` enum classes cannot have finalize methods. |

## Protected constructors

### Enum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Enum(
    name: String, 
    ordinal: Int)
```

Sole constructor. Programmers cannot invoke this constructor. It is for use by code emitted by the compiler in response to enum class declarations.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):- The name of this enum constant, which is the identifier used to declare it. |
| `ordinal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):- The ordinal of this enumeration constant (its position in the enum declaration, where the initial constant is assigned an ordinal of zero). |

## Public methods

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: E): Int
```

Compares this enum with the specified object for order. Returns a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. Enum constants are only comparable to other enum constants of the same enum type. The natural order implemented by this method is the order in which the constants are declared.

| Parameters ||
|-----|----------------------------|
| `o` | the object to be compared. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns true if the specified object is equal to this enum constant.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to be compared for equality with this object. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified object is equal to this enum constant. |

### getDeclaringClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaringClass(): Class<E>
```

Returns the Class object corresponding to this enum constant's enum type. Two enum constants e1 and e2 are of the same enum type if and only if e1.getDeclaringClass() == e2.getDeclaringClass(). (The value returned by this method may differ from the one returned by the [Object.getClass](https://developer.android.com/reference/kotlin/java/lang/Object#getClass())method for enum constants with constant-specific class bodies.)

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<E> | the Class object corresponding to this enum constant's enum type |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this enum constant.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code for this enum constant. |

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun name(): String
```

Returns the name of this enum constant, exactly as declared in its enum declaration.**Most programmers should use the [toString](https://developer.android.com/reference/kotlin/java/lang/Enum#toString())method in preference to this one, as the toString method may return a more user-friendly name.**This method is designed primarily for use in specialized situations where correctness depends on getting the exact name, which will not vary from release to release.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of this enum constant |

### ordinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ordinal(): Int
```

Returns the ordinal of this enumeration constant (its position in its enum declaration, where the initial constant is assigned an ordinal of zero). Most programmers will have no use for this method. It is designed for use by sophisticated enum-based data structures, such as [java.util.EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet.html#) and [java.util.EnumMap](https://developer.android.com/reference/kotlin/java/util/EnumMap.html#).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ordinal of this enumeration constant |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the name of this enum constant, as contained in the declaration. This method may be overridden, though it typically isn't necessary or desirable. An enum class should override this method when a more "programmer-friendly" string form exists.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of this enum constant |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Enum<T>!> valueOf(
    enumClass: Class<T>, 
    name: String
): T
```

Returns the enum constant of the specified enum class with the specified name. The name must match exactly an identifier used to declare an enum constant in this class. (Extraneous whitespace characters are not permitted.)

Note that for a particular enum class`T`, the implicitly declared`public static T valueOf(String)`method on that enum may be used instead of this method to map from a name to the corresponding enum constant. All the constants of an enum class can be obtained by calling the implicit`public static T[] values()`method of that class.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | The enum class whose constant is to be returned |
| `enumClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<T\>:the`Class`object of the enum class from which to return a constant |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the constant to return |
| --- | --- |

| Return ||
|---|-----------------------------------------------------------------------|
| T | the enum constant of the specified enum class with the specified name |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified enum class has no constant with the specified name, or the specified class object does not represent an enum class |
| `java.lang.NullPointerException` | if`enumClass`or`name`is null |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun clone(): Any
```

Throws CloneNotSupportedException. This guarantees that enums are never cloned, which is necessary to preserve their "singleton" status.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | (never returns) |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

enum classes cannot have finalize methods.

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
