# MailTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MailTo

Kotlin| [Java](../android/net/MailTo.md) 
| --- | --- |

```
open class MailTo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.MailTo](../android/net/MailTo.md) |

MailTo URL parser This class parses a mailto scheme URL and then can be queried for the parsed parameters. This implements RFC 2368.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAILTO_SCHEME](../android/net/MailTo.md) <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBody](../android/net/MailTo.md))`()` Retrieve the body line from the parsed mailto URL. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCc](../android/net/MailTo.md))`()` Retrieve the CC address line from the parsed mailto URL. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getHeaders](../android/net/MailTo.md))`()` Retrieve all the parsed email headers from the mailto URL |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubject](../android/net/MailTo.md))`()` Retrieve the subject line from the parsed mailto URL. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTo](../android/net/MailTo.md))`()` Retrieve the To address line from the parsed mailto URL. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMailTo](../android/net/MailTo.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Test to see if the given string is a mailto URL |
| --- | --- |
| openstatic [MailTo](../android/net/MailTo.md)! | [parse](../android/net/MailTo.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse and decode a mailto scheme string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/MailTo.md))`()` <br /> |

## Constants

### MAILTO_SCHEME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAILTO_SCHEME: String
```  

 Value: "mailto:"

## Public methods

### getBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBody(): String!
```

Retrieve the body line from the parsed mailto URL. If no body line was specified, then null is return

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | body or null |

### getCc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCc(): String!
```

Retrieve the CC address line from the parsed mailto URL. This could be several email address that are comma-space delimited. If no CC line was specified, then null is return

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | comma delimited email addresses or null |

### getHeaders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaders(): MutableMap<String!, String!>!
```

Retrieve all the parsed email headers from the mailto URL

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | map containing all parsed values |

### getSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubject(): String!
```

Retrieve the subject line from the parsed mailto URL. If no subject line was specified, then null is return

| Return ||
|-----------------------------------------------------------------------------------|-----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | subject or null |

### getTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTo(): String!
```

Retrieve the To address line from the parsed mailto URL. This could be several email address that are comma-space delimited. If no To line was specified, then null is return

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | comma delimited email addresses or null |

### isMailTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isMailTo(url: String!): Boolean
```

Test to see if the given string is a mailto URL

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to be tested |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the string is a mailto URL |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(url: String!): MailTo!
```

Parse and decode a mailto scheme string. This parser implements RFC 2368. The returned object can be queried for the parsed parameters.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String containing a mailto URL |

| Return ||
|-------------------------------------------------------------------------------|---------------|
| [MailTo](../android/net/MailTo.md)! | MailTo object |

| Exceptions ||
|------------------------------|-----------------------------------|
| `android.net.ParseException` | if the scheme is not a mailto URL |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
