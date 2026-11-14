# WebTriggerInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebTriggerInput

Kotlin| [Java](WebTriggerInput.md) 
| --- | --- |

```
class WebTriggerInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.WebTriggerInput](WebTriggerInput.md) |

The input data for [IsolatedWorker.onWebTrigger(WebTriggerInput, android.os.OutcomeReceiver)](IsolatedWorker.md)).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebTriggerInput](WebTriggerInput.md))`(`destinationUrl:` ` [Uri](../android.net/Uri.md)`, `appPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Creates a new WebTriggerInput. |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WebTriggerInput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAppPackageName](WebTriggerInput.md))`()` The package name of the app where the trigger event occurred |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getData](WebTriggerInput.md))`()` Additional data returned by the server as part of the web trigger registration to be sent to the [IsolatedService](IsolatedService.md). |
| --- | --- |
| [Uri](../android.net/Uri.md) | [getDestinationUrl](WebTriggerInput.md))`()` The destination URL (landing page) where the trigger event occurred. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WebTriggerInput.md))`()` <br /> |

## Public constructors

### WebTriggerInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebTriggerInput(
    destinationUrl: Uri, 
    appPackageName: String, 
    data: ByteArray)
```

Creates a new WebTriggerInput.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destinationUrl` | [Uri](../android.net/Uri.md):The destination URL (landing page) where the trigger event occurred. This value cannot be`null`. |
| `appPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package name of the app where the trigger event occurred This value cannot be`null`. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):Additional data returned by the server as part of the web trigger registration to be sent to the [IsolatedService](IsolatedService.md). This can be`null`if the server does not need to send data to the service for processing web triggers. |
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

### getAppPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppPackageName(): String
```

The package name of the app where the trigger event occurred

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray
```

Additional data returned by the server as part of the web trigger registration to be sent to the [IsolatedService](IsolatedService.md). This can be`null`if the server does not need to send data to the service for processing web triggers. 

### getDestinationUrl

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDestinationUrl(): Uri
```

The destination URL (landing page) where the trigger event occurred.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](../android.net/Uri.md) | This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
