# RenderOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderOutput

Kotlin| [Java](RenderOutput.md) 
| --- | --- |

```
class RenderOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.RenderOutput](RenderOutput.md) |

The result returned by [IsolatedWorker.onRender(RenderInput, android.os.OutcomeReceiver)](IsolatedWorker.md)).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/ondevicepersonalization/RenderOutput.Builder.md) A builder for [RenderOutput](RenderOutput.md) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](RenderOutput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getContent](RenderOutput.md))`()` The HTML content to be rendered in a webview. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTemplateId](RenderOutput.md))`()` A key in the REMOTE_DATA [IsolatedService.getRemoteData(RequestToken)](IsolatedService.md))table that points to an [Apache Velocity](../android/adservices/ondevicepersonalization/velocity.apache.org.md) template. |
| --- | --- |
| [PersistableBundle](../android.os/PersistableBundle.md) | [getTemplateParams](RenderOutput.md))`()` The parameters to be populated in the template from [getTemplateId()](RenderOutput.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](RenderOutput.md))`()` <br /> |

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

The HTML content to be rendered in a webview. If this is null, the ODP service generates HTML from the data in [getTemplateId()](RenderOutput.md))and [getTemplateParams()](RenderOutput.md))as described below. 

### getTemplateId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateId(): String?
```

A key in the REMOTE_DATA [IsolatedService.getRemoteData(RequestToken)](IsolatedService.md))table that points to an [Apache Velocity](../android/adservices/ondevicepersonalization/velocity.apache.org.md) template. This is ignored if [getContent()](RenderOutput.md))is not null. 

### getTemplateParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTemplateParams(): PersistableBundle
```

The parameters to be populated in the template from [getTemplateId()](RenderOutput.md)). This is ignored if [getContent()](RenderOutput.md))is not null. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
