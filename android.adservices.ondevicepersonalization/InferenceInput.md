# InferenceInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InferenceInput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/InferenceInput "View this page in Java") 

```
class InferenceInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.ondevicepersonalization.InferenceInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#) |

Contains all the information needed for a run of model inference. The input of [android.adservices.ondevicepersonalization.ModelManager#run](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#run(android.adservices.ondevicepersonalization.InferenceInput,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput.Builder) A builder for [InferenceInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#) |
| | [Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput.Params) <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBatchSize](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getBatchSize())`()` The number of input examples. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getData](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getData())`()` A byte array that holds input data. |
| [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput) | [getExpectedOutputStructure](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getExpectedOutputStructure())`()` The empty InferenceOutput representing the expected output structure. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [getInputData](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getInputData())`()` Note: use [InferenceInput.getData()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getData())instead. |
| [InferenceInput.Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput.Params) | [getParams](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getParams())`()` The configuration that controls runtime interpreter behavior. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#hashCode())`()` <br /> |

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

### getBatchSize

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBatchSize(): Int
```

The number of input examples. Adopter can set this field to run batching inference. The batch size is 1 by default. The batch size should match the input data size. 

### getData

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray
```

A byte array that holds input data. The inputs should be in the same order as inputs of the model.

For LiteRT, this field is mapped to inputs of runForMultipleInputsOutputs: https://www.tensorflow.org/lite/api_docs/java/org/tensorflow/lite/InterpreterApi#parameters_9 

```kotlin
<code>String[] input0 = {"foo", "bar"}; // string tensor shape is [2].
  int[] input1 = new int[]{3, 2, 1}; // int tensor shape is [3].
  Object[] inputData = {input0, input1, ...};
  byte[] data = serializeObject(inputData);
  </code>
```

For Executorch model, this field is a serialized EValue array.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getExpectedOutputStructure

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExpectedOutputStructure(): InferenceOutput
```

The empty InferenceOutput representing the expected output structure. For LiteRT, the inference code will verify whether this expected output structure matches model output signature.

If a model produce string tensors: 

```kotlin
<code>String[] output = new String[3][2];  // Output tensor shape is [3, 2].
  HashMap&lt;Integer, Object&gt; outputs = new HashMap&lt;&gt;();
  outputs.put(0, output);
  expectedOutputStructure = new InferenceOutput.Builder().setDataOutputs(outputs).build();
  </code>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [InferenceOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceOutput) | This value cannot be`null`. |

### getInputData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputData(): Array<Any!>
```

Note: use [InferenceInput.getData()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput#getData())instead.

An array of input data. The inputs should be in the same order as inputs of the model.

For example, if a model takes multiple inputs: 

```kotlin
<code>String[] input0 = {"foo", "bar"}; // string tensor shape is [2].
  int[] input1 = new int[]{3, 2, 1}; // int tensor shape is [3].
  Object[] inputData = {input0, input1, ...};
  </code>
```
For LiteRT, this field is mapped to inputs of runForMultipleInputsOutputs: https://www.tensorflow.org/lite/api_docs/java/org/tensorflow/lite/InterpreterApi#parameters_9

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | This value cannot be`null`. |

### getParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParams(): InferenceInput.Params
```

The configuration that controls runtime interpreter behavior.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [InferenceInput.Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/InferenceInput.Params) | This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
