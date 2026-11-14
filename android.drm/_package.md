# android.drm

# android.drm

Kotlin| [Java](../android/drm/_package.md)
| --- | --- |

## Interfaces

| [OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) | Interface definition for a callback that receives information about DRM framework errors. |
| --- | --- |
| [OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) | Interface definition for a callback that receives information about DRM processing events. |
| [OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) | Interface definition for a callback that receives status messages and warnings during registration and rights acquisition. |
| [ConstraintsColumns](../android/drm/DrmStore.ConstraintsColumns.md) | Interface definition for the columns that represent DRM constraints. |
| --- | --- |

## Classes

| [DrmConvertedStatus](../android/drm/DrmConvertedStatus.md) | An entity class that wraps converted data, conversion status, and the offset for appending the header and body signature to the converted data. |
| --- | --- |
| [DrmErrorEvent](../android/drm/DrmErrorEvent.md) | An entity class that is passed to the [onError()](../android/drm/DrmManagerClient.OnErrorListener.md))callback. |
| [DrmEvent](../android/drm/DrmEvent.md) | A base class that is used to send asynchronous event information from the DRM framework. |
| [DrmInfo](../android/drm/DrmInfo.md) | An entity class that describes the information required to send transactions between a device and an online DRM server. |
| --- | --- |
| [DrmInfoEvent](../android/drm/DrmInfoEvent.md) | An entity class that is passed to the [onInfo()](../android/drm/DrmManagerClient.OnInfoListener.md))callback. |
| [DrmInfoRequest](../android/drm/DrmInfoRequest.md) | An entity class that is used to pass information to an online DRM server. |
| [DrmInfoStatus](../android/drm/DrmInfoStatus.md) | An entity class that wraps the result of communication between a device and an online DRM server. |
| --- | --- |
| [DrmManagerClient](../android/drm/DrmManagerClient.md) | The main programming interface for the DRM framework. |
| [DrmRights](../android/drm/DrmRights.md) | An entity class that wraps the license information retrieved from the online DRM server. |
| [DrmStore](../android/drm/DrmStore.md) | Defines constants that are used by the DRM framework. |
| --- | --- |
| [DrmSupportInfo](../android/drm/DrmSupportInfo.md) | An entity class that wraps the capability of each DRM plug-in (agent), such as the MIME type and file suffix the DRM plug-in can handle. |
| [DrmUtils](../android/drm/DrmUtils.md) | A utility class that provides operations for parsing extended metadata embedded in DRM constraint information. |
| [ProcessedData](../android/drm/ProcessedData.md) | An entity class that wraps the result of a [processDrmInfo()](../android/drm/DrmManagerClient.md))transaction between a device and a DRM server. |
| --- | --- |
