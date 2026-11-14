# AudioFocusRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioFocusRequest

Kotlin| [Java](../android/media/AudioFocusRequest.md) 
| --- | --- |

```
class AudioFocusRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioFocusRequest](../android/media/AudioFocusRequest.md) |

A class to encapsulate information about an audio focus request. An`AudioFocusRequest`instance is built by [Builder](../android/media/AudioFocusRequest.Builder.md), and is used to request and abandon audio focus, respectively with [AudioManager.requestAudioFocus(AudioFocusRequest)](../android/media/AudioManager.md))and [AudioManager.abandonAudioFocusRequest(AudioFocusRequest)](../android/media/AudioManager.md)).

### What is audio focus?

<br />

Audio focus is a concept introduced in API 8. It is used to convey the fact that a user can only focus on a single audio stream at a time, e.g. listening to music or a podcast, but not both at the same time. In some cases, multiple audio streams can be playing at the same time, but there is only one the user would really listen to (focus on), while the other plays in the background. An example of this is driving directions being spoken while music plays at a reduced volume (a.k.a. ducking).

When an application requests audio focus, it expresses its intention to "own" audio focus to play audio. Let's review the different types of focus requests, the return value after a request, and the responses to a loss.

Note: applications should not play anything until granted focus.

### The different types of focus requests

There are four focus request types. A successful focus request with each will yield different behaviors by the system and the other application that previously held audio focus.

- [AudioManager.AUDIOFOCUS_GAIN](../android/media/AudioManager.md) expresses the fact that your application is now the sole source of audio that the user is listening to. The duration of the audio playback is unknown, and is possibly very long: after the user finishes interacting with your application, (s)he doesn't expect another audio stream to resume. Examples of uses of this focus gain are for music playback, for a game or a video player.
- [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT](../android/media/AudioManager.md) is for a situation when you know your application is temporarily grabbing focus from the current owner, but the user expects playback to go back to where it was once your application no longer requires audio focus. An example is for playing an alarm, or during a VoIP call. The playback is known to be finite: the alarm will time-out or be dismissed, the VoIP call has a beginning and an end. When any of those events ends, and if the user was listening to music when it started, the user expects music to resume, but didn't wish to listen to both at the same time.
- [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK](../android/media/AudioManager.md): this focus request type is similar to`AUDIOFOCUS_GAIN_TRANSIENT`for the temporary aspect of the focus request, but it also expresses the fact during the time you own focus, you allow another application to keep playing at a reduced volume, "ducked". Examples are when playing driving directions or notifications, it's ok for music to keep playing, but not loud enough that it would prevent the directions to be hard to understand. A typical attenuation by the "ducked" application is a factor of 0.2f (or -14dB), that can for instance be applied with`MediaPlayer.setVolume(0.2f)`when using this class for playback.
- [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE](../android/media/AudioManager.md) is also for a temporary request, but also expresses that your application expects the device to not play anything else. This is typically used if you are doing audio recording or speech recognition, and don't want for examples notifications to be played by the system during that time.

An`AudioFocusRequest`instance always contains one of the four types of requests explained above. It is passed when building an`AudioFocusRequest`instance with its builder in the [Builder](../android/media/AudioFocusRequest.Builder.md) constructor [AudioFocusRequest.Builder.Builder(int)](../android/media/AudioFocusRequest.Builder.md)), or with [AudioFocusRequest.Builder.setFocusGain(int)](../android/media/AudioFocusRequest.Builder.md))after copying an existing instance with [AudioFocusRequest.Builder.Builder(AudioFocusRequest)](../android/media/AudioFocusRequest.Builder.md)).
**Note:** If an app targets Android 15 (API level 35) or higher, it cannot request audio focus unless it's the top app or running a foreground service. This requirement is similar to the [requirements for audio playback](../media/media3/session/background-playback.md). If an app requests audio focus when it does not meet these requirements, the method returns [AudioManager.AUDIOFOCUS_REQUEST_FAILED](../android/media/AudioManager.md).

### Qualifying your focus request

#### Use case requiring a focus request

Any focus request is qualified by the [AudioAttributes](../android/media/AudioAttributes.md)(see [Builder.setAudioAttributes(AudioAttributes)](../android/media/AudioFocusRequest.Builder.md))) that describe the audio use case that will follow the request (once it's successful or granted). It is recommended to use the same`AudioAttributes`for the request as the attributes you are using for audio/media playback. 
If no attributes are set, default attributes of [AudioAttributes.USAGE_MEDIA](../android/media/AudioAttributes.md) are used.

#### Delayed focus

Audio focus can be "locked" by the system for a number of reasons: during a phone call, when the car to which the device is connected plays an emergency message... To support these situations, the application can request to be notified when its request is fulfilled, by flagging its request as accepting delayed focus, with [Builder.setAcceptsDelayedFocusGain(boolean)](../android/media/AudioFocusRequest.Builder.md)). 
If focus is requested while being locked by the system, [AudioManager.requestAudioFocus(AudioFocusRequest)](../android/media/AudioManager.md))will return [AudioManager.AUDIOFOCUS_REQUEST_DELAYED](../android/media/AudioManager.md). When focus isn't locked anymore, the focus listener set with [Builder.setOnAudioFocusChangeListener(OnAudioFocusChangeListener)](../android/media/AudioFocusRequest.Builder.md))or with [Builder.setOnAudioFocusChangeListener(OnAudioFocusChangeListener, Handler)](../android/media/AudioFocusRequest.Builder.md))will be called to notify the application it now owns audio focus.

#### Pausing vs ducking

When an application requested audio focus with [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK](../android/media/AudioManager.md), the system will duck the current focus owner.

Note: this behavior is**new for Android O** , whereas applications targeting SDK level up to API 25 had to implement the ducking themselves when they received a focus loss of [AudioManager.AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK](../android/media/AudioManager.md).

But ducking is not always the behavior expected by the user. A typical example is when the device plays driving directions while the user is listening to an audio book or podcast, and expects the audio playback to pause, instead of duck, as it is hard to understand a navigation prompt and spoken content at the same time. Therefore the system will not automatically duck when it detects it would be ducking spoken content: such content is detected when the`AudioAttributes`of the player are qualified by [AudioAttributes.CONTENT_TYPE_SPEECH](../android/media/AudioAttributes.md). Refer for instance to [AudioAttributes.Builder.setContentType(int)](../android/media/AudioAttributes.Builder.md))and [MediaPlayer.setAudioAttributes(AudioAttributes)](../android/media/MediaPlayer.md))if you are writing a media playback application for audio book, podcasts... Since the system will not automatically duck applications that play speech, it calls their focus listener instead to notify them of [AudioManager.AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK](../android/media/AudioManager.md), so they can pause instead. Note that this behavior is independent of the use of`AudioFocusRequest`, but tied to the use of`AudioAttributes`.

If your application requires pausing instead of ducking for any other reason than playing speech, you can also declare so with [Builder.setWillPauseWhenDucked(boolean)](../android/media/AudioFocusRequest.Builder.md)), which will cause the system to call your focus listener instead of automatically ducking.

#### Example

The example below covers the following steps to be found in any application that would play audio, and use audio focus. Here we play an audio book, and our application is intended to pause rather than duck when it loses focus. These steps consist in:

- Creating`AudioAttributes`to be used for the playback and the focus request.
- Configuring and creating the`AudioFocusRequest`instance that defines the intended focus behaviors.
- Requesting audio focus and checking the return code to see if playback can happen right away, or is delayed.
- Implementing a focus change listener to respond to focus gains and losses.

<br />

```kotlin
// initialization of the audio attributes and focus request
  mAudioManager = (AudioManager) Context.getSystemService(Context.AUDIO_SERVICE);
  mPlaybackAttributes = new AudioAttributes.Builder()
          .setUsage(AudioAttributes.USAGE_MEDIA)
          .setContentType(AudioAttributes.CONTENT_TYPE_SPEECH)
          .build();
  mFocusRequest = new AudioFocusRequest.Builder(AudioManager.AUDIOFOCUS_GAIN)
          .setAudioAttributes(mPlaybackAttributes)
          .setAcceptsDelayedFocusGain(true)
          .setWillPauseWhenDucked(true)
          .setOnAudioFocusChangeListener(this, mMyHandler)
          .build();
  mMediaPlayer = new MediaPlayer();
  mMediaPlayer.setAudioAttributes(mPlaybackAttributes);
  final Object mFocusLock = new Object();
 
  boolean mPlaybackDelayed = false;
 
  // requesting audio focus
  int res = mAudioManager.requestAudioFocus(mFocusRequest);
  synchronized (mFocusLock) {
      if (res == AudioManager.AUDIOFOCUS_REQUEST_FAILED) {
          mPlaybackDelayed = false;
      } else if (res == AudioManager.AUDIOFOCUS_REQUEST_GRANTED) {
          mPlaybackDelayed = false;
          playbackNow();
      } else if (res == AudioManager.AUDIOFOCUS_REQUEST_DELAYED) {
         mPlaybackDelayed = true;
      }
  }
 
  // implementation of the OnAudioFocusChangeListener
  @Override
  public void onAudioFocusChange(int focusChange) {
      switch (focusChange) {
          case AudioManager.AUDIOFOCUS_GAIN:
              if (mPlaybackDelayed || mResumeOnFocusGain) {
                  synchronized (mFocusLock) {
                      mPlaybackDelayed = false;
                      mResumeOnFocusGain = false;
                  }
                  playbackNow();
              }
              break;
          case AudioManager.AUDIOFOCUS_LOSS:
              synchronized (mFocusLock) {
                  // this is not a transient loss, we shouldn't automatically resume for now
                  mResumeOnFocusGain = false;
                  mPlaybackDelayed = false;
              }
              pausePlayback();
              break;
          case AudioManager.AUDIOFOCUS_LOSS_TRANSIENT:
          case AudioManager.AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK:
              // we handle all transient losses the same way because we never duck audio books
              synchronized (mFocusLock) {
                  // we should only resume if playback was interrupted
                  mResumeOnFocusGain = mMediaPlayer.isPlaying();
                  mPlaybackDelayed = false;
              }
              pausePlayback();
              break;
      }
  }
 
  // Important:
  // Also set "mResumeOnFocusGain" to false when the user pauses or stops playback: this way your
  // application doesn't automatically restart when it gains focus, even though the user had
  // stopped it.
  
```

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/AudioFocusRequest.Builder.md) Builder class for [AudioFocusRequest](../android/media/AudioFocusRequest.md) objects. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [acceptsDelayedFocusGain](../android/media/AudioFocusRequest.md))`()` Returns whether the application that would use this`AudioFocusRequest`supports a focus gain granted after a temporary request failure. |
| [AudioAttributes](../android/media/AudioAttributes.md) | [getAudioAttributes](../android/media/AudioFocusRequest.md))`()` Returns the [AudioAttributes](../android/media/AudioAttributes.md) set for this`AudioFocusRequest`, or the default attributes if none were set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFocusGain](../android/media/AudioFocusRequest.md))`()` Returns the type of audio focus request configured for this`AudioFocusRequest`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willPauseWhenDucked](../android/media/AudioFocusRequest.md))`()` Returns whether the application that would use this`AudioFocusRequest`would pause when it is requested to duck. |

## Public methods

### acceptsDelayedFocusGain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun acceptsDelayedFocusGain(): Boolean
```

Returns whether the application that would use this`AudioFocusRequest`supports a focus gain granted after a temporary request failure.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether delayed focus gain is supported. |

### getAudioAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioAttributes(): AudioAttributes
```

Returns the [AudioAttributes](../android/media/AudioAttributes.md) set for this`AudioFocusRequest`, or the default attributes if none were set.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [AudioAttributes](../android/media/AudioAttributes.md) | non-null [AudioAttributes](../android/media/AudioAttributes.md). |

### getFocusGain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFocusGain(): Int
```

Returns the type of audio focus request configured for this`AudioFocusRequest`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [AudioManager.AUDIOFOCUS_GAIN](../android/media/AudioManager.md), [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT](../android/media/AudioManager.md), [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK](../android/media/AudioManager.md), and [AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE](../android/media/AudioManager.md). |

### willPauseWhenDucked

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun willPauseWhenDucked(): Boolean
```

Returns whether the application that would use this`AudioFocusRequest`would pause when it is requested to duck.

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the duck/pause behavior. |
