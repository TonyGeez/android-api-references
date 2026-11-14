Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalingDataRequest

Kotlin | [Java](https://developer.android.com/reference/android/media/tv/SignalingDataRequest "View this page in Java")

```
class SignalingDataRequest : BroadcastInfoRequest, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.tv.BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest) ||
| | ↳ | [android.media.tv.SignalingDataRequest](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#) |

Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata.

For more details on each type of metadata that can be requested, refer to the ATSC standard A/344:2023-5 9.2.10 - Query Signaling Data API.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_DATA_NO_GROUP_ID:kotlin.Int` Denotes that theres no group associated with this request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_AEAT:kotlin.String` Advance Emergency Information Table for the requested service(s), LLS_table_id = 4. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_AEI:kotlin.String` SLS Metadata: MMT Application Event Information for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_APD:kotlin.String` SLS Metadata: APD for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_ASD:kotlin.String` SLS Metadata: ATSC Staggercast Descriptor |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_ASPD:kotlin.String` SLS Metadata: Audio Stream Properties Descriptor |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CAD:kotlin.String` SLS Metadata: Caption Asset Descriptor |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CDT:kotlin.String` CertificateData Tablefor the requested service(s), LLS_table_id = 6. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CRIT:kotlin.String` SLS Metadata: MMT Clock Relation Information for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_DCIT:kotlin.String` SLS Metadata: MMT Device Capabilities Information Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_DWD:kotlin.String` SLS Metadata: Distribution Window Desciription for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_EMSG:kotlin.String` SLS Metadata: ROUTE/DASH Application Dynamic Event for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_EVTI:kotlin.String` SLS Metadata: MMT Application Dynamic Event for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_HELD:kotlin.String` SLS Metadata: HTML Entry Pages Location Description for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_IED:kotlin.String` SLS Metadata: Inband Event Descriptor |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPD:kotlin.String` SLS Metadata: DASH MPD for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPIT:kotlin.String` SLS Metadata: MMT Media Presentation Information Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPT:kotlin.String` SLS Metadata: MMT Package Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_OSN:kotlin.String` Onscreen Message Notifications for the requested service(s), LLS_table_id = 5. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_PAT:kotlin.String` SLS Metadata: MMT Package Access Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RDT:kotlin.String` SLS Metadata: Recovery Data Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RRT:kotlin.String` Region Rating Table for the requested service(s), LLS_table_id = 2. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RSAT:kotlin.String` SLS Metadata: Regional Service Availability Table for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SLT:kotlin.String` Service List Table for the requested service(s), LLS_table_id = 1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SMT:kotlin.String` Signed Multitable for the requested service(s), LLS_table_id = 0xFE (254). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SSD:kotlin.String` SLS Metadata: Security Properties Descriptor |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_STSID:kotlin.String` SLS Metadata: S-TSID for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_STT:kotlin.String` System Time Table for the requested service(s), LLS_table_id = 3. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_USBD:kotlin.String` SLS Metadata: USBD for the requested service(s) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_USD:kotlin.String` SLS Metadata: User Service Description for MMTP |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_VSPD:kotlin.String` SLS Metadata: Video Stream Properties Descriptor |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int` Request option: auto update. With this option, a response is sent only when broadcast information is detected for the first time, new values are detected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int` Request option: one-shot With this option, only one response will be given per request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int` Request option: one-way With this option, no response is expected after sending the request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int` Request option: repeat. With this option, a response is sent when related broadcast information is detected, even if the same information has been sent previously. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SignalingDataRequest(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.collections.MutableList)(requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, signalingDataTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#getGroup()()` Gets the group with which any signaling returned will be associated. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#getSignalingDataTypes()()` Gets the signaling data types for which data should be retrieved. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getOption()()` Gets the request option of the request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getRequestId()()` Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getType()()` Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SignalingDataRequest](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### SIGNALING_DATA_NO_GROUP_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_DATA_NO_GROUP_ID: Int
```

Denotes that theres no group associated with this request.

 Value: -1

### SIGNALING_METADATA_AEAT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_AEAT: String
```

Advance Emergency Information Table for the requested service(s), LLS_table_id = 4.

 Value: "AEAT"

### SIGNALING_METADATA_AEI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_AEI: String
```

SLS Metadata: MMT Application Event Information for the requested service(s)

 Value: "AEI"

### SIGNALING_METADATA_APD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_APD: String
```

SLS Metadata: APD for the requested service(s)

 Value: "APD"

### SIGNALING_METADATA_ASD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_ASD: String
```

SLS Metadata: ATSC Staggercast Descriptor

 Value: "ASD"

### SIGNALING_METADATA_ASPD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_ASPD: String
```

SLS Metadata: Audio Stream Properties Descriptor

 Value: "ASPD"

### SIGNALING_METADATA_CAD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_CAD: String
```

SLS Metadata: Caption Asset Descriptor

 Value: "CAD"

### SIGNALING_METADATA_CDT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_CDT: String
```

CertificateData Tablefor the requested service(s), LLS_table_id = 6.

 Value: "CDT"

### SIGNALING_METADATA_CRIT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_CRIT: String
```

SLS Metadata: MMT Clock Relation Information for the requested service(s)

 Value: "CRIT"

### SIGNALING_METADATA_DCIT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_DCIT: String
```

SLS Metadata: MMT Device Capabilities Information Table for the requested service(s)

 Value: "DCIT"

### SIGNALING_METADATA_DWD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_DWD: String
```

SLS Metadata: Distribution Window Desciription for the requested service(s)

 Value: "DWD"

### SIGNALING_METADATA_EMSG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_EMSG: String
```

SLS Metadata: ROUTE/DASH Application Dynamic Event for the requested service(s)

 Value: "EMSG"

### SIGNALING_METADATA_EVTI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_EVTI: String
```

SLS Metadata: MMT Application Dynamic Event for the requested service(s)

 Value: "EVTI"

### SIGNALING_METADATA_HELD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_HELD: String
```

SLS Metadata: HTML Entry Pages Location Description for the requested service(s)

 Value: "HELD"

### SIGNALING_METADATA_IED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_IED: String
```

SLS Metadata: Inband Event Descriptor

 Value: "IED"

### SIGNALING_METADATA_MPD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_MPD: String
```

SLS Metadata: DASH MPD for the requested service(s)

 Value: "MPD"

### SIGNALING_METADATA_MPIT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_MPIT: String
```

SLS Metadata: MMT Media Presentation Information Table for the requested service(s)

 Value: "MPIT"

### SIGNALING_METADATA_MPT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_MPT: String
```

SLS Metadata: MMT Package Table for the requested service(s)

 Value: "MPT"

### SIGNALING_METADATA_OSN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_OSN: String
```

Onscreen Message Notifications for the requested service(s), LLS_table_id = 5.

 Value: "OSN"

### SIGNALING_METADATA_PAT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_PAT: String
```

SLS Metadata: MMT Package Access Table for the requested service(s)

 Value: "PAT"

### SIGNALING_METADATA_RDT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_RDT: String
```

SLS Metadata: Recovery Data Table for the requested service(s)

 Value: "RDT"

### SIGNALING_METADATA_RRT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_RRT: String
```

Region Rating Table for the requested service(s), LLS_table_id = 2.

 Value: "RRT"

### SIGNALING_METADATA_RSAT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_RSAT: String
```

SLS Metadata: Regional Service Availability Table for the requested service(s)

 Value: "RSAT"

### SIGNALING_METADATA_SLT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_SLT: String
```

Service List Table for the requested service(s), LLS_table_id = 1.

 Value: "SLT"

### SIGNALING_METADATA_SMT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_SMT: String
```

Signed Multitable for the requested service(s), LLS_table_id = 0xFE (254).

 Value: "SMT"

### SIGNALING_METADATA_SSD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_SSD: String
```

SLS Metadata: Security Properties Descriptor

 Value: "SSD"

### SIGNALING_METADATA_STSID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_STSID: String
```

SLS Metadata: S-TSID for the requested service(s)

 Value: "STSID"

### SIGNALING_METADATA_STT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_STT: String
```

System Time Table for the requested service(s), LLS_table_id = 3.

 Value: "STT"

### SIGNALING_METADATA_USBD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_USBD: String
```

SLS Metadata: USBD for the requested service(s)

 Value: "USBD"

### SIGNALING_METADATA_USD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_USD: String
```

SLS Metadata: User Service Description for MMTP

 Value: "USD"

### SIGNALING_METADATA_VSPD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNALING_METADATA_VSPD: String
```

SLS Metadata: Video Stream Properties Descriptor

 Value: "VSPD"

## Public constructors

### SignalingDataRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SignalingDataRequest(
    requestId: Int, 
    option: Int, 
    group: Int, 
    signalingDataTypes: MutableList<String!>)
```

| Parameters ||
|---|---|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int` |
| `signalingDataTypes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getGroup

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGroup(): Int
```

Gets the group with which any signaling returned will be associated.

Requested metadata objects will only be returned if they are part of the group specified.

If no group is specified (`https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_DATA_NO_GROUP_ID:kotlin.Int`), the receiver will send all the metadata objects discovered.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The group ID which any signaling returned will be associated. |

### getSignalingDataTypes

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSignalingDataTypes(): MutableList<String!>
```

Gets the signaling data types for which data should be retrieved.

For more details on each type of metadata that can be requested, refer to the ATSC standard A/344:2023-5 9.2.10 - Query Signaling Data API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The signaling data types for which data should be retrieved. This value cannot be `null`. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SignalingDataRequest!>
```
