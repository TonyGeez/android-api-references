Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppComponentFactory

Kotlin | [Java](AppComponentFactory.md)
| --- | --- |

```
open class AppComponentFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AppComponentFactory](AppComponentFactory.md) |

Interface used to control the instantiation of manifest elements.

## Summary

| Public constructors ||
|---|---|
| AppComponentFactory <br /> |

| Public methods ||
|---|---|
| open [Activity](Activity.md) | instantiateActivity Allows application to override the creation of activities. |
| open [Application](Application.md) | instantiateApplication Allows application to override the creation of the application object. |
| open [ClassLoader](../java.lang/ClassLoader.md) | instantiateClassLoader Selects the class loader which will be used by the platform to instantiate app components. |
| --- | --- |
| open [ContentProvider](../android.content/ContentProvider.md) | instantiateProvider Allows application to override the creation of providers. |
| open [BroadcastReceiver](../android.content/BroadcastReceiver.md) | instantiateReceiver Allows application to override the creation of receivers. |
| open [Service](Service.md) | instantiateService Allows application to override the creation of services. |
| --- | --- |

## Public constructors

### AppComponentFactory

```
AppComponentFactory()
```

## Public methods

### instantiateActivity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateActivity(
    cl: ClassLoader, 
    className: String, 
    intent: Intent?
): Activity
```

Allows application to override the creation of activities. This can be used to perform things such as dependency injection or class loader changes to these classes.

This method is only intended to provide a hook for instantiation. It does not provide earlier access to the Activity object. The returned object will not be initialized as a Context yet and should not be used to interact with other android APIs.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default classloader to use for instantiation. This value cannot be `null`. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The class to be instantiated. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md)?: Intent creating the class. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| Activity | This value cannot be `null`. |

### instantiateApplication

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateApplication(
    cl: ClassLoader, 
    className: String
): Application
```

Allows application to override the creation of the application object. This can be used to perform things such as dependency injection or class loader changes to these classes.

This method is only intended to provide a hook for instantiation. It does not provide earlier access to the Application object. The returned object will not be initialized as a Context yet and should not be used to interact with other android APIs.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default classloader to use for instantiation. This value cannot be `null`. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The class to be instantiated. This value cannot be `null`. |

| Return ||
|---|---|
| Application | This value cannot be `null`. |

### instantiateClassLoader

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateClassLoader(
    cl: ClassLoader, 
    aInfo: ApplicationInfo
): ClassLoader
```

Selects the class loader which will be used by the platform to instantiate app components.

The default implementation of this method returns the `cl` parameter unchanged. Applications can override this method to set up a custom class loader or a custom class loader hierarchy and return it to the platform.

The method is a hook invoked before any application components are instantiated or the application Context is initialized. It is intended to allow the application's classes to be loaded from a different source than the base/split APK(s).

The default class loader `cl` is created by the platform and used to load the application's base or split APK(s). Its parent is typically the boot class loader, unless running under instrumentation. Its classname is configurable using the `https://developer.android.com/reference/kotlin/android/R.attr.html#classLoader:kotlin.Int` manifest attribute.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default class loader created by the platform. This value cannot be `null`. |
| `aInfo` | [ApplicationInfo](../android.content.pm/ApplicationInfo.md): Information about the application being loaded. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` | This value cannot be `null`. |

### instantiateProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateProvider(
    cl: ClassLoader, 
    className: String
): ContentProvider
```

Allows application to override the creation of providers. This can be used to perform things such as dependency injection or class loader changes to these classes.

This method is only intended to provide a hook for instantiation. It does not provide earlier access to the ContentProvider object. The returned object will not be initialized with a Context yet and should not be used to interact with other android APIs.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default classloader to use for instantiation. This value cannot be `null`. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The class to be instantiated. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` | This value cannot be `null`. |

### instantiateReceiver

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateReceiver(
    cl: ClassLoader, 
    className: String, 
    intent: Intent?
): BroadcastReceiver
```

Allows application to override the creation of receivers. This can be used to perform things such as dependency injection or class loader changes to these classes.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default classloader to use for instantiation. This value cannot be `null`. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The class to be instantiated. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md)?: Intent creating the class. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` | This value cannot be `null`. |

### instantiateService

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun instantiateService(
    cl: ClassLoader, 
    className: String, 
    intent: Intent?
): Service
```

Allows application to override the creation of services. This can be used to perform things such as dependency injection or class loader changes to these classes.

This method is only intended to provide a hook for instantiation. It does not provide earlier access to the Service object. The returned object will not be initialized as a Context yet and should not be used to interact with other android APIs.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md): The default classloader to use for instantiation. This value cannot be `null`. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The class to be instantiated. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md)?: Intent creating the class. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| Service | This value cannot be `null`. |
