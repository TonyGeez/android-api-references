# android.media

# android.media

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnAudioFocusChangeListener](../android/media/AudioManager.OnAudioFocusChangeListener.md) | Interface definition for a callback to be invoked when the audio focus of the system is updated. |
| --- | --- |
| [OnCommunicationDeviceChangedListener](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md) | Listener registered by client to be notified upon communication audio device change. |
| [OnModeChangedListener](../android/media/AudioManager.OnModeChangedListener.md) | Interface definition of a callback that is notified when the audio mode changes |
| [OnPreferredMixerAttributesChangedListener](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md) | Interface to be notified of changes in the preferred mixer attributes. |
| --- | --- |
| [Key](../android/media/AudioMetadata.Key.md) | Key interface for the`AudioMetadata`map. |
| [AudioMetadataMap](AudioMetadataMap.md) | AudioMetadataMap is a writeable`Map`-style interface of [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) value pairs. |
| [AudioMetadataReadMap](AudioMetadataReadMap.md) | A read only`Map`-style interface of [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) value pairs used for [AudioMetadata](AudioMetadata.md). |
| --- | --- |
| [OnRecordPositionUpdateListener](../android/media/AudioRecord.OnRecordPositionUpdateListener.md) | Interface definition for a callback to be invoked when an AudioRecord has reached a notification marker set by [AudioRecord.setNotificationMarkerPosition(int)](AudioRecord.md))or for periodic updates on the progress of the record head, as set by [AudioRecord.setPositionNotificationPeriod(int)](AudioRecord.md)). |
| [OnRoutingChangedListener](../android/media/AudioRecord.OnRoutingChangedListener.md) | Defines the interface by which applications can receive notifications of routing changes for the associated [AudioRecord](AudioRecord.md). |
| [AudioRecordingMonitor](AudioRecordingMonitor.md) | AudioRecordingMonitor defines an interface implemented by [AudioRecord](AudioRecord.md) and [MediaRecorder](MediaRecorder.md) allowing applications to install a callback and be notified of changes in the capture path while recoding is active. |
| --- | --- |
| [AudioRouting](AudioRouting.md) | AudioRouting defines an interface for controlling routing and routing notifications in AudioTrack and AudioRecord objects. |
| [OnCodecFormatChangedListener](../android/media/AudioTrack.OnCodecFormatChangedListener.md) | Interface definition for a listener for codec format changes. |
| [OnPlaybackPositionUpdateListener](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md) | Interface definition for a callback to be invoked when the playback head position of an AudioTrack has reached a notification marker or has increased by a certain period. |
| --- | --- |
| [OnRoutingChangedListener](../android/media/AudioTrack.OnRoutingChangedListener.md) | Defines the interface by which applications can receive notifications of routing changes for the associated [AudioTrack](AudioTrack.md). |
| [OnImageAvailableListener](../android/media/ImageReader.OnImageAvailableListener.md) | Callback interface for being notified that a new image is available. |
| [OnImageReleasedListener](../android/media/ImageWriter.OnImageReleasedListener.md) | ImageWriter callback interface, used to to asynchronously notify the application of various ImageWriter events. |
| --- | --- |
| [OnJetEventListener](../android/media/JetPlayer.OnJetEventListener.md) | Handles the notification when the JET engine generates an event. |
| [OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md) | Listener used for receiving asynchronous loudness metadata updates. |
| [EventListener](../android/media/MediaCas.EventListener.md) | An interface registered by the caller to [setEventListener](MediaCas.md))to receives scheme-specific notifications from a MediaCas instance. |
| --- | --- |
| [OnFirstTunnelFrameReadyListener](../android/media/MediaCodec.OnFirstTunnelFrameReadyListener.md) | Listener to be called when the first output frame has been decoded and is ready to be rendered for a codec configured for tunnel mode with`KEY_AUDIO_SESSION_ID`. |
| [OnFrameRenderedListener](../android/media/MediaCodec.OnFrameRenderedListener.md) | Listener to be called when an output frame has rendered on the output surface |
| [OnEventListener](../android/media/MediaDrm.OnEventListener.md) | Interface definition for a callback to be invoked when a drm event occurs |
| --- | --- |
| [OnExpirationUpdateListener](../android/media/MediaDrm.OnExpirationUpdateListener.md) | Interface definition for a callback to be invoked when a drm session expiration update occurs |
| [OnKeyStatusChangeListener](../android/media/MediaDrm.OnKeyStatusChangeListener.md) | Interface definition for a callback to be invoked when the keys in a drm session change states. |
| [OnSessionLostStateListener](../android/media/MediaDrm.OnSessionLostStateListener.md) | Interface definition for a callback to be invoked when the session state has been lost and is now invalid |
| --- | --- |
| [MediaDrmThrowable](MediaDrmThrowable.md) | A @ [Throwable](../java.lang/Throwable.md) thrown from [MediaDrm](MediaDrm.md) or @ [MediaCrypto](MediaCrypto.md) APIs |
| [InputReader](../android/media/MediaParser.InputReader.md) | Provides input data to [MediaParser](MediaParser.md). |
| [OutputConsumer](../android/media/MediaParser.OutputConsumer.md) | Receives extracted media sample data and metadata from [MediaParser](MediaParser.md). |
| --- | --- |
| [SeekableInputReader](../android/media/MediaParser.SeekableInputReader.md) | [InputReader](../android/media/MediaParser.InputReader.md) that allows setting the read position. |
| [OnBufferingUpdateListener](../android/media/MediaPlayer.OnBufferingUpdateListener.md) | Interface definition of a callback to be invoked indicating buffering status of a media resource being streamed over the network. |
| [OnCompletionListener](../android/media/MediaPlayer.OnCompletionListener.md) | Interface definition for a callback to be invoked when playback of a media source has completed. |
| --- | --- |
| [OnDrmConfigHelper](../android/media/MediaPlayer.OnDrmConfigHelper.md) | Interface definition of a callback to be invoked when the app can do DRM configuration (get/set properties) before the session is opened. |
| [OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md) | Interface definition of a callback to be invoked when the DRM info becomes available |
| [OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md) | Interface definition of a callback to notify the app when the DRM is ready for key request/response |
| --- | --- |
| [OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) | Interface definition of a callback to be invoked when there has been an error during an asynchronous operation (other errors will throw exceptions at method call time). |
| [OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) | Interface definition of a callback to be invoked to communicate some info and/or warning about the media or its playback. |
| [OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md) | Interface definition of a callback to be invoked when discontinuity in the normal progression of the media time is detected. |
| --- | --- |
| [OnPreparedListener](../android/media/MediaPlayer.OnPreparedListener.md) | Interface definition for a callback to be invoked when the media source is ready for playback. |
| [OnSeekCompleteListener](../android/media/MediaPlayer.OnSeekCompleteListener.md) | Interface definition of a callback to be invoked indicating the completion of a seek operation. |
| [OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md) | Interface definition of a callback to be invoked when a player subtitle track has new subtitle data available. |
| --- | --- |
| [OnTimedMetaDataAvailableListener](../android/media/MediaPlayer.OnTimedMetaDataAvailableListener.md) | Interface definition of a callback to be invoked when a track has timed metadata available. |
| [OnTimedTextListener](../android/media/MediaPlayer.OnTimedTextListener.md) | Interface definition of a callback to be invoked when a timed text is available for display. |
| [OnVideoSizeChangedListener](../android/media/MediaPlayer.OnVideoSizeChangedListener.md) | Interface definition of a callback to be invoked when the video size is first known or updated |
| --- | --- |
| [OnErrorListener](../android/media/MediaRecorder.OnErrorListener.md) | Interface definition for a callback to be invoked when an error occurs while recording. |
| [OnInfoListener](../android/media/MediaRecorder.OnInfoListener.md) | Interface definition of a callback to be invoked to communicate some info and/or warning about the recording. |
| [DeviceSuggestionsUpdatesCallback](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md) | Callback for receiving events about device suggestions |
| --- | --- |
| [OnGetControllerHintsListener](../android/media/MediaRouter2.OnGetControllerHintsListener.md) | A listener interface to send optional app-specific hints when creating a [RoutingController](../android/media/MediaRouter2.RoutingController.md). |
| [MediaScannerConnectionClient](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md) | An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed. |
| [OnScanCompletedListener](../android/media/MediaScannerConnection.OnScanCompletedListener.md) | Interface for notifying clients of the result of scanning a requested media file. |
| --- | --- |
| [OnErrorListener](../android/media/MediaSync.OnErrorListener.md) | Interface definition of a callback to be invoked when there has been an error during an asynchronous operation (other errors will throw exceptions at method call time). |
| [MicrophoneDirection](MicrophoneDirection.md) | Interface defining mechanism for controlling the directionality and field width of audio capture. |
| [OnGetPlaybackPositionListener](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md) | Interface definition for a callback to be invoked when the media playback position is queried. |
| --- | --- |
| [OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md) | Interface definition for a callback to be invoked when one of the metadata values has been updated. |
| [OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md) | Interface definition for a callback to be invoked when the media playback position is requested to be updated. |
| [OnClientUpdateListener](../android/media/RemoteController.OnClientUpdateListener.md) | Interface definition for the callbacks to be invoked whenever media events, metadata and playback status are available. |
| --- | --- |
| [OnLoadCompleteListener](../android/media/SoundPool.OnLoadCompleteListener.md) | <br /> |
| [OnHeadTrackerAvailableListener](../android/media/Spatializer.OnHeadTrackerAvailableListener.md) | Interface to be notified of changes to the availability of a head tracker on the audio device to be used by the spatializer effect. |
| [OnSpatializerStateChangedListener](../android/media/Spatializer.OnSpatializerStateChangedListener.md) | An interface to be notified of changes to the state of the spatializer effect. |
| --- | --- |
| [VolumeAutomation](VolumeAutomation.md) | `VolumeAutomation`defines an interface for automatic volume control of [AudioTrack](AudioTrack.md) and [MediaPlayer](MediaPlayer.md) objects. |

## Classes

| [ApplicationMediaCapabilities](ApplicationMediaCapabilities.md) | ApplicationMediaCapabilities is an immutable class that encapsulates an application's capabilities for handling newer video codec format and media features. |
| --- | --- |
| [AsyncPlayer](AsyncPlayer.md) | Plays a series of audio URIs, but does all the hard work on another thread so that any slowness with preparing or loading doesn't block the calling thread. |
| [AudioAttributes](AudioAttributes.md) | A class to encapsulate a collection of attributes describing information about an audio stream. |
| [AudioDescriptor](AudioDescriptor.md) | The AudioDescriptor contains the information to describe the audio playback/capture capabilities. |
| --- | --- |
| [AudioDeviceCallback](AudioDeviceCallback.md) | AudioDeviceCallback defines the mechanism by which applications can receive notifications of audio device connection and disconnection events. |
| [AudioDeviceInfo](AudioDeviceInfo.md) | Provides information about an audio device. |
| [AudioFocusRequest](AudioFocusRequest.md) | A class to encapsulate information about an audio focus request. |
| --- | --- |
| [AudioFormat](AudioFormat.md) | The [AudioFormat](AudioFormat.md) class is used to access a number of audio format and channel configuration constants. |
| [AudioManager](AudioManager.md) | AudioManager provides access to volume and ringer mode control. |
| [AudioMetadata](AudioMetadata.md) | AudioMetadata class is used to manage typed key-value pairs for configuration and capability requests within the Audio Framework. |
| --- | --- |
| [AudioMixerAttributes](AudioMixerAttributes.md) | Class to represent the attributes of the audio mixer: its format, which represents by an [AudioFormat](AudioFormat.md) object and mixer behavior. |
| [AudioPlaybackCaptureConfiguration](AudioPlaybackCaptureConfiguration.md) | Configuration for capturing audio played by other apps. |
| [AudioPlaybackConfiguration](AudioPlaybackConfiguration.md) | The AudioPlaybackConfiguration class collects the information describing an audio playback session. |
| --- | --- |
| [AudioPresentation](AudioPresentation.md) | The AudioPresentation class encapsulates the information that describes an audio presentation which is available in next generation audio content. |
| [AudioProfile](AudioProfile.md) | An AudioProfile is specific to an audio format and lists supported sampling rates and channel masks for that format. |
| [AudioRecord](AudioRecord.md) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. |
| --- | --- |
| [AudioRecordingConfiguration](AudioRecordingConfiguration.md) | The AudioRecordingConfiguration class collects the information describing an audio recording session. |
| [AudioTimestamp](AudioTimestamp.md) | Structure that groups a position in frame units relative to an assumed audio stream, together with the estimated time when that frame enters or leaves the audio processing pipeline on that device. |
| [AudioTrack](AudioTrack.md) | The AudioTrack class manages and plays a single audio resource for Java applications. |
| --- | --- |
| [CamcorderProfile](CamcorderProfile.md) | Retrieves the predefined camcorder profile settings for camcorder applications. |
| [CameraProfile](CameraProfile.md) | The CameraProfile class is used to retrieve the pre-defined still image capture (jpeg) quality levels (0-100) used for low, medium, and high quality settings in the Camera application. |
| [DrmInitData](DrmInitData.md) | Encapsulates initialization data required by a [MediaDrm](MediaDrm.md) instance. |
| --- | --- |
| [EncoderProfiles](EncoderProfiles.md) | Describes a set of encoding profiles for a given media (audio and/or video) profile. |
| [ExifInterface](ExifInterface.md) | This is a class for reading and writing Exif tags in various image file formats. |
| [FaceDetector](FaceDetector.md) | Identifies the faces of people in a [android.graphics.Bitmap](../android.graphics/Bitmap.md) graphic object. |
| --- | --- |
| [Image](Image.md) | A single complete image buffer to use with a media source such as a [MediaCodec](MediaCodec.md) or a [CameraDevice](../android.hardware.camera2/CameraDevice.md). |
| [ImageReader](ImageReader.md) | The ImageReader class allows direct application access to image data rendered into a [android.view.Surface](../android.view/Surface.md) |
| [ImageWriter](ImageWriter.md) | The ImageWriter class allows an application to produce Image data into a [android.view.Surface](../android.view/Surface.md), and have it be consumed by another component like [CameraDevice](../android.hardware.camera2/CameraDevice.md). |
| --- | --- |
| [JetPlayer](JetPlayer.md) | JetPlayer provides access to JET content playback and control. |
| [LoudnessCodecController](LoudnessCodecController.md) | Class for getting recommended loudness parameter updates for audio decoders as they are used to play back media content according to the encoded format and current audio routing. |
| [MediaActionSound](MediaActionSound.md) | A class for producing sounds that match those produced by various actions taken by the media and camera APIs. |
| --- | --- |
| [MediaCas](MediaCas.md) | MediaCas can be used to obtain keys for descrambling protected media streams, in conjunction with [android.media.MediaDescrambler](MediaDescrambler.md). |
| [MediaCodec](MediaCodec.md) | MediaCodec class can be used to access low-level media codecs, i. |
| [MediaCodecInfo](MediaCodecInfo.md) | Provides information about a given media codec available on the device. |
| --- | --- |
| [MediaCodecList](MediaCodecList.md) | Allows you to enumerate available codecs, each specified as a [MediaCodecInfo](MediaCodecInfo.md) object, find a codec supporting a given format and query the capabilities of a given codec. |
| [MediaCommunicationManager](MediaCommunicationManager.md) | This API is not generally intended for third party application developers. |
| [MediaController2](MediaController2.md) | This API is not generally intended for third party application developers. |
| --- | --- |
| [MediaCrypto](MediaCrypto.md) | MediaCrypto class can be used in conjunction with [android.media.MediaCodec](MediaCodec.md) to decode encrypted media data. |
| [MediaDataSource](MediaDataSource.md) | For supplying media data to the framework. |
| [MediaDescrambler](MediaDescrambler.md) | MediaDescrambler class can be used in conjunction with [android.media.MediaCodec](MediaCodec.md) and [android.media.MediaExtractor](MediaExtractor.md) to decode media data scrambled by conditional access (CA) systems such as those in the ISO/IEC13818-1. |
| --- | --- |
| [MediaDescription](MediaDescription.md) | A simple set of metadata for a media item suitable for display. |
| [MediaDrm](MediaDrm.md) | MediaDrm can be used to obtain keys for decrypting protected media streams, in conjunction with [android.media.MediaCrypto](MediaCrypto.md). |
| [MediaExtractor](MediaExtractor.md) | MediaExtractor facilitates extraction of demuxed, typically encoded, media data from a data source. |
| --- | --- |
| [MediaFeature](MediaFeature.md) | MediaFeature defines various media features, e. |
| [MediaFormat](MediaFormat.md) | Encapsulates the information describing the format of media data, be it audio or video, as well as optional feature metadata. |
| [MediaMetadata](MediaMetadata.md) | Contains metadata about an item, such as the title, artist, etc. |
| --- | --- |
| [MediaMetadataEditor](MediaMetadataEditor.md) | An abstract class for editing and storing metadata that can be published by [RemoteControlClient](RemoteControlClient.md). |
| [MediaMetadataRetriever](MediaMetadataRetriever.md) | MediaMetadataRetriever class provides a unified interface for retrieving frame and meta data from an input media file. |
| [MediaMuxer](MediaMuxer.md) | MediaMuxer facilitates muxing elementary streams. |
| --- | --- |
| [MediaParser](MediaParser.md) | Parses media container formats and extracts contained media samples and metadata. |
| [MediaPlayer](MediaPlayer.md) | MediaPlayer class can be used to control playback of audio/video files and streams. |
| [MediaRecorder](MediaRecorder.md) | Used to record audio and video. |
| --- | --- |
| [MediaRoute2Info](MediaRoute2Info.md) | Describes the properties of a route. |
| [MediaRoute2ProviderService](MediaRoute2ProviderService.md) | Base class for media route provider services. |
| [MediaRouter](MediaRouter.md) | This API is not recommended for new applications. |
| --- | --- |
| [MediaRouter2](MediaRouter2.md) | This API is not generally intended for third party application developers. |
| [MediaScannerConnection](MediaScannerConnection.md) | MediaScannerConnection provides a way for applications to pass a newly created or downloaded media file to the media scanner service. |
| [MediaSession2](MediaSession2.md) | This API is not generally intended for third party application developers. |
| --- | --- |
| [MediaSession2Service](MediaSession2Service.md) | This API is not generally intended for third party application developers. |
| [MediaSync](MediaSync.md) | MediaSync class can be used to synchronously play audio and video streams. |
| [MediaSyncEvent](MediaSyncEvent.md) | The MediaSyncEvent class defines events that can be used to synchronize playback or capture actions between different players and recorders. |
| --- | --- |
| [MediaTimestamp](MediaTimestamp.md) | An immutable object that represents the linear correlation between the media time and the system time. |
| [MicrophoneInfo](MicrophoneInfo.md) | Class providing information on a microphone. |
| [PlaybackParams](PlaybackParams.md) | Structure for common playback params. |
| --- | --- |
| [Rating](Rating.md) | A class to encapsulate rating information used as content metadata. |
| [RemoteControlClient](RemoteControlClient.md) | RemoteControlClient enables exposing information meant to be consumed by remote controls capable of displaying metadata, artwork and media transport control buttons. |
| [RemoteController](RemoteController.md) | The RemoteController class is used to control media playback, display and update media metadata and playback status, published by applications using the [RemoteControlClient](RemoteControlClient.md) class. |
| --- | --- |
| [Ringtone](Ringtone.md) | Ringtone provides a quick method for playing a ringtone, notification, or other similar types of sounds. |
| [RingtoneManager](RingtoneManager.md) | RingtoneManager provides access to ringtones, notification, and other types of sounds. |
| [RouteDiscoveryPreference](RouteDiscoveryPreference.md) | A media route discovery preference describing the features of routes that media router would like to discover and whether to perform active scanning. |
| --- | --- |
| [RouteListingPreference](RouteListingPreference.md) | Allows applications to customize the list of routes used for media routing (for example, in the System UI Output Switcher). |
| [RoutingSessionInfo](RoutingSessionInfo.md) | Describes a routing session which is created when a media route is selected. |
| [Session2Command](Session2Command.md) | This API is not generally intended for third party application developers. |
| --- | --- |
| [Session2CommandGroup](Session2CommandGroup.md) | This API is not generally intended for third party application developers. |
| [Session2Token](Session2Token.md) | This API is not generally intended for third party application developers. |
| [SoundPool](SoundPool.md) | The SoundPool class manages and plays audio resources for applications. |
| --- | --- |
| [Spatializer](Spatializer.md) | Spatializer provides access to querying capabilities and behavior of sound spatialization on the device. |
| [SubtitleData](SubtitleData.md) | Class encapsulating subtitle data, as received through the [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md) interface. |
| [SuggestedDeviceInfo](SuggestedDeviceInfo.md) | Allows applications to suggest routes to the system UI (for example, in the System UI Output Switcher). |
| --- | --- |
| [SyncParams](SyncParams.md) | Structure for common A/V sync params. |
| [ThumbnailUtils](ThumbnailUtils.md) | Utilities for generating visual thumbnails from files. |
| [TimedMetaData](TimedMetaData.md) | Class that embodies one timed metadata access unit, including - a time stamp, and - raw uninterpreted byte-array extracted directly from the container. <br /> |
| --- | --- |
| [TimedText](TimedText.md) | Class to hold the timed text's metadata, including: - The characters for rendering - The rendering position for the timed text <br /> |
| [ToneGenerator](ToneGenerator.md) | This class provides methods to play DTMF tones (ITU-T Recommendation Q.23), call supervisory tones (3GPP TS 22.001, CEPT) and proprietary tones (3GPP TS 31.111). |
| [VolumeProvider](VolumeProvider.md) | Handles requests to adjust or set the volume on a session. |
| --- | --- |
| [VolumeShaper](VolumeShaper.md) | The`VolumeShaper`class is used to automatically control audio volume during media playback, allowing simple implementation of transition effects and ducking. |

## Exceptions

| [DeniedByServerException](DeniedByServerException.md) | Exception thrown when the provisioning server or key server denies a certficate or license for a device. |
| --- | --- |
| [MediaCasException](MediaCasException.md) | Base class for MediaCas exceptions |
| [MediaCasStateException](MediaCasStateException.md) | Base class for MediaCas runtime exceptions |
| [MediaCryptoException](MediaCryptoException.md) | Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object. |
| --- | --- |
| [MediaDrmException](MediaDrmException.md) | Base class for MediaDrm exceptions |
| [MediaDrmResetException](MediaDrmResetException.md) | This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process. |
| [NotProvisionedException](NotProvisionedException.md) | Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate. |
| --- | --- |
| [ResourceBusyException](ResourceBusyException.md) | Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use. |
| [UnsupportedSchemeException](UnsupportedSchemeException.md) | Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device |
