# ToneGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ToneGenerator

Kotlin| [Java](https://developer.android.com/reference/android/media/ToneGenerator "View this page in Java") 
| --- | --- |

```
open class ToneGenerator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ToneGenerator](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#) |

This class provides methods to play DTMF tones (ITU-T Recommendation Q.23), call supervisory tones (3GPP TS 22.001, CEPT) and proprietary tones (3GPP TS 31.111). Depending on call state and routing options, tones are mixed to the downlink audio or output to the speaker phone or headset. This API is not for generating tones over the uplink audio path.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_VOLUME](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#MAX_VOLUME:kotlin.Int) Maximum volume, for use with [ToneGenerator(int,int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_VOLUME](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#MIN_VOLUME:kotlin.Int) Minimum volume setting, for use with [ToneGenerator(int,int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ABBR_ALERT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_ALERT:kotlin.Int) CDMA_ABBR_ALERT tone: 1150Hz+770Hz 400ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ABBR_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_INTERCEPT:kotlin.Int) CDMA Abbr Intercept tone: 440Hz 250ms ON, 620Hz 250ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ABBR_REORDER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_REORDER:kotlin.Int) CDMA Abbr Reorder tone: 480Hz+620Hz 250ms ON, 250ms OFF repeated for 8 times |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ALERT_AUTOREDIAL_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_AUTOREDIAL_LITE:kotlin.Int) CDMA Alert Auto Redial tone: {1245Hz 62ms ON, 659Hz 62ms ON} 3 times, 1245 62ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ALERT_CALL_GUARD](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_CALL_GUARD:kotlin.Int) CDMA ALERT CALL GUARD tone: {1319Hz 125ms ON, 125ms OFF} 3 times |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ALERT_INCALL_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_INCALL_LITE:kotlin.Int) CDMA ALERT INCALL LITE tone: 587Hz 62ms, 784 62ms, 831Hz 62ms, 784Hz 62ms, 1109 62ms, 784Hz 62ms, 831Hz 62ms, 784Hz 62ms |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ALERT_NETWORK_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_NETWORK_LITE:kotlin.Int) CDMA Alert Network Lite tone: 1109Hz 62ms ON, 784Hz 62ms ON, 740Hz 62ms ON 622Hz 62ms ON, 1109Hz 62ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ANSWER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ANSWER:kotlin.Int) CDMA answer tone: silent tone - defintion Frequency 0, 0ms ON, 0ms OFF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALLDROP_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALLDROP_LITE:kotlin.Int) CDMA CALLDROP LITE tone: 1480Hz 125ms, 1397Hz 125ms, 784Hz 125ms |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP:kotlin.Int) ISDN Call Signal Intergroup tone: {2091Hz 32ms ON, 2556 64ms ON} 8 times, 2091Hz 32ms ON, 400ms OFF, {2091Hz 32ms ON, 2556Hz 64ms ON} times, 2091Hz 32ms ON, 4s OFF. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL:kotlin.Int) ISDN Call Signal Normal tone: {2091Hz 32ms ON, 2556 64ms ON} 20 times, 2091 32ms ON, 2556 48ms ON, 4s OFF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_PAT3](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT3:kotlin.Int) ISDN Call sign PAT3 tone: silent tone |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_PAT5](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT5:kotlin.Int) ISDN Pat5 tone: silent tone |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_PAT6](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT6:kotlin.Int) ISDN Pat6 tone: silent tone |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_PAT7](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT7:kotlin.Int) ISDN Pat7 tone: silent tone |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING:kotlin.Int) ISDN Ping Ring tone: {2091Hz 32ms ON, 2556Hz 64ms ON} 5 times 2091Hz 20ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI:kotlin.Int) ISDN Call Signal SP PRI tone:{2091Hz 32ms ON, 2556 64ms ON} 4 times 2091Hz 16ms ON, 200ms OFF, {2091Hz 32ms ON, 2556Hz 64ms ON} 4 times, 2091Hz 16ms ON, 200ms OFF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_CONFIRM](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CONFIRM:kotlin.Int) CDMA Confirm tone: 350Hz+440Hz 100ms ON, 100ms OFF repeated for 3 times |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_DIAL_TONE_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_DIAL_TONE_LITE:kotlin.Int) CDMA Dial tone : 425Hz continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_EMERGENCY_RINGBACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_EMERGENCY_RINGBACK:kotlin.Int) CDMA EMERGENCY RINGBACK tone: {941Hz 125ms ON, 10ms OFF} 3times 4990ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_L:kotlin.Int) TONE_CDMA_HIGH_L tone: {3700Hz 25ms, 4000Hz 25ms} 40 times 4000ms OFF, Repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_L:kotlin.Int) CDMA HIGH PBX L: {3700Hz 25ms, 4000Hz 25ms}20 times, 2000ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SLS:kotlin.Int) CDMA HIGH PBX SSL tone:{3700Hz 25ms, 4000Hz 25ms} 8 times 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 16 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 8 times, 1000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SS:kotlin.Int) CDMA HIGH PBX SS tone: {3700Hz 25ms, 4000Hz 25ms} 8 times 200 ms OFF, {3700Hz 25ms 4000Hz 25ms}8 times, 2000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SSL:kotlin.Int) CDMA HIGH PBX SSL tone:{3700Hz 25ms, 4000Hz 25ms} 8 times 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 16 times, 1000ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_S_X4:kotlin.Int) CDMA HIGH PBX X S4 tone: {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 800ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SLS:kotlin.Int) CDMA HIGH SLS tone: {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 20 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 3000ms OFF, REPEAT |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SS:kotlin.Int) CDMA HIGH SS tone: {3700Hz 25ms, 4000Hz 25ms} repeat 16 times, 400ms OFF, repeat . |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SSL:kotlin.Int) CDMA HIGH SSL tone: {3700Hz 25ms, 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} repeat 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} repeat 16 times, 4000ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SS_2:kotlin.Int) CDMA HIGH SS2 tone: {3700Hz 25ms, 4000Hz 25ms} 20 times, 1000ms OFF, {3700Hz 25ms, 4000Hz 25ms} 20 times, 3000ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_HIGH_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_S_X4:kotlin.Int) CDMA HIGH S X4 tone: {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 2500ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_INTERCEPT:kotlin.Int) CDMA Intercept tone: 440Hz 250ms ON, 620Hz 250ms ON . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_KEYPAD_VOLUME_KEY_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_KEYPAD_VOLUME_KEY_LITE:kotlin.Int) CDMA KEYPAD Volume key lite tone: 941Hz+1477Hz 120ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_L:kotlin.Int) TONE_CDMA_LOW_L tone: {1300Hz 25ms, 1450Hz 25ms} 40 times, 4000ms OFF, Repeat . |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_L:kotlin.Int) CDMA LOW PBX L: {1300Hz 25ms,1450Hz 25ms}20 times, 2000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SLS:kotlin.Int) CDMA HIGH PBX SLS tone:{1300Hz 25ms, 1450Hz 25ms} 8 times 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 16 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 8 times, 1000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SS:kotlin.Int) CDMA LOW PBX SS tone: {1300Hz 25ms, 1450Hz 25ms} 8 times 200 ms OFF, {1300Hz 25ms 1450Hz 25ms}8 times, 2000ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SSL:kotlin.Int) CDMA LOW PBX SSL tone:{1300Hz 25ms, 1450Hz 25ms} 8 times 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 16 times, 1000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_S_X4:kotlin.Int) CDMA LOW PBX X S4 tone: {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 800ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SLS:kotlin.Int) CDMA LOW SLS tone: {1300Hz 25ms, 1450Hz 25ms} 10 times, 500ms OFF, {1300Hz 25ms, 1450Hz 25ms} 20 times, 500ms OFF, {1300Hz 25ms, 1450Hz 25ms} 10 times, 3000ms OFF, REPEAT |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SS:kotlin.Int) CDMA LOW SS tone: {1300z 25ms, 1450Hz 25ms} repeat 16 times, 400ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SSL:kotlin.Int) CDMA LOW SSL tone: {1300Hz 25ms, 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} repeat 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} repeat 16 times, 4000ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SS_2:kotlin.Int) CDMA LOW SS2 tone: {1300Hz 25ms, 1450Hz 25ms} 20 times, 1000ms OFF, {1300Hz 25ms, 1450Hz 25ms} 20 times, 3000ms OFF, repeat . |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_LOW_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_S_X4:kotlin.Int) CDMA LOW S X4 tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 2500ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_L:kotlin.Int) TONE_CDMA_MED_L tone: {2600Hz 25ms, 2900Hz 25ms} 40 times 4000ms OFF, Repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_L:kotlin.Int) CDMA MED PBX L: {2600Hz 25ms, 2900Hz 25ms}20 times, 2000ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SLS:kotlin.Int) CDMA HIGH PBX SLS tone:{2600Hz 25ms, 2900Hz 25ms} 8 times 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 16 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 8 times, 1000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SS:kotlin.Int) CDMA MED PBX SS tone: {2600Hz 25ms, 2900Hz 25ms} 8 times 200 ms OFF, {2600Hz 25ms 2900Hz 25ms}8 times, 2000ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SSL:kotlin.Int) CDMA MED PBX SSL tone:{2600Hz 25ms, 2900Hz 25ms} 8 times 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 16 times, 1000ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_S_X4:kotlin.Int) CDMA MED PBX X S4 tone: {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 800ms OFF, REPEAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SLS:kotlin.Int) CDMA MED SLS tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 20 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 3000ms OFF, REPEAT |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SS:kotlin.Int) CDMA MED SS tone: {2600Hz 25ms, 2900Hz 25ms} repeat 16 times, 400ms OFF, repeat . |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SSL:kotlin.Int) CDMA MED SSL tone: {2600Hz 25ms, 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} repeat 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} repeat 16 times, 4000ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SS_2:kotlin.Int) CDMA MED SS2 tone: {2600Hz 25ms, 2900Hz 25ms} 20 times, 1000ms OFF, {2600Hz 25ms, 2900Hz 25ms} 20 times, 3000ms OFF, repeat . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_MED_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_S_X4:kotlin.Int) CDMA MED S X4 tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 2500ms OFF, REPEAT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_NETWORK_BUSY](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_BUSY:kotlin.Int) CDMA Network Busy tone: 480Hz+620Hz 500ms ON, 500ms OFF continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_NETWORK_BUSY_ONE_SHOT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_BUSY_ONE_SHOT:kotlin.Int) CDMA_NETWORK_BUSY_ONE_SHOT tone: 425Hz 500ms ON, 500ms OFF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_NETWORK_CALLWAITING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_CALLWAITING:kotlin.Int) CDMA Network Callwaiting tone: 440Hz 300ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_NETWORK_USA_RINGBACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_USA_RINGBACK:kotlin.Int) CDMA USA Ringback: 440Hz+480Hz 2s ON, 4000 OFF . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_ONE_MIN_BEEP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ONE_MIN_BEEP:kotlin.Int) CDMA One Min Beep tone: 1150Hz+770Hz 400ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_PIP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_PIP:kotlin.Int) CDMA PIP tone: 480Hz 100ms ON, 100ms OFF repeated for 4 times |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_PRESSHOLDKEY_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_PRESSHOLDKEY_LITE:kotlin.Int) CDMA PRESSHOLDKEY LITE tone: 587Hz 375ms ON, 1175Hz 125ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_REORDER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_REORDER:kotlin.Int) CDMA Reorder tone: 480Hz+620Hz 250ms ON, 250ms OFF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_SIGNAL_OFF](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_SIGNAL_OFF:kotlin.Int) CDMA_SIGNAL_OFF - silent tone |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_CDMA_SOFT_ERROR_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_SOFT_ERROR_LITE:kotlin.Int) CDMA SOFT ERROR LITE tone: 1047Hz 125ms ON, 370Hz 125ms |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_0](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_0:kotlin.Int) DTMF tone for key 0: 1336Hz, 941Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_1](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_1:kotlin.Int) DTMF tone for key 1: 1209Hz, 697Hz, continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_2:kotlin.Int) DTMF tone for key 2: 1336Hz, 697Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_3](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_3:kotlin.Int) DTMF tone for key 3: 1477Hz, 697Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_4:kotlin.Int) DTMF tone for key 4: 1209Hz, 770Hz, continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_5](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_5:kotlin.Int) DTMF tone for key 5: 1336Hz, 770Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_6](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_6:kotlin.Int) DTMF tone for key 6: 1477Hz, 770Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_7](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_7:kotlin.Int) DTMF tone for key 7: 1209Hz, 852Hz, continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_8](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_8:kotlin.Int) DTMF tone for key 8: 1336Hz, 852Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_9](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_9:kotlin.Int) DTMF tone for key 9: 1477Hz, 852Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_A](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_A:kotlin.Int) DTMF tone for key A: 1633Hz, 697Hz, continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_B](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_B:kotlin.Int) DTMF tone for key B: 1633Hz, 770Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_C](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_C:kotlin.Int) DTMF tone for key C: 1633Hz, 852Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_D](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_D:kotlin.Int) DTMF tone for key D: 1633Hz, 941Hz, continuous |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_P](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_P:kotlin.Int) DTMF tone for key #: 1477Hz, 941Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_DTMF_S](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_S:kotlin.Int) DTMF tone for key \*: 1209Hz, 941Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_PROP_ACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_ACK:kotlin.Int) Proprietary tone, positive acknowlegement: 1200Hz, 100ms ON, 100ms OFF 2 bursts |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_PROP_BEEP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_BEEP:kotlin.Int) Proprietary tone, general beep: 400Hz+1200Hz, 35ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_PROP_BEEP2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_BEEP2:kotlin.Int) Proprietary tone, general double beep: twice 400Hz+1200Hz, 35ms ON, 200ms OFF, 35ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_PROP_NACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_NACK:kotlin.Int) Proprietary tone, negative acknowlegement: 300Hz+400Hz+500Hz, 400ms ON |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_PROP_PROMPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_PROMPT:kotlin.Int) Proprietary tone, prompt tone: 400Hz+1200Hz, 200ms ON |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_BUSY](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_BUSY:kotlin.Int) Call supervisory tone, Busy: CEPT: 425Hz, 500ms ON, 500ms OFF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_CALL_WAITING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CALL_WAITING:kotlin.Int) Call supervisory tone, Call Waiting: CEPT, JAPAN: 425Hz, 200ms ON, 600ms OFF, 200ms ON, 3s OFF. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_CONFIRM](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONFIRM:kotlin.Int) Call supervisory tone (IS-95), confirm tone: a 350 Hz tone added to a 440 Hz tone repeated 3 times in a 100 ms on, 100 ms off cycle |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_CONGESTION](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONGESTION:kotlin.Int) Call supervisory tone, Congestion: CEPT, JAPAN: 425Hz, 200ms ON, 200ms OFF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_CONGESTION_ABBREV](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONGESTION_ABBREV:kotlin.Int) Call supervisory tone (IS-95), abbreviated congestion: congestion tone limited to 4 seconds |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_DIAL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_DIAL:kotlin.Int) Call supervisory tone, Dial tone: CEPT: 425Hz, continuous ANSI (IS-95): 350Hz+440Hz, continuous JAPAN: 400Hz, continuous |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_ERROR](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_ERROR:kotlin.Int) Call supervisory tone, Error/Special info: 950Hz+1400Hz+1800Hz, 330ms ON, 1s OFF. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_INTERCEPT:kotlin.Int) Call supervisory tone (IS-95), intercept tone: alternating 440 Hz and 620 Hz tones, each on for 250 ms |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_INTERCEPT_ABBREV](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_INTERCEPT_ABBREV:kotlin.Int) Call supervisory tone (IS-95), abbreviated intercept: intercept tone limited to 4 seconds |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_PIP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_PIP:kotlin.Int) Call supervisory tone (IS-95), pip tone: four bursts of 480 Hz tone (0.1 s on, 0.1 s off). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_RADIO_ACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RADIO_ACK:kotlin.Int) Call supervisory tone, Radio path acknowlegment : CEPT, ANSI: 425Hz, 200ms ON JAPAN: 400Hz, 1s ON, 2s OFF. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_RADIO_NOTAVAIL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RADIO_NOTAVAIL:kotlin.Int) Call supervisory tone, Radio path not available: 425Hz, 200ms ON, 200 OFF 3 bursts |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TONE_SUP_RINGTONE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RINGTONE:kotlin.Int) Call supervisory tone, Ring Tone: CEPT, JAPAN: 425Hz, 1s ON, 4s OFF. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ToneGenerator](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `volume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` ToneGenerator class contructor specifying output stream type and volume. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSessionId](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#getAudioSessionId())`()` Returns the audio session ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#release())`()` Releases resources associated with this ToneGenerator object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [startTone](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#startTone(kotlin.Int))`(`toneType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method starts the playback of a tone of the specified type. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [startTone](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#startTone(kotlin.Int,%20kotlin.Int))`(`toneType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `durationMs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method starts the playback of a tone of the specified type for the specified duration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopTone](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#stopTone())`()` This method stops the tone currently playing playback. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#finalize())`()` <br /> |

## Constants

### MAX_VOLUME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VOLUME: Int
```

Maximum volume, for use with [ToneGenerator(int,int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

 Value: 100

### MIN_VOLUME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VOLUME: Int
```

Minimum volume setting, for use with [ToneGenerator(int,int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

 Value: 0

### TONE_CDMA_ABBR_ALERT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ABBR_ALERT: Int
```

CDMA_ABBR_ALERT tone: 1150Hz+770Hz 400ms ON 

 Value: 97

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ABBR_INTERCEPT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ABBR_INTERCEPT: Int
```

CDMA Abbr Intercept tone: 440Hz 250ms ON, 620Hz 250ms ON 

 Value: 37

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ABBR_REORDER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ABBR_REORDER: Int
```

CDMA Abbr Reorder tone: 480Hz+620Hz 250ms ON, 250ms OFF repeated for 8 times 

 Value: 39

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ALERT_AUTOREDIAL_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ALERT_AUTOREDIAL_LITE: Int
```

CDMA Alert Auto Redial tone: {1245Hz 62ms ON, 659Hz 62ms ON} 3 times, 1245 62ms ON 

 Value: 87

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ALERT_CALL_GUARD

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ALERT_CALL_GUARD: Int
```

CDMA ALERT CALL GUARD tone: {1319Hz 125ms ON, 125ms OFF} 3 times 

 Value: 93

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ALERT_INCALL_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ALERT_INCALL_LITE: Int
```

CDMA ALERT INCALL LITE tone: 587Hz 62ms, 784 62ms, 831Hz 62ms, 784Hz 62ms, 1109 62ms, 784Hz 62ms, 831Hz 62ms, 784Hz 62ms 

 Value: 91

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ALERT_NETWORK_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ALERT_NETWORK_LITE: Int
```

CDMA Alert Network Lite tone: 1109Hz 62ms ON, 784Hz 62ms ON, 740Hz 62ms ON 622Hz 62ms ON, 1109Hz 62ms ON 

 Value: 86

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ANSWER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ANSWER: Int
```

CDMA answer tone: silent tone - defintion Frequency 0, 0ms ON, 0ms OFF 

 Value: 42

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALLDROP_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALLDROP_LITE: Int
```

CDMA CALLDROP LITE tone: 1480Hz 125ms, 1397Hz 125ms, 784Hz 125ms 

 Value: 95

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP: Int
```

ISDN Call Signal Intergroup tone: {2091Hz 32ms ON, 2556 64ms ON} 8 times, 2091Hz 32ms ON, 400ms OFF, {2091Hz 32ms ON, 2556Hz 64ms ON} times, 2091Hz 32ms ON, 4s OFF. 

 Value: 46

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL: Int
```

ISDN Call Signal Normal tone: {2091Hz 32ms ON, 2556 64ms ON} 20 times, 2091 32ms ON, 2556 48ms ON, 4s OFF 

 Value: 45

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_PAT3

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_PAT3: Int
```

ISDN Call sign PAT3 tone: silent tone 

 Value: 48

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_PAT5

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_PAT5: Int
```

ISDN Pat5 tone: silent tone 

 Value: 50

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_PAT6

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_PAT6: Int
```

ISDN Pat6 tone: silent tone 

 Value: 51

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_PAT7

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_PAT7: Int
```

ISDN Pat7 tone: silent tone 

 Value: 52

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING: Int
```

ISDN Ping Ring tone: {2091Hz 32ms ON, 2556Hz 64ms ON} 5 times 2091Hz 20ms ON 

 Value: 49

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI: Int
```

ISDN Call Signal SP PRI tone:{2091Hz 32ms ON, 2556 64ms ON} 4 times 2091Hz 16ms ON, 200ms OFF, {2091Hz 32ms ON, 2556Hz 64ms ON} 4 times, 2091Hz 16ms ON, 200ms OFF 

 Value: 47

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_CONFIRM

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_CONFIRM: Int
```

CDMA Confirm tone: 350Hz+440Hz 100ms ON, 100ms OFF repeated for 3 times 

 Value: 41

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_DIAL_TONE_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_DIAL_TONE_LITE: Int
```

CDMA Dial tone : 425Hz continuous 

 Value: 34

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_EMERGENCY_RINGBACK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_EMERGENCY_RINGBACK: Int
```

CDMA EMERGENCY RINGBACK tone: {941Hz 125ms ON, 10ms OFF} 3times 4990ms OFF, REPEAT... 

 Value: 92

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_L: Int
```

TONE_CDMA_HIGH_L tone: {3700Hz 25ms, 4000Hz 25ms} 40 times 4000ms OFF, Repeat .... 

 Value: 53

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_PBX_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_PBX_L: Int
```

CDMA HIGH PBX L: {3700Hz 25ms, 4000Hz 25ms}20 times, 2000ms OFF, REPEAT.... 

 Value: 71

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_PBX_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_PBX_SLS: Int
```

CDMA HIGH PBX SSL tone:{3700Hz 25ms, 4000Hz 25ms} 8 times 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 16 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 8 times, 1000ms OFF, REPEAT.... 

 Value: 80

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_PBX_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_PBX_SS: Int
```

CDMA HIGH PBX SS tone: {3700Hz 25ms, 4000Hz 25ms} 8 times 200 ms OFF, {3700Hz 25ms 4000Hz 25ms}8 times, 2000ms OFF, REPEAT.... 

 Value: 74

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_PBX_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_PBX_SSL: Int
```

CDMA HIGH PBX SSL tone:{3700Hz 25ms, 4000Hz 25ms} 8 times 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} 16 times, 1000ms OFF, REPEAT.... 

 Value: 77

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_PBX_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_PBX_S_X4: Int
```

CDMA HIGH PBX X S4 tone: {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms 4000Hz 25ms} 8 times, 800ms OFF, REPEAT... 

 Value: 83

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_SLS: Int
```

CDMA HIGH SLS tone: {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 20 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 3000ms OFF, REPEAT 

 Value: 65

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_SS: Int
```

CDMA HIGH SS tone: {3700Hz 25ms, 4000Hz 25ms} repeat 16 times, 400ms OFF, repeat .... 

 Value: 56

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_SSL: Int
```

CDMA HIGH SSL tone: {3700Hz 25ms, 4000Hz 25ms} 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} repeat 8 times, 200ms OFF, {3700Hz 25ms, 4000Hz 25ms} repeat 16 times, 4000ms OFF, repeat ... 

 Value: 59

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_SS_2

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_SS_2: Int
```

CDMA HIGH SS2 tone: {3700Hz 25ms, 4000Hz 25ms} 20 times, 1000ms OFF, {3700Hz 25ms, 4000Hz 25ms} 20 times, 3000ms OFF, repeat .... 

 Value: 62

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_HIGH_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_HIGH_S_X4: Int
```

CDMA HIGH S X4 tone: {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 500ms OFF, {3700Hz 25ms, 4000Hz 25ms} 10 times, 2500ms OFF, REPEAT.... 

 Value: 68

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_INTERCEPT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_INTERCEPT: Int
```

CDMA Intercept tone: 440Hz 250ms ON, 620Hz 250ms ON ... 

 Value: 36

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_KEYPAD_VOLUME_KEY_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_KEYPAD_VOLUME_KEY_LITE: Int
```

CDMA KEYPAD Volume key lite tone: 941Hz+1477Hz 120ms ON 

 Value: 89

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_L: Int
```

TONE_CDMA_LOW_L tone: {1300Hz 25ms, 1450Hz 25ms} 40 times, 4000ms OFF, Repeat .... 

 Value: 55

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_PBX_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_PBX_L: Int
```

CDMA LOW PBX L: {1300Hz 25ms,1450Hz 25ms}20 times, 2000ms OFF, REPEAT.... 

 Value: 73

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_PBX_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_PBX_SLS: Int
```

CDMA HIGH PBX SLS tone:{1300Hz 25ms, 1450Hz 25ms} 8 times 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 16 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 8 times, 1000ms OFF, REPEAT.... 

 Value: 82

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_PBX_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_PBX_SS: Int
```

CDMA LOW PBX SS tone: {1300Hz 25ms, 1450Hz 25ms} 8 times 200 ms OFF, {1300Hz 25ms 1450Hz 25ms}8 times, 2000ms OFF, REPEAT.... 

 Value: 76

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_PBX_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_PBX_SSL: Int
```

CDMA LOW PBX SSL tone:{1300Hz 25ms, 1450Hz 25ms} 8 times 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} 16 times, 1000ms OFF, REPEAT.... 

 Value: 79

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_PBX_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_PBX_S_X4: Int
```

CDMA LOW PBX X S4 tone: {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms 1450Hz 25ms} 8 times, 800ms OFF, REPEAT... 

 Value: 85

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_SLS: Int
```

CDMA LOW SLS tone: {1300Hz 25ms, 1450Hz 25ms} 10 times, 500ms OFF, {1300Hz 25ms, 1450Hz 25ms} 20 times, 500ms OFF, {1300Hz 25ms, 1450Hz 25ms} 10 times, 3000ms OFF, REPEAT 

 Value: 67

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_SS: Int
```

CDMA LOW SS tone: {1300z 25ms, 1450Hz 25ms} repeat 16 times, 400ms OFF, repeat .... 

 Value: 58

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_SSL: Int
```

CDMA LOW SSL tone: {1300Hz 25ms, 1450Hz 25ms} 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} repeat 8 times, 200ms OFF, {1300Hz 25ms, 1450Hz 25ms} repeat 16 times, 4000ms OFF, repeat ... 

 Value: 61

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_SS_2

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_SS_2: Int
```

CDMA LOW SS2 tone: {1300Hz 25ms, 1450Hz 25ms} 20 times, 1000ms OFF, {1300Hz 25ms, 1450Hz 25ms} 20 times, 3000ms OFF, repeat .... 

 Value: 64

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_LOW_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_LOW_S_X4: Int
```

CDMA LOW S X4 tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 2500ms OFF, REPEAT.... 

 Value: 70

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_L: Int
```

TONE_CDMA_MED_L tone: {2600Hz 25ms, 2900Hz 25ms} 40 times 4000ms OFF, Repeat .... 

 Value: 54

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_PBX_L

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_PBX_L: Int
```

CDMA MED PBX L: {2600Hz 25ms, 2900Hz 25ms}20 times, 2000ms OFF, REPEAT.... 

 Value: 72

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_PBX_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_PBX_SLS: Int
```

CDMA HIGH PBX SLS tone:{2600Hz 25ms, 2900Hz 25ms} 8 times 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 16 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 8 times, 1000ms OFF, REPEAT.... 

 Value: 81

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_PBX_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_PBX_SS: Int
```

CDMA MED PBX SS tone: {2600Hz 25ms, 2900Hz 25ms} 8 times 200 ms OFF, {2600Hz 25ms 2900Hz 25ms}8 times, 2000ms OFF, REPEAT.... 

 Value: 75

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_PBX_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_PBX_SSL: Int
```

CDMA MED PBX SSL tone:{2600Hz 25ms, 2900Hz 25ms} 8 times 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} 16 times, 1000ms OFF, REPEAT.... 

 Value: 78

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_PBX_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_PBX_S_X4: Int
```

CDMA MED PBX X S4 tone: {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms 2900Hz 25ms} 8 times, 800ms OFF, REPEAT... 

 Value: 84

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_SLS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_SLS: Int
```

CDMA MED SLS tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 20 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 3000ms OFF, REPEAT 

 Value: 66

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_SS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_SS: Int
```

CDMA MED SS tone: {2600Hz 25ms, 2900Hz 25ms} repeat 16 times, 400ms OFF, repeat .... 

 Value: 57

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_SSL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_SSL: Int
```

CDMA MED SSL tone: {2600Hz 25ms, 2900Hz 25ms} 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} repeat 8 times, 200ms OFF, {2600Hz 25ms, 2900Hz 25ms} repeat 16 times, 4000ms OFF, repeat ... 

 Value: 60

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_SS_2

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_SS_2: Int
```

CDMA MED SS2 tone: {2600Hz 25ms, 2900Hz 25ms} 20 times, 1000ms OFF, {2600Hz 25ms, 2900Hz 25ms} 20 times, 3000ms OFF, repeat .... 

 Value: 63

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_MED_S_X4

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_MED_S_X4: Int
```

CDMA MED S X4 tone: {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 500ms OFF, {2600Hz 25ms, 2900Hz 25ms} 10 times, 2500ms OFF, REPEAT.... 

 Value: 69

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_NETWORK_BUSY

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_NETWORK_BUSY: Int
```

CDMA Network Busy tone: 480Hz+620Hz 500ms ON, 500ms OFF continuous 

 Value: 40

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_NETWORK_BUSY_ONE_SHOT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_NETWORK_BUSY_ONE_SHOT: Int
```

CDMA_NETWORK_BUSY_ONE_SHOT tone: 425Hz 500ms ON, 500ms OFF. 

 Value: 96

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_NETWORK_CALLWAITING

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_NETWORK_CALLWAITING: Int
```

CDMA Network Callwaiting tone: 440Hz 300ms ON 

 Value: 43

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_NETWORK_USA_RINGBACK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_NETWORK_USA_RINGBACK: Int
```

CDMA USA Ringback: 440Hz+480Hz 2s ON, 4000 OFF ... 

 Value: 35

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_ONE_MIN_BEEP

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_ONE_MIN_BEEP: Int
```

CDMA One Min Beep tone: 1150Hz+770Hz 400ms ON 

 Value: 88

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_PIP

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_PIP: Int
```

CDMA PIP tone: 480Hz 100ms ON, 100ms OFF repeated for 4 times 

 Value: 44

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_PRESSHOLDKEY_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_PRESSHOLDKEY_LITE: Int
```

CDMA PRESSHOLDKEY LITE tone: 587Hz 375ms ON, 1175Hz 125ms ON 

 Value: 90

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_REORDER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_REORDER: Int
```

CDMA Reorder tone: 480Hz+620Hz 250ms ON, 250ms OFF... 

 Value: 38

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_SIGNAL_OFF

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_SIGNAL_OFF: Int
```

CDMA_SIGNAL_OFF - silent tone 

 Value: 98

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_CDMA_SOFT_ERROR_LITE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_CDMA_SOFT_ERROR_LITE: Int
```

CDMA SOFT ERROR LITE tone: 1047Hz 125ms ON, 370Hz 125ms 

 Value: 94

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_0: Int
```

DTMF tone for key 0: 1336Hz, 941Hz, continuous

<br />

 Value: 0

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_1: Int
```

DTMF tone for key 1: 1209Hz, 697Hz, continuous 

 Value: 1

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_2: Int
```

DTMF tone for key 2: 1336Hz, 697Hz, continuous 

 Value: 2

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_3: Int
```

DTMF tone for key 3: 1477Hz, 697Hz, continuous 

 Value: 3

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_4

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_4: Int
```

DTMF tone for key 4: 1209Hz, 770Hz, continuous 

 Value: 4

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_5

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_5: Int
```

DTMF tone for key 5: 1336Hz, 770Hz, continuous 

 Value: 5

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_6

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_6: Int
```

DTMF tone for key 6: 1477Hz, 770Hz, continuous 

 Value: 6

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_7

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_7: Int
```

DTMF tone for key 7: 1209Hz, 852Hz, continuous 

 Value: 7

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_8: Int
```

DTMF tone for key 8: 1336Hz, 852Hz, continuous 

 Value: 8

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_9

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_9: Int
```

DTMF tone for key 9: 1477Hz, 852Hz, continuous 

 Value: 9

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_A

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_A: Int
```

DTMF tone for key A: 1633Hz, 697Hz, continuous 

 Value: 12

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_B

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_B: Int
```

DTMF tone for key B: 1633Hz, 770Hz, continuous 

 Value: 13

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_C

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_C: Int
```

DTMF tone for key C: 1633Hz, 852Hz, continuous 

 Value: 14

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_D: Int
```

DTMF tone for key D: 1633Hz, 941Hz, continuous 

 Value: 15

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_P

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_P: Int
```

DTMF tone for key #: 1477Hz, 941Hz, continuous 

 Value: 11

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_DTMF_S

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_DTMF_S: Int
```

DTMF tone for key \*: 1209Hz, 941Hz, continuous 

 Value: 10

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_PROP_ACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_PROP_ACK: Int
```

Proprietary tone, positive acknowlegement: 1200Hz, 100ms ON, 100ms OFF 2 bursts 

 Value: 25

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_PROP_BEEP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_PROP_BEEP: Int
```

Proprietary tone, general beep: 400Hz+1200Hz, 35ms ON 

 Value: 24

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_PROP_BEEP2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_PROP_BEEP2: Int
```

Proprietary tone, general double beep: twice 400Hz+1200Hz, 35ms ON, 200ms OFF, 35ms ON 

 Value: 28

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_PROP_NACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_PROP_NACK: Int
```

Proprietary tone, negative acknowlegement: 300Hz+400Hz+500Hz, 400ms ON 

 Value: 26

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_PROP_PROMPT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_PROP_PROMPT: Int
```

Proprietary tone, prompt tone: 400Hz+1200Hz, 200ms ON 

 Value: 27

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_BUSY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_BUSY: Int
```

Call supervisory tone, Busy: CEPT: 425Hz, 500ms ON, 500ms OFF... ANSI (IS-95): 480Hz+620Hz, 500ms ON, 500ms OFF... JAPAN: 400Hz, 500ms ON, 500ms OFF... 

 Value: 17

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_CALL_WAITING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_CALL_WAITING: Int
```

Call supervisory tone, Call Waiting: CEPT, JAPAN: 425Hz, 200ms ON, 600ms OFF, 200ms ON, 3s OFF... ANSI (IS-95): 440 Hz, 300 ms ON, 9.7 s OFF, (100 ms ON, 100 ms OFF, 100 ms ON, 9.7s OFF ...) 

 Value: 22

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_CONFIRM

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_CONFIRM: Int
```

Call supervisory tone (IS-95), confirm tone: a 350 Hz tone added to a 440 Hz tone repeated 3 times in a 100 ms on, 100 ms off cycle 

 Value: 32

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_CONGESTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_CONGESTION: Int
```

Call supervisory tone, Congestion: CEPT, JAPAN: 425Hz, 200ms ON, 200ms OFF... ANSI (IS-95): 480Hz+620Hz, 250ms ON, 250ms OFF... 

 Value: 18

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_CONGESTION_ABBREV

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_CONGESTION_ABBREV: Int
```

Call supervisory tone (IS-95), abbreviated congestion: congestion tone limited to 4 seconds 

 Value: 31

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_DIAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_DIAL: Int
```

Call supervisory tone, Dial tone: CEPT: 425Hz, continuous ANSI (IS-95): 350Hz+440Hz, continuous JAPAN: 400Hz, continuous 

 Value: 16

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_ERROR: Int
```

Call supervisory tone, Error/Special info: 950Hz+1400Hz+1800Hz, 330ms ON, 1s OFF... 

 Value: 21

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_INTERCEPT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_INTERCEPT: Int
```

Call supervisory tone (IS-95), intercept tone: alternating 440 Hz and 620 Hz tones, each on for 250 ms 

 Value: 29

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_INTERCEPT_ABBREV

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_INTERCEPT_ABBREV: Int
```

Call supervisory tone (IS-95), abbreviated intercept: intercept tone limited to 4 seconds 

 Value: 30

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_PIP

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_PIP: Int
```

Call supervisory tone (IS-95), pip tone: four bursts of 480 Hz tone (0.1 s on, 0.1 s off). 

 Value: 33

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_RADIO_ACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_RADIO_ACK: Int
```

Call supervisory tone, Radio path acknowlegment : CEPT, ANSI: 425Hz, 200ms ON JAPAN: 400Hz, 1s ON, 2s OFF... 

 Value: 19

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_RADIO_NOTAVAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_RADIO_NOTAVAIL: Int
```

Call supervisory tone, Radio path not available: 425Hz, 200ms ON, 200 OFF 3 bursts 

 Value: 20

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### TONE_SUP_RINGTONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TONE_SUP_RINGTONE: Int
```

Call supervisory tone, Ring Tone: CEPT, JAPAN: 425Hz, 1s ON, 4s OFF... ANSI (IS-95): 440Hz + 480Hz, 2s ON, 4s OFF... 

 Value: 23

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int))

## Public constructors

### ToneGenerator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ToneGenerator(
    streamType: Int, 
    volume: Int)
```

ToneGenerator class contructor specifying output stream type and volume.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The streame type used for tone playback (e.g. STREAM_MUSIC). |
| `volume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The volume of the tone, given in percentage of maximum volume (from 0-100). |

## Public methods

### getAudioSessionId

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSessionId(): Int
```

Returns the audio session ID.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ID of the audio session this ToneGenerator belongs to or 0 if an error occured. |

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases resources associated with this ToneGenerator object. It is good practice to call this method when you're done using the ToneGenerator. 

### startTone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startTone(toneType: Int): Boolean
```

This method starts the playback of a tone of the specified type. only one tone can play at a time: if a tone is playing while this method is called, this tone is stopped and replaced by the one requested.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toneType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of tone generated chosen from the following list: - [TONE_DTMF_0](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_0:kotlin.Int) - [TONE_DTMF_1](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_1:kotlin.Int) - [TONE_DTMF_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_2:kotlin.Int) - [TONE_DTMF_3](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_3:kotlin.Int) - [TONE_DTMF_4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_4:kotlin.Int) - [TONE_DTMF_5](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_5:kotlin.Int) - [TONE_DTMF_6](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_6:kotlin.Int) - [TONE_DTMF_7](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_7:kotlin.Int) - [TONE_DTMF_8](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_8:kotlin.Int) - [TONE_DTMF_9](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_9:kotlin.Int) - [TONE_DTMF_A](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_A:kotlin.Int) - [TONE_DTMF_B](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_B:kotlin.Int) - [TONE_DTMF_C](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_C:kotlin.Int) - [TONE_DTMF_D](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_DTMF_D:kotlin.Int) - [TONE_SUP_DIAL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_DIAL:kotlin.Int) - [TONE_SUP_BUSY](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_BUSY:kotlin.Int) - [TONE_SUP_CONGESTION](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONGESTION:kotlin.Int) - [TONE_SUP_RADIO_ACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RADIO_ACK:kotlin.Int) - [TONE_SUP_RADIO_NOTAVAIL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RADIO_NOTAVAIL:kotlin.Int) - [TONE_SUP_ERROR](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_ERROR:kotlin.Int) - [TONE_SUP_CALL_WAITING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CALL_WAITING:kotlin.Int) - [TONE_SUP_RINGTONE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_RINGTONE:kotlin.Int) - [TONE_PROP_BEEP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_BEEP:kotlin.Int) - [TONE_PROP_ACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_ACK:kotlin.Int) - [TONE_PROP_NACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_NACK:kotlin.Int) - [TONE_PROP_PROMPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_PROMPT:kotlin.Int) - [TONE_PROP_BEEP2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_PROP_BEEP2:kotlin.Int) - [TONE_SUP_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_INTERCEPT:kotlin.Int) - [TONE_SUP_INTERCEPT_ABBREV](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_INTERCEPT_ABBREV:kotlin.Int) - [TONE_SUP_CONGESTION_ABBREV](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONGESTION_ABBREV:kotlin.Int) - [TONE_SUP_CONFIRM](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_CONFIRM:kotlin.Int) - [TONE_SUP_PIP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_SUP_PIP:kotlin.Int) - [TONE_CDMA_DIAL_TONE_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_DIAL_TONE_LITE:kotlin.Int) - [TONE_CDMA_NETWORK_USA_RINGBACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_USA_RINGBACK:kotlin.Int) - [TONE_CDMA_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_INTERCEPT:kotlin.Int) - [TONE_CDMA_ABBR_INTERCEPT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_INTERCEPT:kotlin.Int) - [TONE_CDMA_REORDER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_REORDER:kotlin.Int) - [TONE_CDMA_ABBR_REORDER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_REORDER:kotlin.Int) - [TONE_CDMA_NETWORK_BUSY](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_BUSY:kotlin.Int) - [TONE_CDMA_CONFIRM](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CONFIRM:kotlin.Int) - [TONE_CDMA_ANSWER](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ANSWER:kotlin.Int) - [TONE_CDMA_NETWORK_CALLWAITING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_CALLWAITING:kotlin.Int) - [TONE_CDMA_PIP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_PIP:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_NORMAL:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_INTERGROUP:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_SP_PRI:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_PAT3](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT3:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PING_RING:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_PAT5](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT5:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_PAT6](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT6:kotlin.Int) - [TONE_CDMA_CALL_SIGNAL_ISDN_PAT7](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALL_SIGNAL_ISDN_PAT7:kotlin.Int) - [TONE_CDMA_HIGH_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_L:kotlin.Int) - [TONE_CDMA_MED_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_L:kotlin.Int) - [TONE_CDMA_LOW_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_L:kotlin.Int) - [TONE_CDMA_HIGH_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SS:kotlin.Int) - [TONE_CDMA_MED_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SS:kotlin.Int) - [TONE_CDMA_LOW_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SS:kotlin.Int) - [TONE_CDMA_HIGH_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SSL:kotlin.Int) - [TONE_CDMA_MED_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SSL:kotlin.Int) - [TONE_CDMA_LOW_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SSL:kotlin.Int) - [TONE_CDMA_HIGH_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SS_2:kotlin.Int) - [TONE_CDMA_MED_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SS_2:kotlin.Int) - [TONE_CDMA_LOW_SS_2](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SS_2:kotlin.Int) - [TONE_CDMA_HIGH_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_SLS:kotlin.Int) - [TONE_CDMA_MED_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_SLS:kotlin.Int) - [TONE_CDMA_LOW_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_SLS:kotlin.Int) - [TONE_CDMA_HIGH_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_S_X4:kotlin.Int) - [TONE_CDMA_MED_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_S_X4:kotlin.Int) - [TONE_CDMA_LOW_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_S_X4:kotlin.Int) - [TONE_CDMA_HIGH_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_L:kotlin.Int) - [TONE_CDMA_MED_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_L:kotlin.Int) - [TONE_CDMA_LOW_PBX_L](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_L:kotlin.Int) - [TONE_CDMA_HIGH_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SS:kotlin.Int) - [TONE_CDMA_MED_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SS:kotlin.Int) - [TONE_CDMA_LOW_PBX_SS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SS:kotlin.Int) - [TONE_CDMA_HIGH_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SSL:kotlin.Int) - [TONE_CDMA_MED_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SSL:kotlin.Int) - [TONE_CDMA_LOW_PBX_SSL](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SSL:kotlin.Int) - [TONE_CDMA_HIGH_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_SLS:kotlin.Int) - [TONE_CDMA_MED_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_SLS:kotlin.Int) - [TONE_CDMA_LOW_PBX_SLS](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_SLS:kotlin.Int) - [TONE_CDMA_HIGH_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_HIGH_PBX_S_X4:kotlin.Int) - [TONE_CDMA_MED_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_MED_PBX_S_X4:kotlin.Int) - [TONE_CDMA_LOW_PBX_S_X4](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_LOW_PBX_S_X4:kotlin.Int) - [TONE_CDMA_ALERT_NETWORK_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_NETWORK_LITE:kotlin.Int) - [TONE_CDMA_ALERT_AUTOREDIAL_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_AUTOREDIAL_LITE:kotlin.Int) - [TONE_CDMA_ONE_MIN_BEEP](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ONE_MIN_BEEP:kotlin.Int) - [TONE_CDMA_KEYPAD_VOLUME_KEY_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_KEYPAD_VOLUME_KEY_LITE:kotlin.Int) - [TONE_CDMA_PRESSHOLDKEY_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_PRESSHOLDKEY_LITE:kotlin.Int) - [TONE_CDMA_ALERT_INCALL_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_INCALL_LITE:kotlin.Int) - [TONE_CDMA_EMERGENCY_RINGBACK](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_EMERGENCY_RINGBACK:kotlin.Int) - [TONE_CDMA_ALERT_CALL_GUARD](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ALERT_CALL_GUARD:kotlin.Int) - [TONE_CDMA_SOFT_ERROR_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_SOFT_ERROR_LITE:kotlin.Int) - [TONE_CDMA_CALLDROP_LITE](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_CALLDROP_LITE:kotlin.Int) - [TONE_CDMA_NETWORK_BUSY_ONE_SHOT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_NETWORK_BUSY_ONE_SHOT:kotlin.Int) - [TONE_CDMA_ABBR_ALERT](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_ABBR_ALERT:kotlin.Int) - [TONE_CDMA_SIGNAL_OFF](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#TONE_CDMA_SIGNAL_OFF:kotlin.Int) |

**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int)) 

### startTone

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startTone(
    toneType: Int, 
    durationMs: Int
): Boolean
```

This method starts the playback of a tone of the specified type for the specified duration.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toneType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of tone generated @see [startTone(int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#startTone(kotlin.Int)). |
| `durationMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The tone duration in milliseconds. If the tone is limited in time by definition, the actual duration will be the minimum of durationMs and the defined tone duration. Setting durationMs to -1, is equivalent to calling [startTone(int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#startTone(kotlin.Int)). |

### stopTone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopTone(): Unit
```

This method stops the tone currently playing playback. 
**See Also**

- [#ToneGenerator(int, int)](https://developer.android.com/reference/kotlin/android/media/ToneGenerator#ToneGenerator(kotlin.Int,%20kotlin.Int))

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
