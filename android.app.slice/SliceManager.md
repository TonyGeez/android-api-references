Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceManager

```
open class SliceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.SliceManager](SliceManager.md) |

> [!CAUTION]
> **This class was deprecated in API level 35.**
>
> Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#`.

Class to handle interactions with Slices.

The SliceManager manages permissions and pinned state for slices. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#CATEGORY_SLICE:kotlin.String` Category used to resolve intents that can be rendered as slices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#SLICE_METADATA_KEY:kotlin.String` The meta-data key that allows an activity to easily be linked directly to a slice. |

| Public methods ||
|---|---|
| open [Slice](Slice.md)? | bindSlice Turns a slice intent into slice content. |
| open [Slice](Slice.md)? | bindSlice Turns a slice Uri into slice content. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkSlicePermission Determine whether a particular process and user ID has been granted permission to access a specific slice URI. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\> | getPinnedSlices Get the list of currently pinned slices for this app. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](SliceSpec.md)!\> | getPinnedSpecs Get the current set of specs for a pinned slice. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](../android.net/Uri.md)!\> | getSliceDescendants Obtains a list of slices that are descendants of the specified Uri. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | grantSlicePermission Grant permission to access a specific slice Uri to another package. |
| open [Uri](../android.net/Uri.md)? | mapIntentToUri Turns a slice intent into a slice uri. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | pinSlice Ensures that a slice is in a pinned state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | revokeSlicePermission Remove permissions to access a particular content provider Uri that were previously added with grantSlicePermission for a specific target package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unpinSlice Remove a pin for a slice. |

## Constants

### CATEGORY_SLICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_SLICE: String
```

**Deprecated:** *Deprecated in Java.*

Category used to resolve intents that can be rendered as slices.

This category should be included on intent filters on providers that extend SliceProvider.

 Value: "android.app.slice.category.SLICE"

**See Also**

- SliceProvider
- onMapIntentToUri
- mapIntentToUri

### SLICE_METADATA_KEY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SLICE_METADATA_KEY: String
```

**Deprecated:** *Deprecated in Java.*

The meta-data key that allows an activity to easily be linked directly to a slice.

An activity can be statically linked to a slice uri by including a meta-data item for this key that contains a valid slice uri for the same application declaring the activity.

```kotlin
<activity android:name="com.example.mypkg.MyActivity">
      <meta-data android:name="android.metadata.SLICE_URI"
                 android:value="content://com.example.mypkg/main_slice" />
   </activity>
  
```

 Value: "android.metadata.SLICE_URI"

**See Also**

- mapIntentToUri
- onMapIntentToUri

## Public methods

### bindSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindSlice(
    intent: Intent, 
    supportedSpecs: MutableSet<SliceSpec!>
): Slice?
```

**Deprecated:** *Deprecated in Java.*

Turns a slice intent into slice content. Is a shortcut to perform the action of both mapIntentToUri and bindSlice at once.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The intent associated with a slice. This value cannot be `null`. |
| `supportedSpecs` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](SliceSpec.md)!\>: List of supported specs. This value cannot be `null`. |

| Return ||
|---|---|
| Slice | The Slice provided by the app or null if none is given. |

**See Also**

- Slice
- onMapIntentToUri
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#`

### bindSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindSlice(
    uri: Uri, 
    supportedSpecs: MutableSet<SliceSpec!>
): Slice?
```

**Deprecated:** *Deprecated in Java.*

Turns a slice Uri into slice content.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The URI to a slice provider. This value cannot be `null`. |
| `supportedSpecs` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](SliceSpec.md)!\>: List of supported specs. This value cannot be `null`. |

| Return ||
|---|---|
| Slice | The Slice provided by the app or null if none is given. |

**See Also**

- Slice

### checkSlicePermission

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkSlicePermission(
    uri: Uri, 
    pid: Int, 
    uid: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Determine whether a particular process and user ID has been granted permission to access a specific slice URI.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The uri that is being checked. This value cannot be `null`. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The user ID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int` if the given pid/uid is allowed to access that uri, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` |

**See Also**

- grantSlicePermission

### getPinnedSlices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPinnedSlices(): MutableList<Uri!>
```

**Deprecated:** *Deprecated in Java.*

Get the list of currently pinned slices for this app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | This value cannot be `null`. |

**See Also**

- onSlicePinned

### getPinnedSpecs

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPinnedSpecs(uri: Uri!): MutableSet<SliceSpec!>
```

**Deprecated:** *Deprecated in Java.*

Get the current set of specs for a pinned slice.

This is the set of specs supported for a specific pinned slice. It will take into account all clients and returns only specs supported by all.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/slice/SliceSpec!>` | This value cannot be `null`. |

**See Also**

- SliceSpec

### getSliceDescendants

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSliceDescendants(uri: Uri): MutableCollection<Uri!>
```

**Deprecated:** *Deprecated in Java.*

Obtains a list of slices that are descendants of the specified Uri.

Not all slice providers will implement this functionality, in which case, an empty collection will be returned. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The uri to look for descendants under. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | All slices within the space. This value cannot be `null`. |

**See Also**

- onGetSliceDescendants

### grantSlicePermission

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun grantSlicePermission(
    toPackage: String, 
    uri: Uri
): Unit
```

**Deprecated:** *Deprecated in Java.*

Grant permission to access a specific slice Uri to another package.

| Parameters ||
|---|---|
| `toPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package you would like to allow to access the Uri. This value cannot be `null`. |
| `uri` | [Uri](../android.net/Uri.md): The Uri you would like to grant access to. This value cannot be `null`. |

**See Also**

- revokeSlicePermission

### mapIntentToUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mapIntentToUri(intent: Intent): Uri?
```

**Deprecated:** *Deprecated in Java.*

Turns a slice intent into a slice uri. Expects an explicit intent.

This goes through a several stage resolution process to determine if any slice can represent this intent.

1. If the intent contains data that getType is `https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider#SLICE_TYPE:kotlin.String` then the data will be returned.
2. If the intent explicitly points at an activity, and that activity has meta-data for key `https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#SLICE_METADATA_KEY:kotlin.String`, then the Uri specified there will be returned.
3. Lastly, if the intent with `https://developer.android.com/reference/kotlin/android/app/slice/SliceManager#CATEGORY_SLICE:kotlin.String` added resolves to a provider, then the provider will be asked to onMapIntentToUri and that result will be returned.
4. If no slice is found, then `null` is returned.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The intent associated with a slice. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | The Slice Uri provided by the app or null if none exists. |

**See Also**

- Slice
- onMapIntentToUri
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#`

### pinSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pinSlice(
    uri: Uri, 
    specs: MutableSet<SliceSpec!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Ensures that a slice is in a pinned state.

Pinned state is not persisted across reboots, so apps are expected to re-pin any slices they still care about after a reboot.

This may only be called by apps that are the default launcher for the device or the default voice interaction service. Otherwise will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The uri of the slice being pinned. This value cannot be `null`. |
| `specs` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SliceSpec](SliceSpec.md)!\>: The list of supported SliceSpecs of the callback. This value cannot be `null`. |

**See Also**

- onSlicePinned
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`

### revokeSlicePermission

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun revokeSlicePermission(
    toPackage: String, 
    uri: Uri
): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove permissions to access a particular content provider Uri that were previously added with grantSlicePermission for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

| Parameters ||
|---|---|
| `toPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package you would like to allow to access the Uri. This value cannot be `null`. |
| `uri` | [Uri](../android.net/Uri.md): The Uri you would like to revoke access to. This value cannot be `null`. |

**See Also**

- grantSlicePermission

### unpinSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unpinSlice(uri: Uri): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove a pin for a slice.

If the slice has no other pins/callbacks then the slice will be unpinned.

This may only be called by apps that are the default launcher for the device or the default voice interaction service. Otherwise will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): The uri of the slice being unpinned. This value cannot be `null`. |

**See Also**

- pinSlice
- onSliceUnpinned
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String`
