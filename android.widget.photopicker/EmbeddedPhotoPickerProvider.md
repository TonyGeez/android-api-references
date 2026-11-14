# EmbeddedPhotoPickerProvider

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerProvider

Kotlin| [Java](EmbeddedPhotoPickerProvider.md) 
| --- | --- |

```
interface EmbeddedPhotoPickerProvider
```

| [android.widget.photopicker.EmbeddedPhotoPickerProvider](EmbeddedPhotoPickerProvider.md) |

This interface provides an api that callers can use to get a session of embedded PhotoPicker ([EmbeddedPhotoPickerSession](EmbeddedPhotoPickerSession.md)).

Callers can get instance of this class using [EmbeddedPhotoPickerProviderFactory.create(Context)](EmbeddedPhotoPickerProviderFactory.md)).

Under the hood, a service connection with photopicker is established by the implementation of this api. To help establish this connection, a caller must include in their Manifest: 

```kotlin
<code>&lt;queries&gt;
    &lt;intent&gt;
        &lt;action android:name="com.android.photopicker.core.embedded.EmbeddedService.BIND"/&gt;
    &lt;/intent&gt;
  &lt;/queries&gt;
  </code>
```

When a session opens successfully, they would receive an instance of [EmbeddedPhotoPickerSession](EmbeddedPhotoPickerSession.md) and [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) via the [api](EmbeddedPhotoPickerClient.md))

Callers pass an instance of [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md) which is used by service to notify about different events (like sessionError, uri granted/revoked etc) to them. One-to-one relationship of client to session must be maintained by a caller i.e. they shouldn't reuse same callback for more than one openSession requests.

The [EmbeddedPhotoPickerSession](EmbeddedPhotoPickerSession.md) instance can be used to notify photopicker about different events (like resize, configChange etc).

This api is supported on api versions Android U+.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openSession](EmbeddedPhotoPickerProvider.md))`(`hostToken:` ` [IBinder](../android.os/IBinder.md)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `featureInfo:` ` [EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md)`, `clientExecutor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md)`)` Open a new session for displaying content with an initial size of width x height pixels. |

## Public methods

### openSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun openSession(
    hostToken: IBinder, 
    displayId: Int, 
    width: Int, 
    height: Int, 
    featureInfo: EmbeddedPhotoPickerFeatureInfo, 
    clientExecutor: Executor, 
    callback: EmbeddedPhotoPickerClient
): Unit
```

Open a new session for displaying content with an initial size of width x height pixels. [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md) will receive all incoming communication from the PhotoPicker. All incoming calls to [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md) will be made through the provided`clientExecutor`

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hostToken` | [IBinder](../android.os/IBinder.md):Token used for constructing [android.view.SurfaceControlViewHost](../android.view/SurfaceControlViewHost.md). Use [AttachedSurfaceControl.getInputTransferToken()](../android.view/AttachedSurfaceControl.md))to get token of attached [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md). This value cannot be`null`. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Application display id. Use [DisplayManager.getDisplays()](../android.hardware.display/DisplayManager.md))to get the id. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):width of the view, in pixels. |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):height of the view, in pixels. |
| `featureInfo` | [EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md): [EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md) object containing all the required features for the given session. This value cannot be`null`. |
| `clientExecutor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) to invoke callbacks. This value cannot be`null`. |
| --- | --- |
| `callback` | [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md): [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md) object to receive callbacks from photopicker. This value cannot be`null`. |
