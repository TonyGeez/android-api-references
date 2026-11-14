# ConsoleMessage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConsoleMessage

Kotlin| [Java](https://developer.android.com/reference/android/webkit/ConsoleMessage "View this page in Java") 
| --- | --- |

```
open class ConsoleMessage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ConsoleMessage](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#) |

Public class representing a JavaScript console message from WebCore. This could be a issued by a call to one of the`console`logging functions (e.g.`console.log('...')`) or a JavaScript error on the page. To receive notifications of these messages, override the [WebChromeClient.onConsoleMessage(ConsoleMessage)](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient#onConsoleMessage(android.webkit.ConsoleMessage))function.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------|
| | [MessageLevel](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage.MessageLevel) <br /> |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConsoleMessage](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#ConsoleMessage(kotlin.String,%20kotlin.String,%20kotlin.Int,%20android.webkit.ConsoleMessage.MessageLevel))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msgLevel:` ` [ConsoleMessage.MessageLevel](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage.MessageLevel)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lineNumber](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#lineNumber())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [message](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#message())`()` <br /> |
| open [ConsoleMessage.MessageLevel](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage.MessageLevel)! | [messageLevel](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#messageLevel())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [sourceId](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage#sourceId())`()` <br /> |

## Public constructors

### ConsoleMessage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConsoleMessage(
    message: String!, 
    sourceId: String!, 
    lineNumber: Int, 
    msgLevel: ConsoleMessage.MessageLevel!)
```

## Public methods

### lineNumber

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lineNumber(): Int
```  

### message

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun message(): String!
```  

### messageLevel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun messageLevel(): ConsoleMessage.MessageLevel!
```  

### sourceId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sourceId(): String!
```
