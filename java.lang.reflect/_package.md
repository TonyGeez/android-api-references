# java.lang.reflect

# java.lang.reflect

## Interfaces

| [AnnotatedElement](https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement) | Represents an annotated element of the program currently running in this VM. |
| --- | --- |
| [GenericArrayType](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericArrayType) | `GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable. |
| [GenericDeclaration](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericDeclaration) | A common interface for all entities that declare type variables. |
| [InvocationHandler](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationHandler) | `InvocationHandler`is the interface implemented by the*invocation handler*of a proxy instance. |
| --- | --- |
| [Member](https://developer.android.com/reference/kotlin/java/lang/reflect/Member) | Member is an interface that reflects identifying information about a single member (a field or a method) or a constructor. |
| [ParameterizedType](https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType) | ParameterizedType represents a parameterized type such as Collection\<String\>. |
| [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | Type is the common superinterface for all types in the Java programming language. |
| --- | --- |
| [TypeVariable](https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable) | TypeVariable is the common superinterface for type variables of kinds. |
| [WildcardType](https://developer.android.com/reference/kotlin/java/lang/reflect/WildcardType) | WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`. |

## Classes

| [AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject) | The AccessibleObject class is the base class for Field, Method and Constructor objects. |
| --- | --- |
| [Array](https://developer.android.com/reference/kotlin/java/lang/reflect/Array) | The`Array`class provides static methods to dynamically create and access Java arrays. |
| [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor) | `Constructor`provides information about, and access to, a single constructor for a class. |
| [Executable](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable) | A shared superclass for the common functionality of [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method) and [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor). |
| --- | --- |
| [Field](https://developer.android.com/reference/kotlin/java/lang/reflect/Field) | A`Field`provides information about, and dynamic access to, a single field of a class or an interface. |
| [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method) | A`Method`provides information about, and access to, a single method on a class or interface. |
| [Modifier](https://developer.android.com/reference/kotlin/java/lang/reflect/Modifier) | The Modifier class provides`static`methods and constants to decode class and member access modifiers. |
| --- | --- |
| [Parameter](https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter) | Information about method parameters. |
| [Proxy](https://developer.android.com/reference/kotlin/java/lang/reflect/Proxy) | `Proxy`provides static methods for creating dynamic proxy classes and instances, and it is also the superclass of all dynamic proxy classes created by those methods. |
| [RecordComponent](https://developer.android.com/reference/kotlin/java/lang/reflect/RecordComponent) | A`RecordComponent`provides information about, and dynamic access to, a component of a record class. |
| --- | --- |
| [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission) | Legacy security code; do not use. |

## Exceptions

| [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. |
| --- | --- |
| [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException) | InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor. |
| [MalformedParameterizedTypeException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParameterizedTypeException) | Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it. |
| [MalformedParametersException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParametersException) | Thrown when [the](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters())attempts to read method parameters from a class file and determines that one or more parameters are malformed. |
| --- | --- |
| [UndeclaredThrowableException](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException) | Thrown by a method invocation on a proxy instance if its invocation handler's [invoke](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationHandler#invoke(kotlin.Any,%20java.lang.reflect.Method,%20kotlin.Array))method throws a checked exception (a`Throwable`that is not assignable to`RuntimeException`or`Error`) that is not assignable to any of the exception types declared in the`throws`clause of the method that was invoked on the proxy instance and dispatched to the invocation handler. |
