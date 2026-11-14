# Reader

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Reader

Kotlin| [Java](https://developer.android.com/reference/android/se/omapi/Reader "View this page in Java") 
| --- | --- |

```
class Reader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.se.omapi.Reader](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#) |

Instances of this class represent Secure Element Readers supported to this device. These Readers can be physical devices or virtual devices. They can be removable or not. They can contain Secure Element that can or cannot be removed.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeSessions](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#closeSessions())`()` Close all the sessions opened on this reader. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#getName())`()` Return the name of this reader. |
| [SEService](https://developer.android.com/reference/kotlin/android/se/omapi/SEService) | [getSEService](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#getSEService())`()` Return the Secure Element service this reader is bound to. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecureElementPresent](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#isSecureElementPresent())`()` Check if a Secure Element is present in this reader. |
| [Session](https://developer.android.com/reference/kotlin/android/se/omapi/Session) | [openSession](https://developer.android.com/reference/kotlin/android/se/omapi/Reader#openSession())`()` Connects to a Secure Element in this reader. |

## Public methods

### closeSessions

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun closeSessions(): Unit
```

Close all the sessions opened on this reader. All the channels opened by all these sessions will be closed. 

### getName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Return the name of this reader.

- If this reader is a SIM reader, then its name must be "SIM\[Slot\]".
- If the reader is a SD or micro SD reader, then its name must be "SD\[Slot\]"
- If the reader is a embedded SE reader, then its name must be "eSE\[Slot\]"

Slot is a decimal number without leading zeros. The Numbering must start with 1 (e.g. SIM1, SIM2, ... or SD1, SD2, ... or eSE1, eSE2, ...). The slot number "1" for a reader is optional (SIM and SIM1 are both valid for the first SIM-reader, but if there are two readers then the second reader must be named SIM2). This applies also for other SD or SE readers.

<br />

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the reader name, as a String. This value cannot be`null`. |

### getSEService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSEService(): SEService
```

Return the Secure Element service this reader is bound to.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [SEService](https://developer.android.com/reference/kotlin/android/se/omapi/SEService) | the SEService object. This value cannot be`null`. |

### isSecureElementPresent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSecureElementPresent(): Boolean
```

Check if a Secure Element is present in this reader.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the SE is present,`false`otherwise. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the service is not connected |

### openSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openSession(): Session
```

Connects to a Secure Element in this reader. 
This method prepares (initialises) the Secure Element for communication before the Session object is returned (e.g. powers the Secure Element by ICC ON if its not already on). There might be multiple sessions opened at the same time on the same reader. The system ensures the interleaving of APDUs between the respective sessions.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Session](https://developer.android.com/reference/kotlin/android/se/omapi/Session) | a Session object to be used to create Channels. This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------|
| `java.io.IOException` | if something went wrong with the communicating to the Secure Element or the reader. |
