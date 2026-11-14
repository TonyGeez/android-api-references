# JsonReader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsonReader

Kotlin| [Java](https://developer.android.com/reference/android/util/JsonReader "View this page in Java") 

```
class JsonReader : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.util.JsonReader](https://developer.android.com/reference/kotlin/android/util/JsonReader#) |

Reads a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value as a stream of tokens. This stream includes both literal values (strings, numbers, booleans, and nulls) as well as the begin and end delimiters of objects and arrays. The tokens are traversed in depth-first order, the same order that they appear in the JSON document. Within JSON objects, name/value pairs are represented by a single token.

### Parsing JSON

To create a recursive descent parser for your own JSON streams, first create an entry point method that creates a`JsonReader`.

<br />

Next, create handler methods for each structure in your JSON text. You'll need a method for each object type and for each array type.

- Within**array handling** methods, first call [beginArray](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginArray())to consume the array's opening bracket. Then create a while loop that accumulates values, terminating when [hasNext](https://developer.android.com/reference/kotlin/android/util/JsonReader#hasNext())is false. Finally, read the array's closing bracket by calling [endArray](https://developer.android.com/reference/kotlin/android/util/JsonReader#endArray()).
- Within**object handling** methods, first call [beginObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginObject())to consume the object's opening brace. Then create a while loop that assigns values to local variables based on their name. This loop should terminate when [hasNext](https://developer.android.com/reference/kotlin/android/util/JsonReader#hasNext())is false. Finally, read the object's closing brace by calling [endObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#endObject()).

When a nested object or array is encountered, delegate to the corresponding handler method.

When an unknown name is encountered, strict parsers should fail with an exception. Lenient parsers should call [skipValue()](https://developer.android.com/reference/kotlin/android/util/JsonReader#skipValue())to recursively skip the value's nested tokens, which may otherwise conflict.

If a value may be null, you should first check using [peek()](https://developer.android.com/reference/kotlin/android/util/JsonReader#peek()). Null literals can be consumed using either [nextNull()](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextNull())or [skipValue()](https://developer.android.com/reference/kotlin/android/util/JsonReader#skipValue()).

### Example

Suppose we'd like to parse a stream of messages such as the following: 

```kotlin
<code>[
    {
      "id": 912345678901,
      "text": "How do I read JSON on Android?",
      "geo": null,
      "user": {
        "name": "android_newb",
        "followers_count": 41
       }
    },
    {
      "id": 912345678902,
      "text": "@android_newb just use android.util.JsonReader!",
      "geo": [50.454722, -104.606667],
      "user": {
        "name": "jesse",
        "followers_count": 2
      }
    }
  ]</code>
```
This code implements the parser for the above structure: 

```kotlin
<code>public List&lt;Message&gt; readJsonStream(InputStream in) throws IOException {
      JsonReader reader = new JsonReader(new InputStreamReader(in, "UTF-8"));
      try {
        return readMessagesArray(reader);
      } finally {
        reader.close();
      }
    }
 
    public List&lt;Message&gt; readMessagesArray(JsonReader reader) throws IOException {
      List&lt;Message&gt; messages = new ArrayList&lt;Message&gt;();
 
      reader.beginArray();
      while (reader.hasNext()) {
        messages.add(readMessage(reader));
      }
      reader.endArray();
      return messages;
    }
 
    public Message readMessage(JsonReader reader) throws IOException {
      long id = -1;
      String text = null;
      User user = null;
      List&lt;Double&gt; geo = null;
 
      reader.beginObject();
      while (reader.hasNext()) {
        String name = reader.nextName();
        if (name.equals("id")) {
          id = reader.nextLong();
        } else if (name.equals("text")) {
          text = reader.nextString();
        } else if (name.equals("geo") &amp;&amp; reader.peek() != JsonToken.NULL) {
          geo = readDoublesArray(reader);
        } else if (name.equals("user")) {
          user = readUser(reader);
        } else {
          reader.skipValue();
        }
      }
      reader.endObject();
      return new Message(id, text, user, geo);
    }
 
    public List&lt;Double&gt; readDoublesArray(JsonReader reader) throws IOException {
      List&lt;Double&gt; doubles = new ArrayList&lt;Double&gt;();
 
      reader.beginArray();
      while (reader.hasNext()) {
        doubles.add(reader.nextDouble());
      }
      reader.endArray();
      return doubles;
    }
 
    public User readUser(JsonReader reader) throws IOException {
      String username = null;
      int followersCount = -1;
 
      reader.beginObject();
      while (reader.hasNext()) {
        String name = reader.nextName();
        if (name.equals("name")) {
          username = reader.nextString();
        } else if (name.equals("followers_count")) {
          followersCount = reader.nextInt();
        } else {
          reader.skipValue();
        }
      }
      reader.endObject();
      return new User(username, followersCount);
    }</code>
```

### Number Handling

This reader permits numeric values to be read as strings and string values to be read as numbers. For example, both elements of the JSON array`[1, "1"]`may be read using either [nextInt](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextInt())or [nextString](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextString()). This behavior is intended to prevent lossy numeric conversions: double is JavaScript's only numeric type and very large values like`9007199254740993`cannot be represented exactly on that platform. To minimize precision loss, extremely large values should be written and read as strings in JSON.

Each`JsonReader`may be used to read a single JSON stream. Instances of this class are not thread safe.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JsonReader](https://developer.android.com/reference/kotlin/android/util/JsonReader#JsonReader(java.io.Reader))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Creates a new instance that reads a JSON-encoded stream from`in`. |

| Public methods ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beginArray](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginArray())`()` Consumes the next token from the JSON stream and asserts that it is the beginning of a new array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beginObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#beginObject())`()` Consumes the next token from the JSON stream and asserts that it is the beginning of a new object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/util/JsonReader#close())`()` Closes this JSON reader and the underlying [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endArray](https://developer.android.com/reference/kotlin/android/util/JsonReader#endArray())`()` Consumes the next token from the JSON stream and asserts that it is the end of the current array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endObject](https://developer.android.com/reference/kotlin/android/util/JsonReader#endObject())`()` Consumes the next token from the JSON stream and asserts that it is the end of the current object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNext](https://developer.android.com/reference/kotlin/android/util/JsonReader#hasNext())`()` Returns true if the current array or object has another element. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](https://developer.android.com/reference/kotlin/android/util/JsonReader#isLenient())`()` Returns true if this parser is liberal in what it accepts. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextBoolean](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextBoolean())`()` Returns the [boolean](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextDouble())`()` Returns the [double](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextInt())`()` Returns the [int](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextLong())`()` Returns the [long](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nextName](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextName())`()` Returns the next token, a [property name](https://developer.android.com/reference/kotlin/android/util/JsonToken), and consumes it. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [nextNull](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextNull())`()` Consumes the next token from the JSON stream and asserts that it is a literal null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nextString](https://developer.android.com/reference/kotlin/android/util/JsonReader#nextString())`()` Returns the [string](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. |
| [JsonToken](https://developer.android.com/reference/kotlin/android/util/JsonToken)! | [peek](https://developer.android.com/reference/kotlin/android/util/JsonReader#peek())`()` Returns the type of the next token without consuming it. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](https://developer.android.com/reference/kotlin/android/util/JsonReader#setLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Configure this parser to be be liberal in what it accepts. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipValue](https://developer.android.com/reference/kotlin/android/util/JsonReader#skipValue())`()` Skips the next value recursively. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/util/JsonReader#toString())`()` <br /> |

## Public constructors

### JsonReader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JsonReader(in: Reader!)
```

Creates a new instance that reads a JSON-encoded stream from`in`.

## Public methods

### beginArray

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun beginArray(): Unit
```

Consumes the next token from the JSON stream and asserts that it is the beginning of a new array. 

### beginObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun beginObject(): Unit
```

Consumes the next token from the JSON stream and asserts that it is the beginning of a new object. 

### close

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes this JSON reader and the underlying [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#).

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### endArray

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endArray(): Unit
```

Consumes the next token from the JSON stream and asserts that it is the end of the current array. 

### endObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endObject(): Unit
```

Consumes the next token from the JSON stream and asserts that it is the end of the current object. 

### hasNext

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNext(): Boolean
```

Returns true if the current array or object has another element. 

### isLenient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLenient(): Boolean
```

Returns true if this parser is liberal in what it accepts. 

### nextBoolean

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextBoolean(): Boolean
```

Returns the [boolean](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not a boolean or if this reader is closed. |

### nextDouble

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextDouble(): Double
```

Returns the [double](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. If the next token is a string, this method will attempt to parse it as a double using [Double.parseDouble(String)](https://developer.android.com/reference/kotlin/java/lang/Double.html#parseDouble(kotlin.String)).

| Exceptions ||
|-----------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not a literal value. |

### nextInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextInt(): Int
```

Returns the [int](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. If the next token is a string, this method will attempt to parse it as an int. If the next token's numeric value cannot be exactly represented by a Java`int`, this method throws.

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not a literal value. |
| `java.lang.NumberFormatException` | if the next literal value cannot be parsed as a number, or exactly represented as an int. |

### nextLong

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextLong(): Long
```

Returns the [long](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. If the next token is a string, this method will attempt to parse it as a long. If the next token's numeric value cannot be exactly represented by a Java`long`, this method throws.

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not a literal value. |
| `java.lang.NumberFormatException` | if the next literal value cannot be parsed as a number, or exactly represented as a long. |

### nextName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextName(): String!
```

Returns the next token, a [property name](https://developer.android.com/reference/kotlin/android/util/JsonToken), and consumes it.

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | if the next token in the stream is not a property name. |

### nextNull

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextNull(): Unit
```

Consumes the next token from the JSON stream and asserts that it is a literal null.

| Exceptions ||
|-----------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not null or if this reader is closed. |

### nextString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextString(): String!
```

Returns the [string](https://developer.android.com/reference/kotlin/android/util/JsonToken) value of the next token, consuming it. If the next token is a number, this method will return its string form.

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the next token is not a string or if this reader is closed. |

### peek

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun peek(): JsonToken!
```

Returns the type of the next token without consuming it. 

### setLenient

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLenient(lenient: Boolean): Unit
```

Configure this parser to be be liberal in what it accepts. By default, this parser is strict and only accepts JSON as specified by [RFC 4627](http://www.ietf.org/rfc/rfc4627.txt). Setting the parser to lenient causes it to ignore the following syntax errors:

- End of line comments starting with`//`orand ending with a newline character.
- C-style comments starting with`/*`and ending with`*``/`. Such comments may not be nested.
- Names that are unquoted or`'single quoted'`.
- Strings that are unquoted or`'single quoted'`.
- Array elements separated by`;`instead of`,`.
- Unnecessary array separators. These are interpreted as if null was the omitted value.
- Names and values separated by`=`or`=>`instead of`:`.
- Name/value pairs separated by`;`instead of`,`.

<br />

### skipValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun skipValue(): Unit
```

Skips the next value recursively. If it is an object or array, all nested elements are skipped. This method is intended for use when the JSON token stream contains unrecognized or unhandled values. 

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
