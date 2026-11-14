# InferenceOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InferenceOutput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/InferenceOutput "View this page in Java") 
| --- | --- |

```
class InferenceOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#) |

The result returned by [ModelManager.run](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#run(android.adservices.ondevicepersonalization.InferenceInput,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput.Builder) A builder for [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#) |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getData](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#getData())`()` A byte array that holds input data. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [getDataOutputs](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#getDataOutputs())`()` Note: use [InferenceOutput.getData()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#getData())instead. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#hashCode())`()` <br /> |

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

### getData

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray
```

A byte array that holds input data. The inputs should be in the same order as inputs of the model.

For LiteRT, this field is a serialized Map that is mapped to outputs of runForMultipleInputsOutputs: https://www.tensorflow.org/lite/api_docs/java/org/tensorflow/lite/InterpreterApi#parameters_9

For ExecuTorch model, this field is a serialized EValue array.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getDataOutputs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataOutputs(): MutableMap<Int!, Any!>
```

Note: use [InferenceOutput.getData()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput#getData())instead.

A map mapping output indices to multidimensional arrays of output.

For TFLite, this field is mapped to outputs of runForMultipleInputsOutputs: https://www.tensorflow.org/lite/api_docs/java/org/tensorflow/lite/InterpreterApi#parameters_9

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
