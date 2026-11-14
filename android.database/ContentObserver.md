Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentObserver

Kotlin | [Java](https://developer.android.com/reference/android/database/ContentObserver "View this page in Java")
| --- | --- |

```
abstract class ContentObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver#) |

| Known Direct Subclasses [AbstractCursor.SelfContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor.SelfContentObserver), [Loader.ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver.html#) |---|---| | [AbstractCursor.SelfContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor.SelfContentObserver) | Cursors use this class to track changes others make to their URI. | | [Loader.ForceLoadContentObserver](https://developer.android.com/reference/kotlin/android/content/Loader.ForceLoadContentObserver.html#) | An implementation of a ContentObserver that takes care of connecting it to the Loader to have the loader re-load its data when the observer is told it has changed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Receives call backs for changes to content. Must be implemented by objects which are added to a `https://developer.android.com/reference/kotlin/android/database/ContentObservable`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/ContentObserver#ContentObserver(android.os.Handler)(handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Creates a content observer. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#deliverSelfNotifications()()` Returns true if this observer is interested receiving self-change notifications. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#dispatchChange(kotlin.Boolean)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Dispatches a change notification to the observer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#dispatchChange(kotlin.Boolean,%20android.net.Uri)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Dispatches a change notification to the observer. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#dispatchChange(kotlin.Boolean,%20android.net.Uri,%20kotlin.Int)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatches a change notification to the observer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#dispatchChange(kotlin.Boolean,%20kotlin.collections.MutableCollection,%20kotlin.Int)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Dispatches a change notification to the observer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#onChange(kotlin.Boolean)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` This method is called when a content change occurs. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#onChange(kotlin.Boolean,%20android.net.Uri)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` This method is called when a content change occurs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#onChange(kotlin.Boolean,%20android.net.Uri,%20kotlin.Int)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is called when a content change occurs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/ContentObserver#onChange(kotlin.Boolean,%20kotlin.collections.MutableCollection,%20kotlin.Int)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is called when a content change occurs. |
| --- | --- |

## Public constructors

### ContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ContentObserver(handler: Handler!)
```

Creates a content observer.

| Parameters ||
|---|---|
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: The handler to run #onChange on, or null if none. |

## Public methods

### deliverSelfNotifications

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deliverSelfNotifications(): Boolean
```

Returns true if this observer is interested receiving self-change notifications. Subclasses should override this method to indicate whether the observer is interested in receiving notifications for changes that it made to the content itself.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if self-change notifications should be delivered to the observer. |

### dispatchChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchChange(selfChange: Boolean): Unit
```

**Deprecated:** *Callers should migrate towards using a richer overload that provides more details about the change, such as `https://developer.android.com/reference/kotlin/android/database/ContentObserver#dispatchChange(kotlin.Boolean,%20kotlin.collections.MutableCollection,%20kotlin.Int)`.*

Dispatches a change notification to the observer.

If a `https://developer.android.com/reference/kotlin/android/os/Handler.html#` was supplied to the `https://developer.android.com/reference/kotlin/android/database/ContentObserver#` constructor, then a call to the #onChange method is posted to the handler's message queue. Otherwise, the #onChange method is invoked immediately on this thread.

### dispatchChange

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchChange(
    selfChange: Boolean, 
    uri: Uri?
): Unit
```

Dispatches a change notification to the observer. Includes the changed content Uri when available.

If a `https://developer.android.com/reference/kotlin/android/os/Handler.html#` was supplied to the `https://developer.android.com/reference/kotlin/android/database/ContentObserver#` constructor, then a call to the #onChange method is posted to the handler's message queue. Otherwise, the #onChange method is invoked immediately on this thread.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The Uri of the changed content. This value may be `null`. |

### dispatchChange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchChange(
    selfChange: Boolean, 
    uri: Uri?, 
    flags: Int
): Unit
```

Dispatches a change notification to the observer. Includes the changed content Uri when available.

If a `https://developer.android.com/reference/kotlin/android/os/Handler.html#` was supplied to the `https://developer.android.com/reference/kotlin/android/database/ContentObserver#` constructor, then a call to the #onChange method is posted to the handler's message queue. Otherwise, the #onChange method is invoked immediately on this thread.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The Uri of the changed content. This value may be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating details about this change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SYNC_TO_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_DELETE:kotlin.Int` |
| --- | --- |

### dispatchChange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchChange(
    selfChange: Boolean, 
    uris: MutableCollection<Uri!>, 
    flags: Int
): Unit
```

Dispatches a change notification to the observer. Includes the changed content Uris when available.

If a `https://developer.android.com/reference/kotlin/android/os/Handler.html#` was supplied to the `https://developer.android.com/reference/kotlin/android/database/ContentObserver#` constructor, then a call to the #onChange method is posted to the handler's message queue. Otherwise, the #onChange method is invoked immediately on this thread.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The Uri of the changed content. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating details about this change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SYNC_TO_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_DELETE:kotlin.Int` |
| --- | --- |

### onChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChange(selfChange: Boolean): Unit
```

This method is called when a content change occurs.

Subclasses should override this method to handle content changes.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |

### onChange

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChange(
    selfChange: Boolean, 
    uri: Uri?
): Unit
```

This method is called when a content change occurs. Includes the changed content Uri when available.

Subclasses should override this method to handle content changes. To ensure correct operation on older versions of the framework that did not provide richer arguments, applications should implement all overloads.

Example implementation:

```kotlin
<code>
  // Implement the onChange(boolean) method to delegate the change notification to
  // the onChange(boolean, Uri) method to ensure correct operation on older versions
  // of the framework that did not have the onChange(boolean, Uri) method.
  @Override
  public void onChange(boolean selfChange) {
      onChange(selfChange, null);
  }
 
  // Implement the onChange(boolean, Uri) method to take advantage of the new Uri argument.
  @Override
  public void onChange(boolean selfChange, Uri uri) {
      // Handle change.
  }
  </code>
```

<br />

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The Uri of the changed content. This value may be `null`. |

### onChange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChange(
    selfChange: Boolean, 
    uri: Uri?, 
    flags: Int
): Unit
```

This method is called when a content change occurs. Includes the changed content Uri when available.

Subclasses should override this method to handle content changes. To ensure correct operation on older versions of the framework that did not provide richer arguments, applications should implement all overloads.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The Uri of the changed content. This value may be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating details about this change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SYNC_TO_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_DELETE:kotlin.Int` |
| --- | --- |

### onChange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChange(
    selfChange: Boolean, 
    uris: MutableCollection<Uri!>, 
    flags: Int
): Unit
```

This method is called when a content change occurs. Includes the changed content Uris when available.

Subclasses should override this method to handle content changes. To ensure correct operation on older versions of the framework that did not provide richer arguments, applications should implement all overloads.

| Parameters ||
|---|---|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this is a self-change notification. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The Uris of the changed content. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating details about this change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SYNC_TO_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_INSERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#NOTIFY_DELETE:kotlin.Int` |
| --- | --- |
