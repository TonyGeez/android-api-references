# Entity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Entity

Kotlin| [Java](Entity.md) 
| --- | --- |

```
class Entity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.Entity](Entity.md) |

A representation of a item using ContentValues. It contains one top level ContentValue plus a collection of Uri, ContentValues tuples as subvalues. One example of its use is in Contacts, where the top level ContentValue contains the columns from the RawContacts table and the subvalues contain a ContentValues object for each row from the Data table that corresponds to that RawContact. The uri refers to the Data table uri for each row.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| | [NamedContentValues](../android/content/Entity.NamedContentValues.md) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Entity](Entity.md))`(`values:` ` [ContentValues](ContentValues.md)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addSubValue](Entity.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `values:` ` [ContentValues](ContentValues.md)!`)` <br /> |
| [ContentValues](ContentValues.md)! | [getEntityValues](Entity.md))`()` <br /> |
| [ArrayList](../java.util/ArrayList.md)\< [Entity.NamedContentValues](../android/content/Entity.NamedContentValues.md)!\>! | [getSubValues](Entity.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Entity.md))`()` <br /> |

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
