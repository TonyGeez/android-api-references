# PackageManager.OnChecksumsReadyListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnChecksumsReadyListener

Kotlin| [Java](../android/content/pm/PackageManager.OnChecksumsReadyListener.md) 
| --- | --- |

```
@FunctionalInterface interface OnChecksumsReadyListener
```

| [android.content.pm.PackageManager.OnChecksumsReadyListener](../android/content/pm/PackageManager.OnChecksumsReadyListener.md) |

Listener that gets notified when checksums are available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChecksumsReady](../android/content/pm/PackageManager.OnChecksumsReadyListener.md))`(`checksums:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ApkChecksum](../android/content/pm/ApkChecksum.md)!>`)` Called when the checksums are available. |

## Public methods

### onChecksumsReady

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChecksumsReady(checksums: MutableList<ApkChecksum!>): Unit
```

Called when the checksums are available.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checksums` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApkChecksum](../android/content/pm/ApkChecksum.md)!\>:array of checksums. This value cannot be`null`. |
