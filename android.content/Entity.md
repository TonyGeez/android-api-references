# Entity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Entity

Kotlin| [Java](https://developer.android.com/reference/android/content/Entity "View this page in Java") 

```
class Entity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.Entity](https://developer.android.com/reference/kotlin/android/content/Entity#) |

A representation of a item using ContentValues. It contains one top level ContentValue plus a collection of Uri, ContentValues tuples as subvalues. One example of its use is in Contacts, where the top level ContentValue contains the columns from the RawContacts table and the subvalues contain a ContentValues object for each row from the Data table that corresponds to that RawContact. The uri refers to the Data table uri for each row.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| | [NamedContentValues](https://developer.android.com/reference/kotlin/android/content/Entity.NamedContentValues) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Entity](https://developer.android.com/reference/kotlin/android/content/Entity#Entity(android.content.ContentValues))`(`values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addSubValue](https://developer.android.com/reference/kotlin/android/content/Entity#addSubValue(android.net.Uri,%20android.content.ContentValues))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!`)` <br /> |
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)! | [getEntityValues](https://developer.android.com/reference/kotlin/android/content/Entity#getEntityValues())`()` <br /> |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Entity.NamedContentValues](https://developer.android.com/reference/kotlin/android/content/Entity.NamedContentValues)!\>! | [getSubValues](https://developer.android.com/reference/kotlin/android/content/Entity#getSubValues())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/Entity#toString())`()` <br /> |

## Public constructors

### Entity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Entity(values: ContentValues!)
```

## Public methods

### addSubValue

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addSubValue(
    uri: Uri!, 
    values: ContentValues!
): Unit
```  

### getEntityValues

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEntityValues(): ContentValues!
```  

### getSubValues

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubValues(): ArrayList<Entity.NamedContentValues!>!
```  

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
