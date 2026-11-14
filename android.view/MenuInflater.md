# MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuInflater

Kotlin| [Java](https://developer.android.com/reference/android/view/MenuInflater "View this page in Java") 
| --- | --- |

```
open class MenuInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater#) |

This class is used to instantiate menu XML files into Menu objects.

For performance reasons, menu inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use MenuInflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something*file.)

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater#MenuInflater(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Constructs a menu inflater. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/view/MenuInflater#inflate(kotlin.Int,%20android.view.Menu))`(`menuRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!`)` Inflate a menu hierarchy from the specified XML resource. |

## Public constructors

### MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MenuInflater(context: Context!)
```

Constructs a menu inflater. 
**See Also**

- [android.app.Activity#getMenuInflater()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getMenuInflater())

## Public methods

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    menuRes: Int, 
    menu: Menu!
): Unit
```

Inflate a menu hierarchy from the specified XML resource. Throws [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) if there is an error.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID for an XML layout resource to load (e.g.,`R.menu.main_activity`) |
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu)!:The Menu to inflate into. The items and submenus will be added to this Menu. |
