# SmsMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SmsMessage

Kotlin| [Java](SmsMessage.md) 
| --- | --- |

```
open class SmsMessage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SmsMessage](SmsMessage.md) |

A Short Message Service message.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------|
| | [MessageClass](../android/telephony/SmsMessage.MessageClass.md) SMS Class enumeration. |
| open | [SubmitPdu](../android/telephony/SmsMessage.SubmitPdu.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_16BIT](SmsMessage.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_7BIT](SmsMessage.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_8BIT](SmsMessage.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_KSC5601](SmsMessage.md) This value is not defined in global standard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_UNKNOWN](SmsMessage.md) User data text encoding code unit size |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_3GPP](SmsMessage.md) Indicates a 3GPP format SMS message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_3GPP2](SmsMessage.md) Indicates a 3GPP2 format SMS message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_BYTES](SmsMessage.md) The maximum number of payload bytes per message |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_BYTES_WITH_HEADER](SmsMessage.md) The maximum number of payload bytes per message if a user data header is present. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_SEPTETS](SmsMessage.md) The maximum number of payload septets per message |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_SEPTETS_WITH_HEADER](SmsMessage.md) The maximum number of payload septets per message if a user data header is present. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [calculateLength](SmsMessage.md))`(`msgBody:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `use7bitOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [calculateLength](SmsMessage.md))`(`messageBody:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `use7bitOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding. |
| openstatic [SmsMessage](SmsMessage.md)! | [createFromPdu](SmsMessage.md))`(`pdu:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create an SmsMessage from a raw PDU. |
| --- | --- |
| openstatic [SmsMessage](SmsMessage.md)! | [createFromPdu](SmsMessage.md))`(`pdu:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an SmsMessage from a raw PDU with the specified message format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayMessageBody](SmsMessage.md))`()` Returns the message body, or email message body if this message was from an email gateway. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayOriginatingAddress](SmsMessage.md))`()` Returns the originating address, or email from address if this message was from an email gateway. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEmailBody](SmsMessage.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEmailFrom](SmsMessage.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexOnIcc](SmsMessage.md))`()` Returns the record index of the message on the ICC (1-based index). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexOnSim](SmsMessage.md))`()` Returns the record index of the message on the SIM (1-based index). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessageBody](SmsMessage.md))`()` Returns the message body as a String, if it exists and is text based. |
| open [SmsMessage.MessageClass](../android/telephony/SmsMessage.MessageClass.md)! | [getMessageClass](SmsMessage.md))`()` Returns the class of this message. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getOriginatingAddress](SmsMessage.md))`()` Returns the originating address (sender) of this SMS message in String form or null if unavailable. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getPdu](SmsMessage.md))`()` Returns the raw PDU for the message. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProtocolIdentifier](SmsMessage.md))`()` Get protocol identifier. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPseudoSubject](SmsMessage.md))`()` Unofficial convention of a subject line enclosed in parens empty string if not present |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getRecipientAddress](SmsMessage.md))`()` Returns the recipient address(receiver) of this SMS message in String form or null if unavailable. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceCenterAddress](SmsMessage.md))`()` Returns the address of the SMS service center that relayed this message or null if there is none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](SmsMessage.md))`()` GSM: For an SMS-STATUS-REPORT message, this returns the status field from the status report. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatusOnIcc](SmsMessage.md))`()` Returns the status of the message on the ICC (read, unread, sent, unsent). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatusOnSim](SmsMessage.md))`()` Returns the status of the message on the SIM (read, unread, sent, unsent). |
| --- | --- |
| openstatic [SmsMessage.SubmitPdu](../android/telephony/SmsMessage.SubmitPdu.md)! | [getSubmitPdu](SmsMessage.md))`(`scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `statusReportRequested:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Gets an SMS-SUBMIT PDU for a destination address and a message. |
| openstatic [SmsMessage.SubmitPdu](../android/telephony/SmsMessage.SubmitPdu.md)! | [getSubmitPdu](SmsMessage.md))`(`scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationPort:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `statusReportRequested:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Gets an SMS-SUBMIT PDU for a data message to a destination address \& port. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTPLayerLengthForPDU](SmsMessage.md))`(`pdu:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the TP-Layer-Length for the given SMS-SUBMIT PDU Basically, the length in bytes (not hex chars) less the SMSC header FIXME: This method is only used by a CTS test case that isn't run on CDMA devices. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](SmsMessage.md))`()` Returns the service centre timestamp in currentTimeMillis() format |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getUserData](SmsMessage.md))`()` returns the user data section minus the user data header if one was present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCphsMwiMessage](SmsMessage.md))`()` Returns true for CPHS MWI toggle message. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmail](SmsMessage.md))`()` Returns true if message is an email. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMWIClearMessage](SmsMessage.md))`()` returns true if this message is a CPHS voicemail / message waiting indicator (MWI) clear message |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMWISetMessage](SmsMessage.md))`()` returns true if this message is a CPHS voicemail / message waiting indicator (MWI) set message |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMwiDontStore](SmsMessage.md))`()` returns true if this message is a "Message Waiting Indication Group: Discard Message" notification and should not be stored. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReplace](SmsMessage.md))`()` See TS 23. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReplyPathPresent](SmsMessage.md))`()` Returns true iff the`TP-Reply-Path`bit is set in this message. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStatusReportMessage](SmsMessage.md))`()` Return true iff the message is a SMS-STATUS-REPORT message. |

## Constants

### ENCODING_16BIT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_16BIT: Int
```  

 Value: 3

### ENCODING_7BIT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_7BIT: Int
```  

 Value: 1

### ENCODING_8BIT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_8BIT: Int
```  

 Value: 2

### ENCODING_KSC5601

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_KSC5601: Int
```

This value is not defined in global standard. Only in Korea, this is used. 

 Value: 4

### ENCODING_UNKNOWN

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_UNKNOWN: Int
```

User data text encoding code unit size 

 Value: 0

### FORMAT_3GPP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_3GPP: String
```

Indicates a 3GPP format SMS message. 

 Value: "3gpp"

**See Also**

### FORMAT_3GPP2

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_3GPP2: String
```

Indicates a 3GPP2 format SMS message. 

 Value: "3gpp2"

**See Also**

### MAX_USER_DATA_BYTES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_BYTES: Int
```

The maximum number of payload bytes per message 

 Value: 140

### MAX_USER_DATA_BYTES_WITH_HEADER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_BYTES_WITH_HEADER: Int
```

The maximum number of payload bytes per message if a user data header is present. This assumes the header only contains the CONCATENATED_8_BIT_REFERENCE element. 

 Value: 134

### MAX_USER_DATA_SEPTETS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_SEPTETS: Int
```

The maximum number of payload septets per message 

 Value: 160

### MAX_USER_DATA_SEPTETS_WITH_HEADER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_SEPTETS_WITH_HEADER: Int
```

The maximum number of payload septets per message if a user data header is present. This assumes the header only contains the CONCATENATED_8_BIT_REFERENCE element. 

 Value: 153

## Public methods

### calculateLength

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calculateLength(
    msgBody: CharSequence!, 
    use7bitOnly: Boolean
): IntArray!
```

Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msgBody` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the message to encode |
| `use7bitOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, characters that are not part of the radio-specific 7-bit encoding are counted as single space chars. If false, and if the messageBody contains non-7-bit encodable characters, length is calculated using a 16-bit encoding. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an int\[6\] with int\[0\] being the number of SMS's required, int\[1\] the number of code units used, and int\[2\] is the number of code units remaining until the next message. int\[3\] is an indicator of the encoding code unit size (see the ENCODING_\* definitions in SmsConstants). int\[4\] is the GSM national language table to use, or 0 for the default 7-bit alphabet. int\[5\] The GSM national language shift table to use, or 0 for the default 7-bit extension table. |

### calculateLength

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calculateLength(
    messageBody: String!, 
    use7bitOnly: Boolean
): IntArray!
```

Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `messageBody` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to encode |
| `use7bitOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, characters that are not part of the radio specific (GSM / CDMA) alphabet encoding are converted to as a single space characters. If false, a messageBody containing non-GSM or non-CDMA alphabet characters are encoded using 16-bit encoding. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an int\[4\] with int\[0\] being the number of SMS's required, int\[1\] the number of code units used, and int\[2\] is the number of code units remaining until the next message. int\[3\] is the encoding type that should be used for the message. |

### createFromPdu

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromPdu(pdu: ByteArray!): SmsMessage!
```

**Deprecated:** *Use[createFromPdu(byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/telephony/SmsMessage#createFromPdu(kotlin.ByteArray,%20kotlin.String))instead.*

Create an SmsMessage from a raw PDU. Guess format based on Voice technology first, if it fails use other format. All applications which handle incoming SMS messages by processing the`SMS_RECEIVED_ACTION`broadcast intent**must** now pass the new`format`String extra from the intent into the new method`createFromPdu(byte[], String)`which takes an extra format parameter. This is required in order to correctly decode the PDU on devices that require support for both 3GPP and 3GPP2 formats at the same time, such as dual-mode GSM/CDMA and CDMA/LTE phones. 

### createFromPdu

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromPdu(
    pdu: ByteArray!, 
    format: String!
): SmsMessage!
```

Create an SmsMessage from a raw PDU with the specified message format. The message format is passed in the [android.provider.Telephony.Sms.Intents#SMS_RECEIVED_ACTION](../android/provider/Telephony.Sms.Intents.md) as the`format`String extra, and will be either "3gpp" for GSM/UMTS/LTE messages in 3GPP format or "3gpp2" for CDMA/LTE messages in 3GPP2 format.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pdu` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the message PDU from the [android.provider.Telephony.Sms.Intents#SMS_RECEIVED_ACTION](../android/provider/Telephony.Sms.Intents.md) intent |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the format extra from the [android.provider.Telephony.Sms.Intents#SMS_RECEIVED_ACTION](../android/provider/Telephony.Sms.Intents.md) intent |

### getDisplayMessageBody

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayMessageBody(): String!
```

Returns the message body, or email message body if this message was from an email gateway. Returns null if message body unavailable. 

### getDisplayOriginatingAddress

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayOriginatingAddress(): String!
```

Returns the originating address, or email from address if this message was from an email gateway. Returns null if originating address unavailable. 

### getEmailBody

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmailBody(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | if isEmail() is true, body of the email sent through the gateway. null otherwise |

### getEmailFrom

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmailFrom(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | if isEmail() is true, email from address of email sent through the gateway. null otherwise |

### getIndexOnIcc

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndexOnIcc(): Int
```

Returns the record index of the message on the ICC (1-based index).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the record index of the message on the ICC, or -1 if this SmsMessage was not created from a ICC SMS EF record. |

### getIndexOnSim

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndexOnSim(): Int
```

**Deprecated:** *Use getIndexOnIcc instead.*

Returns the record index of the message on the SIM (1-based index).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the record index of the message on the SIM, or -1 if this SmsMessage was not created from a SIM SMS EF record. |

### getMessageBody

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageBody(): String!
```

Returns the message body as a String, if it exists and is text based.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | message body if there is one, otherwise null |

### getMessageClass

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageClass(): SmsMessage.MessageClass!
```

Returns the class of this message. 

### getOriginatingAddress

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOriginatingAddress(): String?
```

Returns the originating address (sender) of this SMS message in String form or null if unavailable.

If the address is a GSM-formatted address, it will be in a format specified by 3GPP 23.040 Sec 9.1.2.5. If it is a CDMA address, it will be a format specified by 3GPP2 C.S005-D Table 2.7.1.3.2.4-2. The choice of format is carrier-specific, so callers of the should be careful to avoid assumptions about the returned content.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a String representation of the address; null if unavailable. |

### getPdu

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPdu(): ByteArray!
```

Returns the raw PDU for the message.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the raw PDU for the message. |

### getProtocolIdentifier

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProtocolIdentifier(): Int
```

Get protocol identifier. 

### getPseudoSubject

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPseudoSubject(): String!
```

Unofficial convention of a subject line enclosed in parens empty string if not present 

### getRecipientAddress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecipientAddress(): String?
```

Returns the recipient address(receiver) of this SMS message in String form or null if unavailable. 

### getServiceCenterAddress

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServiceCenterAddress(): String!
```

Returns the address of the SMS service center that relayed this message or null if there is none. 

### getStatus

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatus(): Int
```

GSM: For an SMS-STATUS-REPORT message, this returns the status field from the status report. This field indicates the status of a previously submitted SMS, if requested. See TS 23.040, 9.2.3.15 TP-Status for a description of values. CDMA: For not interfering with status codes from GSM, the value is shifted to the bits 31-16. The value is composed of an error class (bits 25-24) and a status code (bits 23-16). Possible codes are described in C.S0015-B, v2.0, 4.5.21.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 for GSM or 2 shifted left by 16 for CDMA indicates the previously sent message was received. See TS 23.040, 9.2.3.15 and C.S0015-B, v2.0, 4.5.21 for a description of other possible values. |

### getStatusOnIcc

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatusOnIcc(): Int
```

Returns the status of the message on the ICC (read, unread, sent, unsent).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the status of the message on the ICC. These are: SmsManager.STATUS_ON_ICC_FREE SmsManager.STATUS_ON_ICC_READ SmsManager.STATUS_ON_ICC_UNREAD SmsManager.STATUS_ON_ICC_SEND SmsManager.STATUS_ON_ICC_UNSENT |

### getStatusOnSim

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatusOnSim(): Int
```

**Deprecated:** *Use getStatusOnIcc instead.*

Returns the status of the message on the SIM (read, unread, sent, unsent).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the status of the message on the SIM. These are: SmsManager.STATUS_ON_SIM_FREE SmsManager.STATUS_ON_SIM_READ SmsManager.STATUS_ON_SIM_UNREAD SmsManager.STATUS_ON_SIM_SEND SmsManager.STATUS_ON_SIM_UNSENT |

### getSubmitPdu

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSubmitPdu(
    scAddress: String!, 
    destinationAddress: String!, 
    message: String!, 
    statusReportRequested: Boolean
): SmsMessage.SubmitPdu!
```

Gets an SMS-SUBMIT PDU for a destination address and a message. This method will not attempt to use any GSM national language 7 bit encodings.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Service Centre address. Null means use default. |
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address of the destination for the message. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string representation of the message payload. |
| --- | --- |
| `statusReportRequested` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates whether a report is requested for this message. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [SmsMessage.SubmitPdu](../android/telephony/SmsMessage.SubmitPdu.md)! | a`SubmitPdu`containing the encoded SC address if applicable and the encoded message. Returns null on encode error. |

### getSubmitPdu

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSubmitPdu(
    scAddress: String!, 
    destinationAddress: String!, 
    destinationPort: Short, 
    data: ByteArray!, 
    statusReportRequested: Boolean
): SmsMessage.SubmitPdu!
```

Gets an SMS-SUBMIT PDU for a data message to a destination address \& port. This method will not attempt to use any GSM national language 7 bit encodings.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Service Centre address. Null means use default. |
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address of the destination for the message. |
| `destinationPort` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the port to deliver the message to at the destination. |
| --- | --- |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data for the message. |
| `statusReportRequested` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates whether a report is requested for this message. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [SmsMessage.SubmitPdu](../android/telephony/SmsMessage.SubmitPdu.md)! | a`SubmitPdu`containing the encoded SC address if applicable and the encoded message. Returns null on encode error. |

### getTPLayerLengthForPDU

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTPLayerLengthForPDU(pdu: String!): Int
```

Get the TP-Layer-Length for the given SMS-SUBMIT PDU Basically, the length in bytes (not hex chars) less the SMSC header FIXME: This method is only used by a CTS test case that isn't run on CDMA devices. We should probably deprecate it and remove the obsolete test case. 

### getTimestampMillis

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestampMillis(): Long
```

Returns the service centre timestamp in currentTimeMillis() format 

### getUserData

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserData(): ByteArray!
```

returns the user data section minus the user data header if one was present. 

### isCphsMwiMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCphsMwiMessage(): Boolean
```

Returns true for CPHS MWI toggle message.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is a CPHS MWI toggle message See CPHS 4.2 section B.4.2 |

### isEmail

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmail(): Boolean
```

Returns true if message is an email.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this message came through an email gateway and email sender / subject / parsed body are available |

### isMWIClearMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMWIClearMessage(): Boolean
```

returns true if this message is a CPHS voicemail / message waiting indicator (MWI) clear message 

### isMWISetMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMWISetMessage(): Boolean
```

returns true if this message is a CPHS voicemail / message waiting indicator (MWI) set message 

### isMwiDontStore

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMwiDontStore(): Boolean
```

returns true if this message is a "Message Waiting Indication Group: Discard Message" notification and should not be stored. 

### isReplace

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReplace(): Boolean
```

See TS 23.040 9.2.3.9 returns true if this is a "replace short message" SMS 

### isReplyPathPresent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReplyPathPresent(): Boolean
```

Returns true iff the`TP-Reply-Path`bit is set in this message. 

### isStatusReportMessage

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStatusReportMessage(): Boolean
```

Return true iff the message is a SMS-STATUS-REPORT message.
