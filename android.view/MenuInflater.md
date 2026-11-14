# MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuInflater

Kotlin| [Java](../android/view/MenuInflater.md) 
| --- | --- |

```
open class MenuInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.MenuInflater](../android/view/MenuInflater.md) |

This class is used to instantiate menu XML files into Menu objects.

For performance reasons, menu inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use MenuInflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something*file.)

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MenuInflater](../android/view/MenuInflater.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Constructs a menu inflater. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](../android/view/MenuInflater.md))`(`menuRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](../android/view/Menu.md)!`)` Inflate a menu hierarchy from the specified XML resource. |

## Public constructors

### MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MenuInflater(context: Context!)
```

Constructs a menu inflater. 
**See Also**

- [android.app.Activity#getMenuInflater()](../android/app/Activity.md))

## Public methods

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    menuRes: Int, 
    menu: Menu!
): Unit
```

Inflate a menu hierarchy from the specified XML resource. Throws [InflateException](../android/view/InflateException.md) if there is an error.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID for an XML layout resource to load (e.g.,`R.menu.main_activity`) |
| `menu` | [Menu](../android/view/Menu.md)!:The Menu to inflate into. The items and submenus will be added to this Menu. |
