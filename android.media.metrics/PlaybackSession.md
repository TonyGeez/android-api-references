Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackSession

```
class PlaybackSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#) |

An instance of this class represents a session of media playback used to report playback metrics and events. Create a new instance using `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createPlaybackSession()`.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#close()()` Closes this resource, relinquishing any underlying resources. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#getSessionId()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportBundleMetrics(android.os.PersistableBundle)(metrics: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportNetworkEvent(android.media.metrics.NetworkEvent)(event: https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent)` Reports network event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportPlaybackErrorEvent(android.media.metrics.PlaybackErrorEvent)(event: https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent)` Reports error event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportPlaybackMetrics(android.media.metrics.PlaybackMetrics)(metrics: https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics)` Reports playback metrics. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportPlaybackStateEvent(android.media.metrics.PlaybackStateEvent)(event: https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent)` Reports playback state event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession#reportTrackChangeEvent(android.media.metrics.TrackChangeEvent)(event: https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent)` Reports track change event. |

## Public methods

### close

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getSessionId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionId(): LogSessionId
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId` | This value cannot be `null`. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### reportBundleMetrics

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportBundleMetrics(metrics: PersistableBundle): Unit
```

| Parameters ||
|---|---|
| `metrics` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#): This value cannot be `null`. |

### reportNetworkEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportNetworkEvent(event: NetworkEvent): Unit
```

Reports network event.

| Parameters ||
|---|---|
| `event` | [NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent): This value cannot be `null`. |

### reportPlaybackErrorEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportPlaybackErrorEvent(event: PlaybackErrorEvent): Unit
```

Reports error event.

| Parameters ||
|---|---|
| `event` | [PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent): This value cannot be `null`. |

### reportPlaybackMetrics

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportPlaybackMetrics(metrics: PlaybackMetrics): Unit
```

Reports playback metrics.

| Parameters ||
|---|---|
| `metrics` | [PlaybackMetrics](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics): This value cannot be `null`. |

### reportPlaybackStateEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportPlaybackStateEvent(event: PlaybackStateEvent): Unit
```

Reports playback state event.

| Parameters ||
|---|---|
| `event` | [PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent): This value cannot be `null`. |

### reportTrackChangeEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reportTrackChangeEvent(event: TrackChangeEvent): Unit
```

Reports track change event.

| Parameters ||
|---|---|
| `event` | [TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent): This value cannot be `null`. |
