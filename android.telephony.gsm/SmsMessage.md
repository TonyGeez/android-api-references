# SmsMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SmsMessage

Kotlin| [Java](https://developer.android.com/reference/android/telephony/gsm/SmsMessage "View this page in Java") 

```
open class SmsMessage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.gsm.SmsMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#) |

| **This class was deprecated in API level 4.**
|
| Replaced by android.telephony.SmsMessage that supports both GSM and CDMA.

A Short Message Service message.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| | [MessageClass](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.MessageClass) SMS Class enumeration. |
| open | [SubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.SubmitPdu) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_16BIT](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#ENCODING_16BIT:kotlin.Int) 16-bit encoding scheme (see TS 23.038) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_7BIT](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#ENCODING_7BIT:kotlin.Int) 7-bit encoding scheme (see TS 23.038) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_8BIT](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#ENCODING_8BIT:kotlin.Int) 8-bit encoding scheme (see TS 23.038) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODING_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#ENCODING_UNKNOWN:kotlin.Int) Unknown encoding scheme (see TS 23.038) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_BYTES](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#MAX_USER_DATA_BYTES:kotlin.Int) The maximum number of payload bytes per message |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_SEPTETS](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#MAX_USER_DATA_SEPTETS:kotlin.Int) The maximum number of payload septets per message |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_USER_DATA_SEPTETS_WITH_HEADER](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#MAX_USER_DATA_SEPTETS_WITH_HEADER:kotlin.Int) The maximum number of payload septets per message if a user data header is present. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [SmsMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#SmsMessage())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [calculateLength](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#calculateLength(kotlin.CharSequence,%20kotlin.Boolean))`(`messageBody:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `use7bitOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [calculateLength](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#calculateLength(kotlin.String,%20kotlin.Boolean))`(`messageBody:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `use7bitOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding. |
| openstatic [SmsMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#)! | [createFromPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#createFromPdu(kotlin.ByteArray))`(`pdu:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create an SmsMessage from a raw PDU. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayMessageBody](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getDisplayMessageBody())`()` Returns the message body, or email message body if this message was from an email gateway. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayOriginatingAddress](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getDisplayOriginatingAddress())`()` Returns the originating address, or email from address if this message was from an email gateway. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEmailBody](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getEmailBody())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEmailFrom](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getEmailFrom())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexOnSim](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getIndexOnSim())`()` Returns the record index of the message on the SIM (1-based index). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMessageBody](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getMessageBody())`()` Returns the message body as a String, if it exists and is text based. |
| open [SmsMessage.MessageClass](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.MessageClass)! | [getMessageClass](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getMessageClass())`()` Returns the class of this message. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginatingAddress](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getOriginatingAddress())`()` Returns the originating address (sender) of this SMS message in String form or null if unavailable |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getPdu())`()` Returns the raw PDU for the message. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProtocolIdentifier](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getProtocolIdentifier())`()` Get protocol identifier. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPseudoSubject](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getPseudoSubject())`()` Unofficial convention of a subject line enclosed in parens empty string if not present |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceCenterAddress](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getServiceCenterAddress())`()` Returns the address of the SMS service center that relayed this message or null if there is none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getStatus())`()` GSM: For an SMS-STATUS-REPORT message, this returns the status field from the status report. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatusOnSim](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getStatusOnSim())`()` Returns the status of the message on the SIM (read, unread, sent, unsent). |
| openstatic [SmsMessage.SubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.SubmitPdu)! | [getSubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getSubmitPdu(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Boolean))`(`scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `statusReportRequested:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Get an SMS-SUBMIT PDU for a destination address and a message |
| openstatic [SmsMessage.SubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.SubmitPdu)! | [getSubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getSubmitPdu(kotlin.String,%20kotlin.String,%20kotlin.Short,%20kotlin.ByteArray,%20kotlin.Boolean))`(`scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationPort:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `statusReportRequested:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Get an SMS-SUBMIT PDU for a data message to a destination address \& port |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTPLayerLengthForPDU](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getTPLayerLengthForPDU(kotlin.String))`(`pdu:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the TP-Layer-Length for the given SMS-SUBMIT PDU Basically, the length in bytes (not hex chars) less the SMSC header |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getTimestampMillis())`()` Returns the service centre timestamp in currentTimeMillis() format |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getUserData](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#getUserData())`()` returns the user data section minus the user data header if one was present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCphsMwiMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isCphsMwiMessage())`()` Returns true for CPHS MWI toggle message. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmail](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isEmail())`()` Returns true if message is an email. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMWIClearMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isMWIClearMessage())`()` returns true if this message is a CPHS voicemail / message waiting indicator (MWI) clear message |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMWISetMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isMWISetMessage())`()` returns true if this message is a CPHS voicemail / message waiting indicator (MWI) set message |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMwiDontStore](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isMwiDontStore())`()` returns true if this message is a "Message Waiting Indication Group: Discard Message" notification and should not be stored. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReplace](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isReplace())`()` See TS 23. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReplyPathPresent](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isReplyPathPresent())`()` Returns true iff the`TP-Reply-Path`bit is set in this message. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStatusReportMessage](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage#isStatusReportMessage())`()` Return true iff the message is a SMS-STATUS-REPORT message. |

## Constants

### ENCODING_16BIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_16BIT: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

16-bit encoding scheme (see TS 23.038) 

 Value: 3

### ENCODING_7BIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_7BIT: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

7-bit encoding scheme (see TS 23.038) 

 Value: 1

### ENCODING_8BIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_8BIT: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

8-bit encoding scheme (see TS 23.038) 

 Value: 2

### ENCODING_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING_UNKNOWN: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Unknown encoding scheme (see TS 23.038) 

 Value: 0

### MAX_USER_DATA_BYTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_BYTES: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

The maximum number of payload bytes per message 

 Value: 140

### MAX_USER_DATA_SEPTETS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_SEPTETS: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

The maximum number of payload septets per message 

 Value: 160

### MAX_USER_DATA_SEPTETS_WITH_HEADER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_USER_DATA_SEPTETS_WITH_HEADER: Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

The maximum number of payload septets per message if a user data header is present. This assumes the header only contains the CONCATENATED_8_BIT_REFERENCE element. 

 Value: 153

## Public constructors

### SmsMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SmsMessage()
```

**Deprecated:** *Use android.telephony.SmsMessage.*

## Public methods

### calculateLength

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calculateLength(
    messageBody: CharSequence!, 
    use7bitOnly: Boolean
): IntArray!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `messageBody` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the message to encode |
| `use7bitOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, characters that are not part of the GSM alphabet are counted as a single space char. If false, a messageBody containing non-GSM alphabet characters is calculated for 16-bit encoding. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an int\[4\] with int\[0\] being the number of SMS's required, int\[1\] the number of code units used, and int\[2\] is the number of code units remaining until the next message. int\[3\] is the encoding type that should be used for the message. |

### calculateLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calculateLength(
    messageBody: String!, 
    use7bitOnly: Boolean
): IntArray!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Calculates the number of SMS's required to encode the message body and the number of characters remaining until the next message, given the current encoding.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `messageBody` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message to encode |
| `use7bitOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, characters that are not part of the GSM alphabet are counted as a single space char. If false, a messageBody containing non-GSM alphabet characters is calculated for 16-bit encoding. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an int\[4\] with int\[0\] being the number of SMS's required, int\[1\] the number of code units used, and int\[2\] is the number of code units remaining until the next message. int\[3\] is the encoding type that should be used for the message. |

### createFromPdu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromPdu(pdu: ByteArray!): SmsMessage!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Create an SmsMessage from a raw PDU. 

### getDisplayMessageBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayMessageBody(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the message body, or email message body if this message was from an email gateway. Returns null if message body unavailable. 

### getDisplayOriginatingAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayOriginatingAddress(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the originating address, or email from address if this message was from an email gateway. Returns null if originating address unavailable. 

### getEmailBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmailBody(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | if isEmail() is true, body of the email sent through the gateway. null otherwise |

### getEmailFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmailFrom(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | if isEmail() is true, email from address of email sent through the gateway. null otherwise |

### getIndexOnSim

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndexOnSim(): Int
```

**Deprecated:** *Use android.telephony.SmsMessage and getIndexOnIcc instead.*

Returns the record index of the message on the SIM (1-based index).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the record index of the message on the SIM, or -1 if this SmsMessage was not created from a SIM SMS EF record. |

### getMessageBody

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageBody(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the message body as a String, if it exists and is text based.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | message body is there is one, otherwise null |

### getMessageClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageClass(): SmsMessage.MessageClass!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the class of this message. 

### getOriginatingAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOriginatingAddress(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the originating address (sender) of this SMS message in String form or null if unavailable 

### getPdu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPdu(): ByteArray!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the raw PDU for the message.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the raw PDU for the message. |

### getProtocolIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProtocolIdentifier(): Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Get protocol identifier. 

### getPseudoSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPseudoSubject(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Unofficial convention of a subject line enclosed in parens empty string if not present 

### getServiceCenterAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServiceCenterAddress(): String!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the address of the SMS service center that relayed this message or null if there is none. 

### getStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatus(): Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

GSM: For an SMS-STATUS-REPORT message, this returns the status field from the status report. This field indicates the status of a previously submitted SMS, if requested. See TS 23.040, 9.2.3.15 TP-Status for a description of values. CDMA: For not interfering with status codes from GSM, the value is shifted to the bits 31-16. The value is composed of an error class (bits 25-24) and a status code (bits 23-16). Possible codes are described in C.S0015-B, v2.0, 4.5.21.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 indicates the previously sent message was received. See TS 23.040, 9.9.2.3.15 and C.S0015-B, v2.0, 4.5.21 for a description of other possible values. |

### getStatusOnSim

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatusOnSim(): Int
```

**Deprecated:** *Use android.telephony.SmsMessage and getStatusOnIcc instead.*

Returns the status of the message on the SIM (read, unread, sent, unsent).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the status of the message on the SIM. These are: SmsManager.STATUS_ON_SIM_FREE SmsManager.STATUS_ON_SIM_READ SmsManager.STATUS_ON_SIM_UNREAD SmsManager.STATUS_ON_SIM_SEND SmsManager.STATUS_ON_SIM_UNSENT |

### getSubmitPdu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSubmitPdu(
    scAddress: String!, 
    destinationAddress: String!, 
    message: String!, 
    statusReportRequested: Boolean
): SmsMessage.SubmitPdu!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Get an SMS-SUBMIT PDU for a destination address and a message

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Service Centre address. Null means use default. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [SmsMessage.SubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.SubmitPdu)! | a`SubmitPdu`containing the encoded SC address, if applicable, and the encoded message. Returns null on encode error. |

### getSubmitPdu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSubmitPdu(
    scAddress: String!, 
    destinationAddress: String!, 
    destinationPort: Short, 
    data: ByteArray!, 
    statusReportRequested: Boolean
): SmsMessage.SubmitPdu!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Get an SMS-SUBMIT PDU for a data message to a destination address \& port

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Service Centre address. null == use default |
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address of the destination for the message |
| `destinationPort` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the port to deliver the message to at the destination |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the dat for the message |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [SmsMessage.SubmitPdu](https://developer.android.com/reference/kotlin/android/telephony/gsm/SmsMessage.SubmitPdu)! | a`SubmitPdu`containing the encoded SC address, if applicable, and the encoded message. Returns null on encode error. |

### getTPLayerLengthForPDU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTPLayerLengthForPDU(pdu: String!): Int
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Get the TP-Layer-Length for the given SMS-SUBMIT PDU Basically, the length in bytes (not hex chars) less the SMSC header 

### getTimestampMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestampMillis(): Long
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns the service centre timestamp in currentTimeMillis() format 

### getUserData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserData(): ByteArray!
```

**Deprecated:** *Use android.telephony.SmsMessage.*

returns the user data section minus the user data header if one was present. 

### isCphsMwiMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCphsMwiMessage(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns true for CPHS MWI toggle message.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is a CPHS MWI toggle message See CPHS 4.2 section B.4.2 |

### isEmail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmail(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns true if message is an email.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this message came through an email gateway and email sender / subject / parsed body are available |

### isMWIClearMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMWIClearMessage(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

returns true if this message is a CPHS voicemail / message waiting indicator (MWI) clear message 

### isMWISetMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMWISetMessage(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

returns true if this message is a CPHS voicemail / message waiting indicator (MWI) set message 

### isMwiDontStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMwiDontStore(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

returns true if this message is a "Message Waiting Indication Group: Discard Message" notification and should not be stored. 

### isReplace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReplace(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

See TS 23.040 9.2.3.9 returns true if this is a "replace short message" SMS 

### isReplyPathPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReplyPathPresent(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Returns true iff the`TP-Reply-Path`bit is set in this message. 

### isStatusReportMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStatusReportMessage(): Boolean
```

**Deprecated:** *Use android.telephony.SmsMessage.*

Return true iff the message is a SMS-STATUS-REPORT message.
