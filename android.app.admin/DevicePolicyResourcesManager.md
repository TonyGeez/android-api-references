Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DevicePolicyResourcesManager

```
open class DevicePolicyResourcesManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.admin.DevicePolicyResourcesManager](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#) |

Class containing required APIs to set, reset, and get device policy related resources.

## Summary

| Public methods ||
|---|---|
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20kotlin.String,%20java.util.function.Supplier)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableSource: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultDrawableLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!>)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts a `drawableSource` which could result in returning a different drawable than `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` if an override was set for that specific source. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultDrawableLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!>)` Returns the appropriate updated drawable for the `drawableId` with style `drawableStyle` if one was set using `setDrawables`, otherwise returns the drawable from `defaultDrawableLoader`. |
| open [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawableAsIcon(kotlin.String,%20kotlin.String,%20android.graphics.drawable.Icon)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultIcon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#?)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` but returns an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` instead of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`. |
| open [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawableAsIcon(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.graphics.drawable.Icon)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableSource: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultIcon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#?)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` but returns an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` instead of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawableForDensity(kotlin.String,%20kotlin.String,%20kotlin.Int,%20java.util.function.Supplier)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defaultDrawableLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!>)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts `density`. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawableForDensity(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20java.util.function.Supplier)(drawableId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, drawableSource: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defaultDrawableLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!>)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts `density`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getString(kotlin.String,%20java.util.function.Supplier)(stringId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultStringLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Returns the appropriate updated string for the `stringId` (see `DevicePolicyResources.Strings`) if one was set using `setStrings`, otherwise returns the string from `defaultStringLoader`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getString(kotlin.String,%20java.util.function.Supplier,%20kotlin.Any)(stringId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultStringLoader: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getString(kotlin.String,%20java.util.function.Supplier)` but accepts `formatArgs` and returns a localized formatted string, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java. |

## Public methods

### getDrawable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(
    drawableId: String, 
    drawableStyle: String, 
    drawableSource: String, 
    defaultDrawableLoader: Supplier<Drawable!>
): Drawable?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts a `drawableSource` which could result in returning a different drawable than `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` if an override was set for that specific source.

If `drawableSource` is `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResources#UNDEFINED:kotlin.String`, it returns the appropriate string for `drawableId` and `drawableStyle` similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`.

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultDrawableLoader` returned `null`.

Callers should register for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_DEVICE_POLICY_RESOURCE_UPDATED:kotlin.String` to get notified when a resource has been updated.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `drawableSource` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The source for the caller. This value cannot be `null`. |
| `defaultDrawableLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!\>: To get the default drawable if no updated drawable was set for the provided params. This value cannot be `null`. |

### getDrawable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(
    drawableId: String, 
    drawableStyle: String, 
    defaultDrawableLoader: Supplier<Drawable!>
): Drawable?
```

Returns the appropriate updated drawable for the `drawableId` with style `drawableStyle` if one was set using `setDrawables`, otherwise returns the drawable from `defaultDrawableLoader`.

Also returns the drawable from `defaultDrawableLoader` if `drawableId` is `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResources#UNDEFINED:kotlin.String`.

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultDrawableLoader` returned `null`.

This API uses the screen density returned from `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getConfiguration()`, to set a different value use `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawableForDensity(kotlin.String,%20kotlin.String,%20kotlin.Int,%20java.util.function.Supplier)`.

Callers should register for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_DEVICE_POLICY_RESOURCE_UPDATED:kotlin.String` to get notified when a resource has been updated.

Note that each call to this API loads the resource from the package that called `setDrawables` to set the updated resource.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `defaultDrawableLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!\>: To get the default drawable if no updated drawable was set for the provided params. This value cannot be `null`. |

### getDrawableAsIcon

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableAsIcon(
    drawableId: String, 
    drawableStyle: String, 
    defaultIcon: Icon?
): Icon?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` but returns an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` instead of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `defaultIcon` | [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)?: Returned if no updated drawable was set for the provided params. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#?` | This value may be `null`. |

### getDrawableAsIcon

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableAsIcon(
    drawableId: String, 
    drawableStyle: String, 
    drawableSource: String, 
    defaultIcon: Icon?
): Icon?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20kotlin.String,%20java.util.function.Supplier)` but returns an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` instead of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `drawableSource` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The source for the caller. This value cannot be `null`. |
| `defaultIcon` | [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)?: Returned if no updated drawable was set for the provided params. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#?` | This value may be `null`. |

### getDrawableForDensity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableForDensity(
    drawableId: String, 
    drawableStyle: String, 
    density: Int, 
    defaultDrawableLoader: Supplier<Drawable!>
): Drawable?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts `density`. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawableForDensity(kotlin.Int,%20kotlin.Int,%20android.content.res.Resources.Theme)`.

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultDrawableLoader` returned `null`.

Callers should register for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_DEVICE_POLICY_RESOURCE_UPDATED:kotlin.String` to get notified when a resource has been updated.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired screen density indicated by the resource as found in `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. A value of 0 means to use the density returned from `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getConfiguration()`. |
| `defaultDrawableLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!\>: To get the default drawable if no updated drawable was set for the provided params. This value cannot be `null`. |

### getDrawableForDensity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableForDensity(
    drawableId: String, 
    drawableStyle: String, 
    drawableSource: String, 
    density: Int, 
    defaultDrawableLoader: Supplier<Drawable!>
): Drawable?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getDrawable(kotlin.String,%20kotlin.String,%20kotlin.String,%20java.util.function.Supplier)`, but also accepts `density`. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawableForDensity(kotlin.Int,%20kotlin.Int,%20android.content.res.Resources.Theme)`.

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultDrawableLoader` returned `null`.

Callers should register for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_DEVICE_POLICY_RESOURCE_UPDATED:kotlin.String` to get notified when a resource has been updated.

| Parameters ||
|---|---|
| `drawableId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable ID to get the updated resource for. This value cannot be `null`. |
| `drawableStyle` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The drawable style to use. This value cannot be `null`. |
| `drawableSource` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The source for the caller. This value cannot be `null`. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired screen density indicated by the resource as found in `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. A value of 0 means to use the density returned from `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getConfiguration()`. |
| `defaultDrawableLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!\>: To get the default drawable if no updated drawable was set for the provided params. This value cannot be `null`. |

### getString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(
    stringId: String, 
    defaultStringLoader: Supplier<String!>
): String?
```

Returns the appropriate updated string for the `stringId` (see `DevicePolicyResources.Strings`) if one was set using `setStrings`, otherwise returns the string from `defaultStringLoader`.

Also returns the string from `defaultStringLoader` if `stringId` is `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResources#UNDEFINED:kotlin.String`.

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultStringLoader` returned `null`.

Callers should register for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#ACTION_DEVICE_POLICY_RESOURCE_UPDATED:kotlin.String` to get notified when a resource has been updated.

Note that each call to this API loads the resource from the package that called `setStrings` to set the updated resource.

| Parameters ||
|---|---|
| `stringId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The IDs to get the updated resource for. This value cannot be `null`. |
| `defaultStringLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: To get the default string if no updated string was set for `stringId`. This value cannot be `null`. |

### getString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(
    stringId: String, 
    defaultStringLoader: Supplier<String!>, 
    vararg formatArgs: Any!
): String?
```

Similar to `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyResourcesManager#getString(kotlin.String,%20java.util.function.Supplier)` but accepts `formatArgs` and returns a localized formatted string, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format, (see `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getString(kotlin.Int,%20kotlin.Any)`).

Calls to this API will not return `null` unless no updated drawable was found and the call to `defaultStringLoader` returned `null`.

| Parameters ||
|---|---|
| `stringId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The IDs to get the updated resource for. This value cannot be `null`. |
| `defaultStringLoader` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: To get the default string if no updated string was set for `stringId`. This value cannot be `null`. |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The format arguments that will be used for substitution. This value cannot be `null`. |
