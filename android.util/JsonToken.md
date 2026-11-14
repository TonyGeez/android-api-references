# JsonToken

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsonToken

Kotlin| [Java](JsonToken.md) 
| --- | --- |

```
class JsonToken
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.util.JsonToken](JsonToken.md)\> ||
| | ↳ | [android.util.JsonToken](JsonToken.md) |

| Known Direct Subclasses [JsonToken.BEGIN_ARRAY](JsonToken.md), [JsonToken.BEGIN_OBJECT](JsonToken.md), [JsonToken.BOOLEAN](JsonToken.md), [JsonToken.END_ARRAY](JsonToken.md), [JsonToken.END_DOCUMENT](JsonToken.md), [JsonToken.END_OBJECT](JsonToken.md), [JsonToken.NAME](JsonToken.md), [JsonToken.NULL](JsonToken.md), [JsonToken.NUMBER](JsonToken.md), [JsonToken.STRING](JsonToken.md) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [JsonToken.BEGIN_ARRAY](JsonToken.md) | The opening of a JSON array. | | [JsonToken.BEGIN_OBJECT](JsonToken.md) | The opening of a JSON object. | | [JsonToken.BOOLEAN](JsonToken.md) | A JSON`true`or`false`. | | [JsonToken.END_ARRAY](JsonToken.md) | The closing of a JSON array. | | [JsonToken.END_DOCUMENT](JsonToken.md) | The end of the JSON stream. | | [JsonToken.END_OBJECT](JsonToken.md) | The closing of a JSON object. | | [JsonToken.NAME](JsonToken.md) | A JSON property name. | | [JsonToken.NULL](JsonToken.md) | A JSON`null`. | | [JsonToken.NUMBER](JsonToken.md) | A JSON number represented in this API by a Java`double`,`long`, or`int`. | | [JsonToken.STRING](JsonToken.md) | A JSON string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A structure, name or value type in a JSON-encoded string.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BEGIN_ARRAY](JsonToken.md) The opening of a JSON array. |
| [BEGIN_OBJECT](JsonToken.md) The opening of a JSON object. |
| [BOOLEAN](JsonToken.md) A JSON`true`or`false`. |
| [END_ARRAY](JsonToken.md) The closing of a JSON array. |
| [END_DOCUMENT](JsonToken.md) The end of the JSON stream. |
| [END_OBJECT](JsonToken.md) The closing of a JSON object. |
| [NAME](JsonToken.md) A JSON property name. |
| [NULL](JsonToken.md) A JSON`null`. |
| [NUMBER](JsonToken.md) A JSON number represented in this API by a Java`double`,`long`, or`int`. |
| [STRING](JsonToken.md) A JSON string. |

## Enum values

### BEGIN_ARRAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_ARRAY : JsonToken
```

The opening of a JSON array. Written using [JsonWriter.beginObject](JsonWriter.md))and read using [JsonReader.beginObject](JsonReader.md)). 

### BEGIN_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_OBJECT : JsonToken
```

The opening of a JSON object. Written using [JsonWriter.beginObject](JsonWriter.md))and read using [JsonReader.beginObject](JsonReader.md)). 

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

The closing of a JSON array. Written using [JsonWriter.endArray](JsonWriter.md))and read using [JsonReader.endArray](JsonReader.md)). 

### END_DOCUMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_DOCUMENT : JsonToken
```

The end of the JSON stream. This sentinel value is returned by [android.util.JsonReader#peek()](JsonReader.md))to signal that the JSON-encoded value has no more tokens. 

### END_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_OBJECT : JsonToken
```

The closing of a JSON object. Written using [JsonWriter.endObject](JsonWriter.md))and read using [JsonReader.endObject](JsonReader.md)). 

### NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NAME : JsonToken
```

A JSON property name. Within objects, tokens alternate between names and their values. Written using [JsonWriter.name](JsonWriter.md))and read using [android.util.JsonReader#nextName](JsonReader.md)) 

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
