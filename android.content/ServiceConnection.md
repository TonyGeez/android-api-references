# ServiceConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceConnection

Kotlin| [Java](ServiceConnection.md) 
| --- | --- |

```
interface ServiceConnection
```

| [android.content.ServiceConnection](ServiceConnection.md) |

| Known Direct Subclasses [MediaScannerConnection](../android.media/MediaScannerConnection.md) |---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [MediaScannerConnection](../android.media/MediaScannerConnection.md) | MediaScannerConnection provides a way for applications to pass a newly created or downloaded media file to the media scanner service. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for monitoring the state of an application service. See [android.app.Service](../android.app/Service.md) and android.content.Context#bindService for more information.

Like many callbacks from the system, the methods on this class are called from the main thread of your process.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindingDied](ServiceConnection.md))`(`name:` ` [ComponentName](ComponentName.md)!`)` Called when the binding to this connection is dead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNullBinding](ServiceConnection.md))`(`name:` ` [ComponentName](ComponentName.md)!`)` Called when the service being bound has returned`null`from its [onBind()](../android.app/Service.md))method. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceConnected](ServiceConnection.md))`(`name:` ` [ComponentName](ComponentName.md)!`, `service:` ` [IBinder](../android.os/IBinder.md)!`)` Called when a connection to the Service has been established, with the [android.os.IBinder](../android.os/IBinder.md) of the communication channel to the Service. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDisconnected](ServiceConnection.md))`(`name:` ` [ComponentName](ComponentName.md)!`)` Called when a connection to the Service has been lost. |

## Public methods

### onBindingDied

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBindingDied(name: ComponentName!): Unit
```

Called when the binding to this connection is dead. This means the interface will never receive another connection. The application will need to unbind and rebind the connection to activate it again. This may happen, for example, if the application hosting the service it is bound to has been updated.

**Note:** The app that requested the binding must call [Context.unbindService(ServiceConnection)](Context.md))to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](ComponentName.md)!:The concrete component name of the service whose connection is dead. |

### onNullBinding

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNullBinding(name: ComponentName!): Unit
```

Called when the service being bound has returned`null`from its [onBind()](../android.app/Service.md))method. This indicates that the attempted service binding represented by this ServiceConnection will never become usable.

**Note:** The app that requested the binding must still call [Context.unbindService(ServiceConnection)](Context.md))to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](ComponentName.md)!:The concrete component name of the service whose binding has been rejected by the Service implementation. |

### onServiceConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceConnected(
    name: ComponentName!, 
    service: IBinder!
): Unit
```

Called when a connection to the Service has been established, with the [android.os.IBinder](../android.os/IBinder.md) of the communication channel to the Service.

**Note:**If the system has started to bind your client app to a service, it's possible that your app will never receive this callback. Your app won't receive a callback if there's an issue with the service, such as the service crashing while being created.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](ComponentName.md)!:The concrete component name of the service that has been connected. |
| `service` | [IBinder](../android.os/IBinder.md)!:The IBinder of the Service's communication channel, which you can now make calls on. |

### onServiceDisconnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceDisconnected(name: ComponentName!): Unit
```

Called when a connection to the Service has been lost. This typically happens when the process hosting the service has crashed or been killed. This does*not* remove the ServiceConnection itself -- this binding to the service will remain active, and you will receive a call to [onServiceConnected](ServiceConnection.md))when the Service is next running.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](ComponentName.md)!:The concrete component name of the service whose connection has been lost. |
