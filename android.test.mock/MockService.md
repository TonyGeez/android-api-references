# MockService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockService

Kotlin| [Java](../android/test/mock/MockService.md) 
| --- | --- |

```
open class MockService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.mock.MockService](../android/test/mock/MockService.md) |

| **This class was deprecated in API level 28.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.app.Service](../android/app/Service.md) class.

Provided for use by`android.test.ServiceTestCase`.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachForTesting](../android/test/mock/MockService.md))`(`service:` ` [Service](../android/app/Service.md)!`, `context:` ` [Context](../android/content/Context.md)!`, `serviceClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `application:` ` [Application](../android/app/Application.md)!`)` <br /> |

## Public methods

### attachForTesting

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Service!> attachForTesting(
    service: Service!, 
    context: Context!, 
    serviceClassName: String!, 
    application: Application!
): Unit
```

**Deprecated:** *Deprecated in Java.*
