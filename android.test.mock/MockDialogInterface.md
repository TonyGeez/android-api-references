# MockDialogInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockDialogInterface

Kotlin| [Java](https://developer.android.com/reference/android/test/mock/MockDialogInterface "View this page in Java") 
| --- | --- |

```
open class MockDialogInterface : DialogInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.mock.MockDialogInterface](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface#) |

| **This class was deprecated in API level 24.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.content.DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#) class. All methods are non-functional and throw [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Override it to provide the operations that you need.

## Summary

| Inherited constants ||
|---|---|
| From class [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON1:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON2:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON3:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEGATIVE:kotlin.Int) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_NEUTRAL:kotlin.Int) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#BUTTON_POSITIVE:kotlin.Int) <br /> The identifier for the positive button. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MockDialogInterface](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface#MockDialogInterface())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface#cancel())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface#dismiss())`()` <br /> |

## Public constructors

### MockDialogInterface

```
MockDialogInterface()
```

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

**Deprecated:** *Deprecated in Java.*
