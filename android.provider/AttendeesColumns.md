# CalendarContract.AttendeesColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttendeesColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.AttendeesColumns "View this page in Java") 

```
protected interface AttendeesColumns
```

| [android.provider.CalendarContract.AttendeesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#) |

| Known Direct Subclasses [CalendarContract.Attendees](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Attendees) |--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [CalendarContract.Attendees](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Attendees) | Fields and helpers for interacting with Attendees. | |

Columns from the Attendees table that other tables join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_EMAIL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_EMAIL:kotlin.String) The email address of the attendee. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_IDENTITY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_IDENTITY:kotlin.String) The identity of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.IDENTITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity#IDENTITY:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_ID_NAMESPACE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_ID_NAMESPACE:kotlin.String) The identity name space of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.NAMESPACE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity#NAMESPACE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_NAME:kotlin.String) The name of the attendee. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_RELATIONSHIP](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_RELATIONSHIP:kotlin.String) The relationship of the attendee to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_STATUS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS:kotlin.String) The attendance status of the attendee. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_ACCEPTED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_ACCEPTED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_DECLINED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_DECLINED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_INVITED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_INVITED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_NONE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTENDEE_STATUS_TENTATIVE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_TENTATIVE:kotlin.Int) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ATTENDEE_TYPE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_TYPE:kotlin.String) The type of attendee. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#EVENT_ID:kotlin.String) The id of the event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_ATTENDEE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_ATTENDEE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_NONE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_ORGANIZER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_ORGANIZER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_PERFORMER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_PERFORMER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIONSHIP_SPEAKER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_SPEAKER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_NONE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OPTIONAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_OPTIONAL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REQUIRED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_REQUIRED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_RESOURCE:kotlin.Int) This specifies that an attendee is a resource, like a room, a cabbage, or something and not an actual person. |

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

The identity of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.IDENTITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity#IDENTITY:kotlin.String). This is required only if [ATTENDEE_ID_NAMESPACE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_ID_NAMESPACE:kotlin.String) is present. Column name.

Type: STRING 

 Value: "attendeeIdentity"

### ATTENDEE_ID_NAMESPACE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_ID_NAMESPACE: String
```

The identity name space of the attendee as referenced in [ContactsContract.CommonDataKinds.Identity.NAMESPACE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity#NAMESPACE:kotlin.String). This is required only if [ATTENDEE_IDENTITY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_IDENTITY:kotlin.String) is present. Column name.

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

Type: INTEGER (one of [RELATIONSHIP_ATTENDEE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#RELATIONSHIP_ATTENDEE:kotlin.Int), ...}. 

 Value: "attendeeRelationship"

### ATTENDEE_STATUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTENDEE_STATUS: String
```

The attendance status of the attendee. Column name.

Type: Integer (one of [ATTENDEE_STATUS_ACCEPTED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#ATTENDEE_STATUS_ACCEPTED:kotlin.Int), ...). 

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

Type: Integer (one of [TYPE_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_NONE:kotlin.Int), [TYPE_REQUIRED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_REQUIRED:kotlin.Int), [TYPE_OPTIONAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_OPTIONAL:kotlin.Int), [TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_RESOURCE:kotlin.Int)) 

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
