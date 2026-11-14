# Session

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Session

Kotlin| [Java](../android/se/omapi/Session.md) 
| --- | --- |

```
class Session
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.se.omapi.Session](../android/se/omapi/Session.md) |

Instances of this class represent a connection session to one of the Secure Elements available on the device. These objects can be used to get a communication channel with an Applet in the Secure Element. This channel can be the basic channel or a logical channel.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/se/omapi/Session.md))`()` Close the connection with the Secure Element. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeChannels](../android/se/omapi/Session.md))`()` Close any channel opened on this session. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getATR](../android/se/omapi/Session.md))`()` Get the Answer to Reset of this Secure Element. |
| --- | --- |
| [Reader](../android/se/omapi/Reader.md) | [getReader](../android/se/omapi/Session.md))`()` Get the reader that provides this session. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../android/se/omapi/Session.md))`()` Tells if this session is closed. |
| [Channel](../android/se/omapi/Channel.md)? | [openBasicChannel](../android/se/omapi/Session.md))`(`aid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` This method is provided to ease the development of mobile application and for compliancy with existing applications. |
| --- | --- |
| [Channel](../android/se/omapi/Channel.md)? | [openBasicChannel](../android/se/omapi/Session.md))`(`aid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `p2:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Get an access to the basic channel, as defined in the ISO/IEC 7816-4 specification (the one that has number 0). |
| [Channel](../android/se/omapi/Channel.md)? | [openLogicalChannel](../android/se/omapi/Session.md))`(`aid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` This method is provided to ease the development of mobile application and for compliancy with existing applications. |
| [Channel](../android/se/omapi/Channel.md)? | [openLogicalChannel](../android/se/omapi/Session.md))`(`aid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `p2:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Open a logical channel with the Secure Element, selecting the Applet represented by the given AID. |
| --- | --- |

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close the connection with the Secure Element. This will close any channels opened by this application with this Secure Element. 

### closeChannels

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun closeChannels(): Unit
```

Close any channel opened on this session. 

### getATR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getATR(): ByteArray?
```

Get the Answer to Reset of this Secure Element. 
The returned byte array can be null if the ATR for this Secure Element is not available.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | the ATR as a byte array or null. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if there was an error connecting to SE or if the service was not connected. |

### getReader

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReader(): Reader
```

Get the reader that provides this session.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [Reader](../android/se/omapi/Reader.md) | The Reader object. This value cannot be`null`. |

### isClosed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isClosed(): Boolean
```

Tells if this session is closed.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the session is closed, false otherwise. |

### openBasicChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openBasicChannel(aid: ByteArray?): Channel?
```

This method is provided to ease the development of mobile application and for compliancy with existing applications. This method is equivalent to openBasicChannel(aid, P2=0x00)

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the AID of the Applet to be selected on this channel, as a byte array, or null if no Applet is to be selected. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------|
| [Channel](../android/se/omapi/Channel.md)? | an instance of Channel if available or null. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalStateException` | if the Secure Element session is used after being closed. |
| `java.lang.IllegalArgumentException` | if the aid's length is not within 5 to 16 (inclusive). |
| --- | --- |
| `java.lang.SecurityException` | if the calling application cannot be granted access to this AID or the default Applet on this session. |
| `java.util.NoSuchElementException` | if the AID on the Secure Element is not available or cannot be selected. |
| `java.lang.UnsupportedOperationException` | if the given P2 parameter is not supported by the device |
| --- | --- |

### openBasicChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openBasicChannel(
    aid: ByteArray?, 
    p2: Byte
): Channel?
```

Get an access to the basic channel, as defined in the ISO/IEC 7816-4 specification (the one that has number 0). The obtained object is an instance of the Channel class. If the AID is null, it means no Applet is to be selected on this channel and the default Applet is used. If the AID is defined then the corresponding Applet is selected. Once this channel has been opened by a device application, it is considered as "locked" by this device application, and other calls to this method will return null, until the channel is closed. Some Secure Elements (like the UICC) might always keep the basic channel locked (i.e. return null to applications), to prevent access to the basic channel, while some other might return a channel object implementing some kind of filtering on the commands, restricting the set of accepted command to a smaller set. It is recommended for the UICC to reject the opening of the basic channel to a specific applet, by always answering null to such a request. For other Secure Elements, the recommendation is to accept opening the basic channel on the default applet until another applet is selected on the basic channel. As there is no other way than a reset to select again the default applet, the implementation of the transport API should guarantee that the openBasicChannel(null) command will return null until a reset occurs. With previous release (V2.05) it was not possible to set P2 value, this value was always set to '00'.Except for specific needs it is recommended to keep P2 to '00'. It is recommended that the device allows all values for P2, however only the following values are mandatory: '00', '04', '08', '0C'(as defined in \[2\]) The implementation of the underlying SELECT command within this method shall be based on ISO 7816-4 with following options:

- CLA = '00'
- INS = 'A4'
- P1 = '04' (Select by DF name/application identifier)

The select response data can be retrieved with byte\[\] getSelectResponse(). The API shall handle received status word as follow. If the status word indicates that the Secure Element was able to open a channel (e.g. status word '90 00' or status words referencing a warning in ISO-7816-4: '62 XX' or '63 XX') the API shall keep the channel opened and the next getSelectResponse() shall return the received status word. Other received status codes indicating that the Secure Element was able not to open a channel shall be considered as an error and the corresponding channel shall not be opened. The function without P2 as parameter is provided for backwards compatibility and will fall back to a select command with P2='00'.

<br />

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the AID of the Applet to be selected on this channel, as a byte array, or null if no Applet is to be selected. |
| `p2` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the P2 parameter of the SELECT APDU executed on this channel. This value may be`null`. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------|
| [Channel](../android/se/omapi/Channel.md)? | an instance of Channel if available or null. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalStateException` | if the Secure Element session is used after being closed. |
| `java.lang.IllegalArgumentException` | if the aid's length is not within 5 to 16 (inclusive). |
| --- | --- |
| `java.lang.SecurityException` | if the calling application cannot be granted access to this AID or the default Applet on this session. |
| `java.util.NoSuchElementException` | if the AID on the Secure Element is not available or cannot be selected. |
| `java.lang.UnsupportedOperationException` | if the given P2 parameter is not supported by the device |
| --- | --- |

### openLogicalChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openLogicalChannel(aid: ByteArray?): Channel?
```

This method is provided to ease the development of mobile application and for compliancy with existing applications. This method is equivalent to openLogicalChannel(aid, P2=0x00)

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the AID of the Applet to be selected on this channel, as a byte array. This value may be`null`. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Channel](../android/se/omapi/Channel.md)? | an instance of Channel. Null if the Secure Element is unable to provide a new logical channel. This value may be`null`. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalStateException` | if the Secure Element is used after being closed. |
| `java.lang.IllegalArgumentException` | if the aid's length is not within 5 to 16 (inclusive). |
| --- | --- |
| `java.lang.SecurityException` | if the calling application cannot be granted access to this AID or the default Applet on this session. |
| `java.util.NoSuchElementException` | if the AID on the Secure Element is not available or cannot be selected or a logical channel is already open to a non-multiselectable Applet. |
| `java.lang.UnsupportedOperationException` | if the given P2 parameter is not supported by the device. |
| --- | --- |

### openLogicalChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openLogicalChannel(
    aid: ByteArray?, 
    p2: Byte
): Channel?
```

Open a logical channel with the Secure Element, selecting the Applet represented by the given AID. If the AID is null, which means no Applet is to be selected on this channel, the default Applet is used. It's up to the Secure Element to choose which logical channel will be used. With previous release (V2.05) it was not possible to set P2 value, this value was always set to '00'.Except for specific needs it is recommended to keep P2 to '00'. It is recommended that the device allows all values for P2, however only the following values are mandatory: '00', '04', '08', '0C'(as defined in \[2\]) The implementation of the underlying SELECT command within this method shall be based on ISO 7816-4 with following options:

- CLA = '01' to '03', '40 to 4F'
- INS = 'A4'
- P1 = '04' (Select by DF name/application identifier)

The select response data can be retrieved with byte\[\] getSelectResponse(). The API shall handle received status word as follow. If the status word indicates that the Secure Element was able to open a channel (e.g. status word '90 00' or status words referencing a warning in ISO-7816-4: '62 XX' or '63 XX') the API shall keep the channel opened and the next getSelectResponse() shall return the received status word. Other received status codes indicating that the Secure Element was able not to open a channel shall be considered as an error and the corresponding channel shall not be opened. In case of UICC it is recommended for the API to reject the opening of the logical channel without a specific AID, by always answering null to such a request. The function without P2 as parameter is provided for backwards compatibility and will fall back to a select command with P2=00.

<br />

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the AID of the Applet to be selected on this channel, as a byte array. This value may be`null`. |
| `p2` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the P2 parameter of the SELECT APDU executed on this channel. This value may be`null`. |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Channel](../android/se/omapi/Channel.md)? | an instance of Channel. Null if the Secure Element is unable to provide a new logical channel. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalStateException` | if the Secure Element is used after being closed. |
| `java.lang.IllegalArgumentException` | if the aid's length is not within 5 to 16 (inclusive). |
| --- | --- |
| `java.lang.SecurityException` | if the calling application cannot be granted access to this AID or the default Applet on this session. |
| `java.util.NoSuchElementException` | if the AID on the Secure Element is not available or cannot be selected or a logical channel is already open to a non-multiselectable Applet. |
| `java.lang.UnsupportedOperationException` | if the given P2 parameter is not supported by the device. |
| --- | --- |
