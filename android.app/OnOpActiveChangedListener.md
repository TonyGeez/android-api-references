# AppOpsManager.OnOpActiveChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnOpActiveChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/app/AppOpsManager.OnOpActiveChangedListener "View this page in Java") 
| --- | --- |

```
interface OnOpActiveChangedListener
```

| [android.app.AppOpsManager.OnOpActiveChangedListener](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpActiveChangedListener#) |

Callback for notification of changes to operation active state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpActiveChanged](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpActiveChangedListener#onOpActiveChanged(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.Boolean))`(`op:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the active state of an app-op changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpActiveChanged](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpActiveChangedListener#onOpActiveChanged(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int))`(`op:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attributionTag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `virtualDeviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `attributionFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `attributionChainId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Similar to #onOpActiveChanged(java.lang.String,int,java.lang.String,java.lang.String,boolean,int,int), but also includes the virtual device id of the op is now active or inactive. |

## Public methods

### onOpActiveChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpActiveChanged(
    op: String, 
    uid: Int, 
    packageName: String, 
    active: Boolean
): Unit
```

Called when the active state of an app-op changes.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The operation that changed. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package performing the operation. This value cannot be`null`. |
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the operation became active or inactive. |
| --- | --- |

### onOpActiveChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOpActiveChanged(
    op: String, 
    uid: Int, 
    packageName: String, 
    attributionTag: String?, 
    virtualDeviceId: Int, 
    active: Boolean, 
    attributionFlags: Int, 
    attributionChainId: Int
): Unit
```

Similar to #onOpActiveChanged(java.lang.String,int,java.lang.String,java.lang.String,boolean,int,int), but also includes the virtual device id of the op is now active or inactive.

Implement this method if callbacks are required on all devices. If not implemented explicitly, the default implementation will notify for op state changes on the default device [Context.DEVICE_ID_DEFAULT](https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int) only.

If implemented, #onOpActiveChanged(java.lang.String,int,java.lang.String,java.lang.String,boolean,int,int) will not be called automatically.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The operation that changed. This value cannot be`null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The UID performing the operation. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package performing the operation. This value cannot be`null`. |
| --- | --- |
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The operation's attribution tag. This value may be`null`. |
| `virtualDeviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the virtual device id whose operation has changed |
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the operation became active or inactive. |
| --- | --- |
| `attributionFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the attribution flags for this operation. Value is either`0`or a combination of android.app.AppOpsManager.ATTRIBUTION_FLAG_ACCESSOR, android.app.AppOpsManager.ATTRIBUTION_FLAG_INTERMEDIARY, android.app.AppOpsManager.ATTRIBUTION_FLAG_RECEIVER, and android.app.AppOpsManager.ATTRIBUTION_FLAG_TRUSTED |
| `attributionChainId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the unique id of the attribution chain this op is a part of. |
