# Modifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Modifier

```
open class Modifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.reflect.Modifier](Modifier.md) |

The Modifier class provides`static`methods and constants to decode class and member access modifiers. The sets of modifiers are represented as integers with distinct bit positions representing different modifiers. The values for the constants representing the modifiers are taken from the tables in sections 4.1, 4.4, 4.5, and 4.7 of The Java™ Virtual Machine Specification.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ABSTRACT](Modifier.md) The`int`value representing the`abstract`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINAL](Modifier.md) The`int`value representing the`final`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERFACE](Modifier.md) The`int`value representing the`interface`modifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NATIVE](Modifier.md) The`int`value representing the`native`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIVATE](Modifier.md) The`int`value representing the`private`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTECTED](Modifier.md) The`int`value representing the`protected`modifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUBLIC](Modifier.md) The`int`value representing the`public`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATIC](Modifier.md) The`int`value representing the`static`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRICT](Modifier.md) The`int`value representing the`strictfp`modifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNCHRONIZED](Modifier.md) The`int`value representing the`synchronized`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIENT](Modifier.md) The`int`value representing the`transient`modifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VOLATILE](Modifier.md) The`int`value representing the`volatile`modifier. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [Modifier](Modifier.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [classModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to a class. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [constructorModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to a constructor. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fieldModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to a field. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [interfaceModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to an interface. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAbstract](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`abstract`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinal](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`final`modifier,`false`otherwise. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInterface](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`interface`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNative](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`native`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivate](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`private`modifier,`false`otherwise. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProtected](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`protected`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPublic](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`public`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStatic](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`static`modifier,`false`otherwise. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStrict](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`strictfp`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynchronized](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`synchronized`modifier,`false`otherwise. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransient](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`transient`modifier,`false`otherwise. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVolatile](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return`true`if the integer argument includes the`volatile`modifier,`false`otherwise. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [methodModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to a method. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterModifiers](Modifier.md))`()` Return an`int`value OR-ing together the source language modifiers that can be applied to a parameter. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](Modifier.md))`(`mod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a string describing the access modifier flags in the specified modifier. |

## Constants

### ABSTRACT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ABSTRACT: Int
```

The`int`value representing the`abstract`modifier. 

 Value: 1024

### FINAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINAL: Int
```

The`int`value representing the`final`modifier. 

 Value: 16

### INTERFACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERFACE: Int
```

The`int`value representing the`interface`modifier. 

 Value: 512

### NATIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NATIVE: Int
```

The`int`value representing the`native`modifier. 

 Value: 256

### PRIVATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIVATE: Int
```

The`int`value representing the`private`modifier. 

 Value: 2

### PROTECTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTECTED: Int
```

The`int`value representing the`protected`modifier. 

 Value: 4

### PUBLIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PUBLIC: Int
```

The`int`value representing the`public`modifier. 

 Value: 1

### STATIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATIC: Int
```

The`int`value representing the`static`modifier. 

 Value: 8

### STRICT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRICT: Int
```

The`int`value representing the`strictfp`modifier. 

 Value: 2048

### SYNCHRONIZED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNCHRONIZED: Int
```

The`int`value representing the`synchronized`modifier. 

 Value: 32

### TRANSIENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIENT: Int
```

The`int`value representing the`transient`modifier. 

 Value: 128

### VOLATILE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VOLATILE: Int
```

The`int`value representing the`volatile`modifier. 

 Value: 64

## Public constructors

### Modifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Modifier()
```

## Public methods

### classModifiers

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun classModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to a class.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to a class. |

### constructorModifiers

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun constructorModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to a constructor.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to a constructor. |

### fieldModifiers

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fieldModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to a field.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to a field. |

### interfaceModifiers

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun interfaceModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to an interface.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to an interface. |

### isAbstract

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isAbstract(mod: Int): Boolean
```

Return`true`if the integer argument includes the`abstract`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`abstract`modifier;`false`otherwise. |

### isFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isFinal(mod: Int): Boolean
```

Return`true`if the integer argument includes the`final`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`final`modifier;`false`otherwise. |

### isInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isInterface(mod: Int): Boolean
```

Return`true`if the integer argument includes the`interface`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`interface`modifier;`false`otherwise. |

### isNative

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isNative(mod: Int): Boolean
```

Return`true`if the integer argument includes the`native`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`native`modifier;`false`otherwise. |

### isPrivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isPrivate(mod: Int): Boolean
```

Return`true`if the integer argument includes the`private`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`private`modifier;`false`otherwise. |

### isProtected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isProtected(mod: Int): Boolean
```

Return`true`if the integer argument includes the`protected`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`protected`modifier;`false`otherwise. |

### isPublic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isPublic(mod: Int): Boolean
```

Return`true`if the integer argument includes the`public`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`public`modifier;`false`otherwise. |

### isStatic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isStatic(mod: Int): Boolean
```

Return`true`if the integer argument includes the`static`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`static`modifier;`false`otherwise. |

### isStrict

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isStrict(mod: Int): Boolean
```

Return`true`if the integer argument includes the`strictfp`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`strictfp`modifier;`false`otherwise. |

### isSynchronized

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSynchronized(mod: Int): Boolean
```

Return`true`if the integer argument includes the`synchronized`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`synchronized`modifier;`false`otherwise. |

### isTransient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isTransient(mod: Int): Boolean
```

Return`true`if the integer argument includes the`transient`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`transient`modifier;`false`otherwise. |

### isVolatile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isVolatile(mod: Int): Boolean
```

Return`true`if the integer argument includes the`volatile`modifier,`false`otherwise.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`mod`includes the`volatile`modifier;`false`otherwise. |

### methodModifiers

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun methodModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to a method.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to a method. |

### parameterModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parameterModifiers(): Int
```

Return an`int`value OR-ing together the source language modifiers that can be applied to a parameter.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`value OR-ing together the source language modifiers that can be applied to a parameter. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toString(mod: Int): String!
```

Return a string describing the access modifier flags in the specified modifier. For example: 

```kotlin
public final synchronized strictfp
  
```
The modifier names are returned in an order consistent with the suggested modifier orderings given in sections 8.1.1, 8.3.1, 8.4.3, 8.8.3, and 9.1.1 of The Java™ Language Specification. The full modifier ordering used by this method is:`public protected private abstract static final transient volatile synchronized native strictfp interface `The`interface`modifier discussed in this class is not a true modifier in the Java language and it appears after all other modifiers listed by this method. This method may return a string of modifiers that are not valid modifiers of a Java entity; in other words, no checking is done on the possible validity of the combination of modifiers represented by the input. Note that to perform such checking for a known kind of entity, such as a constructor or method, first AND the argument of`toString`with the appropriate mask from a method like [constructorModifiers](Modifier.md))or [methodModifiers](Modifier.md)).

<br />

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `mod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a set of modifiers |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of the set of modifiers represented by`mod` |
