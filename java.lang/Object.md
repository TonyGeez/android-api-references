Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Object

```
open class Object
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Object](Object.md) |

Class `Object` is the root of the class hierarchy. Every class has `Object` as a superclass. All objects, including arrays, implement the methods of this class.

## Summary

| Public constructors ||
|---|---|
| Object Constructs a new object. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Class](Class.md)\<\*\> | getClass Returns the runtime class of this `Object`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notify Wakes up a single thread that is waiting on this object's monitor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notifyAll Wakes up all threads that are waiting on this object's monitor. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | wait Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | wait Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*, or until a certain amount of real time has elapsed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | wait Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*, or until a certain amount of real time has elapsed. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Creates and returns a copy of this object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### Object

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Object()
```

Constructs a new object.

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

**See Also**

- hashCode
- `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`

### getClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClass(): Class<*>
```

Returns the runtime class of this `Object`. The returned `Class` object is the object that is locked by `static synchronized` methods of the represented class.

**The actual result type is `Class<? extends |X|>` where `|X|` is the erasure of the static type of the expression on which `getClass` is called.** For example, no cast is required in this code fragment:
| --- | --- | --- | --- | --- |

`Number n = 0; ` 
`Class<? extends Number> c = n.getClass(); `

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class<*>` | The `Class` object that represents the runtime class of this object. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

**See Also**

- equals
- identityHashCode

### notify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notify(): Unit
```

Wakes up a single thread that is waiting on this object's monitor. If any threads are waiting on this object, one of them is chosen to be awakened. The choice is arbitrary and occurs at the discretion of the implementation. A thread waits on an object's monitor by calling one of the `wait` methods.

The awakened thread will not be able to proceed until the current thread relinquishes the lock on this object. The awakened thread will compete in the usual manner with any other threads that might be actively competing to synchronize on this object; for example, the awakened thread enjoys no reliable privilege or disadvantage in being the next thread to lock this object.

This method should only be called by a thread that is the owner of this object's monitor. A thread becomes the owner of the object's monitor in one of three ways:

- By executing a synchronized instance method of that object.
- By executing the body of a `synchronized` statement that synchronizes on the object.
- For objects of type `Class,` by executing a synchronized static method of that class.

Only one thread at a time can own an object's monitor.

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if the current thread is not the owner of this object's monitor. |

**See Also**

- notifyAll
- wait

### notifyAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyAll(): Unit
```

Wakes up all threads that are waiting on this object's monitor. A thread waits on an object's monitor by calling one of the `wait` methods.

The awakened threads will not be able to proceed until the current thread relinquishes the lock on this object. The awakened threads will compete in the usual manner with any other threads that might be actively competing to synchronize on this object; for example, the awakened threads enjoy no reliable privilege or disadvantage in being the next thread to lock this object.

This method should only be called by a thread that is the owner of this object's monitor. See the `notify` method for a description of the ways in which a thread can become the owner of a monitor.

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if the current thread is not the owner of this object's monitor. |

**See Also**

- notify
- wait

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### wait

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun wait(): Unit
```

Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*.

In all respects, this method behaves as if `wait(0L, 0)` had been called. See the specification of the wait method for details.

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if the current thread is not the owner of the object's monitor |
| `java.lang.InterruptedException` | if any thread interrupted the current thread before or while the current thread was waiting. The *interrupted status* of the current thread is cleared when this exception is thrown. |

**See Also**

- notify
- notifyAll
- wait
- wait

### wait

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun wait(timeoutMillis: Long): Unit
```

Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*, or until a certain amount of real time has elapsed.

In all respects, this method behaves as if `wait(timeoutMillis, 0)` had been called. See the specification of the wait method for details.

| Parameters ||
|---|---|
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait, in milliseconds |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `timeoutMillis` is negative |
| `java.lang.IllegalMonitorStateException` | if the current thread is not the owner of the object's monitor |
| `java.lang.InterruptedException` | if any thread interrupted the current thread before or while the current thread was waiting. The *interrupted status* of the current thread is cleared when this exception is thrown. |
| --- | --- |

**See Also**

- notify
- notifyAll
- wait
- wait

### wait

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun wait(
    timeoutMillis: Long, 
    nanos: Int
): Unit
```

Causes the current thread to wait until it is awakened, typically by being *notified* or *interrupted*, or until a certain amount of real time has elapsed.

The current thread must own this object's monitor lock. See the notify method for a description of the ways in which a thread can become the owner of a monitor lock.

This method causes the current thread (referred to here as T) to place itself in the wait set for this object and then to relinquish any and all synchronization claims on this object. Note that only the locks on this object are relinquished; any other objects on which the current thread may be synchronized remain locked while the thread waits.

Thread T then becomes disabled for thread scheduling purposes and lies dormant until one of the following occurs:

- Some other thread invokes the `notify` method for this object and thread T happens to be arbitrarily chosen as the thread to be awakened.
- Some other thread invokes the `notifyAll` method for this object.
- Some other thread [interrupts](Thread.md)) thread T.
- The specified amount of real time has elapsed, more or less. The amount of real time, in nanoseconds, is given by the expression `1000000 * timeoutMillis + nanos`. If `timeoutMillis` and `nanos` are both zero, then real time is not taken into consideration and the thread waits until awakened by one of the other causes.
- Thread T is awakened spuriously. (See below.)

The thread T is then removed from the wait set for this object and re-enabled for thread scheduling. It competes in the usual manner with other threads for the right to synchronize on the object; once it has regained control of the object, all its synchronization claims on the object are restored to the status quo ante - that is, to the situation as of the time that the `wait` method was invoked. Thread T then returns from the invocation of the `wait` method. Thus, on return from the `wait` method, the synchronization state of the object and of thread `T` is exactly as it was when the `wait` method was invoked.

A thread can wake up without being notified, interrupted, or timing out, a so-called *spurious wakeup*. While this will rarely occur in practice, applications must guard against it by testing for the condition that should have caused the thread to be awakened, and continuing to wait if the condition is not satisfied. See the example below.

For more information on this topic, see section 14.2, "Condition Queues," in Brian Goetz and others' *Java Concurrency in Practice* (Addison-Wesley, 2006) or Item 69 in Joshua Bloch's *Effective Java, Second Edition* (Addison-Wesley, 2008).

If the current thread is [interrupted](Thread.md)) by any thread before or while it is waiting, then an `InterruptedException` is thrown. The *interrupted status* of the current thread is cleared when this exception is thrown. This exception is not thrown until the lock status of this object has been restored as described above.

| Parameters ||
|---|---|
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait, in milliseconds |
| `nanos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): additional time, in nanoseconds, in the range 0-999999 inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `timeoutMillis` is negative, or if the value of `nanos` is out of range |
| `java.lang.IllegalMonitorStateException` | if the current thread is not the owner of the object's monitor |
| `java.lang.InterruptedException` | if any thread interrupted the current thread before or while the current thread was waiting. The *interrupted status* of the current thread is cleared when this exception is thrown. |
| --- | --- |

**See Also**

- notify
- notifyAll
- wait
- wait

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun clone(): Any
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

**See Also**

- Cloneable

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

**See Also**

- WeakReference
- PhantomReference
