Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntProperty

Kotlin | [Java](IntProperty.md)
| --- | --- |

```
abstract class IntProperty<T : Any!> : Property<T, Int!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.util.Property](Property.md)\<T, [kotlin.Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)\> ||
| | ↳ | [android.util.IntProperty](IntProperty.md) |

An implementation of Property to be used specifically with fields of type `int`. This type-specific subclass enables performance benefit by allowing calls to a setValue function that takes the primitive `int` type and avoids autoboxing and other overhead associated with the `Integer` class.

## Summary

| Public constructors ||
|---|---|
| IntProperty <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the value on `object` which this property represents. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setValue A type-specific variant of set that is faster when dealing with fields of type `int`. |

| Inherited functions ||
|---|---|
| From class Property |---|---| | `V` | get Returns the current value that this property represents on the given `object`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getName Returns the name for this property. <br /> | | `https://developer.android.com/reference/kotlin/java/lang/Class.html#<V>!` | getType Returns the type for this property. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isReadOnly Returns true if the set method does not set the value on the target object (in which case the set method should throw a NoSuchPropertyException exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the of factory method may return a Property with name "foo" for an object that has only a `getFoo()` or `isFoo()` method, but no matching `setFoo()` method. <br /> | | `https://developer.android.com/reference/kotlin/android/util/Property<T, V>!` | of This factory method creates and returns a Property given the `class` and `name` parameters, where the `"name"` parameter represents either: - a public `getName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `getName()` - a public `isName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `isName()` - a public `name` field on the class <br /> If either of the get/is method alternatives is found on the class, but an appropriate `setName()` method is not found, the `Property` will be isReadOnly. Calling the set method on such a property is allowed, but will have no effect. If neither the methods nor the field are found on the class a NoSuchPropertyException exception will be thrown. <br /> | ||

## Public constructors

### IntProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IntProperty(name: String!)
```

## Public methods

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    object: T, 
    value: Int!
): Unit
```

Sets the value on `object` which this property represents. If the method is unable to set the value on the target object it will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` exception.

### setValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setValue(
    object: T, 
    value: Int
): Unit
```

A type-specific variant of set that is faster when dealing with fields of type `int`.
