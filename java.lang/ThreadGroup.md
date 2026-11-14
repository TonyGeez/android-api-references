# ThreadGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadGroup

```
open class ThreadGroup : Thread.UncaughtExceptionHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#) |

A thread group represents a set of threads. In addition, a thread group can also include other thread groups. The thread groups form a tree in which every thread group except the initial thread group has a parent.

A thread is allowed to access information about its own thread group, but not to access information about its thread group's parent thread group or any other thread groups.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#ThreadGroup(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new thread group. |
| [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#ThreadGroup(java.lang.ThreadGroup,%20kotlin.String))`(`parent:` ` [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new thread group. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [activeCount](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#activeCount())`()` Returns an estimate of the number of active threads in this thread group and its subgroups. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [activeGroupCount](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#activeGroupCount())`()` Returns an estimate of the number of active groups in this thread group and its subgroups. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowThreadSuspension](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#allowThreadSuspension(kotlin.Boolean))`(`b:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Used by VM to control lowmem implicit suspension. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())`()` Determines if the currently running thread has permission to modify this thread group. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#destroy())`()` Destroys this thread group and all of its subgroups. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array))`(`list:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)!>!`)` Copies into the specified array every active thread in this thread group and its subgroups. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array,%20kotlin.Boolean))`(`list:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)!>!`, `recurse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Copies into the specified array every active thread in this thread group. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array))`(`list:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!>!`)` Copies into the specified array references to every active subgroup in this thread group and its subgroups. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array,%20kotlin.Boolean))`(`list:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!>!`, `recurse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Copies into the specified array references to every active subgroup in this thread group. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxPriority](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#getMaxPriority())`()` Returns the maximum priority of this thread group. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#getName())`()` Returns the name of this thread group. |
| [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)! | [getParent](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#getParent())`()` Returns the parent of this thread group. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [interrupt](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#interrupt())`()` Interrupts all threads in this thread group. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDaemon](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#isDaemon())`()` Tests if this thread group is a daemon thread group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#isDestroyed())`()` Tests if this thread group has been destroyed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [list](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#list())`()` Prints information about this thread group to the standard output. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [parentOf](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#parentOf(java.lang.ThreadGroup))`(`g:` ` [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!`)` Tests if this thread group is either the thread group argument or one of its ancestor thread groups. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#resume())`()` Resumes all threads in this thread group. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDaemon](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#setDaemon(kotlin.Boolean))`(`daemon:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Changes the daemon status of this thread group. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxPriority](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#setMaxPriority(kotlin.Int))`(`pri:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum priority of the group. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#stop())`()` Stops all threads in this thread group. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [suspend](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#suspend())`()` Suspends all threads in this thread group. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#toString())`()` Returns a string representation of this Thread group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [uncaughtException](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#uncaughtException(java.lang.Thread,%20kotlin.Throwable))`(`t:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Called by the Java Virtual Machine when a thread in this thread group stops because of an uncaught exception, and the thread does not have a specific [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler) installed. |
| --- | --- |

## Public constructors

### ThreadGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ThreadGroup(name: String!)
```

Constructs a new thread group. The parent of this new group is the thread group of the currently running thread.

The`checkAccess`method of the parent thread group is called with no arguments; this may result in a security exception.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the new thread group. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group. |

**See Also**

- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### ThreadGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ThreadGroup(
    parent: ThreadGroup!, 
    name: String!)
```

Creates a new thread group. The parent of this new group is the specified thread group.

The`checkAccess`method of the parent thread group is called with no arguments; this may result in a security exception.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `parent` | [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!:the parent thread group. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the new thread group. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the thread group argument is`null`. |
| `java.lang.SecurityException` | if the current thread cannot create a thread in the specified thread group. |

**See Also**

- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())

## Public methods

### activeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun activeCount(): Int
```

Returns an estimate of the number of active threads in this thread group and its subgroups. Recursively iterates over all subgroups in this thread group.

The value returned is only an estimate because the number of threads may change dynamically while this method traverses internal data structures, and might be affected by the presence of certain system threads. This method is intended primarily for debugging and monitoring purposes.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of active threads in this thread group and in any other thread group that has this thread group as an ancestor |

### activeGroupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun activeGroupCount(): Int
```

Returns an estimate of the number of active groups in this thread group and its subgroups. Recursively iterates over all subgroups in this thread group.

The value returned is only an estimate because the number of thread groups may change dynamically while this method traverses internal data structures. This method is intended primarily for debugging and monitoring purposes.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of active thread groups with this thread group as an ancestor |

### allowThreadSuspension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allowThreadSuspension(b: Boolean): Boolean
```

**Deprecated:** *The definition of this call depends on [suspend](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#suspend()), which is deprecated. Further, the behavior of this call was never specified.*

Used by VM to control lowmem implicit suspension.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):boolean to allow or disallow suspension |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true on success |

### checkAccess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkAccess(): Unit
```

Determines if the currently running thread has permission to modify this thread group.

If there is a security manager, its`checkAccess`method is called with this thread group as its argument. This may result in throwing a`SecurityException`.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread group. |

**See Also**

- [java.lang.SecurityManager#checkAccess(java.lang.ThreadGroup)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkAccess(java.lang.ThreadGroup)) 

### destroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun destroy(): Unit
```

Destroys this thread group and all of its subgroups. This thread group must be empty, indicating that all threads that had been in this thread group have since stopped.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.IllegalThreadStateException` | if the thread group is not empty or if the thread group has already been destroyed. |
| `java.lang.SecurityException` | if the current thread cannot modify this thread group. |

**See Also**

- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### enumerate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enumerate(list: Array<Thread!>!): Int
```

Copies into the specified array every active thread in this thread group and its subgroups.

An invocation of this method behaves in exactly the same way as the invocation
[enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array,%20kotlin.Boolean))`(list, true)`

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)!\>!:an array into which to put the list of threads |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of threads put into the array |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [checkAccess](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())determines that the current thread cannot access this thread group |

### enumerate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enumerate(
    list: Array<Thread!>!, 
    recurse: Boolean
): Int
```

Copies into the specified array every active thread in this thread group. If`recurse`is`true`, this method recursively enumerates all subgroups of this thread group and references to every active thread in these subgroups are also included. If the array is too short to hold all the threads, the extra threads are silently ignored.

An application might use the [activeCount](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#activeCount())method to get an estimate of how big the array should be, however*if the array is too short to hold all the threads, the extra threads are silently ignored.* If it is critical to obtain every active thread in this thread group, the caller should verify that the returned int value is strictly less than the length of`list`.

Due to the inherent race condition in this method, it is recommended that the method only be used for debugging and monitoring purposes.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread)!\>!:an array into which to put the list of threads |
| `recurse` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, recursively enumerate all subgroups of this thread group |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of threads put into the array |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [checkAccess](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())determines that the current thread cannot access this thread group |

### enumerate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enumerate(list: Array<ThreadGroup!>!): Int
```

Copies into the specified array references to every active subgroup in this thread group and its subgroups.

An invocation of this method behaves in exactly the same way as the invocation
[enumerate](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#enumerate(kotlin.Array,%20kotlin.Boolean))`(list, true)`

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!\>!:an array into which to put the list of thread groups |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of thread groups put into the array |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [checkAccess](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())determines that the current thread cannot access this thread group |

### enumerate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enumerate(
    list: Array<ThreadGroup!>!, 
    recurse: Boolean
): Int
```

Copies into the specified array references to every active subgroup in this thread group. If`recurse`is`true`, this method recursively enumerates all subgroups of this thread group and references to every active thread group in these subgroups are also included.

An application might use the [activeGroupCount](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#activeGroupCount())method to get an estimate of how big the array should be, however*if the array is too short to hold all the thread groups, the extra thread groups are silently ignored.* If it is critical to obtain every active subgroup in this thread group, the caller should verify that the returned int value is strictly less than the length of`list`.

Due to the inherent race condition in this method, it is recommended that the method only be used for debugging and monitoring purposes.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!\>!:an array into which to put the list of thread groups |
| `recurse` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, recursively enumerate all subgroups |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of thread groups put into the array |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [checkAccess](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())determines that the current thread cannot access this thread group |

### getMaxPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxPriority(): Int
```

Returns the maximum priority of this thread group. Threads that are part of this group cannot have a higher priority than the maximum priority.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum priority that a thread in this thread group can have. |

**See Also**

- [#setMaxPriority](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#setMaxPriority(kotlin.Int)) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns the name of this thread group.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this thread group. |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(): ThreadGroup!
```

Returns the parent of this thread group.

First, if the parent is not`null`, the`checkAccess`method of the parent thread group is called with no arguments; this may result in a security exception.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)! | the parent of this thread group. The top-level thread group is the only thread group whose parent is`null`. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot modify this thread group. |

**See Also**

- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess())
- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission) 

### interrupt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun interrupt(): Unit
```

Interrupts all threads in this thread group.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

This method then calls the`interrupt`method on all the threads in this thread group and in all of its subgroups.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread group or any of the threads in the thread group. |

**See Also**

- [java.lang.Thread#interrupt()](https://developer.android.com/reference/kotlin/java/lang/Thread#interrupt())
- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### isDaemon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDaemon(): Boolean
```

Tests if this thread group is a daemon thread group. A daemon thread group is automatically destroyed when its last thread is stopped or its last thread group is destroyed.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread group is a daemon thread group;`false`otherwise. |

### isDestroyed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDestroyed(): Boolean
```

Tests if this thread group has been destroyed.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this object is destroyed |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun list(): Unit
```

Prints information about this thread group to the standard output. This method is useful only for debugging. 

### parentOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parentOf(g: ThreadGroup!): Boolean
```

Tests if this thread group is either the thread group argument or one of its ancestor thread groups.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `g` | [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#)!:a thread group. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this thread group is the thread group argument or one of its ancestor thread groups;`false`otherwise. |

### resume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun resume(): Unit
```

**Deprecated:** *This method is used solely in conjunction with`Thread.suspend`and`ThreadGroup.suspend`, both of which have been deprecated, as they are inherently deadlock-prone. See java.lang.Thread#suspend for details.*

Resumes all threads in this thread group.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

This method then calls the`resume`method on all the threads in this thread group and in all of its sub groups.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread group or any of the threads in the thread group. |

**See Also**

- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### setDaemon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDaemon(daemon: Boolean): Unit
```

Changes the daemon status of this thread group.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

A daemon thread group is automatically destroyed when its last thread is stopped or its last thread group is destroyed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `daemon` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, marks this thread group as a daemon thread group; otherwise, marks this thread group as normal. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot modify this thread group. |

**See Also**

- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### setMaxPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMaxPriority(pri: Int): Unit
```

Sets the maximum priority of the group. Threads in the thread group that already have a higher priority are not affected.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

If the`pri`argument is less than [Thread.MIN_PRIORITY](https://developer.android.com/reference/kotlin/java/lang/Thread#MIN_PRIORITY:kotlin.Int) or greater than [Thread.MAX_PRIORITY](https://developer.android.com/reference/kotlin/java/lang/Thread#MAX_PRIORITY:kotlin.Int), it is clamped to those values.

Otherwise, the priority of this ThreadGroup object is set to the smaller of the specified`pri`and the maximum permitted priority of the parent of this thread group. (If this thread group is the system thread group, which has no parent, then its maximum priority is simply set to`pri`.) Then this method is called recursively, with`pri`as its argument, for every thread group that belongs to this thread group.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `pri` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new priority of the thread group. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread cannot modify this thread group. |

**See Also**

- [#getMaxPriority](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#getMaxPriority())
- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stop(): Unit
```

**Deprecated:** *This method is inherently unsafe. See [Thread.stop](https://developer.android.com/reference/kotlin/java/lang/Thread#stop())for details.*

Stops all threads in this thread group.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

This method then calls the`stop`method on all the threads in this thread group and in all of its subgroups.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread group or any of the threads in the thread group. |

**See Also**

- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.Thread#stop()](https://developer.android.com/reference/kotlin/java/lang/Thread#stop())
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### suspend

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun suspend(): Unit
```

**Deprecated:** *This method is inherently deadlock-prone. See java.lang.Thread#suspend for details.*

Suspends all threads in this thread group.

First, the`checkAccess`method of this thread group is called with no arguments; this may result in a security exception.

This method then calls the`suspend`method on all the threads in this thread group and in all of its subgroups.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the current thread is not allowed to access this thread group or any of the threads in the thread group. |

**See Also**

- [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException)
- [java.lang.ThreadGroup#checkAccess()](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup#checkAccess()) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this Thread group.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this thread group. |

### uncaughtException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun uncaughtException(
    t: Thread, 
    e: Throwable
): Unit
```

Called by the Java Virtual Machine when a thread in this thread group stops because of an uncaught exception, and the thread does not have a specific [Thread.UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler) installed.

The`uncaughtException`method of`ThreadGroup`does the following:

- If this thread group has a parent thread group, the`uncaughtException`method of that parent is called with the same two arguments.
- Otherwise, this method checks to see if there is a [uncaught exception handler](https://developer.android.com/reference/kotlin/java/lang/Thread#getDefaultUncaughtExceptionHandler())installed, and if so, its`uncaughtException`method is called with the same two arguments.
- Otherwise, this method determines if the`Throwable`argument is an instance of [ThreadDeath](https://developer.android.com/reference/kotlin/java/lang/ThreadDeath). If so, nothing special is done. Otherwise, a message containing the thread's name, as returned from the thread's [getName](https://developer.android.com/reference/kotlin/java/lang/Thread#getName())method, and a stack backtrace, using the`Throwable`'s java.lang.Throwable#printStackTrace method, is printed to the [standard error stream](https://developer.android.com/reference/kotlin/java/lang/System#err:java.io.PrintStream).

Applications can override this method in subclasses of`ThreadGroup`to provide alternative handling of uncaught exceptions.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `t` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread):the thread that is about to exit. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the uncaught exception. |
