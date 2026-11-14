# java.lang.invoke

# java.lang.invoke

## Interfaces

| [MethodHandleInfo](MethodHandleInfo.md) | A symbolic reference obtained by cracking a direct method handle into its consitutent symbolic parts. |
| --- | --- |
| [TypeDescriptor](TypeDescriptor.md) | An entity that has a type descriptor. |

## Classes

| [CallSite](CallSite.md) | A`CallSite`is a holder for a variable [MethodHandle](MethodHandle.md), which is called its`target`. |
| --- | --- |
| [ConstantCallSite](ConstantCallSite.md) | A`ConstantCallSite`is a [CallSite](CallSite.md) whose target is permanent, and can never be changed. |
| [MethodHandle](MethodHandle.md) | A method handle is a typed, directly executable reference to an underlying method, constructor, field, or similar low-level operation, with optional transformations of arguments or return values. |
| [MethodHandles](MethodHandles.md) | This class consists exclusively of static methods that operate on or return method handles. |
| --- | --- |
| [MethodType](MethodType.md) | A method type represents the arguments and return type accepted and returned by a method handle, or the arguments and return type passed and expected by a method handle caller. |
| [MutableCallSite](MutableCallSite.md) | A`MutableCallSite`is a [CallSite](CallSite.md) whose target variable behaves like an ordinary field. |
| [VarHandle](VarHandle.md) | A VarHandle is a dynamically strongly typed reference to a variable, or to a parametrically-defined family of variables, including static fields, non-static fields, array elements, or components of an off-heap data structure. |
| --- | --- |
| [VolatileCallSite](VolatileCallSite.md) | A`VolatileCallSite`is a [CallSite](CallSite.md) whose target acts like a volatile variable. |

## Exceptions

| [LambdaConversionException](LambdaConversionException.md) | LambdaConversionException |
| --- | --- |
| [StringConcatException](StringConcatException.md) | StringConcatException is thrown by [StringConcatFactory](_package.md) when linkage invariants are violated. |
| [WrongMethodTypeException](WrongMethodTypeException.md) | Thrown to indicate that code has attempted to call a method handle via the wrong method type. |
