# java.lang.invoke

# java.lang.invoke

## Interfaces

| [MethodHandleInfo](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandleInfo) | A symbolic reference obtained by cracking a direct method handle into its consitutent symbolic parts. |
| --- | --- |
| [TypeDescriptor](https://developer.android.com/reference/kotlin/java/lang/invoke/TypeDescriptor) | An entity that has a type descriptor. |

## Classes

| [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) | A`CallSite`is a holder for a variable [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle), which is called its`target`. |
| --- | --- |
| [ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite) | A`ConstantCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) whose target is permanent, and can never be changed. |
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle) | A method handle is a typed, directly executable reference to an underlying method, constructor, field, or similar low-level operation, with optional transformations of arguments or return values. |
| [MethodHandles](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandles) | This class consists exclusively of static methods that operate on or return method handles. |
| --- | --- |
| [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType) | A method type represents the arguments and return type accepted and returned by a method handle, or the arguments and return type passed and expected by a method handle caller. |
| [MutableCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite) | A`MutableCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) whose target variable behaves like an ordinary field. |
| [VarHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle) | A VarHandle is a dynamically strongly typed reference to a variable, or to a parametrically-defined family of variables, including static fields, non-static fields, array elements, or components of an off-heap data structure. |
| --- | --- |
| [VolatileCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite) | A`VolatileCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) whose target acts like a volatile variable. |

## Exceptions

| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException) | LambdaConversionException |
| --- | --- |
| [StringConcatException](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException) | StringConcatException is thrown by [StringConcatFactory](https://developer.android.com/reference/kotlin/java/lang/invoke/package-summary#) when linkage invariants are violated. |
| [WrongMethodTypeException](https://developer.android.com/reference/kotlin/java/lang/invoke/WrongMethodTypeException) | Thrown to indicate that code has attempted to call a method handle via the wrong method type. |
