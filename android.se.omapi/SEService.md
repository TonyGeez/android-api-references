# SEService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SEService

Kotlin| [Java](../android/se/omapi/SEService.md) 
| --- | --- |

```
class SEService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.se.omapi.SEService](../android/se/omapi/SEService.md) |

The SEService realises the communication to available Secure Elements on the device. This is the entry point of this API. It is used to connect to the infrastructure and get access to a list of Secure Element Readers.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnConnectedListener](../android/se/omapi/SEService.OnConnectedListener.md) Interface to send call-backs to the application when the service is connected. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SECURE_ELEMENT_STATE_CHANGED](../android/se/omapi/SEService.md) Broadcast Action: Intent to notify if the secure element state is changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_READER_NAME](../android/se/omapi/SEService.md) Mandatory extra containing the reader name of the state changed secure element. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_READER_STATE](../android/se/omapi/SEService.md) Mandatory extra containing the connected state of the state changed secure element. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SEService](../android/se/omapi/SEService.md))`(`context:` ` [Context](../android/content/Context.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [SEService.OnConnectedListener](../android/se/omapi/SEService.OnConnectedListener.md)`)` Establishes a new connection that can be used to connect to all the Secure Elements available in the system. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Reader](../android/se/omapi/Reader.md)!\> | [getReaders](../android/se/omapi/SEService.md))`()` Returns an array of available Secure Element readers. |
| [Reader](../android/se/omapi/Reader.md) | [getUiccReader](../android/se/omapi/SEService.md))`(`slotNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtain a UICC Reader instance with specific slot number from the SecureElementService |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersion](../android/se/omapi/SEService.md))`()` Returns the version of the OpenMobile API specification this implementation is based on. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/se/omapi/SEService.md))`()` Tells whether or not the service is connected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](../android/se/omapi/SEService.md))`()` Releases all Secure Elements resources allocated by this SEService (including any binding to an underlying service). |

## Constants

### ACTION_SECURE_ELEMENT_STATE_CHANGED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SECURE_ELEMENT_STATE_CHANGED: String
```

Broadcast Action: Intent to notify if the secure element state is changed. 

 Value: "android.se.omapi.action.SECURE_ELEMENT_STATE_CHANGED"

### EXTRA_READER_NAME

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_READER_NAME: String
```

Mandatory extra containing the reader name of the state changed secure element. 

 Value: "android.se.omapi.extra.READER_NAME"

**See Also**

- [android.se.omapi.Reader#getName()](../android/se/omapi/Reader.md)) 

### EXTRA_READER_STATE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_READER_STATE: String
```

Mandatory extra containing the connected state of the state changed secure element. True if the secure element is connected correctly, false otherwise. 

 Value: "android.se.omapi.extra.READER_STATE"

## Public constructors

### SEService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SEService(
    context: Context, 
    executor: Executor, 
    listener: SEService.OnConnectedListener)
```

Establishes a new connection that can be used to connect to all the Secure Elements available in the system. The connection process can be quite long, so it happens in an asynchronous way. It is usable only if the specified listener is called or if isConnected() returns`true`. 
The call-back object passed as a parameter will have its onConnected() method called when the connection actually happen.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the context of the calling application. Cannot be`null`. |
| `listener` | [SEService.OnConnectedListener](../android/se/omapi/SEService.OnConnectedListener.md):a OnConnectedListener object. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):an Executor which will be used when invoking the callback. This value cannot be`null`. |
| --- | --- |

## Public methods

### getReaders

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReaders(): Array<Reader!>
```

Returns an array of available Secure Element readers. There must be no duplicated objects in the returned list. All available readers shall be listed even if no card is inserted.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Reader](../android/se/omapi/Reader.md)!> | An array of Readers. If there are no readers the returned array is of length 0. This value cannot be`null`. |

### getUiccReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUiccReader(slotNumber: Int): Reader
```

Obtain a UICC Reader instance with specific slot number from the SecureElementService

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `slotNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the uicc slot. The index starts from 1. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Reader](../android/se/omapi/Reader.md) | A Reader object for this uicc slot. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the reader object corresponding to the uiccSlotNumber is not exist. |

### getVersion

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): String
```

Returns the version of the OpenMobile API specification this implementation is based on.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String containing the OpenMobile API version (e.g. "3.0"). This value cannot be`null`. |

### isConnected

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

Tells whether or not the service is connected.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the service is connected. |

### shutdown

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shutdown(): Unit
```

Releases all Secure Elements resources allocated by this SEService (including any binding to an underlying service). As a result isConnected() will return false after shutdown() was called. After this method call, the SEService object is not connected. This method should be called when connection to the Secure Element is not needed or in the termination method of the calling application (or part of this application) which is bound to this SEService.
