# ExerciseLap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExerciseLap

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/ExerciseLap "View this page in Java") 

```
class ExerciseLap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.datatypes.ExerciseLap](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#) |

Captures the time of a lap within exercise session. Part of [ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord).

Each record contains the start and end time and optional [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length) of the lap (e.g. pool length while swimming or a track lap while running). There may or may not be direct correlation with [ExerciseSegment](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegment) start and end times, e.g. [ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord) of type running without any segments can be divided as laps of different lengths.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap.Builder) Builder class for [ExerciseLap](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#) |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | [getEndTime](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#getEndTime())`()` <br /> |
| [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length)? | [getLength](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#getLength())`()` <br /> |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | [getStartTime](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#getStartTime())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap#hashCode())`()` <br /> |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | This value cannot be`null`. |

### getLength

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLength(): Length?
```

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [Length](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length)? | This value may be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
