# UrlQuerySanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UrlQuerySanitizer

Kotlin| [Java](UrlQuerySanitizer.md) 
| --- | --- |

```
open class UrlQuerySanitizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.UrlQuerySanitizer](UrlQuerySanitizer.md) |

Sanitizes the Query portion of a URL. Simple example: 

```kotlin
UrlQuerySanitizer sanitizer = new UrlQuerySanitizer();
  sanitizer.setAllowUnregisteredParamaters(true);
  sanitizer.parseUrl("http://example.com/?name=Joe+User");
  String name = sanitizer.getValue("name"));
  // name now contains "Joe_User"
  
```
Register ValueSanitizers to customize the way individual parameters are sanitized: 

```kotlin
UrlQuerySanitizer sanitizer = new UrlQuerySanitizer();
  sanitizer.registerParamater("name", UrlQuerySanitizer.createSpaceLegal());
  sanitizer.parseUrl("http://example.com/?name=Joe+User");
  String name = sanitizer.getValue("name"));
  // name now contains "Joe User". (The string is first decoded, which
  // converts the '+' to a ' '. Then the string is sanitized, which
  // converts the ' ' to an '_'. (The ' ' is converted because the default
  unregistered parameter sanitizer does not allow any special characters,
  and ' ' is a special character.)
  
```

<br />

There are several ways to create ValueSanitizers. In order of increasing sophistication:

1. Call one of the UrlQuerySanitizer.createXXX() methods.
2. Construct your own instance of UrlQuerySanitizer.IllegalCharacterValueSanitizer.
3. Subclass UrlQuerySanitizer.ValueSanitizer to define your own value sanitizer.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [IllegalCharacterValueSanitizer](../android/net/UrlQuerySanitizer.IllegalCharacterValueSanitizer.md) Sanitize values based on which characters they contain. |
| open | [ParameterValuePair](../android/net/UrlQuerySanitizer.ParameterValuePair.md) A simple tuple that holds parameter-value pairs. |
| abstract | [ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md) A functor used to sanitize a single query value. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UrlQuerySanitizer](UrlQuerySanitizer.md))`()` Constructs a UrlQuerySanitizer. |
| [UrlQuerySanitizer](UrlQuerySanitizer.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a UrlQuerySanitizer and parses a URL. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAllButNulAndAngleBracketsLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that allows any special characters except angle brackets ('\<' and '\>') and Nul ('\\0'). |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAllButNulLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that allows everything except Nul ('\\0') characters. |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAllButWhitespaceLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that allows everything except Nul ('\\0') characters, space (' '), and other whitespace characters. |
| --- | --- |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAllIllegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that does not allow any special characters, and also does not allow script URLs. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowUnregisteredParamaters](UrlQuerySanitizer.md))`()` Get whether or not unregistered parameters are allowed. |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAmpAndSpaceLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that does not allow any special characters except ampersand ('\&') and space (' '). |
| --- | --- |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getAmpLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that does not allow any special characters except ampersand ('\&'). |
| open [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getEffectiveValueSanitizer](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the effective value sanitizer for a parameter. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UrlQuerySanitizer.ParameterValuePair](../android/net/UrlQuerySanitizer.ParameterValuePair.md)!\>! | [getParameterList](UrlQuerySanitizer.md))`()` An array list of all of the parameter-value pairs in the sanitized query, in the order they appeared in the query. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getParameterSet](UrlQuerySanitizer.md))`()` Get a set of all of the parameters found in the sanitized query. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPreferFirstRepeatedParameter](UrlQuerySanitizer.md))`()` Get whether or not the first occurrence of a repeated parameter is preferred. |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getSpaceLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that does not allow any special characters except space (' '). |
| --- | --- |
| open [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getUnregisteredParameterValueSanitizer](UrlQuerySanitizer.md))`()` Get the current value sanitizer used when processing unregistered parameter values. |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getUrlAndSpaceLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that allows all the characters used by encoded URLs and allows spaces, which are not technically legal in encoded URLs, but commonly appear anyway. |
| static [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getUrlLegal](UrlQuerySanitizer.md))`()` Return a value sanitizer that allows all the characters used by encoded URLs. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the value for a parameter in the current sanitized query. |
| open [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | [getValueSanitizer](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the value sanitizer for a parameter. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasParameter](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check if a parameter exists in the current sanitized query. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseQuery](UrlQuerySanitizer.md))`(`query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse a query. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseUrl](UrlQuerySanitizer.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the query parameters out of an encoded URL. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerParameter](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `valueSanitizer:` ` [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!`)` Register a value sanitizer for a particular parameter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerParameters](UrlQuerySanitizer.md))`(`parameters:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `valueSanitizer:` ` [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!`)` Register a value sanitizer for an array of parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowUnregisteredParamaters](UrlQuerySanitizer.md))`(`allowUnregisteredParamaters:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether or not unregistered parameters are allowed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferFirstRepeatedParameter](UrlQuerySanitizer.md))`(`preferFirstRepeatedParameter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether or not the first occurrence of a repeated parameter is preferred. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUnregisteredParameterValueSanitizer](UrlQuerySanitizer.md))`(`sanitizer:` ` [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!`)` Set the value sanitizer used when processing unregistered parameter values. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [unescape](UrlQuerySanitizer.md))`(`string:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addSanitizedEntry](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Record a sanitized parameter-value pair. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](UrlQuerySanitizer.md))`()` Clear the existing entries. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decodeHexDigit](UrlQuerySanitizer.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Convert a character that represents a hexidecimal digit into an integer. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHexDigit](UrlQuerySanitizer.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Test if a character is a hexidecimal digit. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseEntry](UrlQuerySanitizer.md))`(`parameter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse an escaped parameter-value pair. |

## Public constructors

### UrlQuerySanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UrlQuerySanitizer()
```

Constructs a UrlQuerySanitizer.

Defaults:

- unregistered parameters are not allowed.
- the last instance of a repeated parameter is preferred.
- The default value sanitizer is an AllIllegal value sanitizer. 

### UrlQuerySanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UrlQuerySanitizer(url: String!)
```

Constructs a UrlQuerySanitizer and parses a URL. This constructor is provided for convenience when the default parsing behavior is acceptable.

Because the URL is parsed before the constructor returns, there isn't a chance to configure the sanitizer to change the parsing behavior.

` UrlQuerySanitizer sanitizer = new UrlQuerySanitizer(myUrl); String name = sanitizer.getValue("name"); `

Defaults:

- unregistered parameters*are*allowed.
- the last instance of a repeated parameter is preferred.
- The default value sanitizer is an AllIllegal value sanitizer.

## Public methods

### getAllButNulAndAngleBracketsLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAllButNulAndAngleBracketsLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that allows any special characters except angle brackets ('\<' and '\>') and Nul ('\\0'). Allows script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getAllButNulLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAllButNulLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that allows everything except Nul ('\\0') characters. Script URLs are allowed.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getAllButWhitespaceLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAllButWhitespaceLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that allows everything except Nul ('\\0') characters, space (' '), and other whitespace characters. Script URLs are allowed.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getAllIllegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAllIllegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that does not allow any special characters, and also does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getAllowUnregisteredParamaters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllowUnregisteredParamaters(): Boolean
```

Get whether or not unregistered parameters are allowed. If not allowed, they will be dropped when a query is parsed.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if unregistered parameters are allowed. |

**See Also**

- [#setAllowUnregisteredParamaters(boolean)](UrlQuerySanitizer.md)) 

### getAmpAndSpaceLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAmpAndSpaceLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that does not allow any special characters except ampersand ('\&') and space (' '). Does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getAmpLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAmpLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that does not allow any special characters except ampersand ('\&'). Does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getEffectiveValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEffectiveValueSanitizer(parameter: String!): UrlQuerySanitizer.ValueSanitizer!
```

Get the effective value sanitizer for a parameter. Like getValueSanitizer, except if there is no value sanitizer registered for a parameter, and unregistered parameters are allowed, then the default value sanitizer is returned.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an unescaped parameter |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | the effective value sanitizer for a parameter. |

### getParameterList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameterList(): MutableList<UrlQuerySanitizer.ParameterValuePair!>!
```

An array list of all of the parameter-value pairs in the sanitized query, in the order they appeared in the query. May contain duplicate parameters.

**Note:**Do not modify this list. Treat it as a read-only list. 

### getParameterSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameterSet(): MutableSet<String!>!
```

Get a set of all of the parameters found in the sanitized query.

Note: Do not modify this set. Treat it as a read-only set.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | all the parameters found in the current query. |

### getPreferFirstRepeatedParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferFirstRepeatedParameter(): Boolean
```

Get whether or not the first occurrence of a repeated parameter is preferred.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the first occurrence of a repeated parameter is preferred. |

**See Also**

- [#setPreferFirstRepeatedParameter(boolean)](UrlQuerySanitizer.md)) 

### getSpaceLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSpaceLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that does not allow any special characters except space (' '). Does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getUnregisteredParameterValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnregisteredParameterValueSanitizer(): UrlQuerySanitizer.ValueSanitizer!
```

Get the current value sanitizer used when processing unregistered parameter values.

**Note:**The default unregistered parameter value sanitizer is one that doesn't allow any special characters, similar to what is returned by calling createAllIllegal.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | the current ValueSanitizer used to sanitize unregistered parameter values. |

### getUrlAndSpaceLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getUrlAndSpaceLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that allows all the characters used by encoded URLs and allows spaces, which are not technically legal in encoded URLs, but commonly appear anyway. Does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getUrlLegal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getUrlLegal(): UrlQuerySanitizer.ValueSanitizer!
```

Return a value sanitizer that allows all the characters used by encoded URLs. Does not allow script URLs.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | a value sanitizer |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(parameter: String!): String!
```

Get the value for a parameter in the current sanitized query. Returns null if the parameter does not exit.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unencoded name of a parameter. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the sanitized unencoded value of the parameter, or null if the parameter does not exist. |

### getValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValueSanitizer(parameter: String!): UrlQuerySanitizer.ValueSanitizer!
```

Get the value sanitizer for a parameter. Returns null if there is no value sanitizer registered for the parameter.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unescaped parameter |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)! | the currently registered value sanitizer for this parameter. |

**See Also**

- [#registerParameter(String, android.net.UrlQuerySanitizer.ValueSanitizer)](UrlQuerySanitizer.md)) 

### hasParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasParameter(parameter: String!): Boolean
```

Check if a parameter exists in the current sanitized query.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the unencoded name of a parameter. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the parameter exists in the current sanitized queary. |

### parseQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseQuery(query: String!): Unit
```

Parse a query. A query string is any number of parameter-value clauses separated by any non-zero number of ampersands. A parameter-value clause is a parameter followed by an equal sign, followed by a value. If the equal sign is missing, the value is assumed to be the empty string.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the query to parse. |

### parseUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseUrl(url: String!): Unit
```

Parse the query parameters out of an encoded URL. Works by extracting the query portion from the URL and then calling parseQuery(). If there is no query portion it is treated as if the query portion is an empty string.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the encoded URL to parse. |

### registerParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerParameter(
    parameter: String!, 
    valueSanitizer: UrlQuerySanitizer.ValueSanitizer!
): Unit
```

Register a value sanitizer for a particular parameter. Can also be used to replace or remove an already-set value sanitizer.

Registering a non-null value sanitizer for a particular parameter makes that parameter a registered parameter.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an unencoded parameter name |
| `valueSanitizer` | [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!:the value sanitizer to use for a particular parameter. May be null in order to unregister that parameter. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer#getAllowUnregisteredParamaters()> 

### registerParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerParameters(
    parameters: Array<String!>!, 
    valueSanitizer: UrlQuerySanitizer.ValueSanitizer!
): Unit
```

Register a value sanitizer for an array of parameters.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:An array of unencoded parameter names. |
| `valueSanitizer` | [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!: |

**See Also**

- [#registerParameter](UrlQuerySanitizer.md)) 

### setAllowUnregisteredParamaters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAllowUnregisteredParamaters(allowUnregisteredParamaters: Boolean): Unit
```

Set whether or not unregistered parameters are allowed. If they are not allowed, then they will be dropped when a query is sanitized.

Defaults to false.

| Parameters ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `allowUnregisteredParamaters` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to allow unregistered parameters. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer#getAllowUnregisteredParamaters()> 

### setPreferFirstRepeatedParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferFirstRepeatedParameter(preferFirstRepeatedParameter: Boolean): Unit
```

Set whether or not the first occurrence of a repeated parameter is preferred. True means the first repeated parameter is preferred. False means that the last repeated parameter is preferred.

The preferred parameter is the one that is returned when getParameter is called.

defaults to false.

| Parameters ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `preferFirstRepeatedParameter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the first repeated parameter is preferred. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer#getPreferFirstRepeatedParameter()> 

### setUnregisteredParameterValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUnregisteredParameterValueSanitizer(sanitizer: UrlQuerySanitizer.ValueSanitizer!): Unit
```

Set the value sanitizer used when processing unregistered parameter values.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sanitizer` | [UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md)!:set the ValueSanitizer used to sanitize unregistered parameter values. |

### unescape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unescape(string: String!): String!
```

## Protected methods

### addSanitizedEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun addSanitizedEntry(
    parameter: String!, 
    value: String!
): Unit
```

Record a sanitized parameter-value pair. Override if you want to do additional filtering or validation.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an unescaped parameter |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a sanitized unescaped value |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clear(): Unit
```

Clear the existing entries. Called to get ready to parse a new query string. 

### decodeHexDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun decodeHexDigit(c: Char): Int
```

Convert a character that represents a hexidecimal digit into an integer. If the character is not a hexidecimal digit, then -1 is returned. Both upper case and lower case hex digits are allowed.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the hexidecimal digit. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer value of the hexidecimal digit. |

### isHexDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun isHexDigit(c: Char): Boolean
```

Test if a character is a hexidecimal digit. Both upper case and lower case hex digits are allowed.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character to test |

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if c is a hex digit. |

### parseEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun parseEntry(
    parameter: String!, 
    value: String!
): Unit
```

Parse an escaped parameter-value pair. The default implementation unescapes both the parameter and the value, then looks up the effective value sanitizer for the parameter and uses it to sanitize the value. If all goes well then addSanitizedValue is called with the unescaped parameter and the sanitized unescaped value.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------|
| `parameter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an escaped parameter |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an unsanitized escaped value |
