# JsonToken

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsonToken

Kotlin| [Java](https://developer.android.com/reference/android/util/JsonToken "View this page in Java") 

```
class JsonToken
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.util.JsonToken](https://developer.android.com/reference/kotlin/android/util/JsonToken#)\> ||
| | ↳ | [android.util.JsonToken](https://developer.android.com/reference/kotlin/android/util/JsonToken#) |

| Known Direct Subclasses [JsonToken.BEGIN_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_ARRAY), [JsonToken.BEGIN_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_OBJECT), [JsonToken.BOOLEAN](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BOOLEAN), [JsonToken.END_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_ARRAY), [JsonToken.END_DOCUMENT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_DOCUMENT), [JsonToken.END_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_OBJECT), [JsonToken.NAME](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NAME), [JsonToken.NULL](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NULL), [JsonToken.NUMBER](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NUMBER), [JsonToken.STRING](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:STRING) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [JsonToken.BEGIN_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_ARRAY) | The opening of a JSON array. | | [JsonToken.BEGIN_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_OBJECT) | The opening of a JSON object. | | [JsonToken.BOOLEAN](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BOOLEAN) | A JSON`true`or`false`. | | [JsonToken.END_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_ARRAY) | The closing of a JSON array. | | [JsonToken.END_DOCUMENT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_DOCUMENT) | The end of the JSON stream. | | [JsonToken.END_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_OBJECT) | The closing of a JSON object. | | [JsonToken.NAME](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NAME) | A JSON property name. | | [JsonToken.NULL](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NULL) | A JSON`null`. | | [JsonToken.NUMBER](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NUMBER) | A JSON number represented in this API by a Java`double`,`long`, or`int`. | | [JsonToken.STRING](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:STRING) | A JSON string. | |

A structure, name or value type in a JSON-encoded string.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BEGIN_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_ARRAY) The opening of a JSON array. |
| [BEGIN_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BEGIN_OBJECT) The opening of a JSON object. |
| [BOOLEAN](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:BOOLEAN) A JSON`true`or`false`. |
| [END_ARRAY](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_ARRAY) The closing of a JSON array. |
| [END_DOCUMENT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_DOCUMENT) The end of the JSON stream. |
| [END_OBJECT](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:END_OBJECT) The closing of a JSON object. |
| [NAME](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NAME) A JSON property name. |
| [NULL](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NULL) A JSON`null`. |
| [NUMBER](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:NUMBER) A JSON number represented in this API by a Java`double`,`long`, or`int`. |
| [STRING](https://developer.android.com/reference/kotlin/android/util/JsonToken#ENUM_VALUE:STRING) A JSON string. |

## Enum values

### BEGIN_ARRAY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_ARRAY : JsonToken
```

The opening of a JSON array. Written using [JsonWriter.beginObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginObject())and read using [JsonReader.beginObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginObject()). 

### BEGIN_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BEGIN_OBJECT : JsonToken
```

The opening of a JSON object. Written using [JsonWriter.beginObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginObject())and read using [JsonReader.beginObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginObject()). 

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

The closing of a JSON array. Written using [JsonWriter.endArray](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endArray())and read using [JsonReader.endArray](https://developer.android.com/reference/kotlin/android/util/JsonReader#endArray()). 

### END_DOCUMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_DOCUMENT : JsonToken
```

The end of the JSON stream. This sentinel value is returned by [android.util.JsonReader#peek()](https://developer.android.com/reference/kotlin/android/util/JsonReader#peek())to signal that the JSON-encoded value has no more tokens. 

### END_OBJECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val END_OBJECT : JsonToken
```

The closing of a JSON object. Written using [JsonWriter.endObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endObject())and read using [JsonReader.endObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#endObject()). 

### NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NAME : JsonToken
```

A JSON property name. Within objects, tokens alternate between names and their values. Written using [JsonWriter.name](https://developer.android.com/reference/kotlin/android/util/JsonWriter#name(kotlin.String))and read using [android.util.JsonReader#nextName](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextName()) 

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
