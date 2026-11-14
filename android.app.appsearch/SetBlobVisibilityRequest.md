# SetBlobVisibilityRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

# SetBlobVisibilityRequest

Kotlin| [Java](../android/app/appsearch/SetBlobVisibilityRequest.md) 
| --- | --- |

```
open class SetBlobVisibilityRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SetBlobVisibilityRequest](../android/app/appsearch/SetBlobVisibilityRequest.md) |

Request to configure the visibility settings of blobs in AppSearch.

Used with [AppSearchSession.setBlobVisibility](../android/app/appsearch/AppSearchSession.md))to specify visibility and display properties for blob namespaces. You can control which blob namespaces are displayed on system UI surfaces and which are accessible based on specific visibility configurations.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/appsearch/SetBlobVisibilityRequest.Builder.md) Builder for [SetBlobVisibilityRequest](../android/app/appsearch/SetBlobVisibilityRequest.md) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getNamespacesNotDisplayedBySystem](../android/app/appsearch/SetBlobVisibilityRequest.md))`()` Returns all the blob namespaces that are opted out of being displayed and visible on any system UI surface. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md)!\>!\> | [getNamespacesVisibleToConfigs](../android/app/appsearch/SetBlobVisibilityRequest.md))`()` Returns a mapping of blob namespaces to the set of [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) s that have access to that namespace. |

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

Returns a mapping of blob namespaces to the set of [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) s that have access to that namespace.

All conditions in a single [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) are "AND" relationship. A caller must match all conditions to have the access. All [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) s in the set of a blob namespace are "OR" relationship. A caller could have access if they matches any [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) in the set.

This method provides the set of [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md) for all blob namespaces.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SchemaVisibilityConfig](../android/app/appsearch/SchemaVisibilityConfig.md)!>!> | This value cannot be`null`. |

**See Also**

- [android.app.appsearch.SetBlobVisibilityRequest.Builder#addNamespaceVisibleToConfig](../android/app/appsearch/SetBlobVisibilityRequest.Builder.md))
