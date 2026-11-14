Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaQualityManager

Kotlin | [Java](MediaQualityManager.md)
| --- | --- |

```
class MediaQualityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.MediaQualityManager](MediaQualityManager.md) |

Central system API to the overall media quality, which arbitrates interaction between applications and media quality service.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback` Callback used to monitor status of ambient backlight. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.PictureProfileCallback` Callback used to monitor status of picture profiles |
| | `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.ProfileQueryParams` Options for profile queries. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.SoundProfileCallback` Callback used to monitor status of sound profiles. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addActiveProcessingPictureListener Adds an active picture listener for the contents owner by the caller. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createPictureProfile Creates a picture profile and store it in the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createSoundProfile Creates a sound profile and store it in the system. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PictureProfile](PictureProfile.md)!\> | getAvailablePictureProfiles Gets profiles that available to the caller. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SoundProfile](SoundProfile.md)!\> | getAvailableSoundProfiles Gets profiles that available to the caller package. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ParameterCapability](ParameterCapability.md)!\> | getParameterCapabilities Gets capability information of the given parameters. |
| --- | --- |
| [PictureProfile](PictureProfile.md)? | getPictureProfile Gets picture profile by given profile type and name. |
| [SoundProfile](SoundProfile.md)? | getSoundProfile Gets sound profile by given profile type and name. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAmbientBacklightEnabled Returns `true` if ambient backlight is enabled; `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoPictureQualityEnabled Returns `true` if auto picture quality is enabled; `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoSoundQualityEnabled Returns `true` if auto sound quality is enabled; `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSuperResolutionEnabled Returns `true` if super resolution is enabled; `false` otherwise. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerAmbientBacklightCallback Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerPictureProfileCallback Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.PictureProfileCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerSoundProfileCallback Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.SoundProfileCallback`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeActiveProcessingPictureListener Removes an active picture listener for the contents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removePictureProfile Removes a picture profile from the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeSoundProfile Removes a sound profile from the system. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAmbientBacklightEnabled Enables or disables the ambient backlight detection. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAmbientBacklightSettings Set the ambient backlight settings. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterAmbientBacklightCallback Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterPictureProfileCallback Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.PictureProfileCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterSoundProfileCallback Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.SoundProfileCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updatePictureProfile Updates an existing picture profile and store it in the system. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updateSoundProfile Updates an existing sound profile and store it in the system. |

## Public methods

### addActiveProcessingPictureListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addActiveProcessingPictureListener(
    executor: Executor, 
    listener: Consumer<MutableList<ActiveProcessingPicture!>!>
): Unit
```

Adds an active picture listener for the contents owner by the caller.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `listener` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActiveProcessingPicture](ActiveProcessingPicture.md)!\>!\>: This value cannot be `null`. |

### createPictureProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createPictureProfile(pp: PictureProfile): Unit
```

Creates a picture profile and store it in the system.

If the profile is created successfully, onPictureProfileAdded is invoked.

| Parameters ||
|---|---|
| `pp` | [PictureProfile](PictureProfile.md): the PictureProfile object to be created. This value cannot be `null`. |

### createSoundProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createSoundProfile(sp: SoundProfile): Unit
```

Creates a sound profile and store it in the system.

If the profile is created successfully, onSoundProfileAdded is invoked.

| Parameters ||
|---|---|
| `sp` | [SoundProfile](SoundProfile.md): the SoundProfile object to be created. This value cannot be `null`. |

### getAvailablePictureProfiles

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailablePictureProfiles(options: MediaQualityManager.ProfileQueryParams?): MutableList<PictureProfile!>
```

Gets profiles that available to the caller.

If areParametersIncluded is `false`, getParameters of the returned profiles are empty bundles.

| Parameters ||
|---|---|
| `options` | [MediaQualityManager.ProfileQueryParams](../android/media/quality/MediaQualityManager.ProfileQueryParams.md)?: the options of the query. `null` if default options are used. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile!>` | the corresponding picture profile if available; `null` if the name doesn't exist. |

### getAvailableSoundProfiles

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableSoundProfiles(options: MediaQualityManager.ProfileQueryParams?): MutableList<SoundProfile!>
```

Gets profiles that available to the caller package.

If areParametersIncluded is `false`, getParameters of the returned profiles are empty bundles.

| Parameters ||
|---|---|
| `options` | [MediaQualityManager.ProfileQueryParams](../android/media/quality/MediaQualityManager.ProfileQueryParams.md)?: the options of the query. `null` if default options are used. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/quality/SoundProfile!>` | the corresponding sound profile if available; `null` if the none available. |

### getParameterCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameterCapabilities(names: MutableList<String!>): MutableList<ParameterCapability!>
```

Gets capability information of the given parameters.

If a name isn't found, a corresponding ParameterCapability instance is in the return list, and isSupported is `false`.

| Parameters ||
|---|---|
| `names` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: the parameter names. Commonly used names can be found in MediaQualityContract. Vendor-defined names are also permitted. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/quality/ParameterCapability!>` | This value cannot be `null`. |

### getPictureProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPictureProfile(
    type: Int, 
    name: String, 
    options: MediaQualityManager.ProfileQueryParams?
): PictureProfile?
```

Gets picture profile by given profile type and name.

If areParametersIncluded is `false`, getParameters of the returned profile is an empty bundle.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the profile. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_APPLICATION:kotlin.Int` |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the profile. This value cannot be `null`. |
| `options` | [MediaQualityManager.ProfileQueryParams](../android/media/quality/MediaQualityManager.ProfileQueryParams.md)?: the options of the query. `null` if default options are used. |
| --- | --- |

| Return ||
|---|---|
| PictureProfile | the corresponding picture profile if available; `null` if the name doesn't exist. |

### getSoundProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSoundProfile(
    type: Int, 
    name: String, 
    options: MediaQualityManager.ProfileQueryParams?
): SoundProfile?
```

Gets sound profile by given profile type and name.

If areParametersIncluded is `false`, getParameters of the returned profile is an empty bundle.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the profile. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/SoundProfile#TYPE_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/SoundProfile#TYPE_APPLICATION:kotlin.Int` |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the profile. This value cannot be `null`. |
| `options` | [MediaQualityManager.ProfileQueryParams](../android/media/quality/MediaQualityManager.ProfileQueryParams.md)?: the options of the query. `null` if default options are used. |
| --- | --- |

| Return ||
|---|---|
| SoundProfile | the corresponding sound profile if available; `null` if the name doesn't exist. |

### isAmbientBacklightEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAmbientBacklightEnabled(): Boolean
```

Returns `true` if ambient backlight is enabled; `false` otherwise.

### isAutoPictureQualityEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAutoPictureQualityEnabled(): Boolean
```

Returns `true` if auto picture quality is enabled; `false` otherwise.

### isAutoSoundQualityEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAutoSoundQualityEnabled(): Boolean
```

Returns `true` if auto sound quality is enabled; `false` otherwise.

### isSuperResolutionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSuperResolutionEnabled(): Boolean
```

Returns `true` if super resolution is enabled; `false` otherwise.

### registerAmbientBacklightCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAmbientBacklightCallback(
    executor: Executor, 
    callback: MediaQualityManager.AmbientBacklightCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaQualityManager.AmbientBacklightCallback](../android/media/quality/MediaQualityManager.AmbientBacklightCallback.md): This value cannot be `null`. |

### registerPictureProfileCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerPictureProfileCallback(
    executor: Executor, 
    callback: MediaQualityManager.PictureProfileCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.PictureProfileCallback`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaQualityManager.PictureProfileCallback](../android/media/quality/MediaQualityManager.PictureProfileCallback.md): This value cannot be `null`. |

### registerSoundProfileCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerSoundProfileCallback(
    executor: Executor, 
    callback: MediaQualityManager.SoundProfileCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.SoundProfileCallback`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaQualityManager.SoundProfileCallback](../android/media/quality/MediaQualityManager.SoundProfileCallback.md): This value cannot be `null`. |

### removeActiveProcessingPictureListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeActiveProcessingPictureListener(listener: Consumer<MutableList<ActiveProcessingPicture!>!>): Unit
```

Removes an active picture listener for the contents.

| Parameters ||
|---|---|
| `listener` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActiveProcessingPicture](ActiveProcessingPicture.md)!\>!\>: This value cannot be `null`. |

### removePictureProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removePictureProfile(profileId: String): Unit
```

Removes a picture profile from the system.

| Parameters ||
|---|---|
| `profileId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the id of the object to be removed. This value cannot be `null`. |

### removeSoundProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeSoundProfile(profileId: String): Unit
```

Removes a sound profile from the system.

| Parameters ||
|---|---|
| `profileId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the id of the object to be removed. This value cannot be `null`. |

### setAmbientBacklightEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAmbientBacklightEnabled(enabled: Boolean): Unit
```

Enables or disables the ambient backlight detection.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to enable, `false` to disable. |

### setAmbientBacklightSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAmbientBacklightSettings(settings: AmbientBacklightSettings): Unit
```

Set the ambient backlight settings.

| Parameters ||
|---|---|
| `settings` | [AmbientBacklightSettings](AmbientBacklightSettings.md): The settings to use for the backlight detector. This value cannot be `null`. |

### unregisterAmbientBacklightCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterAmbientBacklightCallback(callback: MediaQualityManager.AmbientBacklightCallback): Unit
```

Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback`.

| Parameters ||
|---|---|
| `callback` | [MediaQualityManager.AmbientBacklightCallback](../android/media/quality/MediaQualityManager.AmbientBacklightCallback.md): This value cannot be `null`. |

### unregisterPictureProfileCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterPictureProfileCallback(callback: MediaQualityManager.PictureProfileCallback): Unit
```

Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.PictureProfileCallback`.

| Parameters ||
|---|---|
| `callback` | [MediaQualityManager.PictureProfileCallback](../android/media/quality/MediaQualityManager.PictureProfileCallback.md): This value cannot be `null`. |

### unregisterSoundProfileCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterSoundProfileCallback(callback: MediaQualityManager.SoundProfileCallback): Unit
```

Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.SoundProfileCallback`.

| Parameters ||
|---|---|
| `callback` | [MediaQualityManager.SoundProfileCallback](../android/media/quality/MediaQualityManager.SoundProfileCallback.md): This value cannot be `null`. |

### updatePictureProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updatePictureProfile(
    profileId: String, 
    pp: PictureProfile
): Unit
```

Updates an existing picture profile and store it in the system.

| Parameters ||
|---|---|
| `profileId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the id of the object to be updated. This value cannot be `null`. |
| `pp` | [PictureProfile](PictureProfile.md): the PictureProfile object to be updated. This value cannot be `null`. |

### updateSoundProfile

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateSoundProfile(
    profileId: String, 
    sp: SoundProfile
): Unit
```

Updates an existing sound profile and store it in the system.

| Parameters ||
|---|---|
| `profileId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the id of the object to be updated. This value cannot be `null`. |
| `sp` | [SoundProfile](SoundProfile.md): the SoundProfile object to be updated. This value cannot be `null`. |
