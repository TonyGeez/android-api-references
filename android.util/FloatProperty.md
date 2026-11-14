# FloatProperty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatProperty

Kotlin| [Java](https://developer.android.com/reference/android/util/FloatProperty "View this page in Java") 
| --- | --- |

```
abstract class FloatProperty<T : Any!> : Property<T, Float!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.util.Property](https://developer.android.com/reference/kotlin/android/util/Property)\<T, [kotlin.Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)\> ||
| | ↳ | [android.util.FloatProperty](https://developer.android.com/reference/kotlin/android/util/FloatProperty#) |

An implementation of [android.util.Property](https://developer.android.com/reference/kotlin/android/util/Property) to be used specifically with fields of type`float`. This type-specific subclass enables performance benefit by allowing calls to a [setValue()](https://developer.android.com/reference/kotlin/android/util/FloatProperty#setValue(android.util.FloatProperty.T,%20kotlin.Float))function that takes the primitive`float`type and avoids autoboxing and other overhead associated with the`Float`class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FloatProperty](https://developer.android.com/reference/kotlin/android/util/FloatProperty#FloatProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/util/FloatProperty#set(android.util.FloatProperty.T,%20kotlin.Float))`(`object:` `T`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/util/FloatProperty#setValue(android.util.FloatProperty.T,%20kotlin.Float))`(`object:` `T`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` A type-specific variant of [set(java.lang.Object,java.lang.Float)](https://developer.android.com/reference/kotlin/android/util/FloatProperty#set(android.util.FloatProperty.T,%20kotlin.Float))that is faster when dealing with fields of type`float`. |

| Inherited functions ||
|---|---|
| From class [Property](https://developer.android.com/reference/kotlin/android/util/Property) |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V | [get](https://developer.android.com/reference/kotlin/android/util/Property#get(android.util.Property.T))`(`object:` `T`)` <br /> Returns the current value that this property represents on the given`object`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/util/Property#getName())`()` <br /> Returns the name for this property. <br /> | | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>! | [getType](https://developer.android.com/reference/kotlin/android/util/Property#getType())`()` <br /> Returns the type for this property. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly())`()` <br /> Returns true if the [set(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V))method does not set the value on the target object (in which case the [set()](https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V))method should throw a [NoSuchPropertyException](https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException) exception). This may happen if the Property wraps functionality that allows querying the underlying value but not setting it. For example, the [of(java.lang.Class,java.lang.Class,java.lang.String)](https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String))factory method may return a Property with name "foo" for an object that has only a`getFoo()`or`isFoo()`method, but no matching`setFoo()`method. <br /> | | [Property](https://developer.android.com/reference/kotlin/android/util/Property)<T,` `V>! | [of](https://developer.android.com/reference/kotlin/android/util/Property#of(java.lang.Class,%20java.lang.Class,%20kotlin.String))`(`hostType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `valueType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> This factory method creates and returns a Property given the`class`and`name`parameters, where the`"name"`parameter represents either: - a public`getName()`method on the class which takes no arguments, plus an optional public`setName()`method which takes a value of the same type returned by`getName()` - a public`isName()`method on the class which takes no arguments, plus an optional public`setName()`method which takes a value of the same type returned by`isName()` - a public`name`field on the class <br /> If either of the get/is method alternatives is found on the class, but an appropriate`setName()`method is not found, the`Property`will be [readOnly](https://developer.android.com/reference/kotlin/android/util/Property#isReadOnly()). Calling the [set(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V))method on such a property is allowed, but will have no effect. If neither the methods nor the field are found on the class a [NoSuchPropertyException](https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException) exception will be thrown. <br /> | ||

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

A type-specific variant of [set(java.lang.Object,java.lang.Float)](https://developer.android.com/reference/kotlin/android/util/FloatProperty#set(android.util.FloatProperty.T,%20kotlin.Float))that is faster when dealing with fields of type`float`.
