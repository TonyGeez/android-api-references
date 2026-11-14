# Pair

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Pair

Kotlin| [Java](../android/util/Pair.md) 
| --- | --- |

```
open class Pair<F : Any!, S : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Pair](../android/util/Pair.md) |

Container to ease passing around a tuple of two objects. This object provides a sensible implementation of equals(), returning true if equals() is true on each of the contained objects.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Pair](../android/util/Pair.md))`(`first:` `F`, `second:` `S`)` Constructor for a Pair. |

| Public methods ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Pair](../android/util/Pair.md)\<A,B\>! | [create](../android/util/Pair.md))`(`a:` `A`, `b:` `B`)` Convenience method for creating an appropriately typed pair. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/util/Pair.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks the two objects for equality by delegating to their respective [Object.equals(Object)](../java/lang/Object.md))methods. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/util/Pair.md))`()` Compute a hash code using the hash codes of the underlying objects |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/util/Pair.md))`()` <br /> |

| Properties ||
|---|--------------------------------------------------------------------------------------------------------------|
| F | [first](../android/util/Pair.md) <br /> |
| S | [second](../android/util/Pair.md) <br /> |

## Public constructors

### Pair

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Pair(
    first: F, 
    second: S)
```

Constructor for a Pair.

| Parameters ||
|----------|---------------------------------|
| `first` | F:the first object in the Pair |
| `second` | S:the second object in the pair |

## Public methods

### create

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <A : Any!, B : Any!> create(
    a: A, 
    b: B
): Pair<A, B>!
```

Convenience method for creating an appropriately typed pair.

| Parameters ||
|-----|---------------------------------|
| `a` | A:the first object in the Pair |
| `b` | B:the second object in the pair |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Pair](../android/util/Pair.md)<A,` `B>! | a Pair that is templatized with the types of a and b |

### equals

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Checks the two objects for equality by delegating to their respective [Object.equals(Object)](../java/lang/Object.md))methods.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the [Pair](../android/util/Pair.md) to which this one is to be checked for equality This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the underlying objects of the Pair are both considered equal |

### hashCode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Compute a hash code using the hash codes of the underlying objects

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hashcode of the Pair |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### first

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val first: F
```  

### second

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val second: S
```
