# EmbeddedPhotoPickerProviderFactory

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerProviderFactory

Kotlin | [Java](../android/widget/photopicker/EmbeddedPhotoPickerProviderFactory.md) 
| --- | --- |

```
open class EmbeddedPhotoPickerProviderFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.photopicker.EmbeddedPhotoPickerProviderFactory](../android/widget/photopicker/EmbeddedPhotoPickerProviderFactory.md) |

Interface to get instance of [EmbeddedPhotoPickerProvider](../android/widget/photopicker/EmbeddedPhotoPickerProvider.md) class to request a new [EmbeddedPhotoPickerSession](../android/widget/photopicker/EmbeddedPhotoPickerSession.md).

This class creates and maintains the binding/unbinding to embedded photopicker service on behalf of the caller. It makes IPC call to the service using binder android.widget.photopicker.IEmbeddedPhotoPicker to get a new session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [EmbeddedPhotoPickerProvider](../android/widget/photopicker/EmbeddedPhotoPickerProvider.md) | [create](../android/widget/photopicker/EmbeddedPhotoPickerProviderFactory.md))`(`context:` ` [Context](../android/content/Context.md)`)` Returns an implementation of [EmbeddedPhotoPickerProvider](../android/widget/photopicker/EmbeddedPhotoPickerProvider.md) class. |

## Public methods

### create

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
open static fun create(context: Context): EmbeddedPhotoPickerProvider
```

Returns an implementation of [EmbeddedPhotoPickerProvider](../android/widget/photopicker/EmbeddedPhotoPickerProvider.md) class.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md): This value cannot be `null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [EmbeddedPhotoPickerProvider](../android/widget/photopicker/EmbeddedPhotoPickerProvider.md) | This value cannot be `null`. |
