# ConsoleMessage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConsoleMessage

Kotlin| [Java](../android/webkit/ConsoleMessage.md) 
| --- | --- |

```
open class ConsoleMessage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ConsoleMessage](../android/webkit/ConsoleMessage.md) |

Public class representing a JavaScript console message from WebCore. This could be a issued by a call to one of the`console`logging functions (e.g.`console.log('...')`) or a JavaScript error on the page. To receive notifications of these messages, override the [WebChromeClient.onConsoleMessage(ConsoleMessage)](../android/webkit/WebChromeClient.md))function.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------|
| | [MessageLevel](../android/webkit/ConsoleMessage.MessageLevel.md) <br /> |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConsoleMessage](../android/webkit/ConsoleMessage.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msgLevel:` ` [ConsoleMessage.MessageLevel](../android/webkit/ConsoleMessage.MessageLevel.md)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lineNumber](../android/webkit/ConsoleMessage.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [message](../android/webkit/ConsoleMessage.md))`()` <br /> |
| open [ConsoleMessage.MessageLevel](../android/webkit/ConsoleMessage.MessageLevel.md)! | [messageLevel](../android/webkit/ConsoleMessage.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [sourceId](../android/webkit/ConsoleMessage.md))`()` <br /> |

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
