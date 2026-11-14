# java.lang.reflect

# java.lang.reflect

## Interfaces

| [AnnotatedElement](../java/lang/reflect/AnnotatedElement.md) | Represents an annotated element of the program currently running in this VM. |
| --- | --- |
| [GenericArrayType](../java/lang/reflect/GenericArrayType.md) | `GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable. |
| [GenericDeclaration](../java/lang/reflect/GenericDeclaration.md) | A common interface for all entities that declare type variables. |
| [InvocationHandler](../java/lang/reflect/InvocationHandler.md) | `InvocationHandler`is the interface implemented by the*invocation handler*of a proxy instance. |
| --- | --- |
| [Member](../java/lang/reflect/Member.md) | Member is an interface that reflects identifying information about a single member (a field or a method) or a constructor. |
| [ParameterizedType](../java/lang/reflect/ParameterizedType.md) | ParameterizedType represents a parameterized type such as Collection\<String\>. |
| [Type](../java/lang/reflect/Type.md) | Type is the common superinterface for all types in the Java programming language. |
| --- | --- |
| [TypeVariable](../java/lang/reflect/TypeVariable.md) | TypeVariable is the common superinterface for type variables of kinds. |
| [WildcardType](../java/lang/reflect/WildcardType.md) | WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`. |

## Classes

| [AccessibleObject](../java/lang/reflect/AccessibleObject.md) | The AccessibleObject class is the base class for Field, Method and Constructor objects. |
| --- | --- |
| [Array](../java/lang/reflect/Array.md) | The`Array`class provides static methods to dynamically create and access Java arrays. |
| [Constructor](../java/lang/reflect/Constructor.md) | `Constructor`provides information about, and access to, a single constructor for a class. |
| [Executable](../java/lang/reflect/Executable.md) | A shared superclass for the common functionality of [Method](../java/lang/reflect/Method.md) and [Constructor](../java/lang/reflect/Constructor.md). |
| --- | --- |
| [Field](../java/lang/reflect/Field.md) | A`Field`provides information about, and dynamic access to, a single field of a class or an interface. |
| [Method](../java/lang/reflect/Method.md) | A`Method`provides information about, and access to, a single method on a class or interface. |
| [Modifier](../java/lang/reflect/Modifier.md) | The Modifier class provides`static`methods and constants to decode class and member access modifiers. |
| --- | --- |
| [Parameter](../java/lang/reflect/Parameter.md) | Information about method parameters. |
| [Proxy](../java/lang/reflect/Proxy.md) | `Proxy`provides static methods for creating dynamic proxy classes and instances, and it is also the superclass of all dynamic proxy classes created by those methods. |
| [RecordComponent](../java/lang/reflect/RecordComponent.md) | A`RecordComponent`provides information about, and dynamic access to, a component of a record class. |
| --- | --- |
| [ReflectPermission](../java/lang/reflect/ReflectPermission.md) | Legacy security code; do not use. |

## Exceptions

| [GenericSignatureFormatError](../java/lang/reflect/GenericSignatureFormatError.md) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. |
| --- | --- |
| [InvocationTargetException](../java/lang/reflect/InvocationTargetException.md) | InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor. |
| [MalformedParameterizedTypeException](../java/lang/reflect/MalformedParameterizedTypeException.md) | Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it. |
| [MalformedParametersException](../java/lang/reflect/MalformedParametersException.md) | Thrown when [the](../java/lang/reflect/Executable.md))attempts to read method parameters from a class file and determines that one or more parameters are malformed. |
| --- | --- |
| [UndeclaredThrowableException](../java/lang/reflect/UndeclaredThrowableException.md) | Thrown by a method invocation on a proxy instance if its invocation handler's [invoke](../java/lang/reflect/InvocationHandler.md))method throws a checked exception (a`Throwable`that is not assignable to`RuntimeException`or`Error`) that is not assignable to any of the exception types declared in the`throws`clause of the method that was invoked on the proxy instance and dispatched to the invocation handler. |
