# CountDownTimer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CountDownTimer

Kotlin| [Java](../android/os/CountDownTimer.md) 
| --- | --- |

```
abstract class CountDownTimer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.CountDownTimer](../android/os/CountDownTimer.md) |

Schedule a countdown until a time in the future, with regular notifications on intervals along the way. Example of showing a 30 second countdown in a text field:

<br />

<br />

### Kotlin

```kotlin
object : CountDownTimer(30000, 1000) {
 
      override fun onTick(millisUntilFinished: Long) {
          mTextField.setText("seconds remaining: " + millisUntilFinished / 1000)
      }
 
      override fun onFinish() {
          mTextField.setText("done!")
      }
  }.start()
  
```

### Java

```kotlin
new CountDownTimer(30000, 1000) {
 
      public void onTick(long millisUntilFinished) {
          mTextField.setText("seconds remaining: " + millisUntilFinished / 1000);
      }
 
      public void onFinish() {
          mTextField.setText("done!");
      }
  }.start();
  
```

<br />

<br />

The calls to [onTick(long)](../android/os/CountDownTimer.md))are synchronized to this object so that one call to [onTick(long)](../android/os/CountDownTimer.md))won't ever occur before the previous callback is complete. This is only relevant when the implementation of [onTick(long)](../android/os/CountDownTimer.md))takes an amount of time to execute that is significant compared to the countdown interval.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CountDownTimer](../android/os/CountDownTimer.md))`(`millisInFuture:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `countDownInterval:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/os/CountDownTimer.md))`()` Cancel the countdown. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinish](../android/os/CountDownTimer.md))`()` Callback fired when the time is up. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTick](../android/os/CountDownTimer.md))`(`millisUntilFinished:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback fired on regular interval. |
| --- | --- |
| [CountDownTimer](../android/os/CountDownTimer.md)! | [start](../android/os/CountDownTimer.md))`()` Start the countdown. |

## Public constructors

### CountDownTimer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CountDownTimer(
    millisInFuture: Long, 
    countDownInterval: Long)
```

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `millisInFuture` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of millis in the future from the call to [start()](../android/os/CountDownTimer.md))until the countdown is done and [onFinish()](../android/os/CountDownTimer.md))is called. |
| `countDownInterval` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The interval along the way to receive [onTick(long)](../android/os/CountDownTimer.md))callbacks. |

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Cancel the countdown. 

### onFinish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFinish(): Unit
```

Callback fired when the time is up. 

### onTick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTick(millisUntilFinished: Long): Unit
```

Callback fired on regular interval.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------|
| `millisUntilFinished` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The amount of time until finished. |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(): CountDownTimer!
```

Start the countdown.
