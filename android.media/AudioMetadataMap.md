# AudioMetadataMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadataMap

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioMetadataMap "View this page in Java") 

```
interface AudioMetadataMap : AudioMetadataReadMap
```

| [android.media.AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap#) |

AudioMetadataMap is a writeable`Map`-style interface of [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key) value pairs. This interface is not guaranteed to be thread-safe unless the underlying implementation for the`AudioMetadataMap`states it as thread safe. {@see AudioMetadataReadMap}

## Summary

| Public methods ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT? | [remove](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap#remove(android.media.AudioMetadata.Key))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`)` Removes the value associated with the key. |
| abstractT? | [set](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap#set(android.media.AudioMetadata.Key,%20android.media.AudioMetadataMap.set.T))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`, `value:` `T`)` Sets a value for the key. |

| Inherited functions ||
|---|---|
| From class [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#containsKey(android.media.AudioMetadata.Key))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`)` <br /> Returns true if the key exists in the map. <br /> | | [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap#) | [dup](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#dup())`()` <br /> Returns a copy of the map. This is intended for safe conversion between a [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap) interface and a [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap#) interface. Currently only simple objects are used for key values which means a shallow copy is sufficient. <br /> | | T? | [get](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#get(android.media.AudioMetadata.Key))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`)` <br /> Returns the value associated with the key. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#size())`()` <br /> Returns the number of elements in the map. <br /> | ||

## Public methods

### remove

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> remove(key: AudioMetadata.Key<T>): T?
```

Removes the value associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)\<T\>:interface for storing the value. This value cannot be`null`. |
| `<T>` | type of value. |

| Return ||
|----|-------------------------------------------------|
| T? | the value of the key, null if it doesn't exist. |

### set

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> set(
    key: AudioMetadata.Key<T>, 
    value: T
): T?
```

Sets a value for the key.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)\<T\>:interface for storing the value. This value cannot be`null`. |
| `<T>` | type of value. |
| `value` | T:a non-null value of type T. |

| Return ||
|----|---------------------------------------------------------------------|
| T? | the previous value associated with key or null if it doesn't exist. |
