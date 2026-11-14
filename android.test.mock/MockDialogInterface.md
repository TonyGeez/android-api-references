# MockDialogInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockDialogInterface

Kotlin| [Java](../android/test/mock/MockDialogInterface.md) 
| --- | --- |

```
open class MockDialogInterface : DialogInterface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.mock.MockDialogInterface](../android/test/mock/MockDialogInterface.md) |

| **This class was deprecated in API level 24.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.content.DialogInterface](../android/content/DialogInterface.md) class. All methods are non-functional and throw [java.lang.UnsupportedOperationException](../java/lang/UnsupportedOperationException.md). Override it to provide the operations that you need.

## Summary

| Inherited constants ||
|---|---|
| From class [DialogInterface](../android/content/DialogInterface.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](../android/content/DialogInterface.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](../android/content/DialogInterface.md) <br /> The identifier for the negative button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](../android/content/DialogInterface.md) <br /> The identifier for the neutral button. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](../android/content/DialogInterface.md) <br /> The identifier for the positive button. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MockDialogInterface](../android/test/mock/MockDialogInterface.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/test/mock/MockDialogInterface.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](../android/test/mock/MockDialogInterface.md))`()` <br /> |

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
