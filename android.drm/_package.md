# android.drm

# android.drm

Kotlin| [Java](https://developer.android.com/reference/android/drm/package-summary "View this page in Java")

## Interfaces

| [OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener) | Interface definition for a callback that receives information about DRM framework errors. |
| [OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener) | Interface definition for a callback that receives information about DRM processing events. |
| [OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener) | Interface definition for a callback that receives status messages and warnings during registration and rights acquisition. |
| [ConstraintsColumns](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns) | Interface definition for the columns that represent DRM constraints. |

## Classes

| [DrmConvertedStatus](https://developer.android.com/reference/kotlin/android/drm/DrmConvertedStatus) | An entity class that wraps converted data, conversion status, and the offset for appending the header and body signature to the converted data. |
| [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent) | An entity class that is passed to the [onError()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener#onError(android.drm.DrmManagerClient,%20android.drm.DrmErrorEvent))callback. |
| [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) | A base class that is used to send asynchronous event information from the DRM framework. |
| [DrmInfo](https://developer.android.com/reference/kotlin/android/drm/DrmInfo) | An entity class that describes the information required to send transactions between a device and an online DRM server. |
| [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent) | An entity class that is passed to the [onInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener#onInfo(android.drm.DrmManagerClient,%20android.drm.DrmInfoEvent))callback. |
| [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest) | An entity class that is used to pass information to an online DRM server. |
| [DrmInfoStatus](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus) | An entity class that wraps the result of communication between a device and an online DRM server. |
| [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient) | The main programming interface for the DRM framework. |
| [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights) | An entity class that wraps the license information retrieved from the online DRM server. |
| [DrmStore](https://developer.android.com/reference/kotlin/android/drm/DrmStore) | Defines constants that are used by the DRM framework. |
| [DrmSupportInfo](https://developer.android.com/reference/kotlin/android/drm/DrmSupportInfo) | An entity class that wraps the capability of each DRM plug-in (agent), such as the MIME type and file suffix the DRM plug-in can handle. |
| [DrmUtils](https://developer.android.com/reference/kotlin/android/drm/DrmUtils) | A utility class that provides operations for parsing extended metadata embedded in DRM constraint information. |
| [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData) | An entity class that wraps the result of a [processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))transaction between a device and a DRM server. |
