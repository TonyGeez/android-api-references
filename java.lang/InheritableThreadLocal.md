# InheritableThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InheritableThreadLocal

```
open class InheritableThreadLocal<T : Any!> : ThreadLocal<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.lang.ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal)\<T\> ||
| | ↳ | [java.lang.InheritableThreadLocal](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal#) |

This class extends `ThreadLocal` to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. Normally the child's values will be identical to the parent's; however, the child's value can be made an arbitrary function of the parent's by overriding the `childValue` method in this class.

Inheritable thread-local variables are used in preference to ordinary thread-local variables when the per-thread-attribute being maintained in the variable (e.g., User ID, Transaction ID) must be automatically transmitted to any child threads that are created.

Note: During the creation of a new [thread](https://developer.android.com/reference/kotlin/java/lang/Thread#Thread(java.lang.ThreadGroup,%20java.lang.Runnable,%20kotlin.String,%20kotlin.Long,%20kotlin.Boolean)), it is possible to *opt out* of receiving initial values for inheritable thread-local variables.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InheritableThreadLocal](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal#InheritableThreadLocal())`()` Creates an inheritable thread local variable. |

| Protected methods ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open T | [childValue](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal#childValue(java.lang.InheritableThreadLocal.T))`(`parentValue:` `T`)` Computes the child's initial value for this inheritable thread-local variable as a function of the parent's value at the time the child thread is created. |

| Inherited functions ||
|---|---|
| From class [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T? | [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get())`()` Returns the value in the current thread's copy of this thread-local variable. If the variable has no value for the current thread, it is first initialized to the value returned by an invocation of the [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue()) method. <br /> | | T? | [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue())`()` Returns the current thread's "initial value" for this thread-local variable. This method will be invoked the first time a thread accesses the variable with the [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get()) method, unless the thread previously invoked the [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T)) method, in which case the `initialValue` method will not be invoked for the thread. Normally, this method is invoked at most once per thread, but it may be invoked again in case of subsequent invocations of [remove](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#remove()) followed by [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#remove())`()` Removes the current thread's value for this thread-local variable. If this thread-local variable is subsequently [read](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get()) by the current thread, its value will be reinitialized by invoking its [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue()) method, unless its value is [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T)) by the current thread in the interim. This may result in multiple invocations of the `initialValue` method in the current thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T))`(`value:` `T`)` Sets the current thread's copy of this thread-local variable to the specified value. Most subclasses will have no need to override this method, relying solely on the [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue()) method to set the values of thread-locals. <br /> | | [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal)<S> | [withInitial](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#withInitial(java.util.function.Supplier))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` `S>`)` Creates a thread local variable. The initial value of the variable is determined by invoking the `get` method on the `Supplier`. <br /> | ||

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
