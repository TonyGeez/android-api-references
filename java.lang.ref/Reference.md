# Reference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Reference

```
abstract class Reference<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ref.Reference](Reference.md) |

| Known Direct Subclasses [PhantomReference](PhantomReference.md), [SoftReference](SoftReference.md), [WeakReference](WeakReference.md) |---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [PhantomReference](PhantomReference.md) | Phantom reference objects, which are enqueued after the collector determines that their referents may otherwise be reclaimed. | | [SoftReference](SoftReference.md) | Soft reference objects, which are cleared at the discretion of the garbage collector in response to memory demand. | | [WeakReference](WeakReference.md) | Weak reference objects, which do not prevent their referents from being made finalizable, finalized, and then reclaimed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract base class for reference objects. This class defines the operations common to all reference objects. Because reference objects are implemented in close cooperation with the garbage collector, this class may not be subclassed directly.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](Reference.md))`()` Clears this reference object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enqueue](Reference.md))`()` Adds this reference object to the queue with which it is registered, if any. |
| openT? | [get](Reference.md))`()` Returns this reference object's referent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnqueued](Reference.md))`()` Tests if this reference object is in its associated queue, if any. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reachabilityFence](Reference.md))`(`ref:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Ensures that the object referenced by the given reference remains [*strongly reachable*](_package.md), regardless of any prior actions of the program that might otherwise cause the object to become unreachable; thus, the referenced object is not reclaimable by garbage collection at least until after the invocation of this method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refersTo](Reference.md))`(`obj:` `T`)` Tests if the referent of this reference object is`obj`. |
| --- | --- |

| Protected methods ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](Reference.md))`()` Throws [CloneNotSupportedException](../java.lang/CloneNotSupportedException.md). |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Clears this reference object. Invoking this method will not cause this object to be enqueued.

This method is invoked only by Java code; when the garbage collector clears references it does so directly, without invoking this method. 

### enqueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enqueue(): Boolean
```

Adds this reference object to the queue with which it is registered, if any.

This method is invoked only by Java code; when the garbage collector enqueues references it does so directly, without invoking this method.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this reference object was successfully enqueued;`false`if it was already enqueued or if it was not registered with a queue when it was created |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(): T?
```

Returns this reference object's referent. If this reference object has been cleared, either by the program or by the garbage collector, then this method returns`null`.

| Return ||
|----|----------------------------------------------------------------------------------------------|
| T? | The object to which this reference refers, or`null`if this reference object has been cleared |

### isEnqueued

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEnqueued(): Boolean
```

**Deprecated:** *This method was never implemented to test if a reference object has been cleared and enqueued as it was previously specified since 1.2. This method could be misused due to the inherent race condition or without an associated`ReferenceQueue`. An application relying on this method to release critical resources could cause serious performance issue. An application should use [ReferenceQueue](ReferenceQueue.md) to reliably determine what reference objects that have been enqueued or`refersTo(null)`to determine if this reference object has been cleared.*

Tests if this reference object is in its associated queue, if any. This method returns`true`only if all of the following conditions are met:

- this reference object was registered with a queue when it was created; and
- the garbage collector has added this reference object to the queue or [enqueue()](Reference.md))is called; and
- this reference object is not yet removed from the queue.

Otherwise, this method returns`false`. This method may return`false`if this reference object has been cleared but not enqueued due to the race condition.

<br />

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if this reference object is in its associated queue (if any). |

### reachabilityFence

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reachabilityFence(ref: Any!): Unit
```

Ensures that the object referenced by the given reference remains [*strongly reachable*](_package.md), regardless of any prior actions of the program that might otherwise cause the object to become unreachable; thus, the referenced object is not reclaimable by garbage collection at least until after the invocation of this method. Invocation of this method does not itself initiate garbage collection or finalization.

This method establishes an ordering for [*strong reachability*](_package.md) with respect to garbage collection. It controls relations that are otherwise only implicit in a program -- the reachability conditions triggering garbage collection. This method is designed for use in uncommon situations of premature finalization where using`synchronized`blocks or methods, or using other synchronization facilities are not possible or do not provide the desired control. This method is applicable only when reclamation may have visible effects, which is possible for objects with finalizers (See [Section 12.6 17 of The Java™ Language Specification](https://docs.oracle.com/javase/specs/jls/se8/html/jls-12.html#jls-12.6)) that are implemented in ways that rely on ordering control for correctness.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `ref` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the reference. If`null`, this method has no effect. |

### refersTo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun refersTo(obj: T): Boolean
```

Tests if the referent of this reference object is`obj`. Using a`null``obj`returns`true`if the reference object has been cleared. Prefer this to a comparison with the result of`get`.

| Parameters ||
|-------|---------------------------------------------------------------|
| `obj` | T:the object to compare with this reference object's referent |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`obj`is the referent of this reference object |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clone(): Any!
```

Throws [CloneNotSupportedException](../java.lang/CloneNotSupportedException.md). A`Reference`cannot be meaningfully cloned. Construct a new`Reference`instead.

| Return ||
|-----------------------------------------------------------------------------|------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | never returns normally |

| Exceptions ||
|----------------------------------------|--------|
| `java.lang.CloneNotSupportedException` | always |
