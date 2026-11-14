# SAXNotRecognizedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXNotRecognizedException

```
open class SAXNotRecognizedException : SAXException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [org.xml.sax.SAXException](../org/xml/sax/SAXException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [org.xml.sax.SAXNotRecognizedException](../org/xml/sax/SAXNotRecognizedException.md) |

Exception class for an unrecognized identifier. *This module, both source code and documentation, is in the Public Domain, and comes with **NO WARRANTY**.* See <http://www.saxproject.org> for further information.

An XMLReader will throw this exception when it finds an unrecognized feature or property identifier; SAX applications and extensions may use this class for other, similar purposes.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXNotRecognizedException](../org/xml/sax/SAXNotRecognizedException.md))`()` Default constructor. |
| [SAXNotRecognizedException](../org/xml/sax/SAXNotRecognizedException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a new exception with the given message. |

| Inherited functions ||
|---|---|
| From class [SAXException](../org/xml/sax/SAXException.md) |----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Exception](../java/lang/Exception.md)! | [getException](../org/xml/sax/SAXException.md))`()` Return the embedded exception, if any. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../org/xml/sax/SAXException.md))`()` Override toString to pick up any embedded exception. <br /> | ||

| Inherited properties ||
|---|---|
| From class [SAXException](../org/xml/sax/SAXException.md) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../org/xml/sax/SAXException.md) Return a detail message for this exception. If there is an embedded exception, and if the SAXException has no detail message of its own, this method will return the detail message from the embedded exception. <br /> | ||

## Public constructors

### SAXNotRecognizedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXNotRecognizedException()
```

Default constructor. 

### SAXNotRecognizedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXNotRecognizedException(message: String!)
```

Construct a new exception with the given message.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text message of the exception. |
