# RenderOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderOutput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/RenderOutput "View this page in Java") 
| --- | --- |

```
class RenderOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.RenderOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#) |

The result returned by [IsolatedWorker.onRender(RenderInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput.Builder) A builder for [RenderOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getContent](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getContent())`()` The HTML content to be rendered in a webview. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTemplateId](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateId())`()` A key in the REMOTE_DATA [IsolatedService.getRemoteData(RequestToken)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getRemoteData(android.adservices.ondevicepersonalization.RequestToken))table that points to an [Apache Velocity](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/velocity.apache.org) template. |
| --- | --- |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getTemplateParams](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateParams())`()` The parameters to be populated in the template from [getTemplateId()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateId()). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#hashCode())`()` <br /> |

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

### getContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContent(): String?
```

The HTML content to be rendered in a webview. If this is null, the ODP service generates HTML from the data in [getTemplateId()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateId())and [getTemplateParams()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateParams())as described below. 

### getTemplateId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateId(): String?
```

A key in the REMOTE_DATA [IsolatedService.getRemoteData(RequestToken)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getRemoteData(android.adservices.ondevicepersonalization.RequestToken))table that points to an [Apache Velocity](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/velocity.apache.org) template. This is ignored if [getContent()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getContent())is not null. 

### getTemplateParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateParams(): PersistableBundle
```

The parameters to be populated in the template from [getTemplateId()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getTemplateId()). This is ignored if [getContent()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput#getContent())is not null. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
