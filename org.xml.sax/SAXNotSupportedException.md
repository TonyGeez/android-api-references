# SAXNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXNotSupportedException

```
open class SAXNotSupportedException : SAXException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) ||
| | | | ↳ | [org.xml.sax.SAXNotSupportedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotSupportedException#) |

Exception class for an unsupported operation.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

An XMLReader will throw this exception when it recognizes a feature or property identifier, but cannot perform the requested operation (setting a state or value). Other SAX2 applications and extensions may use this class for similar purposes.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXNotSupportedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotSupportedException#SAXNotSupportedException())`()` Construct a new exception with no message. |
| [SAXNotSupportedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotSupportedException#SAXNotSupportedException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a new exception with the given message. |

| Inherited functions ||
|---|---|
| From class [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) |----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [getException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#getException())`()` <br /> Return the embedded exception, if any. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#toString())`()` <br /> Override toString to pick up any embedded exception. <br /> | ||

| Inherited properties ||
|---|---|
| From class [SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException#message:kotlin.String) <br /> Return a detail message for this exception. If there is an embedded exception, and if the SAXException has no detail message of its own, this method will return the detail message from the embedded exception. <br /> | ||

## Public constructors

### SAXNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXNotSupportedException()
```

Construct a new exception with no message. 

### SAXNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXNotSupportedException(message: String!)
```

Construct a new exception with the given message.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text message of the exception. |
