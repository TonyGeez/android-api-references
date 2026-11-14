# SaveCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveCallback

Kotlin| [Java](SaveCallback.md) 
| --- | --- |

```
class SaveCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.SaveCallback](SaveCallback.md) |

Handles save requests from the [AutofillService](AutofillService.md) into the [Activity](../android.app/Activity.md) being autofilled.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](SaveCallback.md))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))could not be handled by the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](SaveCallback.md))`()` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))was successfully handled by the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](SaveCallback.md))`(`intentSender:` ` [IntentSender](../android.content/IntentSender.md)`)` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))was successfully handled by the service. |
| --- | --- |

## Public methods

### onFailure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onFailure(message: CharSequence!): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))could not be handled by the service.

This method is just used for logging purposes, the Android System won't call the service again in case of failures---if you need to recover from the failure, just save the [SaveRequest](SaveRequest.md) and try again later.

**Note:** for apps targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) or higher, this method just logs the message on`logcat`; for apps targetting older SDKs, it also displays the message to user using a [android.widget.Toast](../android.widget/Toast.md).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:error message.**Note:** this message should**not**contain PII (Personally Identifiable Information, such as username or email address). |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess()](SaveCallback.md)), or [onSuccess(android.content.IntentSender)](SaveCallback.md))was already called. |

### onSuccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))was successfully handled by the service.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess(android.content.IntentSender)](SaveCallback.md)), or [onFailure(java.lang.CharSequence)](SaveCallback.md))was already called. |

### onSuccess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(intentSender: IntentSender): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))was successfully handled by the service.

This method is useful when the service requires extra work---for example, launching an activity asking the user to authenticate first ---before it can process the request, as the intent will be launched from the context of the activity being autofilled and hence will be part of that activity's stack.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intentSender` | [IntentSender](../android.content/IntentSender.md):intent that will be launched from the context of activity being autofilled. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess()](SaveCallback.md)), or [onFailure(java.lang.CharSequence)](SaveCallback.md))was already called. |
