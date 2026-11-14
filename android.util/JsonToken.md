# JsonToken

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsonToken

Kotlin| [Java](../android/util/JsonToken.md) 
| --- | --- |

```
class JsonToken
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.util.JsonToken](../android/util/JsonToken.md)\> ||
| | ↳ | [android.util.JsonToken](../android/util/JsonToken.md) |

| Known Direct Subclasses [JsonToken.BEGIN_ARRAY](../android/util/JsonToken.md), [JsonToken.BEGIN_OBJECT](../android/util/JsonToken.md), [JsonToken.BOOLEAN](../android/util/JsonToken.md), [JsonToken.END_ARRAY](../android/util/JsonToken.md), [JsonToken.END_DOCUMENT](../android/util/JsonToken.md), [JsonToken.END_OBJECT](../android/util/JsonToken.md), [JsonToken.NAME](../android/util/JsonToken.md), [JsonToken.NULL](../android/util/JsonToken.md), [JsonToken.NUMBER](../android/util/JsonToken.md), [JsonToken.STRING](../android/util/JsonToken.md) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [JsonToken.BEGIN_ARRAY](../android/util/JsonToken.md) | The opening of a JSON array. | | [JsonToken.BEGIN_OBJECT](../android/util/JsonToken.md) | The opening of a JSON object. | | [JsonToken.BOOLEAN](../android/util/JsonToken.md) | A JSON`true`or`false`. | | [JsonToken.END_ARRAY](../android/util/JsonToken.md) | The closing of a JSON array. | | [JsonToken.END_DOCUMENT](../android/util/JsonToken.md) | The end of the JSON stream. | | [JsonToken.END_OBJECT](../android/util/JsonToken.md) | The closing of a JSON object. | | [JsonToken.NAME](../android/util/JsonToken.md) | A JSON property name. | | [JsonToken.NULL](../android/util/JsonToken.md) | A JSON`null`. | | [JsonToken.NUMBER](../android/util/JsonToken.md) | A JSON number represented in this API by a Java`double`,`long`, or`int`. | | [JsonToken.STRING](../android/util/JsonToken.md) | A JSON string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A structure, name or value type in a JSON-encoded string.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BEGIN_ARRAY](../android/util/JsonToken.md) The opening of a JSON array. |
| [BEGIN_OBJECT](../android/util/JsonToken.md) The opening of a JSON object. |
| [BOOLEAN](../android/util/JsonToken.md) A JSON`true`or`false`. |
| [END_ARRAY](../android/util/JsonToken.md) The closing of a JSON array. |
| [END_DOCUMENT](../android/util/JsonToken.md) The end of the JSON stream. |
| [END_OBJECT](../android/util/JsonToken.md) The closing of a JSON object. |
| [NAME](../android/util/JsonToken.md) A JSON property name. |
| [NULL](../android/util/JsonToken.md) A JSON`null`. |
| [NUMBER](../android/util/JsonToken.md) A JSON number represented in this API by a Java`double`,`long`, or`int`. |
| [STRING](../android/util/JsonToken.md) A JSON string. |

## Enum values

### BEGIN_ARRAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_ARRAY : JsonToken
```

The opening of a JSON array. Written using [JsonWriter.beginObject](../android/util/JsonWriter.md))and read using [JsonReader.beginObject](../android/util/JsonReader.md)). 

### BEGIN_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_OBJECT : JsonToken
```

The opening of a JSON object. Written using [JsonWriter.beginObject](../android/util/JsonWriter.md))and read using [JsonReader.beginObject](../android/util/JsonReader.md)). 

### BOOLEAN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BOOLEAN : JsonToken
```

A JSON`true`or`false`. 

### END_ARRAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_ARRAY : JsonToken
```

The closing of a JSON array. Written using [JsonWriter.endArray](../android/util/JsonWriter.md))and read using [JsonReader.endArray](../android/util/JsonReader.md)). 

### END_DOCUMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_DOCUMENT : JsonToken
```

The end of the JSON stream. This sentinel value is returned by [android.util.JsonReader#peek()](../android/util/JsonReader.md))to signal that the JSON-encoded value has no more tokens. 

### END_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_OBJECT : JsonToken
```

The closing of a JSON object. Written using [JsonWriter.endObject](../android/util/JsonWriter.md))and read using [JsonReader.endObject](../android/util/JsonReader.md)). 

### NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NAME : JsonToken
```

A JSON property name. Within objects, tokens alternate between names and their values. Written using [JsonWriter.name](../android/util/JsonWriter.md))and read using [android.util.JsonReader#nextName](../android/util/JsonReader.md)) 

### NULL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NULL : JsonToken
```

A JSON`null`. 

### NUMBER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NUMBER : JsonToken
```

A JSON number represented in this API by a Java`double`,`long`, or`int`. 

### STRING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val STRING : JsonToken
```

A JSON string.
