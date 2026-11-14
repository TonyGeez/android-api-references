# StateSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateSet

Kotlin| [Java](../android/util/StateSet.md) 
| --- | --- |

```
open class StateSet
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.StateSet](../android/util/StateSet.md) |

State sets are arrays of positive ints where each element represents the state of a [android.view.View](../android/view/View.md)(e.g. focused, selected, visible, etc.). A [android.view.View](../android/view/View.md) may be in one or more of those states. A state spec is an array of signed ints where each element represents a required (if positive) or an undesired (if negative) [android.view.View](../android/view/View.md) state. Utils dealing with state sets. In theory we could encapsulate the state set and state spec arrays and not have static methods here but there is some concern about performance since these methods are called during view drawing.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dump](../android/util/StateSet.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWildCard](../android/util/StateSet.md))`(`stateSetOrSpec:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Return whether the stateSetOrSpec is matched by all StateSets. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [stateSetMatches](../android/util/StateSet.md))`(`stateSpec:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether the state matches the desired stateSpec. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [stateSetMatches](../android/util/StateSet.md))`(`stateSpec:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `stateSet:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Return whether the stateSet matches the desired stateSpec. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [trimStateSet](../android/util/StateSet.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `newSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [NOTHING](../android/util/StateSet.md) A state set that does not contain any valid states. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [WILD_CARD](../android/util/StateSet.md) A state specification that will be matched by all StateSets. |

## Public methods

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dump(states: IntArray!): String!
```  

### isWildCard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWildCard(stateSetOrSpec: IntArray!): Boolean
```

Return whether the stateSetOrSpec is matched by all StateSets.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------|
| `stateSetOrSpec` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:a state set or state spec. |

### stateSetMatches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stateSetMatches(
    stateSpec: IntArray!, 
    state: Int
): Boolean
```

Return whether the state matches the desired stateSpec.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stateSpec` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of required (if positive) or prohibited (if negative) [android.view.View](../android/view/View.md) states. |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a [android.view.View](../android/view/View.md) state |

### stateSetMatches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stateSetMatches(
    stateSpec: IntArray!, 
    stateSet: IntArray!
): Boolean
```

Return whether the stateSet matches the desired stateSpec.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stateSpec` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of required (if positive) or prohibited (if negative) [android.view.View](../android/view/View.md) states. |
| `stateSet` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of [android.view.View](../android/view/View.md) states |

### trimStateSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun trimStateSet(
    states: IntArray!, 
    newSize: Int
): IntArray!
```

## Properties

### NOTHING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTHING: IntArray!
```

A state set that does not contain any valid states. 

### WILD_CARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WILD_CARD: IntArray!
```

A state specification that will be matched by all StateSets.
