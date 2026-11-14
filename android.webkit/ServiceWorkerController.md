# ServiceWorkerController

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerController

Kotlin| [Java](https://developer.android.com/reference/android/webkit/ServiceWorkerController "View this page in Java") 
| --- | --- |

```
abstract class ServiceWorkerController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#) |

Manages Service Workers used by WebView.

Example usage: 

```kotlin
ServiceWorkerController swController = ServiceWorkerController.getInstance();
  swController.setServiceWorkerClient(new ServiceWorkerClient() {
    @Override
    public WebResourceResponse shouldInterceptRequest(WebResourceRequest request) {
      // Capture request here and generate response or allow pass-through
      // by returning null.
      return null;
    }
  });
  
```

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#ServiceWorkerController())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#) | [getInstance](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#getInstance())`()` Returns the default ServiceWorkerController instance. |
| abstract [ServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings) | [getServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#getServiceWorkerWebSettings())`()` Gets the settings for all service workers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#setServiceWorkerClient(android.webkit.ServiceWorkerClient))`(`client:` ` [ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient)?`)` Sets the client to capture service worker related callbacks. |
| --- | --- |

## Public constructors

### ServiceWorkerController

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceWorkerController()
```

**Deprecated:** *This class should not be constructed by applications, use [getInstance()](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#getInstance())instead to fetch the singleton instance.*

## Public methods

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): ServiceWorkerController
```

Returns the default ServiceWorkerController instance. At present there is only one ServiceWorkerController instance for all WebView instances, however this restriction may be relaxed in the future.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController#) | the default ServiceWorkerController instance This value cannot be`null`. |

### getServiceWorkerWebSettings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getServiceWorkerWebSettings(): ServiceWorkerWebSettings
```

Gets the settings for all service workers.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings) | the current ServiceWorkerWebSettings This value cannot be`null`. |

### setServiceWorkerClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setServiceWorkerClient(client: ServiceWorkerClient?): Unit
```

Sets the client to capture service worker related callbacks. A [ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient) should be set before any service workers are active, e.g. a safe place is before any WebView instances are created or pages loaded.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `client` | [ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient)?:This value may be`null`. |
