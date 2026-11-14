Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsafeIntentLaunchViolation

Kotlin | [Java](UnsafeIntentLaunchViolation.md)
| --- | --- |

```
class UnsafeIntentLaunchViolation : Violation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [android.os.strictmode.Violation](Violation.md) ||
| | | ↳ | [android.os.strictmode.UnsafeIntentLaunchViolation](UnsafeIntentLaunchViolation.md) |
| --- | --- | --- | --- |

Violation raised when your app launches an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which originated from outside your app.

Violations may indicate security vulnerabilities in the design of your app, where a malicious app could trick you into granting `https://developer.android.com/reference/kotlin/android/net/Uri.html#` permissions or launching unexported components. Here are some typical design patterns that can be used to safely resolve these violations:

- The ideal approach is to migrate to using a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`, which ensures that your launch is performed using the identity of the original creator, completely avoiding the security issues described above.
- If using a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` isn't feasible, an alternative approach is to create a brand new `https://developer.android.com/reference/kotlin/android/content/Intent.html#` and carefully copy only specific values from the original `https://developer.android.com/reference/kotlin/android/content/Intent.html#` after careful validation.

Note that this *may* detect false-positives if your app sends itself an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which is first routed through the OS, such as using android.content.Intent#createChooser. In these cases, careful inspection is required to determine if the return point into your app is appropriately protected with a signature permission or marked as unexported. If the return point is not protected, your app is likely vulnerable to malicious apps.

## Summary

| Public constructors ||
|---|---|
| UnsafeIntentLaunchViolation <br /> |

| Public methods ||
|---|---|
| [Intent](../android.content/Intent.md)? | getIntent Return the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which caused this violation to be raised. |

| Inherited functions ||
|---|---|
| From class Violation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html` | fillInStackTrace Fills in the execution stack trace. This method records within this `Throwable` object information about the current state of the stack frames for the current thread. If the stack trace of this `Throwable` [is not](../java.lang/Throwable.md)), calling this method has no effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | hashCode Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`. The general contract of `hashCode` is: - Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application. - If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result. - It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html` | initCause Initializes the *cause* of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.) This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with Throwable or Throwable, this method cannot be called even once. An example of using this method on a legacy throwable type without other support for setting the cause is: ```kotlin try { lowLevelOp(); } catch (LowLevelException le) { throw (HighLevelException) new HighLevelException().initCause(le); // Legacy constructor } ``` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setStackTrace Sets the stack trace elements that will be returned by getStackTrace and printed by printStackTrace and related methods. This method, which is designed for use by RPC frameworks and other advanced systems, allows the client to override the default stack trace that is either generated by fillInStackTrace when a throwable is constructed or deserialized when a throwable is read from a serialization stream. If the stack trace of this `Throwable` [is not](../java.lang/Throwable.md)), calling this method has no effect other than validating its argument. <br /> | ||

## Public constructors

### UnsafeIntentLaunchViolation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsafeIntentLaunchViolation(intent: Intent)
```

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |

## Public methods

### getIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntent(): Intent?
```

Return the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which caused this violation to be raised. Note that this value is not available if this violation has been serialized since intents cannot be serialized.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | This value may be `null`. |
