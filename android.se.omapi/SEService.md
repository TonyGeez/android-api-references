# SEService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SEService

Kotlin| [Java](https://developer.android.com/reference/android/se/omapi/SEService "View this page in Java") 
| --- | --- |

```
class SEService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.se.omapi.SEService](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#) |

The SEService realises the communication to available Secure Elements on the device. This is the entry point of this API. It is used to connect to the infrastructure and get access to a list of Secure Element Readers.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnConnectedListener](https://developer.android.com/reference/kotlin/android/se/omapi/SEService.OnConnectedListener) Interface to send call-backs to the application when the service is connected. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SECURE_ELEMENT_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#ACTION_SECURE_ELEMENT_STATE_CHANGED:kotlin.String) Broadcast Action: Intent to notify if the secure element state is changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_READER_NAME](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#EXTRA_READER_NAME:kotlin.String) Mandatory extra containing the reader name of the state changed secure element. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_READER_STATE](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#EXTRA_READER_STATE:kotlin.String) Mandatory extra containing the connected state of the state changed secure element. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SEService](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#SEService(android.content.Context,%20java.util.concurrent.Executor,%20android.se.omapi.SEService.OnConnectedListener))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [SEService.OnConnectedListener](https://developer.android.com/reference/kotlin/android/se/omapi/SEService.OnConnectedListener)`)` Establishes a new connection that can be used to connect to all the Secure Elements available in the system. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Reader](https://developer.android.com/reference/kotlin/android/se/omapi/Reader)!\> | [getReaders](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#getReaders())`()` Returns an array of available Secure Element readers. |
| [Reader](https://developer.android.com/reference/kotlin/android/se/omapi/Reader) | [getUiccReader](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#getUiccReader(kotlin.Int))`(`slotNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtain a UICC Reader instance with specific slot number from the SecureElementService |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#getVersion())`()` Returns the version of the OpenMobile API specification this implementation is based on. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#isConnected())`()` Tells whether or not the service is connected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/android/se/omapi/SEService#shutdown())`()` Releases all Secure Elements resources allocated by this SEService (including any binding to an underlying service). |

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

- [android.se.omapi.Reader#getName()](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#getName()) 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context of the calling application. Cannot be`null`. |
| `listener` | [SEService.OnConnectedListener](https://developer.android.com/reference/kotlin/android/se/omapi/SEService.OnConnectedListener):a OnConnectedListener object. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):an Executor which will be used when invoking the callback. This value cannot be`null`. |
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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Reader](https://developer.android.com/reference/kotlin/android/se/omapi/Reader)!> | An array of Readers. If there are no readers the returned array is of length 0. This value cannot be`null`. |

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
| [Reader](https://developer.android.com/reference/kotlin/android/se/omapi/Reader) | A Reader object for this uicc slot. This value cannot be`null`. |

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
