# Member

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Member

```
interface Member
```

| [java.lang.reflect.Member](../java/lang/reflect/Member.md) |

| Known Direct Subclasses [Executable](../java/lang/reflect/Executable.md), [Field](../java/lang/reflect/Field.md) |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Executable](../java/lang/reflect/Executable.md) | A shared superclass for the common functionality of [Method](../java/lang/reflect/Method.md) and [Constructor](../java/lang/reflect/Constructor.md). | | [Field](../java/lang/reflect/Field.md) | A`Field`provides information about, and dynamic access to, a single field of a class or an interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Constructor](../java/lang/reflect/Constructor.md), [Method](../java/lang/reflect/Method.md) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [Constructor](../java/lang/reflect/Constructor.md) | `Constructor`provides information about, and access to, a single constructor for a class. | | [Method](../java/lang/reflect/Method.md) | A`Method`provides information about, and access to, a single method on a class or interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Member is an interface that reflects identifying information about a single member (a field or a method) or a constructor.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECLARED](../java/lang/reflect/Member.md) Identifies the set of declared members of a class or interface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUBLIC](../java/lang/reflect/Member.md) Identifies the set of all public members of a class or interface, including inherited members. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Class](../java/lang/Class.md)\<\*\> | [getDeclaringClass](../java/lang/reflect/Member.md))`()` Returns the Class object representing the class or interface that declares the member or constructor represented by this Member. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](../java/lang/reflect/Member.md))`()` Returns the Java language modifiers for the member or constructor represented by this Member, as an integer. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../java/lang/reflect/Member.md))`()` Returns the simple name of the underlying member or constructor represented by this Member. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynthetic](../java/lang/reflect/Member.md))`()` Returns`true`if this member was introduced by the compiler; returns`false`otherwise. |

## Constants

### DECLARED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECLARED: Int
```

Identifies the set of declared members of a class or interface. Inherited members are not included. 

 Value: 1

### PUBLIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PUBLIC: Int
```

Identifies the set of all public members of a class or interface, including inherited members. 

 Value: 0

## Public methods

### getDeclaringClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDeclaringClass(): Class<*>
```

Returns the Class object representing the class or interface that declares the member or constructor represented by this Member.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*> | an object representing the declaring class of the underlying member |

### getModifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getModifiers(): Int
```

Returns the Java language modifiers for the member or constructor represented by this Member, as an integer. The Modifier class should be used to decode the modifiers in the integer.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Java language modifiers for the underlying member |

**See Also**

- [java.lang.reflect.Modifier](../java/lang/reflect/Modifier.md) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String
```

Returns the simple name of the underlying member or constructor represented by this Member.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the simple name of the underlying member |

### isSynthetic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSynthetic(): Boolean
```

Returns`true`if this member was introduced by the compiler; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this member was introduced by the compiler. |
