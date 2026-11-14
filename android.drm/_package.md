# android.drm

# android.drm

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) | Interface definition for a callback that receives information about DRM framework errors. |
| --- | --- |
| [OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) | Interface definition for a callback that receives information about DRM processing events. |
| [OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) | Interface definition for a callback that receives status messages and warnings during registration and rights acquisition. |
| [ConstraintsColumns](../android/drm/DrmStore.ConstraintsColumns.md) | Interface definition for the columns that represent DRM constraints. |
| --- | --- |

## Classes

| [DrmConvertedStatus](DrmConvertedStatus.md) | An entity class that wraps converted data, conversion status, and the offset for appending the header and body signature to the converted data. |
| --- | --- |
| [DrmErrorEvent](DrmErrorEvent.md) | An entity class that is passed to the [onError()](../android/drm/DrmManagerClient.OnErrorListener.md))callback. |
| [DrmEvent](DrmEvent.md) | A base class that is used to send asynchronous event information from the DRM framework. |
| [DrmInfo](DrmInfo.md) | An entity class that describes the information required to send transactions between a device and an online DRM server. |
| --- | --- |
| [DrmInfoEvent](DrmInfoEvent.md) | An entity class that is passed to the [onInfo()](../android/drm/DrmManagerClient.OnInfoListener.md))callback. |
| [DrmInfoRequest](DrmInfoRequest.md) | An entity class that is used to pass information to an online DRM server. |
| [DrmInfoStatus](DrmInfoStatus.md) | An entity class that wraps the result of communication between a device and an online DRM server. |
| --- | --- |
| [DrmManagerClient](DrmManagerClient.md) | The main programming interface for the DRM framework. |
| [DrmRights](DrmRights.md) | An entity class that wraps the license information retrieved from the online DRM server. |
| [DrmStore](DrmStore.md) | Defines constants that are used by the DRM framework. |
| --- | --- |
| [DrmSupportInfo](DrmSupportInfo.md) | An entity class that wraps the capability of each DRM plug-in (agent), such as the MIME type and file suffix the DRM plug-in can handle. |
| [DrmUtils](DrmUtils.md) | A utility class that provides operations for parsing extended metadata embedded in DRM constraint information. |
| [ProcessedData](ProcessedData.md) | An entity class that wraps the result of a [processDrmInfo()](DrmManagerClient.md))transaction between a device and a DRM server. |
| --- | --- |
