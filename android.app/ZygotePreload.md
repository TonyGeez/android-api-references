# ZygotePreload

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZygotePreload

Kotlin| [Java](https://developer.android.com/reference/android/app/ZygotePreload "View this page in Java") 

```
interface ZygotePreload
```

| [android.app.ZygotePreload](https://developer.android.com/reference/kotlin/android/app/ZygotePreload#) |

This is the interface to be implemented for the class that is specified by the [android:zygotePreloadName](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_zygotePreloadName:kotlin.Int) of the \<application\> tag. It is responsible for preloading application code and data, that will be shared by all isolated services that have the [android:useAppZygote](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService_useAppZygote:kotlin.Int) attribute of the \<service\> tag set to`true`. Note that implementations of this class must provide a default constructor with no arguments.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doPreload](https://developer.android.com/reference/kotlin/android/app/ZygotePreload#doPreload(android.content.pm.ApplicationInfo))`(`appInfo:` ` [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)`)` This method is called once every time the Application Zygote is started. |

## Public methods

### doPreload

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doPreload(appInfo: ApplicationInfo): Unit
```

This method is called once every time the Application Zygote is started. It is normally started the first time an isolated service that uses it is started. The Application Zygote will be stopped when all isolated services that use it are stopped.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#):The ApplicationInfo object belonging to the application This value cannot be`null`. |
