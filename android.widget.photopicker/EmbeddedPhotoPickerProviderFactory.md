# EmbeddedPhotoPickerProviderFactory

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerProviderFactory

Kotlin | [Java](https://developer.android.com/reference/android/widget/photopicker/EmbeddedPhotoPickerProviderFactory "View this page in Java") 
| --- | --- |

```
open class EmbeddedPhotoPickerProviderFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.photopicker.EmbeddedPhotoPickerProviderFactory](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProviderFactory#) |

Interface to get instance of [EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider) class to request a new [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession).

This class creates and maintains the binding/unbinding to embedded photopicker service on behalf of the caller. It makes IPC call to the service using binder android.widget.photopicker.IEmbeddedPhotoPicker to get a new session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider) | [create](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProviderFactory#create(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Returns an implementation of [EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider) class. |

## Public methods

### create

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
open static fun create(context: Context): EmbeddedPhotoPickerProvider
```

Returns an implementation of [EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider) class.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider) | This value cannot be `null`. |
