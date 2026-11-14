# SmsManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SmsManager

Kotlin| [Java](../android/telephony/gsm/SmsManager.md) 
| --- | --- |

```
class SmsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.gsm.SmsManager](../android/telephony/gsm/SmsManager.md) |

| **This class was deprecated in API level 4.**
|
| Replaced by android.telephony.SmsManager that supports both GSM and CDMA.

Manages SMS operations such as sending data, text, and pdu SMS messages. Get this object by calling the static method SmsManager.getDefault().

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_ERROR_GENERIC_FAILURE](../android/telephony/gsm/SmsManager.md) Generic failure cause |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_ERROR_NO_SERVICE](../android/telephony/gsm/SmsManager.md) Failed because service is currently unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_ERROR_NULL_PDU](../android/telephony/gsm/SmsManager.md) Failed because no pdu provided |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_ERROR_RADIO_OFF](../android/telephony/gsm/SmsManager.md) Failed because radio was explicitly turned off |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ON_SIM_FREE](../android/telephony/gsm/SmsManager.md) Free space (TS 51.011 10.5.3). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ON_SIM_READ](../android/telephony/gsm/SmsManager.md) Received and read (TS 51.011 10.5.3). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ON_SIM_SENT](../android/telephony/gsm/SmsManager.md) Stored and sent (TS 51.011 10.5.3). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ON_SIM_UNREAD](../android/telephony/gsm/SmsManager.md) Received and unread (TS 51.011 10.5.3). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ON_SIM_UNSENT](../android/telephony/gsm/SmsManager.md) Stored and unsent (TS 51.011 10.5.3). |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ArrayList](../java/util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [divideMessage](../android/telephony/gsm/SmsManager.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Divide a text message into several messages, none bigger than the maximum SMS message size. |
| static [SmsManager](../android/telephony/gsm/SmsManager.md)! | [getDefault](../android/telephony/gsm/SmsManager.md))`()` Get the default instance of the SmsManager |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDataMessage](../android/telephony/gsm/SmsManager.md))`(`destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `destinationPort:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `sentIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`, `deliveryIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`)` Send a data based SMS to a specific application port. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendMultipartTextMessage](../android/telephony/gsm/SmsManager.md))`(`destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parts:` ` [ArrayList](../java/util/ArrayList.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sentIntents:` ` [ArrayList](../java/util/ArrayList.md)< [PendingIntent](../android/app/PendingIntent.md)!>!`, `deliveryIntents:` ` [ArrayList](../java/util/ArrayList.md)< [PendingIntent](../android/app/PendingIntent.md)!>!`)` Send a multi-part text based SMS. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendTextMessage](../android/telephony/gsm/SmsManager.md))`(`destinationAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scAddress:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sentIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`, `deliveryIntent:` ` [PendingIntent](../android/app/PendingIntent.md)!`)` Send a text based SMS. |

## Constants

### RESULT_ERROR_GENERIC_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_ERROR_GENERIC_FAILURE: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Generic failure cause 

 Value: 1

### RESULT_ERROR_NO_SERVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_ERROR_NO_SERVICE: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Failed because service is currently unavailable 

 Value: 4

### RESULT_ERROR_NULL_PDU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_ERROR_NULL_PDU: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Failed because no pdu provided 

 Value: 3

### RESULT_ERROR_RADIO_OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_ERROR_RADIO_OFF: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Failed because radio was explicitly turned off 

 Value: 2

### STATUS_ON_SIM_FREE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ON_SIM_FREE: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Free space (TS 51.011 10.5.3). 

 Value: 0

### STATUS_ON_SIM_READ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ON_SIM_READ: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Received and read (TS 51.011 10.5.3). 

 Value: 1

### STATUS_ON_SIM_SENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ON_SIM_SENT: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Stored and sent (TS 51.011 10.5.3). 

 Value: 5

### STATUS_ON_SIM_UNREAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ON_SIM_UNREAD: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Received and unread (TS 51.011 10.5.3). 

 Value: 3

### STATUS_ON_SIM_UNSENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ON_SIM_UNSENT: Int
```

**Deprecated:** *Use android.telephony.SmsManager.*

Stored and unsent (TS 51.011 10.5.3). 

 Value: 7

## Public methods

### divideMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun divideMessage(text: String!): ArrayList<String!>!
```

**Deprecated:** *Use android.telephony.SmsManager.*

Divide a text message into several messages, none bigger than the maximum SMS message size.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the original message. Must not be null. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ArrayList](../java/util/ArrayList.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an`ArrayList`of strings that, in order, comprise the original message |

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(): SmsManager!
```

**Deprecated:** *Use android.telephony.SmsManager.*

Get the default instance of the SmsManager

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------|
| [SmsManager](../android/telephony/gsm/SmsManager.md)! | the default instance of the SmsManager |

### sendDataMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendDataMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    destinationPort: Short, 
    data: ByteArray!, 
    sentIntent: PendingIntent!, 
    deliveryIntent: PendingIntent!
): Unit
```

**Deprecated:** *Use android.telephony.SmsManager.*

Send a data based SMS to a specific application port.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:is the service center address or null to use the current default SMSC |
| `destinationPort` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the port to deliver the message to |
| --- | --- |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the body of the message to send |
| `sentIntent` | [PendingIntent](../android/app/PendingIntent.md)!:if not NULL this`PendingIntent`is broadcast when the message is sucessfully sent, or failed. The result code will be`Activity.RESULT_OK`` for success, or one of these errors: ``RESULT_ERROR_GENERIC_FAILURE`` ``RESULT_ERROR_RADIO_OFF`` ``RESULT_ERROR_NULL_PDU``. The per-application based SMS control checks sentIntent. If sentIntent is NULL the caller will be checked against all unknown applicaitons, which cause smaller number of SMS to be sent in checking period.` |
| `deliveryIntent` | [PendingIntent](../android/app/PendingIntent.md)!:if not NULL this`PendingIntent`is broadcast when the message is delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if destinationAddress or data are empty |

### sendMultipartTextMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendMultipartTextMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    parts: ArrayList<String!>!, 
    sentIntents: ArrayList<PendingIntent!>!, 
    deliveryIntents: ArrayList<PendingIntent!>!
): Unit
```

**Deprecated:** *Use android.telephony.SmsManager.*

Send a multi-part text based SMS. The callee should have already divided the message into correctly sized parts by calling`divideMessage`.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:is the service center address or null to use the current default SMSC |
| `parts` | [ArrayList](../java/util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an`ArrayList`of strings that, in order, comprise the original message |
| --- | --- |
| `sentIntents` | [ArrayList](../java/util/ArrayList.md)\< [PendingIntent](../android/app/PendingIntent.md)!\>!:if not null, an`ArrayList`of`PendingIntent`s (one for each message part) that is broadcast when the corresponding message part has been sent. The result code will be`Activity.RESULT_OK`` for success, or one of these errors: ``RESULT_ERROR_GENERIC_FAILURE`` ``RESULT_ERROR_RADIO_OFF`` ``RESULT_ERROR_NULL_PDU``. The per-application based SMS control checks sentIntent. If sentIntent is NULL the caller will be checked against all unknown applicaitons, which cause smaller number of SMS to be sent in checking period.` |
| `deliveryIntents` | [ArrayList](../java/util/ArrayList.md)\< [PendingIntent](../android/app/PendingIntent.md)!\>!:if not null, an`ArrayList`of`PendingIntent`s (one for each message part) that is broadcast when the corresponding message part has been delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if destinationAddress or data are empty |

### sendTextMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendTextMessage(
    destinationAddress: String!, 
    scAddress: String!, 
    text: String!, 
    sentIntent: PendingIntent!, 
    deliveryIntent: PendingIntent!
): Unit
```

**Deprecated:** *Use android.telephony.SmsManager.*

Send a text based SMS.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destinationAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the address to send the message to |
| `scAddress` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:is the service center address or null to use the current default SMSC |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the body of the message to send |
| --- | --- |
| `sentIntent` | [PendingIntent](../android/app/PendingIntent.md)!:if not NULL this`PendingIntent`is broadcast when the message is successfully sent, or failed. The result code will be`Activity.RESULT_OK`` for success, or one of these errors: ``RESULT_ERROR_GENERIC_FAILURE`` ``RESULT_ERROR_RADIO_OFF`` ``RESULT_ERROR_NULL_PDU``. The per-application based SMS control checks sentIntent. If sentIntent is NULL the caller will be checked against all unknown applications, which cause smaller number of SMS to be sent in checking period.` |
| `deliveryIntent` | [PendingIntent](../android/app/PendingIntent.md)!:if not NULL this`PendingIntent`is broadcast when the message is delivered to the recipient. The raw pdu of the status report is in the extended data ("pdu"). |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if destinationAddress or text are empty |
