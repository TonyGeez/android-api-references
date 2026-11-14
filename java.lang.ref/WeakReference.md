# WeakReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WeakReference

```
open class WeakReference<T : Any!> : Reference<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.ref.Reference](https://developer.android.com/reference/kotlin/java/lang/ref/Reference)\<T\> ||
| | ↳ | [java.lang.ref.WeakReference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference#) |

Weak reference objects, which do not prevent their referents from being made finalizable, finalized, and then reclaimed. Weak references are most often used to implement canonicalizing mappings.

Suppose that the garbage collector determines at a certain point in time that an object is [weakly reachable](https://docs.oracle.com/javase/8/docs/api/java/lang/ref/package-summary.html#reachability). At that time it will atomically clear all weak references to that object and all weak references to any other weakly-reachable objects from which that object is reachable through a chain of strong and soft references. At the same time it will declare all of the formerly weakly-reachable objects to be finalizable. At the same time or at some later time it will enqueue those newly-cleared weak references that are registered with reference queues.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WeakReference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference#WeakReference(java.lang.ref.WeakReference.T))`(`referent:` `T`)` Creates a new weak reference that refers to the given object. |
| [WeakReference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference#WeakReference(java.lang.ref.WeakReference.T,%20java.lang.ref.ReferenceQueue))`(`referent:` `T`, `q:` ` [ReferenceQueue](https://developer.android.com/reference/kotlin/java/lang/ref/ReferenceQueue)<in` `T>!`)` Creates a new weak reference that refers to the given object and is registered with the given queue. |

| Inherited functions ||
|---|---|
| From class [Reference](https://developer.android.com/reference/kotlin/java/lang/ref/Reference) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#clear())`()` <br /> Clears this reference object. Invoking this method will not cause this object to be enqueued. This method is invoked only by Java code; when the garbage collector clears references it does so directly, without invoking this method. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#clone())`()` <br /> Throws [CloneNotSupportedException](https://developer.android.com/reference/kotlin/java/lang/CloneNotSupportedException.html#). A`Reference`cannot be meaningfully cloned. Construct a new`Reference`instead. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enqueue](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#enqueue())`()` <br /> Adds this reference object to the queue with which it is registered, if any. This method is invoked only by Java code; when the garbage collector enqueues references it does so directly, without invoking this method. <br /> | | T? | [get](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#get())`()` <br /> Returns this reference object's referent. If this reference object has been cleared, either by the program or by the garbage collector, then this method returns`null`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnqueued](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#isEnqueued())`()` <br /> Tests if this reference object is in its associated queue, if any. This method returns`true`only if all of the following conditions are met: - this reference object was registered with a queue when it was created; and - the garbage collector has added this reference object to the queue or [enqueue()](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#enqueue())is called; and - this reference object is not yet removed from the queue. Otherwise, this method returns`false`. This method may return`false`if this reference object has been cleared but not enqueued due to the race condition. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reachabilityFence](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#reachabilityFence(kotlin.Any))`(`ref:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Ensures that the object referenced by the given reference remains [*strongly reachable*](https://developer.android.com/reference/kotlin/java/lang/ref/package-summary#reachability), regardless of any prior actions of the program that might otherwise cause the object to become unreachable; thus, the referenced object is not reclaimable by garbage collection at least until after the invocation of this method. Invocation of this method does not itself initiate garbage collection or finalization. This method establishes an ordering for [*strong reachability*](https://developer.android.com/reference/kotlin/java/lang/ref/package-summary#reachability) with respect to garbage collection. It controls relations that are otherwise only implicit in a program -- the reachability conditions triggering garbage collection. This method is designed for use in uncommon situations of premature finalization where using`synchronized`blocks or methods, or using other synchronization facilities are not possible or do not provide the desired control. This method is applicable only when reclamation may have visible effects, which is possible for objects with finalizers (See [Section 12.6 17 of The Java™ Language Specification](https://docs.oracle.com/javase/specs/jls/se8/html/jls-12.html#jls-12.6)) that are implemented in ways that rely on ordering control for correctness. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refersTo](https://developer.android.com/reference/kotlin/java/lang/ref/Reference#refersTo(java.lang.ref.Reference.T))`(`obj:` `T`)` <br /> Tests if the referent of this reference object is`obj`. Using a`null``obj`returns`true`if the reference object has been cleared. Prefer this to a comparison with the result of`get`. <br /> | ||

## Public constructors

### WeakReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WeakReference(referent: T)
```

Creates a new weak reference that refers to the given object. The new reference is not registered with any queue.

| Parameters ||
|------------|-----------------------------------------------|
| `referent` | T:object the new weak reference will refer to |

### WeakReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WeakReference(
    referent: T, 
    q: ReferenceQueue<in T>!)
```

Creates a new weak reference that refers to the given object and is registered with the given queue.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `referent` | T:object the new weak reference will refer to |
| `q` | [ReferenceQueue](https://developer.android.com/reference/kotlin/java/lang/ref/ReferenceQueue)\<inT\>!:the queue with which the reference is to be registered, or`null`if registration is not required |
