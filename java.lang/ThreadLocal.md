# ThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadLocal

```
open class ThreadLocal<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ThreadLocal](../java/lang/ThreadLocal.md) |

| Known Direct Subclasses [InheritableThreadLocal](../java/lang/InheritableThreadLocal.md) |-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InheritableThreadLocal](../java/lang/InheritableThreadLocal.md) | This class extends`ThreadLocal`to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. | |
| --- | --- | --- | --- | --- | --- | --- |

This class provides thread-local variables. These variables differ from their normal counterparts in that each thread that accesses one (via its`get`or`set`method) has its own, independently initialized copy of the variable.`ThreadLocal`instances are typically private static fields in classes that wish to associate state with a thread (e.g., a user ID or Transaction ID).

For example, the class below generates unique identifiers local to each thread. A thread's id is assigned the first time it invokes`ThreadId.get()`and remains unchanged on subsequent calls. 

```kotlin
import java.util.concurrent.atomic.AtomicInteger;
 
  public class ThreadId {
      // Atomic integer containing the next thread ID to be assigned
      private static final AtomicInteger nextId = new AtomicInteger(0);
 
      // Thread local variable containing each thread's ID
      private static final ThreadLocal<Integer> threadId =
          new ThreadLocal<Integer>() {
              @Override protected Integer initialValue() {
                  return nextId.getAndIncrement();
          }
      };
 
      // Returns the current thread's unique ID, assigning it if necessary
      public static int get() {
          return threadId.get();
      }
  }
  
```

Each thread holds an implicit reference to its copy of a thread-local variable as long as the thread is alive and the`ThreadLocal`instance is accessible; after a thread goes away, all of its copies of thread-local instances are subject to garbage collection (unless other references to these copies exist).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [ThreadLocal](../java/lang/ThreadLocal.md))`()` Creates a thread local variable. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT? | [get](../java/lang/ThreadLocal.md))`()` Returns the value in the current thread's copy of this thread-local variable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](../java/lang/ThreadLocal.md))`()` Removes the current thread's value for this thread-local variable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../java/lang/ThreadLocal.md))`(`value:` `T`)` Sets the current thread's copy of this thread-local variable to the specified value. |
| --- | --- |
| openstatic [ThreadLocal](../java/lang/ThreadLocal.md)\<S\> | [withInitial](../java/lang/ThreadLocal.md))`(`supplier:` ` [Supplier](../java/util/function/Supplier.md)<out` `S>`)` Creates a thread local variable. |

| Protected methods ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT? | [initialValue](../java/lang/ThreadLocal.md))`()` Returns the current thread's "initial value" for this thread-local variable. |

## Public constructors

### ThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ThreadLocal()
```

Creates a thread local variable. 
**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#withInitial(java.util.function.Supplier)>

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(): T?
```

Returns the value in the current thread's copy of this thread-local variable. If the variable has no value for the current thread, it is first initialized to the value returned by an invocation of the [initialValue](../java/lang/ThreadLocal.md))method.

| Return ||
|----|-------------------------------------------------|
| T? | the current thread's value of this thread-local |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): Unit
```

Removes the current thread's value for this thread-local variable. If this thread-local variable is subsequently [read](../java/lang/ThreadLocal.md))by the current thread, its value will be reinitialized by invoking its [initialValue](../java/lang/ThreadLocal.md))method, unless its value is [set](../java/lang/ThreadLocal.md))by the current thread in the interim. This may result in multiple invocations of the`initialValue`method in the current thread. 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(value: T): Unit
```

Sets the current thread's copy of this thread-local variable to the specified value. Most subclasses will have no need to override this method, relying solely on the [initialValue](../java/lang/ThreadLocal.md))method to set the values of thread-locals.

| Parameters ||
|---------|-----------------------------------------------------------------------------|
| `value` | T:the value to be stored in the current thread's copy of this thread-local. |

### withInitial

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <S : Any!> withInitial(supplier: Supplier<out S>): ThreadLocal<S>
```

Creates a thread local variable. The initial value of the variable is determined by invoking the`get`method on the`Supplier`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<S>` | the type of the thread local's value |
| `supplier` | [Supplier](../java/util/function/Supplier.md)\<outS\>:the supplier to be used to determine the initial value |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ThreadLocal](../java/lang/ThreadLocal.md)<S> | a new thread local variable |

| Exceptions ||
|----------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if the specified supplier is null |

## Protected methods

### initialValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun initialValue(): T?
```

Returns the current thread's "initial value" for this thread-local variable. This method will be invoked the first time a thread accesses the variable with the [get](../java/lang/ThreadLocal.md))method, unless the thread previously invoked the [set](../java/lang/ThreadLocal.md))method, in which case the`initialValue`method will not be invoked for the thread. Normally, this method is invoked at most once per thread, but it may be invoked again in case of subsequent invocations of [remove](../java/lang/ThreadLocal.md))followed by [get](../java/lang/ThreadLocal.md)).

| Return ||
|----|-----------------------------------------|
| T? | the initial value for this thread-local |

**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#withInitial(java.util.function.Supplier)>
