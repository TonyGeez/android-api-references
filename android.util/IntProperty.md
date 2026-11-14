Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntProperty

Kotlin | [Java](https://developer.android.com/reference/android/util/IntProperty "View this page in Java")
| --- | --- |

```
abstract class IntProperty<T : Any!> : Property<T, Int!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.util.Property](https://developer.android.com/reference/kotlin/android/util/Property)\<T, [kotlin.Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)\> ||
| | ↳ | [android.util.IntProperty](https://developer.android.com/reference/kotlin/android/util/IntProperty#) |

An implementation of `https://developer.android.com/reference/kotlin/android/util/Property` to be used specifically with fields of type `int`. This type-specific subclass enables performance benefit by allowing calls to a `https://developer.android.com/reference/kotlin/android/util/IntProperty#setValue(android.util.IntProperty.T,%20kotlin.Int)` function that takes the primitive `int` type and avoids autoboxing and other overhead associated with the `Integer` class.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/IntProperty#IntProperty(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/IntProperty#set(android.util.IntProperty.T,%20kotlin.Int)(object: T, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!)` Sets the value on `object` which this property represents. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/IntProperty#setValue(android.util.IntProperty.T,%20kotlin.Int)(object: T, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` A type-specific variant of `https://developer.android.com/reference/kotlin/android/util/IntProperty#set(android.util.IntProperty.T,%20kotlin.Int)` that is faster when dealing with fields of type `int`. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/util/Property` |---|---| | `V` | `https://developer.android.com/reference/kotlin/android/util/Property#get(android.util.Property.T)(object: T)` Returns the current value that this property represents on the given `object`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/util/Property#getName()()` Returns the name for this property. <br /> | | `https://developer.android.com/reference/kotlin/java/lang/Class.html#<V>!` | `https://developer.android.com/reference/kotlin/android/util/Property#getType()()` Returns the type for this property. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly()()` Returns true if the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method does not set the value on the target object (in which case the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method should throw a `https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException` exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the `https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String)` factory method may return a Property with name "foo" for an object that has only a `getFoo()` or `isFoo()` method, but no matching `setFoo()` method. <br /> | | `https://developer.android.com/reference/kotlin/android/util/Property<T, V>!` | `https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String)(hostType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!, valueType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<V>!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` This factory method creates and returns a Property given the `class` and `name` parameters, where the `"name"` parameter represents either: - a public `getName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `getName()` - a public `isName()` method on the class which takes no arguments, plus an optional public `setName()` method which takes a value of the same type returned by `isName()` - a public `name` field on the class <br /> If either of the get/is method alternatives is found on the class, but an appropriate `setName()` method is not found, the `Property` will be `https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly()`. Calling the `https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V)` method on such a property is allowed, but will have no effect. If neither the methods nor the field are found on the class a `https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException` exception will be thrown. <br /> | ||

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

A type-specific variant of `https://developer.android.com/reference/kotlin/android/util/IntProperty#set(android.util.IntProperty.T,%20kotlin.Int)` that is faster when dealing with fields of type `int`.
