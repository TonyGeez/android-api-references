Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultisensoryManager

```
open class MultisensoryManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.multisensory.MultisensoryManager](MultisensoryManager.md) |

Provides capabilities to deliver audio-haptic feedback from the Multisensory Design System in Android.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_CANCEL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_CONTINUOUS:kotlin.Int` Inform the user that their drag gesture has resulted in an incremental value change. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_DISCRETE:kotlin.Int` Inform the user that their drag gesture has resulted in a stepped value change. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_THRESHOLD_LIMIT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_FAILURE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_FAILURE_HIGH_EMPHASIS:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_DELETE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_RETURN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_SPACEBAR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_STANDARD:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_LOCK:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_LONG_PRESS:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_PAUSE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_START:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_STOP:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SUCCESS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWIPE_INDICATOR_THRESHOLD_LIMIT:kotlin.Int` Inform the user that their swipe gesture has crossed a threshold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWITCH_OFF:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWITCH_ON:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_HIGH_EMPHASIS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_LOW_EMPHASIS:kotlin.Int` Played when a user taps on any UI element that can be interacted with but is not otherwise defined. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_MEDIUM_EMPHASIS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_UNLOCK:kotlin.Int` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | playToken Deliver multisensory feedback associated with the given multisensory token constant. |

## Constants

### TOKEN_CANCEL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_CANCEL: Int
```

 Value: 6

### TOKEN_DRAG_INDICATOR_CONTINUOUS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_DRAG_INDICATOR_CONTINUOUS: Int
```

Inform the user that their drag gesture has resulted in an incremental value change.

This token can be used to create a continuous effect affected by MultisensoryManager

 Value: 17

### TOKEN_DRAG_INDICATOR_DISCRETE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_DRAG_INDICATOR_DISCRETE: Int
```

Inform the user that their drag gesture has resulted in a stepped value change.

This token can be used to create a continuous effect affected by MultisensoryManager

 Value: 18

### TOKEN_DRAG_INDICATOR_THRESHOLD_LIMIT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_DRAG_INDICATOR_THRESHOLD_LIMIT: Int
```

 Value: 16

### TOKEN_FAILURE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_FAILURE: Int
```

 Value: 1

### TOKEN_FAILURE_HIGH_EMPHASIS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_FAILURE_HIGH_EMPHASIS: Int
```

 Value: 0

### TOKEN_KEYPRESS_DELETE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_KEYPRESS_DELETE: Int
```

 Value: 22

### TOKEN_KEYPRESS_RETURN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_KEYPRESS_RETURN: Int
```

 Value: 21

### TOKEN_KEYPRESS_SPACEBAR

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_KEYPRESS_SPACEBAR: Int
```

 Value: 20

### TOKEN_KEYPRESS_STANDARD

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_KEYPRESS_STANDARD: Int
```

 Value: 19

### TOKEN_LOCK

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_LOCK: Int
```

 Value: 10

### TOKEN_LONG_PRESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_LONG_PRESS: Int
```

 Value: 11

### TOKEN_PAUSE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_PAUSE: Int
```

 Value: 4

### TOKEN_START

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_START: Int
```

 Value: 3

### TOKEN_STOP

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_STOP: Int
```

 Value: 5

### TOKEN_SUCCESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_SUCCESS: Int
```

 Value: 2

### TOKEN_SWIPE_INDICATOR_THRESHOLD_LIMIT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_SWIPE_INDICATOR_THRESHOLD_LIMIT: Int
```

Inform the user that their swipe gesture has crossed a threshold. This indicates that the swipe action beyond the threshold will activate when the swipe is completed.

 Value: 12

### TOKEN_SWITCH_OFF

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_SWITCH_OFF: Int
```

 Value: 8

### TOKEN_SWITCH_ON

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_SWITCH_ON: Int
```

 Value: 7

### TOKEN_TAP_HIGH_EMPHASIS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_TAP_HIGH_EMPHASIS: Int
```

 Value: 13

### TOKEN_TAP_LOW_EMPHASIS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_TAP_LOW_EMPHASIS: Int
```

Played when a user taps on any UI element that can be interacted with but is not otherwise defined.

 Value: 15

### TOKEN_TAP_MEDIUM_EMPHASIS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_TAP_MEDIUM_EMPHASIS: Int
```

 Value: 14

### TOKEN_UNLOCK

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOKEN_UNLOCK: Int
```

 Value: 9

## Public methods

### playToken

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun playToken(tokenConstant: Int): Unit
```

Deliver multisensory feedback associated with the given multisensory token constant.

If the token defines audio-haptic feedback, audio and haptics will be played with the best synchronization possible. If the token only corresponds to haptics, only haptics will play.

| Parameters ||
|---|---|
| `tokenConstant` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The token constant to play. Must be one of the constants defined by the MultisensoryManager. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_FAILURE_HIGH_EMPHASIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_PAUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_STOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_CANCEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWITCH_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWITCH_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_UNLOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_LOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_LONG_PRESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_SWIPE_INDICATOR_THRESHOLD_LIMIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_HIGH_EMPHASIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_MEDIUM_EMPHASIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_TAP_LOW_EMPHASIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_SPACEBAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_RETURN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_KEYPRESS_DELETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_CONTINUOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_DISCRETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager#TOKEN_DRAG_INDICATOR_THRESHOLD_LIMIT:kotlin.Int` |
