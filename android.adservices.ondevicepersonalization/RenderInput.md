# RenderInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderInput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/RenderInput "View this page in Java") 
| --- | --- |

```
class RenderInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.RenderInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#) |

The input data for [IsolatedWorker.onRender(RenderInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RenderInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#RenderInput(kotlin.Int,%20kotlin.Int,%20android.adservices.ondevicepersonalization.RenderingConfig))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `renderingConfig:` ` [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig)?`)` Creates a new RenderInput. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#getHeight())`()` The height of the slot. |
| [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig)? | [getRenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#getRenderingConfig())`()` A [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig) within an [ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput) that was returned by [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#getWidth())`()` The width of the slot. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput#hashCode())`()` <br /> |

## Public constructors

### RenderInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RenderInput(
    width: Int, 
    height: Int, 
    renderingConfig: RenderingConfig?)
```

Creates a new RenderInput.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the slot. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the slot. |
| `renderingConfig` | [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig)?:A [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig) within an [ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput) that was returned by [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)). This value may be`null`. |
| --- | --- |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getHeight

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

The height of the slot. 

### getRenderingConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRenderingConfig(): RenderingConfig?
```

A [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig) within an [ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput) that was returned by [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig)? | This value may be`null`. |

### getWidth

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

The width of the slot. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
