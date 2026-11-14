# ThreadLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadLocal

```
open class ThreadLocal<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#) |

| Known Direct Subclasses [InheritableThreadLocal](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal) |-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InheritableThreadLocal](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal) | This class extends`ThreadLocal`to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. | |
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
| [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#ThreadLocal())`()` Creates a thread local variable. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT? | [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get())`()` Returns the value in the current thread's copy of this thread-local variable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#remove())`()` Removes the current thread's value for this thread-local variable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T))`(`value:` `T`)` Sets the current thread's copy of this thread-local variable to the specified value. |
| --- | --- |
| openstatic [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#)\<S\> | [withInitial](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#withInitial(java.util.function.Supplier))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` `S>`)` Creates a thread local variable. |

| Protected methods ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT? | [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue())`()` Returns the current thread's "initial value" for this thread-local variable. |

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

Returns the value in the current thread's copy of this thread-local variable. If the variable has no value for the current thread, it is first initialized to the value returned by an invocation of the [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue())method.

| Return ||
|----|-------------------------------------------------|
| T? | the current thread's value of this thread-local |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): Unit
```

Removes the current thread's value for this thread-local variable. If this thread-local variable is subsequently [read](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get())by the current thread, its value will be reinitialized by invoking its [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue())method, unless its value is [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T))by the current thread in the interim. This may result in multiple invocations of the`initialValue`method in the current thread. 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(value: T): Unit
```

Sets the current thread's copy of this thread-local variable to the specified value. Most subclasses will have no need to override this method, relying solely on the [initialValue](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#initialValue())method to set the values of thread-locals.

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
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<outS\>:the supplier to be used to determine the initial value |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#)<S> | a new thread local variable |

| Exceptions ||
|----------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if the specified supplier is null |

## Protected methods

### initialValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun initialValue(): T?
```

Returns the current thread's "initial value" for this thread-local variable. This method will be invoked the first time a thread accesses the variable with the [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get())method, unless the thread previously invoked the [set](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#set(java.lang.ThreadLocal.T))method, in which case the`initialValue`method will not be invoked for the thread. Normally, this method is invoked at most once per thread, but it may be invoked again in case of subsequent invocations of [remove](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#remove())followed by [get](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#get()).

| Return ||
|----|-----------------------------------------|
| T? | the initial value for this thread-local |

**See Also**

- <https://developer.android.com/reference/kotlin/java/lang/ThreadLocal#withInitial(java.util.function.Supplier)>
