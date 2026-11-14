# EmbeddedPhotoPickerClient

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerClient

Kotlin| [Java](https://developer.android.com/reference/android/widget/photopicker/EmbeddedPhotoPickerClient "View this page in Java") 
| --- | --- |

```
interface EmbeddedPhotoPickerClient
```

| [android.widget.photopicker.EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#) |

Callback to define mechanisms by which can apps can receive notifications about different events from embedded photopicker for the corresponding Session ([EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession)).

PhotoPicker will invoke the methods of this interface on the Executor provided by the caller in [EmbeddedPhotoPickerProvider.openSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider#openSession(android.os.IBinder,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.widget.photopicker.EmbeddedPhotoPickerFeatureInfo,%20java.util.concurrent.Executor,%20android.widget.photopicker.EmbeddedPhotoPickerClient))

Any methods on a single instance of this object will always be invoked in a non-concurrent or thread safe way. In other words, all methods are invoked in a serial execution manner on the executor passed by the caller. Hence callers wouldn't need any buffer or locking mechanism on their end.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSelectionComplete](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onSelectionComplete())`()` Reports that the user is done with their selection and should collapse the picker. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionError](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onSessionError(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Reports that terminal error has occurred in the session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionOpened](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onSessionOpened(android.widget.photopicker.EmbeddedPhotoPickerSession))`(`session:` ` [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession)`)` Reports that session of app with photopicker was established successfully. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUriPermissionGranted](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onUriPermissionGranted(kotlin.collections.MutableList))`(`uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Reports that URI permission has been granted to the item selected by the user. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUriPermissionRevoked](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onUriPermissionRevoked(kotlin.collections.MutableList))`(`uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Reports that URI permission has been revoked of the item deselected by the user. |

## Public methods

### onSelectionComplete

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun onSelectionComplete(): Unit
```

Reports that the user is done with their selection and should collapse the picker.

This doesn't necessarily mean that the session should be closed, but rather the user has indicated that they are done selecting images and should go back to the app. 

### onSessionError

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun onSessionError(cause: Throwable): Unit
```

Reports that terminal error has occurred in the session. Any further events notified on this session will be ignored. The embedded photopicker view will be torn down along with session upon error.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):This value cannot be`null`. |

### onSessionOpened

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun onSessionOpened(session: EmbeddedPhotoPickerSession): Unit
```

Reports that session of app with photopicker was established successfully. Also shares [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession) handle containing the view with the caller that should be used to notify the session of UI events.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession):This value cannot be`null`. |

### onUriPermissionGranted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun onUriPermissionGranted(uris: MutableList<Uri!>): Unit
```

Reports that URI permission has been granted to the item selected by the user.

It is possible that the permission to the URI was revoked if the item was unselected by user before the URI is actually accessed by the caller. Hence callers must handle`SecurityException`when attempting to read or use the URI in response to this callback.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:This value cannot be`null`. |

### onUriPermissionRevoked

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun onUriPermissionRevoked(uris: MutableList<Uri!>): Unit
```

Reports that URI permission has been revoked of the item deselected by the user.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:This value cannot be`null`. |
