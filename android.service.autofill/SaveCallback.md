# SaveCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveCallback

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/SaveCallback "View this page in Java") 
| --- | --- |

```
class SaveCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.SaveCallback](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#) |

Handles save requests from the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) into the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) being autofilled.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onFailure(kotlin.CharSequence))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))could not be handled by the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess())`()` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))was successfully handled by the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess(android.content.IntentSender))`(`intentSender:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)`)` Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))was successfully handled by the service. |
| --- | --- |

## Public methods

### onFailure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onFailure(message: CharSequence!): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))could not be handled by the service.

This method is just used for logging purposes, the Android System won't call the service again in case of failures---if you need to recover from the failure, just save the [SaveRequest](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest) and try again later.

**Note:** for apps targeting [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or higher, this method just logs the message on`logcat`; for apps targetting older SDKs, it also displays the message to user using a [android.widget.Toast](https://developer.android.com/reference/kotlin/android/widget/Toast.html#).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:error message.**Note:** this message should**not**contain PII (Personally Identifiable Information, such as username or email address). |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess()](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess()), or [onSuccess(android.content.IntentSender)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess(android.content.IntentSender))was already called. |

### onSuccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))was successfully handled by the service.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess(android.content.IntentSender)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess(android.content.IntentSender)), or [onFailure(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onFailure(kotlin.CharSequence))was already called. |

### onSuccess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(intentSender: IntentSender): Unit
```

Notifies the Android System that an [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))was successfully handled by the service.

This method is useful when the service requires extra work---for example, launching an activity asking the user to authenticate first ---before it can process the request, as the intent will be launched from the context of the activity being autofilled and hence will be part of that activity's stack.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intentSender` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#):intent that will be launched from the context of activity being autofilled. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method, [onSuccess()](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onSuccess()), or [onFailure(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback#onFailure(kotlin.CharSequence))was already called. |
