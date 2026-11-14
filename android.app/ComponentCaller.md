# ComponentCaller

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentCaller

Kotlin| [Java](https://developer.android.com/reference/android/app/ComponentCaller "View this page in Java") 
| --- | --- |

```
class ComponentCaller
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#) |

Represents the app that launched the component. See below for the APIs available on the component caller.

**Note** , that in [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) only [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) has access to [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#) instances.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkContentUriPermission](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#checkContentUriPermission(android.net.Uri,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `modeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether this component caller had access to a specific content URI at launch time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPackage](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#getPackage())`()` Returns the package name of this component caller. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUid](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#getUid())`()` Returns the uid of this component caller. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#hashCode())`()` <br /> |

## Public methods

### checkContentUriPermission

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkContentUriPermission(
    uri: Uri, 
    modeFlags: Int
): Int
```

Determines whether this component caller had access to a specific content URI at launch time. Apps can use this API to validate content URIs coming from other apps.

**Note** , in [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) only [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) has access to [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#) instances.

Before using this method, note the following:

- You must have access to the supplied URI, otherwise it will throw a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#).
- This is not a real time check, i.e. the permissions have been computed at launch time.
- This method will return the correct result for content URIs passed at launch time, specifically the ones from [Intent.getData()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()), [Intent.EXTRA_STREAM](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String), and [Intent.getClipData()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData())in the intent of`startActivity(intent)`. For others, it will throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The content uri that is being checked This value cannot be`null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The access modes to check Value is either`0`or a combination of [android.content.Intent#FLAG_GRANT_READ_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int), and [android.content.Intent#FLAG_GRANT_WRITE_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PackageManager.PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int) if this activity caller is allowed to access that uri, or [PackageManager.PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int) if it is not Value is [android.content.pm.PackageManager#PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int), or [android.content.pm.PackageManager#PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int) |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if uri is a non-content URI or it wasn't passed at launch in [Intent.getData()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()), [Intent.EXTRA_STREAM](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_STREAM:kotlin.String), and [Intent.getClipData()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()) |
| `java.lang.SecurityException` | if you don't have access to uri |

**See Also**

- [android.content.Context#checkContentUriPermissionFull(Uri, int, int, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#checkContentUriPermissionFull(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getPackage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackage(): String?
```

Returns the package name of this component caller.

**Note** , in [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) only [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) has access to [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#) instances.

<br />

### Requirements for [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) callers

In order to receive the calling app's package name, at least one of the following has to be met:

- The calling app must call [ActivityOptions.setShareIdentityEnabled(boolean)](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean))with a value of`true`and launch this activity with the resulting`ActivityOptions`.
- The launched activity has the same uid as the calling app.
- The launched activity is running in a package that is signed with the same key used to sign the platform (typically only system packages such as Settings will meet this meet this requirement).

These are the same requirements for [getUid()](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#getUid()); if any of these are met, then these methods can be used to obtain the uid and package name of the calling app. If none are met, then`null`is returned.

Note, even if the above conditions are not met, the calling app's identity may still be available from [Activity.getCallingPackage()](https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage())if this activity was started with`Activity#startActivityForResult`to allow validation of the result's recipient.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the package name of the calling app or null if the current component cannot access the identity of the calling app or the caller is invalid |

**See Also**

- [android.app.ActivityOptions#setShareIdentityEnabled(boolean)](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean))
- [android.app.Activity#getLaunchedFromPackage()](https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromPackage()) 

### getUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUid(): Int
```

Returns the uid of this component caller.

**Note** , in [android.os.Build.VERSION_CODES#VANILLA_ICE_CREAM](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int) only [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) has access to [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#) instances.

<br />

### Requirements for [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) callers

In order to receive the calling app's uid, at least one of the following has to be met:

- The calling app must call [ActivityOptions.setShareIdentityEnabled(boolean)](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean))with a value of`true`and launch this activity with the resulting`ActivityOptions`.
- The launched activity has the same uid as the calling app.
- The launched activity is running in a package that is signed with the same key used to sign the platform (typically only system packages such as Settings will meet this requirement).

These are the same requirements for [getPackage()](https://developer.android.com/reference/kotlin/android/app/ComponentCaller#getPackage()); if any of these are met, then these methods can be used to obtain the uid and package name of the calling app. If none are met, then [Process.INVALID_UID](https://developer.android.com/reference/kotlin/android/os/Process.html#INVALID_UID:kotlin.Int) is returned.

Note, even if the above conditions are not met, the calling app's identity may still be available from [Activity.getCallingPackage()](https://developer.android.com/reference/kotlin/android/app/Activity#getCallingPackage())if this activity was started with`Activity#startActivityForResult`to allow validation of the result's recipient.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the uid of the calling app or [Process.INVALID_UID](https://developer.android.com/reference/kotlin/android/os/Process.html#INVALID_UID:kotlin.Int) if the current component cannot access the identity of the calling app or the caller is invalid |

**See Also**

- [android.app.ActivityOptions#setShareIdentityEnabled(boolean)](https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setShareIdentityEnabled(kotlin.Boolean))
- [android.app.Activity#getLaunchedFromUid()](https://developer.android.com/reference/kotlin/android/app/Activity#getLaunchedFromUid()) 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
