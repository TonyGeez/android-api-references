# android.widget.photopicker

## Interfaces

| [EmbeddedPhotoPickerClient](EmbeddedPhotoPickerClient.md) | Callback to define mechanisms by which can apps can receive notifications about different events from embedded photopicker for the corresponding Session (EmbeddedPhotoPickerSession). |
| --- | --- |
| [EmbeddedPhotoPickerProvider](EmbeddedPhotoPickerProvider.md) | This interface provides an api that callers can use to get a session of embedded PhotoPicker (EmbeddedPhotoPickerSession). |
| [EmbeddedPhotoPickerSession](EmbeddedPhotoPickerSession.md) | Class that holds the embedded photopicker view wrapped in `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#` that can be embedded by the caller in their view hierarchy by placing it in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` via its setChildSurfacePackage api. |

## Classes

| [EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md) | An immutable parcel to carry information regarding desired features of caller for a given session. |
| --- | --- |
| [EmbeddedPhotoPickerProviderFactory](EmbeddedPhotoPickerProviderFactory.md) | Interface to get instance of EmbeddedPhotoPickerProvider class to request a new EmbeddedPhotoPickerSession. |
| [EmbeddedPhotoPickerUiCustomizationParams](EmbeddedPhotoPickerUiCustomizationParams.md) | Defines UI customization options specific to the embedded Photo Picker interface. |
| [PhotoPickerSelectionParams](../android/widget/photopicker/PhotoPickerSelectionParams.md) | An immutable parcel that carries constraints to be applied to media items displayed in the Photo Picker. |
| --- | --- |
| [PhotoPickerUiCustomizationParams](PhotoPickerUiCustomizationParams.md) | Defines UI customization options for the system's Photo Picker interface. |
