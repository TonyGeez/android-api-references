# InheritableThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InheritableThreadLocal

```
open class InheritableThreadLocal<T : Any!> : ThreadLocal<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.ThreadLocal](ThreadLocal.md)\<T\> ||
| | ↳ | [java.lang.InheritableThreadLocal](InheritableThreadLocal.md) |

This class extends `ThreadLocal` to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. Normally the child's values will be identical to the parent's; however, the child's value can be made an arbitrary function of the parent's by overriding the `childValue` method in this class.

Inheritable thread-local variables are used in preference to ordinary thread-local variables when the per-thread-attribute being maintained in the variable (e.g., User ID, Transaction ID) must be automatically transmitted to any child threads that are created.

Note: During the creation of a new [thread](Thread.md)), it is possible to *opt out* of receiving initial values for inheritable thread-local variables.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InheritableThreadLocal](InheritableThreadLocal.md))`()` Creates an inheritable thread local variable. |

| Protected methods ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open T | [childValue](InheritableThreadLocal.md))`(`parentValue:` `T`)` Computes the child's initial value for this inheritable thread-local variable as a function of the parent's value at the time the child thread is created. |

| Inherited functions ||
|---|---|
| From class [ThreadLocal](ThreadLocal.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T? | [get](ThreadLocal.md))`()` Returns the value in the current thread's copy of this thread-local variable. If the variable has no value for the current thread, it is first initialized to the value returned by an invocation of the [initialValue](ThreadLocal.md)) method. <br /> | | T? | [initialValue](ThreadLocal.md))`()` Returns the current thread's "initial value" for this thread-local variable. This method will be invoked the first time a thread accesses the variable with the [get](ThreadLocal.md)) method, unless the thread previously invoked the [set](ThreadLocal.md)) method, in which case the `initialValue` method will not be invoked for the thread. Normally, this method is invoked at most once per thread, but it may be invoked again in case of subsequent invocations of [remove](ThreadLocal.md)) followed by [get](ThreadLocal.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](ThreadLocal.md))`()` Removes the current thread's value for this thread-local variable. If this thread-local variable is subsequently [read](ThreadLocal.md)) by the current thread, its value will be reinitialized by invoking its [initialValue](ThreadLocal.md)) method, unless its value is [set](ThreadLocal.md)) by the current thread in the interim. This may result in multiple invocations of the `initialValue` method in the current thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](ThreadLocal.md))`(`value:` `T`)` Sets the current thread's copy of this thread-local variable to the specified value. Most subclasses will have no need to override this method, relying solely on the [initialValue](ThreadLocal.md)) method to set the values of thread-locals. <br /> | | [ThreadLocal](ThreadLocal.md)<S> | [withInitial](ThreadLocal.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` `S>`)` Creates a thread local variable. The initial value of the variable is determined by invoking the `get` method on the `Supplier`. <br /> | ||

## Public constructors

### InheritableThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InheritableThreadLocal()
```

Creates an inheritable thread local variable.

## Protected methods

### childValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun childValue(parentValue: T): T
```

Computes the child's initial value for this inheritable thread-local variable as a function of the parent's value at the time the child thread is created. This method is called from within the parent thread before the child is started.

This method merely returns its input argument, and should be overridden if a different behavior is desired.

| Parameters ||
|---------------|------------------------------|
| `parentValue` | T: the parent thread's value |

| Return ||
|---|----------------------------------|
| T | the child thread's initial value |
