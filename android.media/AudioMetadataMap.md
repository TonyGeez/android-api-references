# AudioMetadataMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadataMap

Kotlin| [Java](../android/media/AudioMetadataMap.md) 
| --- | --- |

```
interface AudioMetadataMap : AudioMetadataReadMap
```

| [android.media.AudioMetadataMap](../android/media/AudioMetadataMap.md) |

AudioMetadataMap is a writeable`Map`-style interface of [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) value pairs. This interface is not guaranteed to be thread-safe unless the underlying implementation for the`AudioMetadataMap`states it as thread safe. {@see AudioMetadataReadMap}

## Summary

| Public methods ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT? | [remove](../android/media/AudioMetadataMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`)` Removes the value associated with the key. |
| abstractT? | [set](../android/media/AudioMetadataMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`, `value:` `T`)` Sets a value for the key. |

| Inherited functions ||
|---|---|
| From class [AudioMetadataReadMap](../android/media/AudioMetadataReadMap.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](../android/media/AudioMetadataReadMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`)` <br /> Returns true if the key exists in the map. <br /> | | [AudioMetadataMap](../android/media/AudioMetadataMap.md) | [dup](../android/media/AudioMetadataReadMap.md))`()` <br /> Returns a copy of the map. This is intended for safe conversion between a [AudioMetadataReadMap](../android/media/AudioMetadataReadMap.md) interface and a [AudioMetadataMap](../android/media/AudioMetadataMap.md) interface. Currently only simple objects are used for key values which means a shallow copy is sufficient. <br /> | | T? | [get](../android/media/AudioMetadataReadMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`)` <br /> Returns the value associated with the key. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../android/media/AudioMetadataReadMap.md))`()` <br /> Returns the number of elements in the map. <br /> | ||

## Public methods

### remove

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> remove(key: AudioMetadata.Key<T>): T?
```

Removes the value associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)\<T\>:interface for storing the value. This value cannot be`null`. |
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
| `key` | [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)\<T\>:interface for storing the value. This value cannot be`null`. |
| `<T>` | type of value. |
| `value` | T:a non-null value of type T. |
| --- | --- |

| Return ||
|----|---------------------------------------------------------------------|
| T? | the previous value associated with key or null if it doesn't exist. |
