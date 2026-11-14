# MockService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockService

Kotlin| [Java](https://developer.android.com/reference/android/test/mock/MockService "View this page in Java") 

```
open class MockService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.mock.MockService](https://developer.android.com/reference/kotlin/android/test/mock/MockService#) |

| **This class was deprecated in API level 28.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) class.

Provided for use by`android.test.ServiceTestCase`.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachForTesting](https://developer.android.com/reference/kotlin/android/test/mock/MockService#attachForTesting(android.app.Service,%20android.content.Context,%20kotlin.String,%20android.app.Application))`(`service:` ` [Service](https://developer.android.com/reference/kotlin/android/app/Service.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `serviceClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `application:` ` [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!`)` <br /> |

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
