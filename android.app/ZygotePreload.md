# ZygotePreload

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZygotePreload

Kotlin| [Java](../android/app/ZygotePreload.md) 
| --- | --- |

```
interface ZygotePreload
```

| [android.app.ZygotePreload](../android/app/ZygotePreload.md) |

This is the interface to be implemented for the class that is specified by the [android:zygotePreloadName](../android/R.styleable.md) of the \<application\> tag. It is responsible for preloading application code and data, that will be shared by all isolated services that have the [android:useAppZygote](../android/R.styleable.md) attribute of the \<service\> tag set to`true`. Note that implementations of this class must provide a default constructor with no arguments.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doPreload](../android/app/ZygotePreload.md))`(`appInfo:` ` [ApplicationInfo](../android/content/pm/ApplicationInfo.md)`)` This method is called once every time the Application Zygote is started. |

## Public methods

### doPreload

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doPreload(appInfo: ApplicationInfo): Unit
```

This method is called once every time the Application Zygote is started. It is normally started the first time an isolated service that uses it is started. The Application Zygote will be stopped when all isolated services that use it are stopped.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appInfo` | [ApplicationInfo](../android/content/pm/ApplicationInfo.md):The ApplicationInfo object belonging to the application This value cannot be`null`. |
