# TrainingExamplesInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrainingExamplesInput

Kotlin| [Java](TrainingExamplesInput.md) 
| --- | --- |

```
class TrainingExamplesInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.TrainingExamplesInput](TrainingExamplesInput.md) |

The input data for [IsolatedWorker.onTrainingExamples](IsolatedWorker.md)).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TrainingExamplesInput](TrainingExamplesInput.md))`(`populationName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `taskName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `resumptionToken:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `collectionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Creates a new TrainingExamplesInput. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](TrainingExamplesInput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCollectionName](TrainingExamplesInput.md))`()` The data collection name to use to create training examples. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPopulationName](TrainingExamplesInput.md))`()` The name of the federated compute population. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getResumptionToken](TrainingExamplesInput.md))`()` Token used to support the resumption of training. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTaskName](TrainingExamplesInput.md))`()` The name of the task within the population. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](TrainingExamplesInput.md))`()` <br /> |
| --- | --- |

## Public constructors

### TrainingExamplesInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrainingExamplesInput(
    populationName: String, 
    taskName: String, 
    resumptionToken: ByteArray?, 
    collectionName: String?)
```

Creates a new TrainingExamplesInput.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `populationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the federated compute population. It should match the population name in [FederatedComputeInput.getPopulationName](FederatedComputeInput.md)). This value cannot be`null`. |
| `taskName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the task within the population. It should match task plan configured at remote federated compute server. One population may have multiple tasks. The task name can be used to uniquely identify the job. This value cannot be`null`. |
| `resumptionToken` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:Token used to support the resumption of training. If client app wants to use resumption token to track what examples are already used in previous federated compute jobs, it need set [TrainingExampleRecord.Builder.setResumptionToken](../android/adservices/ondevicepersonalization/TrainingExampleRecord.Builder.md)), OnDevicePersonalization will store it and pass it here for generating new training examples. This value may be`null`. |
| --- | --- |
| `collectionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The data collection name to use to create training examples. This value may be`null`. |

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

### getCollectionName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCollectionName(): String?
```

The data collection name to use to create training examples.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getPopulationName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPopulationName(): String
```

The name of the federated compute population. It should match the population name in [android.adservices.ondevicepersonalization.FederatedComputeInput#getPopulationName](FederatedComputeInput.md)).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getResumptionToken

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResumptionToken(): ByteArray?
```

Token used to support the resumption of training. If client app wants to use resumption token to track what examples are already used in previous federated compute jobs, it need set [TrainingExampleRecord.Builder.setResumptionToken](../android/adservices/ondevicepersonalization/TrainingExampleRecord.Builder.md)), OnDevicePersonalization will store it and pass it here for generating new training examples.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getTaskName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTaskName(): String
```

The name of the task within the population. It should match task plan configured at remote federated compute server. One population may have multiple tasks. The task name can be used to uniquely identify the job.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
