# ApplicationRuntime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationRuntime

```
class ApplicationRuntime
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [dalvik.system.ApplicationRuntime](https://developer.android.com/reference/kotlin/dalvik/system/ApplicationRuntime#) |

Provides APIs to retrieve the information about the application loaded in the current runtime.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DexFile.OptimizationInfo](https://developer.android.com/reference/kotlin/dalvik/system/DexFile.OptimizationInfo) | [getBaseApkOptimizationInfo](https://developer.android.com/reference/kotlin/dalvik/system/ApplicationRuntime#getBaseApkOptimizationInfo())`()` Returns the optimization status of the base APK loaded in this process. |

## Public methods

### getBaseApkOptimizationInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBaseApkOptimizationInfo(): DexFile.OptimizationInfo
```

Returns the optimization status of the base APK loaded in this process. If no base APK has been loaded in this process, this methods returns an object, but the contents are undefined.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [DexFile.OptimizationInfo](https://developer.android.com/reference/kotlin/dalvik/system/DexFile.OptimizationInfo) | This value cannot be`null`. |
