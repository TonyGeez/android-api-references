# ConfirmationCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfirmationCallback

Kotlin| [Java](https://developer.android.com/reference/android/security/ConfirmationCallback "View this page in Java") 
| --- | --- |

```
abstract class ConfirmationCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.ConfirmationCallback](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#) |

Callback class used when signaling that a prompt is no longer being presented.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConfirmationCallback](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#ConfirmationCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCanceled](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#onCanceled())`()` Called when the requested prompt was dismissed by the application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfirmed](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#onConfirmed(kotlin.ByteArray))`(`dataThatWasConfirmed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Called when the requested prompt was accepted by the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismissed](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#onDismissed())`()` Called when the requested prompt was dismissed (not accepted) by the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#onError(kotlin.Throwable))`(`e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Called when the requested prompt was dismissed because of a low-level error. |

## Public constructors

### ConfirmationCallback

```
ConfirmationCallback()
```

## Public methods

### onCanceled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCanceled(): Unit
```

Called when the requested prompt was dismissed by the application. 

### onConfirmed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onConfirmed(dataThatWasConfirmed: ByteArray): Unit
```

Called when the requested prompt was accepted by the user. The format of 'dataThatWasConfirmed' parameter is a [CBOR](http://cbor.io/) encoded map (type 5) with (at least) the keys**prompt** and**extra**. The keys are encoded as CBOR text string (type 3). The value of promptText is encoded as CBOR text string (type 3), and the value of extraData is encoded as CBOR byte string (type 2). Other keys may be added in the future.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataThatWasConfirmed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the data that was confirmed, see above for the format. This value cannot be`null`. |

### onDismissed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDismissed(): Unit
```

Called when the requested prompt was dismissed (not accepted) by the user. 

### onError

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(e: Throwable!): Unit
```

Called when the requested prompt was dismissed because of a low-level error.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------|
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:a throwable representing the error. |
