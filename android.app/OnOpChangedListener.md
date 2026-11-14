# AppOpsManager.OnOpChangedListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnOpChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/app/AppOpsManager.OnOpChangedListener "View this page in Java") 

```
interface OnOpChangedListener
```

| [android.app.AppOpsManager.OnOpChangedListener](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#) |

Callback for notification of changes to operation state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpChanged](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#onOpChanged(kotlin.String,%20kotlin.String))`(`op:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOpChanged](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#onOpChanged(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String))`(`op:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `userId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `persistentDeviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Similar to [onOpChanged(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#onOpChanged(kotlin.String,%20kotlin.String))but includes user and the device for which the op mode has changed. |

## Public methods

### onOpChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOpChanged(
    op: String!, 
    packageName: String!
): Unit
```  

### onOpChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOpChanged(
    op: String, 
    packageName: String, 
    userId: Int, 
    persistentDeviceId: String
): Unit
```

Similar to [onOpChanged(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#onOpChanged(kotlin.String,%20kotlin.String))but includes user and the device for which the op mode has changed.

Implement this method if callbacks are required on all devices. If not implemented explicitly, the default implementation will notify for op changes on the default device only.

If implemented, [onOpChanged(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener#onOpChanged(kotlin.String,%20kotlin.String))will not be called automatically.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The Op that changed. This value cannot be`null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Package of the app whose Op changed. Can be empty in the case of a change which is not package specific (such as global restrictions) which may imply a change to the op or package being listened to. This value cannot be`null`. |
| `userId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):User id of the app whose Op changed. |
| `persistentDeviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):persistent device id whose Op changed. This value cannot be`null`. |
