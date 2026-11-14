# ServiceWorkerController

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerController

Kotlin| [Java](ServiceWorkerController.md) 
| --- | --- |

```
abstract class ServiceWorkerController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ServiceWorkerController](ServiceWorkerController.md) |

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
| [ServiceWorkerController](ServiceWorkerController.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ServiceWorkerController](ServiceWorkerController.md) | [getInstance](ServiceWorkerController.md))`()` Returns the default ServiceWorkerController instance. |
| abstract [ServiceWorkerWebSettings](ServiceWorkerWebSettings.md) | [getServiceWorkerWebSettings](ServiceWorkerController.md))`()` Gets the settings for all service workers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceWorkerClient](ServiceWorkerController.md))`(`client:` ` [ServiceWorkerClient](ServiceWorkerClient.md)?`)` Sets the client to capture service worker related callbacks. |
| --- | --- |

## Public constructors

### ServiceWorkerController

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceWorkerController()
```

**Deprecated:** *This class should not be constructed by applications, use [getInstance()](ServiceWorkerController.md))instead to fetch the singleton instance.*

## Public methods

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): ServiceWorkerController
```

Returns the default ServiceWorkerController instance. At present there is only one ServiceWorkerController instance for all WebView instances, however this restriction may be relaxed in the future.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ServiceWorkerController](ServiceWorkerController.md) | the default ServiceWorkerController instance This value cannot be`null`. |

### getServiceWorkerWebSettings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getServiceWorkerWebSettings(): ServiceWorkerWebSettings
```

Gets the settings for all service workers.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ServiceWorkerWebSettings](ServiceWorkerWebSettings.md) | the current ServiceWorkerWebSettings This value cannot be`null`. |

### setServiceWorkerClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setServiceWorkerClient(client: ServiceWorkerClient?): Unit
```

Sets the client to capture service worker related callbacks. A [ServiceWorkerClient](ServiceWorkerClient.md) should be set before any service workers are active, e.g. a safe place is before any WebView instances are created or pages loaded.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `client` | [ServiceWorkerClient](ServiceWorkerClient.md)?:This value may be`null`. |
