# ServiceLoader

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceLoader

```
class ServiceLoader<S : Any!> : MutableIterable<S>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#) |

A facility to load implementations of a service.

A*service* is a well-known interface or class for which zero, one, or many service providers exist. A*service provider* (or just*provider* ) is a class that implements or subclasses the well-known interface or class. A`ServiceLoader`is an object that locates and loads service providers deployed in the run time environment at a time of an application's choosing. Application code refers only to the service, not to service providers, and is assumed to be capable of choosing between multiple service providers (based on the functionality they expose through the service), and handling the possibility that no service providers are located.

## Obtaining a service loader

An application obtains a service loader for a given service by invoking one of the static`load`methods of`ServiceLoader`.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider) Represents a service provider located by`ServiceLoader`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional)\<S\>! | [findFirst](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#findFirst())`()` Load the first available service provider of this loader's service. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<S\> | [iterator](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#iterator())`()` Returns an iterator to lazily load and instantiate the available providers of this loader's service. |
| static [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)\<S\>! | [load](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#load(java.lang.Class))`(`service:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<S>!`)` Creates a new service loader for the given service type, using the current thread's [context class loader](https://developer.android.com/reference/kotlin/java/lang/Thread.html#getContextClassLoader()). |
| --- | --- |
| static [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)\<S\>! | [load](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#load(java.lang.Class,%20java.lang.ClassLoader))`(`service:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<S>!`, `loader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` Creates a new service loader for the given service. |
| static [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)\<S\>! | [loadInstalled](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#loadInstalled(java.lang.Class))`(`service:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<S>!`)` Creates a new service loader for the given service type, using the extension class loader. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reload](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#reload())`()` Clear this loader's provider cache so that all providers will be reloaded. |
| --- | --- |
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\< [ServiceLoader.Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider)\<S\>!\>! | [stream](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#stream())`()` Returns a stream to lazily load available providers of this loader's service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#toString())`()` Returns a string describing this service. |

## Public methods

### findFirst

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findFirst(): Optional<S>!
```

Load the first available service provider of this loader's service. This convenience method is equivalent to invoking the [iterator()](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#iterator())method and obtaining the first element. It therefore returns the first element from the provider cache if possible, it otherwise attempts to load and instantiate the first provider.

The following example loads the first available service provider. If no service providers are located then it uses a default implementation. 

```kotlin
<code>CodecFactory factory = ServiceLoader.load(CodecFactory.class)
                                         .findFirst()
                                         .orElse(DEFAULT_CODECSET_FACTORY);
  </code>
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional)<S>! | The first service provider or empty`Optional`if no service providers are located |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.ServiceConfigurationError` | If a provider class cannot be loaded for any of the reasons specified in the [Errors](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#errors) section above. |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun iterator(): MutableIterator<S>
```

Returns an iterator to lazily load and instantiate the available providers of this loader's service.

To achieve laziness the actual work of locating and instantiating providers is done by the iterator itself. Its [hasNext](https://developer.android.com/reference/kotlin/java/util/Iterator#hasNext())and [next](https://developer.android.com/reference/kotlin/java/util/Iterator#next())methods can therefore throw a [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError) for any of the reasons specified in the [Errors](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#errors) section above. To write robust code it is only necessary to catch`ServiceConfigurationError`when using the iterator. If an error is thrown then subsequent invocations of the iterator will make a best effort to locate and instantiate the next available provider, but in general such recovery cannot be guaranteed.

Caching: The iterator returned by this method first yields all of the elements of the provider cache, in the order that they were loaded. It then lazily loads and instantiates any remaining service providers, adding each one to the cache in turn. If this loader's provider caches are cleared by invoking the [reload](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#reload())method then existing iterators for this service loader should be discarded. The`hasNext`and`next`methods of the iterator throw if used after the provider cache has been cleared.

The iterator returned by this method does not support removal. Invoking its [remove](https://developer.android.com/reference/kotlin/java/util/Iterator#remove())method will cause an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) to be thrown.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<S> | An iterator that lazily loads providers for this loader's service |

### load

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <S : Any!> load(service: Class<S>!): ServiceLoader<S>!
```

Creates a new service loader for the given service type, using the current thread's [context class loader](https://developer.android.com/reference/kotlin/java/lang/Thread.html#getContextClassLoader()).

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
| `service` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<S\>!:The interface or abstract class representing the service |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)<S>! | A new service loader |

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
| `service` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<S\>!:The interface or abstract class representing the service |
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!:The class loader to be used to load provider-configuration files and provider classes, or`null`if the system class loader (or, failing that, the bootstrap class loader) is to be used |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)<S>! | A new service loader |

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
| `service` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<S\>!:The interface or abstract class representing the service |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [ServiceLoader](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#)<S>! | A new service loader |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.util.ServiceConfigurationError` | if the service type is not accessible to the caller |

### reload

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reload(): Unit
```

Clear this loader's provider cache so that all providers will be reloaded.

After invoking this method, subsequent invocations of the [iterator](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#iterator())or [stream](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#stream())methods will lazily locate providers (and instantiate in the case of`iterator`) from scratch, just as is done by a newly-created service loader.

This method is intended for use in situations in which new service providers can be installed into a running Java virtual machine. 

### stream

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): Stream<ServiceLoader.Provider<S>!>!
```

Returns a stream to lazily load available providers of this loader's service. The stream elements are of type [Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider), the`Provider`'s [get](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider#get())method must be invoked to get or instantiate the provider.

To achieve laziness the actual work of locating providers is done when processing the stream. If a service provider cannot be loaded for any of the reasons specified in the [Errors](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#errors) section above then [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError) is thrown by whatever method caused the service provider to be loaded.

Caching: When processing the stream then providers that were previously loaded by stream operations are processed first, in load order. It then lazily loads any remaining service providers. If this loader's provider caches are cleared by invoking the [reload](https://developer.android.com/reference/kotlin/java/util/ServiceLoader#reload())method then existing streams for this service loader should be discarded. The returned stream's source [spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) is*fail-fast* and will throw [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if the provider cache has been cleared.

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
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)< [ServiceLoader.Provider](https://developer.android.com/reference/kotlin/java/util/ServiceLoader.Provider)<S>!>! | A stream that lazily loads providers for this loader's service |

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this service.

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A descriptive string |
