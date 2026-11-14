# AudioMetadataReadMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadataReadMap

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioMetadataReadMap "View this page in Java") 
| --- | --- |

```
interface AudioMetadataReadMap
```

| [android.media.AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#) |

| Known Direct Subclasses [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) | AudioMetadataMap is a writeable`Map`-style interface of [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key) value pairs. | |
| --- | --- | --- | --- | --- | --- | --- |

A read only`Map`-style interface of [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key) value pairs used for [AudioMetadata](https://developer.android.com/reference/kotlin/android/media/AudioMetadata).

Using a [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key) interface, this map looks up the corresponding value. Read-only maps are thread-safe for lookup, but the underlying object values may need their own thread protection if mutable.
{@see AudioMetadataMap}

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#containsKey(android.media.AudioMetadata.Key))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`)` Returns true if the key exists in the map. |
| abstract [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) | [dup](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#dup())`()` Returns a copy of the map. |
| abstractT? | [get](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#get(android.media.AudioMetadata.Key))`(`key:` ` [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)<T>`)` Returns the value associated with the key. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#size())`()` Returns the number of elements in the map. |

## Public methods

### containsKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> containsKey(key: AudioMetadata.Key<T>): Boolean
```

Returns true if the key exists in the map.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)\<T\>:interface for requesting the value. This value cannot be`null`. |
| `<T>` | type of value. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if key exists in the Map. |

### dup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dup(): AudioMetadataMap
```

Returns a copy of the map. This is intended for safe conversion between a [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap#) interface and a [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) interface. Currently only simple objects are used for key values which means a shallow copy is sufficient.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) | a Map copied from the existing map. This value cannot be`null`. |

### get

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> get(key: AudioMetadata.Key<T>): T?
```

Returns the value associated with the key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key)\<T\>:interface for requesting the value. This value cannot be`null`. |
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
