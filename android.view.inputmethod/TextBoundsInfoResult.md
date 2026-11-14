# TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextBoundsInfoResult

Kotlin| [Java](TextBoundsInfoResult.md) 
| --- | --- |

```
class TextBoundsInfoResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.TextBoundsInfoResult](TextBoundsInfoResult.md) |

The object that holds the result of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CANCELLED](TextBoundsInfoResult.md) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the request is cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_FAILED](TextBoundsInfoResult.md) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the request failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_SUCCESS](TextBoundsInfoResult.md) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the editor successfully returns a [TextBoundsInfo](TextBoundsInfo.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_UNSUPPORTED](TextBoundsInfoResult.md) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the editor doesn't implement the method. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextBoundsInfoResult](TextBoundsInfoResult.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a [TextBoundsInfoResult](TextBoundsInfoResult.md) object with no [TextBoundsInfo](TextBoundsInfo.md). |
| [TextBoundsInfoResult](TextBoundsInfoResult.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textBoundsInfo:` ` [TextBoundsInfo](TextBoundsInfo.md)?`)` Create a [TextBoundsInfoResult](TextBoundsInfoResult.md) object. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](TextBoundsInfoResult.md))`()` Return the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call. |
| [TextBoundsInfo](TextBoundsInfo.md)? | [getTextBoundsInfo](TextBoundsInfoResult.md))`()` Return the [TextBoundsInfo](TextBoundsInfo.md) provided by the editor. |

## Constants

### CODE_CANCELLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CANCELLED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the request is cancelled. This happens when the [InputConnection](InputConnection.md) is or becomes invalidated while requesting the [TextBoundsInfo](TextBoundsInfo.md), for example because a new`InputConnection`was started, or due to [InputMethodManager.invalidateInput](InputMethodManager.md)). 

 Value: 3

### CODE_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_FAILED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the request failed. This result code is returned when the editor can't provide a valid [TextBoundsInfo](TextBoundsInfo.md). (e.g. The editor view is not laid out.) 

 Value: 2

### CODE_SUCCESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_SUCCESS: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the editor successfully returns a [TextBoundsInfo](TextBoundsInfo.md). 

 Value: 1

### CODE_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_UNSUPPORTED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))when the editor doesn't implement the method. 

 Value: 0

## Public constructors

### TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextBoundsInfoResult(resultCode: Int)
```

Create a [TextBoundsInfoResult](TextBoundsInfoResult.md) object with no [TextBoundsInfo](TextBoundsInfo.md). The given`resultCode`can't be [CODE_SUCCESS](TextBoundsInfoResult.md).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call. Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](TextBoundsInfoResult.md), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](TextBoundsInfoResult.md) |

### TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextBoundsInfoResult(
    resultCode: Int, 
    textBoundsInfo: TextBoundsInfo?)
```

Create a [TextBoundsInfoResult](TextBoundsInfoResult.md) object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call. Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](TextBoundsInfoResult.md), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](TextBoundsInfoResult.md) |
| `textBoundsInfo` | [TextBoundsInfo](TextBoundsInfo.md)?:the returned [TextBoundsInfo](TextBoundsInfo.md) of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call. It can't be null if the`resultCode`is [CODE_SUCCESS](TextBoundsInfoResult.md). |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the resultCode is [CODE_SUCCESS](TextBoundsInfoResult.md) but the given`textBoundsInfo`is null. |

## Public methods

### getResultCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultCode(): Int
```

Return the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md))call. Its value is one of the [CODE_UNSUPPORTED](TextBoundsInfoResult.md), [CODE_SUCCESS](TextBoundsInfoResult.md), [CODE_FAILED](TextBoundsInfoResult.md) and [CODE_CANCELLED](TextBoundsInfoResult.md).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](TextBoundsInfoResult.md), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](TextBoundsInfoResult.md), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](TextBoundsInfoResult.md) |

### getTextBoundsInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextBoundsInfo(): TextBoundsInfo?
```

Return the [TextBoundsInfo](TextBoundsInfo.md) provided by the editor. It is non-null if the`resultCode`is [CODE_SUCCESS](TextBoundsInfoResult.md). Otherwise, it can be null in the following conditions:

- the editor doesn't support [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](InputConnection.md)).
- the editor doesn't have the text bounds information at the moment. (e.g. the editor view is not laid out yet.)
- the [InputConnection](InputConnection.md) is or become inactive during the request.

<br />
