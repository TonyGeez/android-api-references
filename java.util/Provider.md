# ServiceLoader.Provider

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Provider

```
interface Provider<S : Any!> : Supplier<S>
```

| [java.util.ServiceLoader.Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider#) |

Represents a service provider located by`ServiceLoader`.

When using a loader's [stream()](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#stream())method then the elements are of type`Provider`. This allows processing to select or filter on the provider class without instantiating the provider.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| abstractS | [get](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider#get())`()` Returns an instance of the provider. |
| abstract [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<outS\>! | [type](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider#type())`()` Returns the provider type. |

## Public methods

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(): S
```

Returns an instance of the provider.

| Return ||
|---|------------------------------|
| S | An instance of the provider. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.ServiceConfigurationError` | If the service provider cannot be instantiated, or in the case of a provider factory, the public static "`provider()`" method returns`null`or throws an error or exception. The`ServiceConfigurationError`will carry an appropriate cause where possible. |

### type

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun type(): Class<out S>!
```

Returns the provider type. There is no guarantee that this type is accessible or that it has a public no-args constructor. The [get()](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider#get())method should be used to obtain the provider instance.

When a module declares that the provider class is created by a provider factory then this method returns the return type of its public static "`provider()`" method.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` `S>! | The provider type |
