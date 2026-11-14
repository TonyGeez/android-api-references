# AtomicMarkableReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicMarkableReference

```
open class AtomicMarkableReference<V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicMarkableReference](AtomicMarkableReference.md) |

An`AtomicMarkableReference`maintains an object reference along with a mark bit, that can be updated atomically.

Implementation note: This implementation maintains markable references by creating internal objects representing "boxed" \[reference, boolean\] pairs.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicMarkableReference](AtomicMarkableReference.md))`(`initialRef:` `V`, `initialMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new`AtomicMarkableReference`with the given initial values. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [attemptMark](AtomicMarkableReference.md))`(`expectedReference:` `V`, `newMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value of the mark to the given update value if the current reference is`==`to the expected reference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicMarkableReference.md))`(`expectedReference:` `V`, `newReference:` `V`, `expectedMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value of both the reference and mark to the given update values if the current reference is`==`to the expected reference and the current mark is equal to the expected mark. |
| openV | [get](AtomicMarkableReference.md))`(`markHolder:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` Returns the current values of both the reference and the mark. |
| --- | --- |
| openV | [getReference](AtomicMarkableReference.md))`()` Returns the current value of the reference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMarked](AtomicMarkableReference.md))`()` Returns the current value of the mark. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicMarkableReference.md))`(`newReference:` `V`, `newMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Unconditionally sets the value of both the reference and mark. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicMarkableReference.md))`(`expectedReference:` `V`, `newReference:` `V`, `expectedMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newMark:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value of both the reference and mark to the given update values if the current reference is`==`to the expected reference and the current mark is equal to the expected mark. |

## Public constructors

### AtomicMarkableReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicMarkableReference(
    initialRef: V, 
    initialMark: Boolean)
```

Creates a new`AtomicMarkableReference`with the given initial values.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------|
| `initialRef` | V:the initial reference |
| `initialMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the initial mark |

## Public methods

### attemptMark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attemptMark(
    expectedReference: V, 
    newMark: Boolean
): Boolean
```

Atomically sets the value of the mark to the given update value if the current reference is`==`to the expected reference. Any given invocation of this operation may fail (return`false`) spuriously, but repeated invocation when the current value holds the expected value and no other thread is also attempting to set the value will eventually succeed.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value for the mark |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareAndSet(
    expectedReference: V, 
    newReference: V, 
    expectedMark: Boolean, 
    newMark: Boolean
): Boolean
```

Atomically sets the value of both the reference and mark to the given update values if the current reference is`==`to the expected reference and the current mark is equal to the expected mark.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newReference` | V:the new value for the reference |
| `expectedMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value of the mark |
| --- | --- |
| `newMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value for the mark |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(markHolder: BooleanArray!): V
```

Returns the current values of both the reference and the mark. Typical usage is`boolean[1] holder; ref = v.get(holder); `.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `markHolder` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:an array of size of at least one. On return,`markHolder[0]`will hold the value of the mark. |

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

### isMarked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMarked(): Boolean
```

Returns the current value of the mark.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the current value of the mark |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    newReference: V, 
    newMark: Boolean
): Unit
```

Unconditionally sets the value of both the reference and mark.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------|
| `newReference` | V:the new value for the reference |
| `newMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value for the mark |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun weakCompareAndSet(
    expectedReference: V, 
    newReference: V, 
    expectedMark: Boolean, 
    newMark: Boolean
): Boolean
```

Atomically sets the value of both the reference and mark to the given update values if the current reference is`==`to the expected reference and the current mark is equal to the expected mark. This operation may fail spuriously and does not provide ordering guarantees, so is only rarely an appropriate alternative to`compareAndSet`.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------|
| `expectedReference` | V:the expected value of the reference |
| `newReference` | V:the new value for the reference |
| `expectedMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value of the mark |
| --- | --- |
| `newMark` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value for the mark |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
