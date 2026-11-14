# ServiceConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceConnection

Kotlin| [Java](https://developer.android.com/reference/android/content/ServiceConnection "View this page in Java") 

```
interface ServiceConnection
```

| [android.content.ServiceConnection](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#) |

| Known Direct Subclasses [MediaScannerConnection](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#) |---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [MediaScannerConnection](https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#) | MediaScannerConnection provides a way for applications to pass a newly created or downloaded media file to the media scanner service. | |

Interface for monitoring the state of an application service. See [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) and android.content.Context#bindService for more information.

Like many callbacks from the system, the methods on this class are called from the main thread of your process.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindingDied](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onBindingDied(android.content.ComponentName))`(`name:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!`)` Called when the binding to this connection is dead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNullBinding](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onNullBinding(android.content.ComponentName))`(`name:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!`)` Called when the service being bound has returned`null`from its [onBind()](https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent))method. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceConnected](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onServiceConnected(android.content.ComponentName,%20android.os.IBinder))`(`name:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!`, `service:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!`)` Called when a connection to the Service has been established, with the [android.os.IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) of the communication channel to the Service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDisconnected](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onServiceDisconnected(android.content.ComponentName))`(`name:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!`)` Called when a connection to the Service has been lost. |

## Public methods

### onBindingDied

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBindingDied(name: ComponentName!): Unit
```

Called when the binding to this connection is dead. This means the interface will never receive another connection. The application will need to unbind and rebind the connection to activate it again. This may happen, for example, if the application hosting the service it is bound to has been updated.

**Note:** The app that requested the binding must call [Context.unbindService(ServiceConnection)](https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection))to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!:The concrete component name of the service whose connection is dead. |

### onNullBinding

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNullBinding(name: ComponentName!): Unit
```

Called when the service being bound has returned`null`from its [onBind()](https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent))method. This indicates that the attempted service binding represented by this ServiceConnection will never become usable.

**Note:** The app that requested the binding must still call [Context.unbindService(ServiceConnection)](https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection))to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!:The concrete component name of the service whose binding has been rejected by the Service implementation. |

### onServiceConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceConnected(
    name: ComponentName!, 
    service: IBinder!
): Unit
```

Called when a connection to the Service has been established, with the [android.os.IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) of the communication channel to the Service.

**Note:**If the system has started to bind your client app to a service, it's possible that your app will never receive this callback. Your app won't receive a callback if there's an issue with the service, such as the service crashing while being created.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!:The concrete component name of the service that has been connected. |
| `service` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!:The IBinder of the Service's communication channel, which you can now make calls on. |

### onServiceDisconnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceDisconnected(name: ComponentName!): Unit
```

Called when a connection to the Service has been lost. This typically happens when the process hosting the service has crashed or been killed. This does*not* remove the ServiceConnection itself -- this binding to the service will remain active, and you will receive a call to [onServiceConnected](https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onServiceConnected(android.content.ComponentName,%20android.os.IBinder))when the Service is next running.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName)!:The concrete component name of the service whose connection has been lost. |
