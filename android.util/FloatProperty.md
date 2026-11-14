# FloatProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatProperty

Kotlin| [Java](../android/util/FloatProperty.md) 
| --- | --- |

```
abstract class FloatProperty<T : Any!> : Property<T, Float!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.util.Property](../android/util/Property.md)\<T, [kotlin.Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)\> ||
| | ↳ | [android.util.FloatProperty](../android/util/FloatProperty.md) |

An implementation of [android.util.Property](../android/util/Property.md) to be used specifically with fields of type`float`. This type-specific subclass enables performance benefit by allowing calls to a [setValue()](../android/util/FloatProperty.md))function that takes the primitive`float`type and avoids autoboxing and other overhead associated with the`Float`class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FloatProperty](../android/util/FloatProperty.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/util/FloatProperty.md))`(`object:` `T`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](../android/util/FloatProperty.md))`(`object:` `T`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` A type-specific variant of [set(java.lang.Object,java.lang.Float)](../android/util/FloatProperty.md))that is faster when dealing with fields of type`float`. |

| Inherited functions ||
|---|---|
| From class [Property](../android/util/Property.md) |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V | [get](../android/util/Property.md))`(`object:` `T`)` <br /> Returns the current value that this property represents on the given`object`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/util/Property.md))`()` <br /> Returns the name for this property. <br /> | | [Class](../java/lang/Class.md)<V>! | [getType](../android/util/Property.md))`()` <br /> Returns the type for this property. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../android/util/Property.md))`()` <br /> Returns true if the [set(java.lang.Object,java.lang.Object)](../android/util/Property.md))method does not set the value on the target object (in which case the [set()](../android/util/Property.md))method should throw a [NoSuchPropertyException](../android/util/NoSuchPropertyException.md) exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the [of(java.lang.Class,java.lang.Class,java.lang.String)](../android/util/Property.md))factory method may return a Property with name "foo" for an object that has only a`getFoo()`or`isFoo()`method, but no matching`setFoo()`method. <br /> | | [Property](../android/util/Property.md)<T,` `V>! | [of](../android/util/Property.md))`(`hostType:` ` [Class](../java/lang/Class.md)<T>!`, `valueType:` ` [Class](../java/lang/Class.md)<V>!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> This factory method creates and returns a Property given the`class`and`name`parameters, where the`"name"`parameter represents either: - a public`getName()`method on the class which takes no arguments, plus an optional public`setName()`method which takes a value of the same type returned by`getName()` - a public`isName()`method on the class which takes no arguments, plus an optional public`setName()`method which takes a value of the same type returned by`isName()` - a public`name`field on the class <br /> If either of the get/is method alternatives is found on the class, but an appropriate`setName()`method is not found, the`Property`will be [readOnly](../android/util/Property.md)). Calling the [set(java.lang.Object,java.lang.Object)](../android/util/Property.md))method on such a property is allowed, but will have no effect. If neither the methods nor the field are found on the class a [NoSuchPropertyException](../android/util/NoSuchPropertyException.md) exception will be thrown. <br /> | ||

## Public constructors

### FloatProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FloatProperty(name: String!)
```

## Public methods

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(
    object: T, 
    value: Float!
): Unit
```  

### setValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setValue(
    object: T, 
    value: Float
): Unit
```

A type-specific variant of [set(java.lang.Object,java.lang.Float)](../android/util/FloatProperty.md))that is faster when dealing with fields of type`float`.
