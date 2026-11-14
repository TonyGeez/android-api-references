# AudioMetadataReadMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadataReadMap

Kotlin| [Java](AudioMetadataReadMap.md) 
| --- | --- |

```
interface AudioMetadataReadMap
```

| [android.media.AudioMetadataReadMap](AudioMetadataReadMap.md) |

| Known Direct Subclasses [AudioMetadataMap](AudioMetadataMap.md) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AudioMetadataMap](AudioMetadataMap.md) | AudioMetadataMap is a writeable`Map`-style interface of [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) value pairs. | |
| --- | --- | --- | --- | --- | --- | --- |

A read only`Map`-style interface of [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) value pairs used for [AudioMetadata](AudioMetadata.md).

Using a [AudioMetadata.Key](../android/media/AudioMetadata.Key.md) interface, this map looks up the corresponding value. Read-only maps are thread-safe for lookup, but the underlying object values may need their own thread protection if mutable.
{@see AudioMetadataMap}

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](AudioMetadataReadMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`)` Returns true if the key exists in the map. |
| abstract [AudioMetadataMap](AudioMetadataMap.md) | [dup](AudioMetadataReadMap.md))`()` Returns a copy of the map. |
| abstractT? | [get](AudioMetadataReadMap.md))`(`key:` ` [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)<T>`)` Returns the value associated with the key. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](AudioMetadataReadMap.md))`()` Returns the number of elements in the map. |

## Public methods

### containsKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> containsKey(key: AudioMetadata.Key<T>): Boolean
```

Returns true if the key exists in the map.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)\<T\>:interface for requesting the value. This value cannot be`null`. |
| `<T>` | type of value. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if key exists in the Map. |

### dup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dup(): AudioMetadataMap
```

Returns a copy of the map. This is intended for safe conversion between a [AudioMetadataReadMap](AudioMetadataReadMap.md) interface and a [AudioMetadataMap](AudioMetadataMap.md) interface. Currently only simple objects are used for key values which means a shallow copy is sufficient.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [AudioMetadataMap](AudioMetadataMap.md) | a Map copied from the existing map. This value cannot be`null`. |

### get

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> get(key: AudioMetadata.Key<T>): T?
```

Returns the value associated with the key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](../android/media/AudioMetadata.Key.md)\<T\>:interface for requesting the value. This value cannot be`null`. |
| `<T>` | type of value. |

| Return ||
|----|-----------------------------------------------------------------------|
| T? | returns the value of associated with key or null if it doesn't exist. |

### size

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Int
```

Returns the number of elements in the map.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |
