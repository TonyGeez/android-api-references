Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Property

Kotlin | [Java](Property.md)
| --- | --- |

```
abstract class Property<T : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Property](Property.md) |

| Known Direct Subclasses [FloatProperty](FloatProperty.md), [IntProperty](IntProperty.md) |---|---| | [FloatProperty](FloatProperty.md) | An implementation of `https://developer.android.com/reference/kotlin/android/util/Property#` to be used specifically with fields of type `float`. | | [IntProperty](IntProperty.md) | An implementation of `https://developer.android.com/reference/kotlin/android/util/Property#` to be used specifically with fields of type `int`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A property is an abstraction that can be used to represent a mutable value that is held in a *host* object. The Property's `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` or `https://developer.android.com/reference/kotlin/android/util/Property#get(android.util.Property.T)` methods can be implemented in terms of the private fields of the host object, or via "setter" and "getter" methods or by some other mechanism, as appropriate.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Property#Property(java.lang.Class,%20kotlin.String)(type: https://developer.android.com/reference/kotlin/java/lang/Class.html#<V>!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` A constructor that takes an identifying name and `https://developer.android.com/reference/kotlin/android/util/Property#getType()` for the property. |

| Public methods ||
|---|---|
| abstract V | `https://developer.android.com/reference/kotlin/android/util/Property#get(android.util.Property.T)(object: T)` Returns the current value that this property represents on the given `object`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/util/Property#getName()()` Returns the name for this property. |
| open [Class](../java.lang/Class.md)\<V\>! | `https://developer.android.com/reference/kotlin/android/util/Property#getType()()` Returns the type for this property. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly()()` Returns true if the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method does not set the value on the target object (in which case the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method should throw a `https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException` exception). |
| open static [Property](Property.md)\<T, V\>! | `https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String)(hostType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!, valueType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<V>!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` This factory method creates and returns a Property given the `class` and `name` parameters, where the `"name"` parameter represents either: - a public `getName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `getName()` - a public `isName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `isName()` - a public `name` field on the class <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)(object: T, value: V)` Sets the value on `object` which this property represents. |
| --- | --- |

## Public constructors

### Property

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Property(
    type: Class<V>!, 
    name: String!)
```

A constructor that takes an identifying name and `https://developer.android.com/reference/kotlin/android/util/Property#getType()` for the property.

## Public methods

### get

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(object: T): V
```

Returns the current value that this property represents on the given `object`.

### getName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

Returns the name for this property.

### getType

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): Class<V>!
```

Returns the type for this property.

### isReadOnly

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isReadOnly(): Boolean
```

Returns true if the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method does not set the value on the target object (in which case the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method should throw a `https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException` exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the `https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String)` factory method may return a Property with name "foo" for an object that has only a `getFoo()` or `isFoo()` method, but no matching `setFoo()` method.

### of

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!, V : Any!> of(
    hostType: Class<T>!, 
    valueType: Class<V>!, 
    name: String!
): Property<T, V>!
```

This factory method creates and returns a Property given the `class` and `name` parameters, where the `"name"` parameter represents either:

- a public `getName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `getName()`
- a public `isName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `isName()`
- a public `name` field on the class

<br />

If either of the get/is method alternatives is found on the class, but an appropriate `setName()` method is not found, the `Property` will be `https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly()`. Calling the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method on such a property is allowed, but will have no effect.

If neither the methods nor the field are found on the class a `https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException` exception will be thrown.

### set

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    object: T, 
    value: V
): Unit
```

Sets the value on `object` which this property represents. If the method is unable to set the value on the target object it will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` exception.
