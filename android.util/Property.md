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

| Known Direct Subclasses [FloatProperty](FloatProperty.md), [IntProperty](IntProperty.md) |---|---| | [FloatProperty](FloatProperty.md) | An implementation of Property to be used specifically with fields of type `float`. | | [IntProperty](IntProperty.md) | An implementation of Property to be used specifically with fields of type `int`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A property is an abstraction that can be used to represent a mutable value that is held in a *host* object. The Property's set or get methods can be implemented in terms of the private fields of the host object, or via "setter" and "getter" methods or by some other mechanism, as appropriate.

## Summary

| Public constructors ||
|---|---|
| Property A constructor that takes an identifying name and getType for the property. |

| Public methods ||
|---|---|
| abstract V | get Returns the current value that this property represents on the given `object`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getName Returns the name for this property. |
| open [Class](../java.lang/Class.md)\<V\>! | getType Returns the type for this property. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isReadOnly Returns true if the set method does not set the value on the target object (in which case the set method should throw a NoSuchPropertyException exception). |
| open static [Property](Property.md)\<T, V\>! | of This factory method creates and returns a Property given the `class` and `name` parameters, where the `"name"` parameter represents either: - a public `getName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `getName()` - a public `isName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `isName()` - a public `name` field on the class <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the value on `object` which this property represents. |
| --- | --- |

## Public constructors

### Property

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Property(
    type: Class<V>!, 
    name: String!)
```

A constructor that takes an identifying name and getType for the property.

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

Returns true if the set method does not set the value on the target object (in which case the set method should throw a NoSuchPropertyException exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the of factory method may return a Property with name "foo" for an object that has only a `getFoo()` or `isFoo()` method, but no matching `setFoo()` method.

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

If either of the get/is method alternatives is found on the class, but an appropriate `setName()` method is not found, the `Property` will be isReadOnly. Calling the set method on such a property is allowed, but will have no effect.

If neither the methods nor the field are found on the class a NoSuchPropertyException exception will be thrown.

### set

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    object: T, 
    value: V
): Unit
```

Sets the value on `object` which this property represents. If the method is unable to set the value on the target object it will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` exception.
