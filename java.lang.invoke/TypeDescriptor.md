# TypeDescriptor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeDescriptor

```
interface TypeDescriptor
```

| [java.lang.invoke.TypeDescriptor](../java/lang/invoke/TypeDescriptor.md) |

| Known Direct Subclasses [TypeDescriptor.OfField](../java/lang/invoke/TypeDescriptor.OfField.md), [TypeDescriptor.OfMethod](../java/lang/invoke/TypeDescriptor.OfMethod.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [TypeDescriptor.OfField](../java/lang/invoke/TypeDescriptor.OfField.md) | An entity that has a field type descriptor. | | [TypeDescriptor.OfMethod](../java/lang/invoke/TypeDescriptor.OfMethod.md) | An entity that has a method type descriptor Method descriptors conforming to JVMS {@jvms 4. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Class](../java/lang/Class.md), [MethodType](../java/lang/invoke/MethodType.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](../java/lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. | | [MethodType](../java/lang/invoke/MethodType.md) | A method type represents the arguments and return type accepted and returned by a method handle, or the arguments and return type passed and expected by a method handle caller. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An entity that has a type descriptor.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OfField](../java/lang/invoke/TypeDescriptor.OfField.md) An entity that has a field type descriptor. |
| abstract | [OfMethod](../java/lang/invoke/TypeDescriptor.OfMethod.md) An entity that has a method type descriptor Method descriptors conforming to JVMS {@jvms 4. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [descriptorString](../java/lang/invoke/TypeDescriptor.md))`()` Returns the descriptor string for this`TypeDescriptor`object. |

## Public methods

### descriptorString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descriptorString(): String!
```

Returns the descriptor string for this`TypeDescriptor`object. If this`TypeDescriptor`object can be described in nominal form, then this method returns a type descriptor as specified in JVMS {@jvms 4.3}. The result descriptor string can be used to produce a`java.lang.constant.ConstantDesc nominal descriptor`. Otherwise, the result string is not a type descriptor. No`java.lang.constant.ConstantDesc nominal descriptor`can be produced from the result string.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the descriptor string for this`TypeDescriptor`object |
