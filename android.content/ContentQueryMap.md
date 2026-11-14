# ContentQueryMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentQueryMap

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentQueryMap "View this page in Java") 

```
open class ContentQueryMap : Observable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.Observable](https://developer.android.com/reference/kotlin/java/util/Observable.html#) ||
| | ↳ | [android.content.ContentQueryMap](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#) |

Caches the contents of a cursor into a Map of String-\>ContentValues and optionally keeps the cache fresh by registering for updates on the content backing the cursor. The column of the database that is to be used as the key of the map is user-configurable, and the ContentValues contains all columns other than the one that is designated the key.

The cursor data is accessed by row key and column name via getValue().

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ContentQueryMap](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#ContentQueryMap(android.database.Cursor,%20kotlin.String,%20kotlin.Boolean,%20android.os.Handler))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `columnNameOfKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keepUpdated:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `handlerForUpdateNotifications:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Creates a ContentQueryMap that caches the content backing the cursor |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#close())`()` <br /> |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!\>! | [getRows](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#getRows())`()` <br /> |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)! | [getValues](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#getValues(kotlin.String))`(`rowName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Access the ContentValues for the row specified by rowName |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requery](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#requery())`()` Requeries the cursor and reads the contents into the cache |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepUpdated](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#setKeepUpdated(kotlin.Boolean))`(`keepUpdated:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change whether or not the ContentQueryMap will register with the cursor's ContentProvider for change notifications. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/content/ContentQueryMap#finalize())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Observable](https://developer.android.com/reference/kotlin/java/util/Observable.html#) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addObserver](https://developer.android.com/reference/kotlin/java/util/Observable.html#addObserver(java.util.Observer))`(`o:` ` [Observer](https://developer.android.com/reference/kotlin/java/util/Observer.html#)!`)` <br /> Adds an observer to the set of observers for this object, provided that it is not the same as some observer already in the set. The order in which notifications will be delivered to multiple observers is not specified. See the class comment. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearChanged](https://developer.android.com/reference/kotlin/java/util/Observable.html#clearChanged())`()` <br /> Indicates that this object has no longer changed, or that it has already notified all of its observers of its most recent change, so that the`hasChanged`method will now return`false`. This method is called automatically by the`notifyObservers`methods. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countObservers](https://developer.android.com/reference/kotlin/java/util/Observable.html#countObservers())`()` <br /> Returns the number of observers of this`Observable`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteObserver](https://developer.android.com/reference/kotlin/java/util/Observable.html#deleteObserver(java.util.Observer))`(`o:` ` [Observer](https://developer.android.com/reference/kotlin/java/util/Observer.html#)!`)` <br /> Deletes an observer from the set of observers of this object. Passing`null`to this method will have no effect. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteObservers](https://developer.android.com/reference/kotlin/java/util/Observable.html#deleteObservers())`()` <br /> Clears the observer list so that this object no longer has any observers. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChanged](https://developer.android.com/reference/kotlin/java/util/Observable.html#hasChanged())`()` <br /> Tests if this object has changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyObservers](https://developer.android.com/reference/kotlin/java/util/Observable.html#notifyObservers())`()` <br /> If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed. Each observer has its`update`method called with two arguments: this observable object and`null`. In other words, this method is equivalent to: `notifyObservers(null)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyObservers](https://developer.android.com/reference/kotlin/java/util/Observable.html#notifyObservers(kotlin.Any))`(`arg:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> If this object has changed, as indicated by the`hasChanged`method, then notify all of its observers and then call the`clearChanged`method to indicate that this object has no longer changed. Each observer has its`update`method called with two arguments: this observable object and the`arg`argument. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChanged](https://developer.android.com/reference/kotlin/java/util/Observable.html#setChanged())`()` <br /> Marks this`Observable`object as having been changed; the`hasChanged`method will now return`true`. <br /> | ||

## Public constructors

### ContentQueryMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ContentQueryMap(
    cursor: Cursor!, 
    columnNameOfKey: String!, 
    keepUpdated: Boolean, 
    handlerForUpdateNotifications: Handler!)
```

Creates a ContentQueryMap that caches the content backing the cursor

| Parameters ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the cursor whose contents should be cached |
| `columnNameOfKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the column that is to be used as the key of the values map |
| `keepUpdated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the cursor's ContentProvider should be monitored for changes and the map updated when changes do occur |
| `handlerForUpdateNotifications` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:the Handler that should be used to receive notifications of changes (if requested). Normally you pass null here, but if you know that the thread that is creating this isn't a thread that can receive messages then you can create your own handler and use that here. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```  

### getRows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRows(): MutableMap<String!, ContentValues!>!
```  

### getValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValues(rowName: String!): ContentValues!
```

Access the ContentValues for the row specified by rowName

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `rowName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:which row to read |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)! | the ContentValues for the row, or null if the row wasn't present in the cursor |

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requery(): Unit
```

Requeries the cursor and reads the contents into the cache 

### setKeepUpdated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeepUpdated(keepUpdated: Boolean): Unit
```

Change whether or not the ContentQueryMap will register with the cursor's ContentProvider for change notifications. If you use a ContentQueryMap in an activity you should call this with false in onPause(), which means you need to call it with true in onResume() if want it to be kept updated.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keepUpdated` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true the ContentQueryMap should be registered with the cursor's ContentProvider, false otherwise |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
