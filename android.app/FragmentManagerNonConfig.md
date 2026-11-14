# FragmentManagerNonConfig

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentManagerNonConfig

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentManagerNonConfig "View this page in Java") 

```
open class FragmentManagerNonConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.FragmentManagerNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentManagerNonConfig#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManagerNonConfig

FragmentManagerNonConfig stores the retained instance fragments across activity recreation events.

Apps should treat objects of this type as opaque, returned by and passed to the state save and restore process for fragments in [FragmentController.retainNonConfig()](https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNonConfig())and android.app.FragmentController#restoreAllState(Parcelable,android.app.FragmentManagerNonConfig).

## Summary
