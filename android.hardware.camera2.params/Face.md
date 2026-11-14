Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Face

Kotlin | [Java](Face.md)
| --- | --- |

```
class Face
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.Face](Face.md) |

Describes a face detected in an image.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face.Builder` Builds a Face object. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#ID_UNSUPPORTED:kotlin.Int` The ID is `-1` when the optional set of fields is unsupported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MAX:kotlin.Int` The maximum possible value for the confidence level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MIN:kotlin.Int` The minimum possible value for the confidence level. |
| --- | --- |

| Public methods ||
|---|---|
| [Rect](../android.graphics/Rect.md)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getBounds()()` Bounds of the face. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getId()()` An unique id per face while the face is visible to the tracker. |
| [Point](../android.graphics/Point.md)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getLeftEyePosition()()` The coordinates of the center of the left eye. |
| --- | --- |
| [Point](../android.graphics/Point.md)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getMouthPosition()()` The coordinates of the center of the mouth. |
| [Point](../android.graphics/Point.md)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getRightEyePosition()()` The coordinates of the center of the right eye. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getScore()()` The confidence level for the detection of the face. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#toString()()` Represent the Face as a string for debugging purposes. |

## Constants

### ID_UNSUPPORTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ID_UNSUPPORTED: Int
```

The ID is `-1` when the optional set of fields is unsupported.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getId()`

### SCORE_MAX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCORE_MAX: Int
```

The maximum possible value for the confidence level.

 Value: 100

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getScore()`

### SCORE_MIN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCORE_MIN: Int
```

The minimum possible value for the confidence level.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getScore()`

## Public methods

### getBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBounds(): Rect!
```

Bounds of the face.

A rectangle relative to the sensor's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with (0,0) representing the top-left corner of the active array rectangle.

There is no constraints on the Rectangle value other than it is not-`null`.

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

An unique id per face while the face is visible to the tracker.

If the face leaves the field-of-view and comes back, it may get a new id.

This is an optional field and may not be supported on all devices. If the id is {@value #ID_UNSUPPORTED} then the leftEyePosition, rightEyePosition, and mouthPositions are guaranteed to be `null`. Otherwise, each of leftEyePosition, rightEyePosition, and mouthPosition may be independently null or not-null. When devices report the value of key `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureResult.Key` as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#`, the face id of each face is expected to be {@value #ID_UNSUPPORTED}.

This value will either be {@value #ID_UNSUPPORTED} or otherwise greater than `0`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#ID_UNSUPPORTED:kotlin.Int`

### getLeftEyePosition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeftEyePosition(): Point!
```

The coordinates of the center of the left eye.

The coordinates are in the same space as the ones for `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getBounds()`. This is an optional field and may not be supported on all devices. If not supported, the value will always be set to null. This value will always be null only if `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getId()` returns {@value #ID_UNSUPPORTED}.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Point.html#!` | The left eye position, or `null` if unknown. |

### getMouthPosition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMouthPosition(): Point!
```

The coordinates of the center of the mouth.

The coordinates are in the same space as the ones for `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getBounds()`. This is an optional field and may not be supported on all devices. If not supported, the value will always be set to null. This value will always be null only if `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getId()` returns {@value #ID_UNSUPPORTED}.

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Point.html#!` | The mouth position, or `null` if unknown. |

### getRightEyePosition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRightEyePosition(): Point!
```

The coordinates of the center of the right eye.

The coordinates are in the same space as the ones for `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getBounds()`.This is an optional field and may not be supported on all devices. If not supported, the value will always be set to null. This value will always be null only if `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#getId()` returns {@value #ID_UNSUPPORTED}.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Point.html#!` | The right eye position, or `null` if unknown. |

### getScore

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScore(): Int
```

The confidence level for the detection of the face.

The range is {@value #SCORE_MIN} to {@value #SCORE_MAX}. {@value #SCORE_MAX} is the highest confidence.

Depending on the device, even very low-confidence faces may be listed, so applications should filter out faces with low confidence, depending on the use case. For a typical point-and-shoot camera application that wishes to display rectangles around detected faces, filtering out faces with confidence less than half of {@value #SCORE_MAX} is recommended.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MIN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MAX:kotlin.Int` inclusive |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MAX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face#SCORE_MIN:kotlin.Int`

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Represent the Face as a string for debugging purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
