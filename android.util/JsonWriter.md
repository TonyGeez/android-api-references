# JsonWriter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsonWriter

Kotlin| [Java](https://developer.android.com/reference/android/util/JsonWriter "View this page in Java") 
| --- | --- |

```
class JsonWriter : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#) |

Writes a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value to a stream, one token at a time. The stream includes both literal values (strings, numbers, booleans and nulls) as well as the begin and end delimiters of objects and arrays.

### Encoding JSON

To encode your data as JSON, create a new`JsonWriter`. Each JSON document must contain one top-level array or object. Call methods on the writer as you walk the structure's contents, nesting arrays and objects as necessary:

- To write**arrays** , first call [beginArray()](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginArray()). Write each of the array's elements with the appropriate #value methods or by nesting other arrays and objects. Finally close the array using [endArray()](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endArray()).
- To write**objects** , first call [beginObject()](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginObject()). Write each of the object's properties by alternating calls to [name](https://developer.android.com/reference/kotlin/android/util/JsonWriter#name(kotlin.String))with the property's value. Write property values with the appropriate #value method or by nesting other objects or arrays. Finally close the object using [endObject()](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endObject()).

### Example

Suppose we'd like to encode a stream of messages such as the following: 

```kotlin
<code>[
    {
      "id": 912345678901,
      "text": "How do I write JSON on Android?",
      "geo": null,
      "user": {
        "name": "android_newb",
        "followers_count": 41
       }
    },
    {
      "id": 912345678902,
      "text": "@android_newb just use android.util.JsonWriter!",
      "geo": [50.454722, -104.606667],
      "user": {
        "name": "jesse",
        "followers_count": 2
      }
    }
  ]</code>
```
This code encodes the above structure: 

```kotlin
<code>public void writeJsonStream(OutputStream out, List&lt;Message&gt; messages) throws IOException {
      JsonWriter writer = new JsonWriter(new OutputStreamWriter(out, "UTF-8"));
      writer.setIndent("  ");
      writeMessagesArray(writer, messages);
      writer.close();
    }
 
    public void writeMessagesArray(JsonWriter writer, List&lt;Message&gt; messages) throws IOException {
      writer.beginArray();
      for (Message message : messages) {
        writeMessage(writer, message);
      }
      writer.endArray();
    }
 
    public void writeMessage(JsonWriter writer, Message message) throws IOException {
      writer.beginObject();
      writer.name("id").value(message.getId());
      writer.name("text").value(message.getText());
      if (message.getGeo() != null) {
        writer.name("geo");
        writeDoublesArray(writer, message.getGeo());
      } else {
        writer.name("geo").nullValue();
      }
      writer.name("user");
      writeUser(writer, message.getUser());
      writer.endObject();
    }
 
    public void writeUser(JsonWriter writer, User user) throws IOException {
      writer.beginObject();
      writer.name("name").value(user.getName());
      writer.name("followers_count").value(user.getFollowersCount());
      writer.endObject();
    }
 
    public void writeDoublesArray(JsonWriter writer, List&lt;Double&gt; doubles) throws IOException {
      writer.beginArray();
      for (Double value : doubles) {
        writer.value(value);
      }
      writer.endArray();
    }</code>
```

<br />

Each`JsonWriter`may be used to write a single JSON stream. Instances of this class are not thread safe. Calls that would result in a malformed JSON string will fail with an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#JsonWriter(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` Creates a new instance that writes a JSON-encoded stream to`out`. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [beginArray](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginArray())`()` Begins encoding a new array. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [beginObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#beginObject())`()` Begins encoding a new object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/util/JsonWriter#close())`()` Flushes and closes this writer and the underlying [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#). |
| --- | --- |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [endArray](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endArray())`()` Ends encoding the current array. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [endObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endObject())`()` Ends encoding the current object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/android/util/JsonWriter#flush())`()` Ensures all buffered data is written to the underlying [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#) and flushes that writer. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](https://developer.android.com/reference/kotlin/android/util/JsonWriter#isLenient())`()` Returns true if this writer has relaxed syntax rules. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [name](https://developer.android.com/reference/kotlin/android/util/JsonWriter#name(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes the property name. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [nullValue](https://developer.android.com/reference/kotlin/android/util/JsonWriter#nullValue())`()` Encodes`null`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndent](https://developer.android.com/reference/kotlin/android/util/JsonWriter#setIndent(kotlin.String))`(`indent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the indentation string to be repeated for each level of indentation in the encoded document. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](https://developer.android.com/reference/kotlin/android/util/JsonWriter#setLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Configure this writer to relax its syntax rules. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [value](https://developer.android.com/reference/kotlin/android/util/JsonWriter#value(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Encodes`value`. |
| --- | --- |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [value](https://developer.android.com/reference/kotlin/android/util/JsonWriter#value(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Encodes`value`. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [value](https://developer.android.com/reference/kotlin/android/util/JsonWriter#value(kotlin.Number))`(`value:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`)` Encodes`value`. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [value](https://developer.android.com/reference/kotlin/android/util/JsonWriter#value(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes`value`. |
| --- | --- |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | [value](https://developer.android.com/reference/kotlin/android/util/JsonWriter#value(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Encodes`value`. |

## Public constructors

### JsonWriter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JsonWriter(out: Writer!)
```

Creates a new instance that writes a JSON-encoded stream to`out`. For best performance, ensure [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#) is buffered; wrapping in [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter.html#) if necessary.

## Public methods

### beginArray

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun beginArray(): JsonWriter!
```

Begins encoding a new array. Each call to this method must be paired with a call to [endArray](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endArray()).

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### beginObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun beginObject(): JsonWriter!
```

Begins encoding a new object. Each call to this method must be paired with a call to [endObject](https://developer.android.com/reference/kotlin/android/util/JsonWriter#endObject()).

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### close

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Flushes and closes this writer and the underlying [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#).

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if the JSON document is incomplete. |

### endArray

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endArray(): JsonWriter!
```

Ends encoding the current array.

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### endObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endObject(): JsonWriter!
```

Ends encoding the current object.

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### flush

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flush(): Unit
```

Ensures all buffered data is written to the underlying [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#) and flushes that writer. 

### isLenient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLenient(): Boolean
```

Returns true if this writer has relaxed syntax rules. 

### name

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun name(name: String!): JsonWriter!
```

Encodes the property name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the forthcoming value. May not be null. |

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### nullValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nullValue(): JsonWriter!
```

Encodes`null`.

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### setIndent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIndent(indent: String!): Unit
```

Sets the indentation string to be repeated for each level of indentation in the encoded document. If`indent.isEmpty()`the encoded document will be compact. Otherwise the encoded document will be more human-readable.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `indent` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string containing only whitespace. |

### setLenient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLenient(lenient: Boolean): Unit
```

Configure this writer to relax its syntax rules. By default, this writer only emits well-formed JSON as specified by [RFC 4627](http://www.ietf.org/rfc/rfc4627.txt). Setting the writer to lenient permits the following:

- Top-level values of any type. With strict writing, the top-level value must be an object or an array.
- Numbers may be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()).

<br />

### value

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(value: Boolean): JsonWriter!
```

Encodes`value`.

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### value

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(value: Double): JsonWriter!
```

Encodes`value`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite())unless this writer is lenient. |

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### value

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(value: Number!): JsonWriter!
```

Encodes`value`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite())unless this writer is lenient. |

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### value

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(value: String!): JsonWriter!
```

Encodes`value`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the literal string value, or null to encode a null literal. |

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |

### value

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(value: Long): JsonWriter!
```

Encodes`value`.

| Return ||
|----------------------------------------------------------------------------------------|--------------|
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter#)! | this writer. |
