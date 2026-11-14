# AtomicStampedReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicStampedReference

```
open class AtomicStampedReference<V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicStampedReference](../java/util/concurrent/atomic/AtomicStampedReference.md) |

An`AtomicStampedReference`maintains an object reference along with an integer "stamp", that can be updated atomically.

Implementation note: This implementation maintains stamped references by creating internal objects representing "boxed" \[reference, integer\] pairs.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicStampedReference](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`initialRef:` `V`, `initialStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`AtomicStampedReference`with the given initial values. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [attemptStamp](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`expectedReference:` `V`, `newStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value of the stamp to the given update value if the current reference is`==`to the expected reference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`expectedReference:` `V`, `newReference:` `V`, `expectedStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value of both the reference and stamp to the given update values if the current reference is`==`to the expected reference and the current stamp is equal to the expected stamp. |
| openV | [get](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`stampHolder:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Returns the current values of both the reference and the stamp. |
| --- | --- |
| openV | [getReference](../java/util/concurrent/atomic/AtomicStampedReference.md))`()` Returns the current value of the reference. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStamp](../java/util/concurrent/atomic/AtomicStampedReference.md))`()` Returns the current value of the stamp. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`newReference:` `V`, `newStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Unconditionally sets the value of both the reference and stamp. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](../java/util/concurrent/atomic/AtomicStampedReference.md))`(`expectedReference:` `V`, `newReference:` `V`, `expectedStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newStamp:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value of both the reference and stamp to the given update values if the current reference is`==`to the expected reference and the current stamp is equal to the expected stamp. |

## Public constructors

### AtomicStampedReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicStampedReference(
    initialRef: V, 
    initialStamp: Int)
```

Creates a new`AtomicStampedReference`with the given initial values.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------|
| `initialRef` | V:the initial reference |
| `initialStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial stamp |

## Public methods

### attemptStamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attemptStamp(
    expectedReference: V, 
    newStamp: Int
): Boolean
```

Atomically sets the value of the stamp to the given update value if the current reference is`==`to the expected reference. Any given invocation of this operation may fail (return`false`) spuriously, but repeated invocation when the current value holds the expected value and no other thread is also attempting to set the value will eventually succeed.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value for the stamp |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareAndSet(
    expectedReference: V, 
    newReference: V, 
    expectedStamp: Int, 
    newStamp: Int
): Boolean
```

Atomically sets the value of both the reference and stamp to the given update values if the current reference is`==`to the expected reference and the current stamp is equal to the expected stamp.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newReference` | V:the new value for the reference |
| `expectedStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value of the stamp |
| --- | --- |
| `newStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value for the stamp |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(stampHolder: IntArray!): V
```

Returns the current values of both the reference and the stamp. Typical usage is`int[1] holder; ref = v.get(holder); `.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stampHolder` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of size of at least one. On return,`stampHolder[0]`will hold the value of the stamp. |

| Return ||
|---|------------------------------------|
| V | the current value of the reference |

### getReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReference(): V
```

Returns the current value of the reference.

| Return ||
|---|------------------------------------|
| V | the current value of the reference |

### getStamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStamp(): Int
```

Returns the current value of the stamp.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current value of the stamp |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    newReference: V, 
    newStamp: Int
): Unit
```

Unconditionally sets the value of both the reference and stamp.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------|
| `newReference` | V:the new value for the reference |
| `newStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value for the stamp |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun weakCompareAndSet(
    expectedReference: V, 
    newReference: V, 
    expectedStamp: Int, 
    newStamp: Int
): Boolean
```

Atomically sets the value of both the reference and stamp to the given update values if the current reference is`==`to the expected reference and the current stamp is equal to the expected stamp. This operation may fail spuriously and does not provide ordering guarantees, so is only rarely an appropriate alternative to`compareAndSet`.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newReference` | V:the new value for the reference |
| `expectedStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value of the stamp |
| --- | --- |
| `newStamp` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value for the stamp |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
