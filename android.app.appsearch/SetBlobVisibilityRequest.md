# SetBlobVisibilityRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

# SetBlobVisibilityRequest

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/SetBlobVisibilityRequest "View this page in Java") 

```
open class SetBlobVisibilityRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.SetBlobVisibilityRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest#) |

Request to configure the visibility settings of blobs in AppSearch.

Used with [AppSearchSession.setBlobVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setBlobVisibility(android.app.appsearch.SetBlobVisibilityRequest,%20java.util.concurrent.Executor,%20java.util.function.Consumer))to specify visibility and display properties for blob namespaces. You can control which blob namespaces are displayed on system UI surfaces and which are accessible based on specific visibility configurations.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest.Builder) Builder for [SetBlobVisibilityRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest#) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getNamespacesNotDisplayedBySystem](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest#getNamespacesNotDisplayedBySystem())`()` Returns all the blob namespaces that are opted out of being displayed and visible on any system UI surface. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig)!\>!\> | [getNamespacesVisibleToConfigs](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest#getNamespacesVisibleToConfigs())`()` Returns a mapping of blob namespaces to the set of [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) s that have access to that namespace. |

## Public methods

### getNamespacesNotDisplayedBySystem

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
open fun getNamespacesNotDisplayedBySystem(): MutableSet<String!>
```

Returns all the blob namespaces that are opted out of being displayed and visible on any system UI surface.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getNamespacesVisibleToConfigs

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
open fun getNamespacesVisibleToConfigs(): MutableMap<String!, MutableSet<SchemaVisibilityConfig!>!>
```

Returns a mapping of blob namespaces to the set of [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) s that have access to that namespace.

All conditions in a single [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) are "AND" relationship. A caller must match all conditions to have the access. All [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) s in the set of a blob namespace are "OR" relationship. A caller could have access if they matches any [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) in the set.

This method provides the set of [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) for all blob namespaces.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig)!>!> | This value cannot be`null`. |

**See Also**

- [android.app.appsearch.SetBlobVisibilityRequest.Builder#addNamespaceVisibleToConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SetBlobVisibilityRequest.Builder#addNamespaceVisibleToConfig(kotlin.String,%20android.app.appsearch.SchemaVisibilityConfig))
