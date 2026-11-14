# CalendarContract.AttendeesColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttendeesColumns

Kotlin| [Java](../android/provider/CalendarContract.AttendeesColumns.md) 
| --- | --- |

```
protected interface AttendeesColumns
```

| [android.provider.CalendarContract.AttendeesColumns](../android/provider/CalendarContract.AttendeesColumns.md) |

| Known Direct Subclasses [CalendarContract.Attendees](../android/provider/CalendarContract.Attendees.md) |--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [CalendarContract.Attendees](../android/provider/CalendarContract.Attendees.md) | Fields and helpers for interacting with Attendees. | |
| --- | --- | --- | --- | --- | --- | --- |

Columns from the Attendees table that other tables join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_EMAIL](../android/provider/CalendarContract.AttendeesColumns.md) The email address of the attendee. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_IDENTITY](../android/provider/CalendarContract.AttendeesColumns.md) The identity of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.IDENTITY](../android/provider/ContactsContract.CommonDataKinds.Identity.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_ID_NAMESPACE](../android/provider/CalendarContract.AttendeesColumns.md) The identity name space of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.NAMESPACE](../android/provider/ContactsContract.CommonDataKinds.Identity.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_NAME](../android/provider/CalendarContract.AttendeesColumns.md) The name of the attendee. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_RELATIONSHIP](../android/provider/CalendarContract.AttendeesColumns.md) The relationship of the attendee to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_STATUS](../android/provider/CalendarContract.AttendeesColumns.md) The attendance status of the attendee. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_ACCEPTED](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_DECLINED](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_INVITED](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_NONE](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_TENTATIVE](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_TYPE](../android/provider/CalendarContract.AttendeesColumns.md) The type of attendee. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](../android/provider/CalendarContract.AttendeesColumns.md) The id of the event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_ATTENDEE](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_NONE](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_ORGANIZER](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_PERFORMER](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_SPEAKER](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NONE](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OPTIONAL](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REQUIRED](../android/provider/CalendarContract.AttendeesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RESOURCE](../android/provider/CalendarContract.AttendeesColumns.md) This specifies that an attendee is a resource, like a room, a cabbage, or something and not an actual person. |

## Constants

### ATTENDEE_EMAIL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_EMAIL: String
```

The email address of the attendee. Column name.

Type: STRING 

 Value: "attendeeEmail"

### ATTENDEE_IDENTITY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_IDENTITY: String
```

The identity of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.IDENTITY](../android/provider/ContactsContract.CommonDataKinds.Identity.md). This is required only if [ATTENDEE_ID_NAMESPACE](../android/provider/CalendarContract.AttendeesColumns.md) is present. Column name.

Type: STRING 

 Value: "attendeeIdentity"

### ATTENDEE_ID_NAMESPACE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_ID_NAMESPACE: String
```

The identity name space of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.NAMESPACE](../android/provider/ContactsContract.CommonDataKinds.Identity.md). This is required only if [ATTENDEE_IDENTITY](../android/provider/CalendarContract.AttendeesColumns.md) is present. Column name.

Type: STRING 

 Value: "attendeeIdNamespace"

### ATTENDEE_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_NAME: String
```

The name of the attendee. Column name.

Type: STRING 

 Value: "attendeeName"

### ATTENDEE_RELATIONSHIP

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_RELATIONSHIP: String
```

The relationship of the attendee to the user. Column name.

Type: INTEGER (one of [RELATIONSHIP_ATTENDEE](../android/provider/CalendarContract.AttendeesColumns.md), ...}. 

 Value: "attendeeRelationship"

### ATTENDEE_STATUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS: String
```

The attendance status of the attendee. Column name.

Type: Integer (one of [ATTENDEE_STATUS_ACCEPTED](../android/provider/CalendarContract.AttendeesColumns.md), ...). 

 Value: "attendeeStatus"

### ATTENDEE_STATUS_ACCEPTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS_ACCEPTED: Int
```  

 Value: 1

### ATTENDEE_STATUS_DECLINED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS_DECLINED: Int
```  

 Value: 2

### ATTENDEE_STATUS_INVITED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS_INVITED: Int
```  

 Value: 3

### ATTENDEE_STATUS_NONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS_NONE: Int
```  

 Value: 0

### ATTENDEE_STATUS_TENTATIVE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS_TENTATIVE: Int
```  

 Value: 4

### ATTENDEE_TYPE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_TYPE: String
```

The type of attendee. Column name.

Type: Integer (one of [TYPE_NONE](../android/provider/CalendarContract.AttendeesColumns.md), [TYPE_REQUIRED](../android/provider/CalendarContract.AttendeesColumns.md), [TYPE_OPTIONAL](../android/provider/CalendarContract.AttendeesColumns.md), [TYPE_RESOURCE](../android/provider/CalendarContract.AttendeesColumns.md)) 

 Value: "attendeeType"

### EVENT_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ID: String
```

The id of the event. Column name.

Type: INTEGER 

 Value: "event_id"

### RELATIONSHIP_ATTENDEE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIONSHIP_ATTENDEE: Int
```  

 Value: 1

### RELATIONSHIP_NONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIONSHIP_NONE: Int
```  

 Value: 0

### RELATIONSHIP_ORGANIZER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIONSHIP_ORGANIZER: Int
```  

 Value: 2

### RELATIONSHIP_PERFORMER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIONSHIP_PERFORMER: Int
```  

 Value: 3

### RELATIONSHIP_SPEAKER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIONSHIP_SPEAKER: Int
```  

 Value: 4

### TYPE_NONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NONE: Int
```  

 Value: 0

### TYPE_OPTIONAL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OPTIONAL: Int
```  

 Value: 2

### TYPE_REQUIRED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REQUIRED: Int
```  

 Value: 1

### TYPE_RESOURCE

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RESOURCE: Int
```

This specifies that an attendee is a resource, like a room, a cabbage, or something and not an actual person. 

 Value: 3
