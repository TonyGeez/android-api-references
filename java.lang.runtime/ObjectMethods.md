# ObjectMethods

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectMethods

```
open class ObjectMethods
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.runtime.ObjectMethods](../java/lang/runtime/ObjectMethods.md) |

Bootstrap methods for state-driven implementations of core methods, including [Object.equals(Object)](../java/lang/Object.md)), [Object.hashCode()](../java/lang/Object.md)), and [Object.toString()](../java/lang/Object.md)). These methods may be used, for example, by Java compiler implementations to implement the bodies of [Object](../java/lang/Object.md) methods for record classes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [bootstrap](../java/lang/runtime/ObjectMethods.md))`(`lookup:` ` [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)`, `methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `type:` ` [TypeDescriptor](../java/lang/invoke/TypeDescriptor.md)`, `recordClass:` ` [Class](../java/lang/Class.md)<*>`, `names:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `vararg` `getters:` ` [MethodHandle](../java/lang/invoke/MethodHandle.md)!`)` Bootstrap method to generate the [Object.equals(Object)](../java/lang/Object.md)), [Object.hashCode()](../java/lang/Object.md)), and [Object.toString()](../java/lang/Object.md))methods, based on a description of the component names and accessor methods, for either`invokedynamic`call sites or dynamic constant pool entries. |

## Public methods

### bootstrap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun bootstrap(
    lookup: MethodHandles.Lookup, 
    methodName: String, 
    type: TypeDescriptor, 
    recordClass: Class<*>, 
    names: String?, 
    vararg getters: MethodHandle!
): Any
```

Bootstrap method to generate the [Object.equals(Object)](../java/lang/Object.md)), [Object.hashCode()](../java/lang/Object.md)), and [Object.toString()](../java/lang/Object.md))methods, based on a description of the component names and accessor methods, for either`invokedynamic`call sites or dynamic constant pool entries. For more detail on the semantics of the generated methods see the specification of [java.lang.Record#equals(Object)](../java/lang/Record.md)), [java.lang.Record#hashCode()](../java/lang/Record.md))and [java.lang.Record#toString()](../java/lang/Record.md)).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookup` | [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md):Every bootstrap method is expected to have a`lookup`which usually represents a lookup context with the accessibility privileges of the caller. This is because`invokedynamic`call sites always provide a`lookup`to the corresponding bootstrap method, but this method just ignores the`lookup`parameter |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the method to generate, which must be one of`"equals"`,`"hashCode"`, or`"toString"` |
| `type` | [TypeDescriptor](../java/lang/invoke/TypeDescriptor.md):a [MethodType](../java/lang/invoke/MethodType.md) corresponding the descriptor type for the method, which must correspond to the descriptor for the corresponding [Object](../java/lang/Object.md) method, if linking an`invokedynamic`call site, or the constant`MethodHandle.class`, if linking a dynamic constant |
| --- | --- |
| `recordClass` | [Class](../java/lang/Class.md)\<\*\>:the record class hosting the record components |
| `names` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the list of component names, joined into a string separated by ";", or the empty string if there are no components. Maybe be null, if the`methodName`is`"equals"`or`"hashCode"`. |
| `getters` | [MethodHandle](../java/lang/invoke/MethodHandle.md)!:method handles for the accessor methods for the components |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a call site if invoked by indy, or a method handle if invoked by a condy |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the bootstrap arguments are invalid or inconsistent |
| `java.lang.Throwable` | if any exception is thrown during call site construction |
