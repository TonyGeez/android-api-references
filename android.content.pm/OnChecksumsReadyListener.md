# PackageManager.OnChecksumsReadyListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnChecksumsReadyListener

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/PackageManager.OnChecksumsReadyListener "View this page in Java") 

```
@FunctionalInterface interface OnChecksumsReadyListener
```

| [android.content.pm.PackageManager.OnChecksumsReadyListener](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.OnChecksumsReadyListener#) |

Listener that gets notified when checksums are available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChecksumsReady](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.OnChecksumsReadyListener#onChecksumsReady(kotlin.collections.MutableList))`(`checksums:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ApkChecksum](https://developer.android.com/reference/kotlin/android/content/pm/ApkChecksum)!>`)` Called when the checksums are available. |

## Public methods

### onChecksumsReady

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChecksumsReady(checksums: MutableList<ApkChecksum!>): Unit
```

Called when the checksums are available.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checksums` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApkChecksum](https://developer.android.com/reference/kotlin/android/content/pm/ApkChecksum)!\>:array of checksums. This value cannot be`null`. |
