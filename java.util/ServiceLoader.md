# ServiceLoader

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceLoader

```
class ServiceLoader<S : Any!> : MutableIterable<S>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.ServiceLoader](../java/util/ServiceLoader.md) |

A facility to load implementations of a service.

A*service* is a well-known interface or class for which zero, one, or many service providers exist. A*service provider* (or just*provider* ) is a class that implements or subclasses the well-known interface or class. A`ServiceLoader`is an object that locates and loads service providers deployed in the run time environment at a time of an application's choosing. Application code refers only to the service, not to service providers, and is assumed to be capable of choosing between multiple service providers (based on the functionality they expose through the service), and handling the possibility that no service providers are located.

## Obtaining a service loader

An application obtains a service loader for a given service by invoking one of the static`load`methods of`ServiceLoader`.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Provider](../java/util/ServiceLoader.Provider.md) Represents a service provider located by`ServiceLoader`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](../java/util/Optional.md)\<S\>! | [findFirst](../java/util/ServiceLoader.md))`()` Load the first available service provider of this loader's service. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<S\> | [iterator](../java/util/ServiceLoader.md))`()` Returns an iterator to lazily load and instantiate the available providers of this loader's service. |
| static [ServiceLoader](../java/util/ServiceLoader.md)\<S\>! | [load](../java/util/ServiceLoader.md))`(`service:` ` [Class](../java/lang/Class.md)<S>!`)` Creates a new service loader for the given service type, using the current thread's [context class loader](../java/lang/Thread.md)). |
| --- | --- |
| static [ServiceLoader](../java/util/ServiceLoader.md)\<S\>! | [load](../java/util/ServiceLoader.md))`(`service:` ` [Class](../java/lang/Class.md)<S>!`, `loader:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` Creates a new service loader for the given service. |
| static [ServiceLoader](../java/util/ServiceLoader.md)\<S\>! | [loadInstalled](../java/util/ServiceLoader.md))`(`service:` ` [Class](../java/lang/Class.md)<S>!`)` Creates a new service loader for the given service type, using the extension class loader. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reload](../java/util/ServiceLoader.md))`()` Clear this loader's provider cache so that all providers will be reloaded. |
| --- | --- |
| [Stream](../java/util/stream/Stream.md)\< [ServiceLoader.Provider](../java/util/ServiceLoader.Provider.md)\<S\>!\>! | [stream](../java/util/ServiceLoader.md))`()` Returns a stream to lazily load available providers of this loader's service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/ServiceLoader.md))`()` Returns a string describing this service. |

## Public methods

### findFirst

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findFirst(): Optional<S>!
```

Load the first available service provider of this loader's service. This convenience method is equivalent to invoking the [iterator()](../java/util/ServiceLoader.md))method and obtaining the first element. It therefore returns the first element from the provider cache if possible, it otherwise attempts to load and instantiate the first provider.

The following example loads the first available service provider. If no service providers are located then it uses a default implementation. 

```kotlin
<code>CodecFactory factory = ServiceLoader.load(CodecFactory.class)
                                         .findFirst()
                                         .orElse(DEFAULT_CODECSET_FACTORY);
  </code>
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Optional](../java/util/Optional.md)<S>! | The first service provider or empty`Optional`if no service providers are located |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.ServiceConfigurationError` | If a provider class cannot be loaded for any of the reasons specified in the [Errors](../java/util/ServiceLoader.md) section above. |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun iterator(): MutableIterator<S>
```

Returns an iterator to lazily load and instantiate the available providers of this loader's service.

To achieve laziness the actual work of locating and instantiating providers is done by the iterator itself. Its [hasNext](../java/util/Iterator.md))and [next](../java/util/Iterator.md))methods can therefore throw a [ServiceConfigurationError](../java/util/ServiceConfigurationError.md) for any of the reasons specified in the [Errors](../java/util/ServiceLoader.md) section above. To write robust code it is only necessary to catch`ServiceConfigurationError`when using the iterator. If an error is thrown then subsequent invocations of the iterator will make a best effort to locate and instantiate the next available provider, but in general such recovery cannot be guaranteed.

Caching: The iterator returned by this method first yields all of the elements of the provider cache, in the order that they were loaded. It then lazily loads and instantiates any remaining service providers, adding each one to the cache in turn. If this loader's provider caches are cleared by invoking the [reload](../java/util/ServiceLoader.md))method then existing iterators for this service loader should be discarded. The`hasNext`and`next`methods of the iterator throw if used after the provider cache has been cleared.

The iterator returned by this method does not support removal. Invoking its [remove](../java/util/Iterator.md))method will cause an [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) to be thrown.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<S> | An iterator that lazily loads providers for this loader's service |

### load

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <S : Any!> load(service: Class<S>!): ServiceLoader<S>!
```

Creates a new service loader for the given service type, using the current thread's [context class loader](../java/lang/Thread.md)).

An invocation of this convenience method of the form 

```kotlin
<code>ServiceLoader.load(service)
  </code>
```
is equivalent to 

```kotlin
<code>ServiceLoader.load(service, Thread.currentThread().getContextClassLoader())
  </code>
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `<S>` | the class of the service type |
| `service` | [Class](../java/lang/Class.md)\<S\>!:The interface or abstract class representing the service |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](../java/util/ServiceLoader.md)<S>! | A new service loader |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.util.ServiceConfigurationError` | if the service type is not accessible to the caller |

### load

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <S : Any!> load(
    service: Class<S>!, 
    loader: ClassLoader!
): ServiceLoader<S>!
```

Creates a new service loader for the given service. The service loader uses the given class loader as the starting point to locate service providers for the service.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<S>` | the class of the service type |
| `service` | [Class](../java/lang/Class.md)\<S\>!:The interface or abstract class representing the service |
| `loader` | [ClassLoader](../java/lang/ClassLoader.md)!:The class loader to be used to load provider-configuration files and provider classes, or`null`if the system class loader (or, failing that, the bootstrap class loader) is to be used |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](../java/util/ServiceLoader.md)<S>! | A new service loader |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.util.ServiceConfigurationError` | if the service type is not accessible to the caller |

### loadInstalled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <S : Any!> loadInstalled(service: Class<S>!): ServiceLoader<S>!
```

Creates a new service loader for the given service type, using the extension class loader.

This convenience method simply locates the extension class loader, call it`extClassLoader`, and then returns 

```kotlin
<code>ServiceLoader.load(service, extClassLoader)
  </code>
```

This method is intended for use when only installed providers are desired. The resulting service will only find and load providers that have been installed into the current Java virtual machine.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `<S>` | the class of the service type |
| `service` | [Class](../java/lang/Class.md)\<S\>!:The interface or abstract class representing the service |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](../java/util/ServiceLoader.md)<S>! | A new service loader |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.util.ServiceConfigurationError` | if the service type is not accessible to the caller |

### reload

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reload(): Unit
```

Clear this loader's provider cache so that all providers will be reloaded.

After invoking this method, subsequent invocations of the [iterator](../java/util/ServiceLoader.md))or [stream](../java/util/ServiceLoader.md))methods will lazily locate providers (and instantiate in the case of`iterator`) from scratch, just as is done by a newly-created service loader.

This method is intended for use in situations in which new service providers can be installed into a running Java virtual machine. 

### stream

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): Stream<ServiceLoader.Provider<S>!>!
```

Returns a stream to lazily load available providers of this loader's service. The stream elements are of type [Provider](../java/util/ServiceLoader.Provider.md), the`Provider`'s [get](../java/util/ServiceLoader.Provider.md))method must be invoked to get or instantiate the provider.

To achieve laziness the actual work of locating providers is done when processing the stream. If a service provider cannot be loaded for any of the reasons specified in the [Errors](../java/util/ServiceLoader.md) section above then [ServiceConfigurationError](../java/util/ServiceConfigurationError.md) is thrown by whatever method caused the service provider to be loaded.

Caching: When processing the stream then providers that were previously loaded by stream operations are processed first, in load order. It then lazily loads any remaining service providers. If this loader's provider caches are cleared by invoking the [reload](../java/util/ServiceLoader.md))method then existing streams for this service loader should be discarded. The returned stream's source [spliterator](../java/util/Spliterator.md) is*fail-fast* and will throw [ConcurrentModificationException](../java/util/ConcurrentModificationException.md) if the provider cache has been cleared.

The following examples demonstrate usage. The first example creates a stream of`CodecFactory`objects, the second example is the same except that it sorts the providers by provider class name (and so locate all providers). 

```kotlin
<code>Stream&lt;CodecFactory&gt; providers = ServiceLoader.load(CodecFactory.class)
             .stream()
             .map(Provider::get);
 
     Stream&lt;CodecFactory&gt; providers = ServiceLoader.load(CodecFactory.class)
             .stream()
             .sorted(Comparator.comparing(p -&gt; p.type().getName()))
             .map(Provider::get);
  </code>
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [ServiceLoader.Provider](../java/util/ServiceLoader.Provider.md)<S>!>! | A stream that lazily loads providers for this loader's service |

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this service.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A descriptive string |
