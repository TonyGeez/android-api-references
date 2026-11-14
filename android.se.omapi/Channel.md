Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Channel

Kotlin | [Java](Channel.md)
| --- | --- |

```
class Channel : Channel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.se.omapi.Channel](Channel.md) |

Instances of this class represent an ISO/IEC 7816-4 channel opened to a Secure Element. It can be either a logical channel or the basic channel. They can be used to send APDUs to the secure element. Channels are opened by calling the Session.openBasicChannel(byte\[\]) or Session.openLogicalChannel(byte\[\]) methods.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#close()()` Closes this channel to the Secure Element. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#getSelectResponse()()` Returns the data as received from the application select command inclusively the status word received at applet selection. |
| [Session](Session.md) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#getSession()()` Get the session that has opened this channel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#isBasicChannel()()` Returns a boolean telling if this channel is the basic channel. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#isOpen()()` Tells if this channel is open. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#selectNext()()` Performs a selection of the next Applet on this channel that matches to the partial AID specified in the openBasicChannel(byte\[\] aid) or openLogicalChannel(byte\[\] aid) method. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/se/omapi/Channel#transmit(kotlin.ByteArray)(command: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Transmit an APDU command (as per ISO/IEC 7816-4) to the Secure Element. |

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this channel to the Secure Element. If the method is called when the channel is already closed, this method will be ignored. The close() method shall wait for completion of any pending transmit(byte\[\] command) before closing the channel.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### getSelectResponse

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectResponse(): ByteArray?
```

Returns the data as received from the application select command inclusively the status word received at applet selection. The returned byte array contains the data bytes in the following order: \[\<first data byte\>, ..., \<last data byte\>, \<sw1\>, \<sw2\>\]

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The data as returned by the application select command inclusively the status word. Only the status word if the application select command has no returned data. Returns null if an application select command has not been performed or the selection response can not be retrieved by the reader implementation. |

### getSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSession(): Session
```

Get the session that has opened this channel.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/se/omapi/Session` | the session object this channel is bound to. This value cannot be `null`. |

### isBasicChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBasicChannel(): Boolean
```

Returns a boolean telling if this channel is the basic channel.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this channel is a basic channel. `false` if this channel is a logical channel. |

### isOpen

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOpen(): Boolean
```

Tells if this channel is open.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if the channel is closed or in case of an error. `true` otherwise. |

### selectNext

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun selectNext(): Boolean
```

Performs a selection of the next Applet on this channel that matches to the partial AID specified in the openBasicChannel(byte\[\] aid) or openLogicalChannel(byte\[\] aid) method. This mechanism can be used by a device application to iterate through all Applets matching to the same partial AID. If selectNext() returns true a new Applet was successfully selected on this channel. If no further Applet exists with matches to the partial AID this method returns false and the already selected Applet stays selected. 
Since the API cannot distinguish between a partial and full AID the API shall rely on the response of the Secure Element for the return value of this method. 
The implementation of the underlying SELECT command within this method shall use the same values as the corresponding openBasicChannel(byte\[\] aid) or openLogicalChannel(byte\[\] aid) command with the option: 
P2='02' (Next occurrence) 
The select response stored in the Channel object shall be updated with the APDU response of the SELECT command.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if new Applet was selected on this channel. `false` the already selected Applet stays selected on this channel. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalStateException` | if the channel is used after being closed. |
| `java.lang.UnsupportedOperationException` | if this operation is not supported by the card. |
| --- | --- |

### transmit

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transmit(command: ByteArray): ByteArray
```

Transmit an APDU command (as per ISO/IEC 7816-4) to the Secure Element. The underlying layers generate as many TPDUs as necessary to transport this APDU. The API shall ensure that all available data returned from Secure Element, including concatenated responses, are retrieved and made available to the calling application. If a warning status code is received the API wont check for further response data but will return all data received so far and the warning status code. 
The transport part is invisible from the application. The generated response is the response of the APDU which means that all protocols related responses are handled inside the API or the underlying implementation. 
The transmit method shall support extended length APDU commands independently of the coding within the ATR. 
For status word '61 XX' the API or underlying implementation shall issue a GET RESPONSE command as specified by ISO 7816-4 standard with LE=XX; for the status word '6C XX', the API or underlying implementation shall reissue the input command with LE=XX. For other status words, the API (or underlying implementation) shall return the complete response including data and status word to the device application. The API (or underlying implementation) shall not handle internally the received status words. The channel shall not be closed even if the Secure Element answered with an error code. The system ensures the synchronization between all the concurrent calls to this method, and that only one APDU will be sent at a time, irrespective of the number of TPDUs that might be required to transport it to the SE. The entire APDU communication to this SE is locked to the APDU. 
The channel information in the class byte in the APDU will be ignored. The system will add any required information to ensure the APDU is transported on this channel. The only restrictions on the set of commands that can be sent is defined below, the API implementation shall be able to send all other commands: 

- MANAGE_CHANNEL commands are not allowed.
- SELECT by DF Name (p1=04) are not allowed.
- CLA bytes with channel numbers are de-masked.

<br />

| Parameters ||
|---|---|
| `command` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the APDU command to be transmitted, as a byte array. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | the response received, as a byte array. The returned byte array contains the data bytes in the following order: \[\<first data byte\>, ..., \<last data byte\>, \<sw1\>, \<sw2\>\]. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is a communication problem to the reader or the Secure Element. |
| `java.lang.IllegalArgumentException` | if INS byte is invalid according to \[2\] (0x6x or 0x9x). |
| `java.lang.IllegalStateException` | if the channel is used after being closed. |
| --- | --- |
| `java.lang.NullPointerException` | if command is NULL. |
| `java.lang.SecurityException` | if the command is filtered by the security policy. |
