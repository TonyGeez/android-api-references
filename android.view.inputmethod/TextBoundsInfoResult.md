# TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextBoundsInfoResult

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/TextBoundsInfoResult "View this page in Java") 
| --- | --- |

```
class TextBoundsInfoResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#) |

The object that holds the result of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CANCELLED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_CANCELLED:kotlin.Int) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the request is cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_FAILED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_FAILED:kotlin.Int) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the request failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the editor successfully returns a [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_UNSUPPORTED:kotlin.Int) Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the editor doesn't implement the method. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#TextBoundsInfoResult(kotlin.Int))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#) object with no [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo). |
| [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#TextBoundsInfoResult(kotlin.Int,%20android.view.inputmethod.TextBoundsInfo))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `textBoundsInfo:` ` [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo)?`)` Create a [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#) object. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#getResultCode())`()` Return the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call. |
| [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo)? | [getTextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#getTextBoundsInfo())`()` Return the [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo) provided by the editor. |

## Constants

### CODE_CANCELLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CANCELLED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the request is cancelled. This happens when the [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection) is or becomes invalidated while requesting the [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo), for example because a new`InputConnection`was started, or due to [InputMethodManager.invalidateInput](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#invalidateInput(android.view.View)). 

 Value: 3

### CODE_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_FAILED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the request failed. This result code is returned when the editor can't provide a valid [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo). (e.g. The editor view is not laid out.) 

 Value: 2

### CODE_SUCCESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_SUCCESS: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the editor successfully returns a [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo). 

 Value: 1

### CODE_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_UNSUPPORTED: Int
```

Result for [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))when the editor doesn't implement the method. 

 Value: 0

## Public constructors

### TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextBoundsInfoResult(resultCode: Int)
```

Create a [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#) object with no [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo). The given`resultCode`can't be [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call. Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_UNSUPPORTED:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_FAILED:kotlin.Int), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_CANCELLED:kotlin.Int) |

### TextBoundsInfoResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextBoundsInfoResult(
    resultCode: Int, 
    textBoundsInfo: TextBoundsInfo?)
```

Create a [TextBoundsInfoResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#) object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call. Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_UNSUPPORTED:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_FAILED:kotlin.Int), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_CANCELLED:kotlin.Int) |
| `textBoundsInfo` | [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo)?:the returned [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo) of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call. It can't be null if the`resultCode`is [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int). |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the resultCode is [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int) but the given`textBoundsInfo`is null. |

## Public methods

### getResultCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultCode(): Int
```

Return the result code of the [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer))call. Its value is one of the [CODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_UNSUPPORTED:kotlin.Int), [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int), [CODE_FAILED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_FAILED:kotlin.Int) and [CODE_CANCELLED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_CANCELLED:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.inputmethod.TextBoundsInfoResult#CODE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_UNSUPPORTED:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int), [android.view.inputmethod.TextBoundsInfoResult#CODE_FAILED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_FAILED:kotlin.Int), or [android.view.inputmethod.TextBoundsInfoResult#CODE_CANCELLED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_CANCELLED:kotlin.Int) |

### getTextBoundsInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextBoundsInfo(): TextBoundsInfo?
```

Return the [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo) provided by the editor. It is non-null if the`resultCode`is [CODE_SUCCESS](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfoResult#CODE_SUCCESS:kotlin.Int). Otherwise, it can be null in the following conditions:

- the editor doesn't support [InputConnection.requestTextBoundsInfo(RectF, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#requestTextBoundsInfo(android.graphics.RectF,%20java.util.concurrent.Executor,%20java.util.function.Consumer)).
- the editor doesn't have the text bounds information at the moment. (e.g. the editor view is not laid out yet.)
- the [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection) is or become inactive during the request.

<br />
