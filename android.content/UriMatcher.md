# UriMatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UriMatcher

Kotlin| [Java](../android/content/UriMatcher.md) 
| --- | --- |

```
open class UriMatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.UriMatcher](../android/content/UriMatcher.md) |

Utility class to aid in matching URIs in content providers.

To use this class, build up a tree of`UriMatcher`objects. For example: 

```kotlin
private static final int PEOPLE = 1;
    private static final int PEOPLE_ID = 2;
    private static final int PEOPLE_PHONES = 3;
    private static final int PEOPLE_PHONES_ID = 4;
    private static final int PEOPLE_CONTACTMETHODS = 7;
    private static final int PEOPLE_CONTACTMETHODS_ID = 8;
 
    private static final int DELETED_PEOPLE = 20;
 
    private static final int PHONES = 9;
    private static final int PHONES_ID = 10;
    private static final int PHONES_FILTER = 14;
 
    private static final int CONTACTMETHODS = 18;
    private static final int CONTACTMETHODS_ID = 19;
 
    private static final int CALLS = 11;
    private static final int CALLS_ID = 12;
    private static final int CALLS_FILTER = 15;
 
    private static final UriMatcher sURIMatcher = new UriMatcher(UriMatcher.NO_MATCH);
 
    static
    {
        sURIMatcher.addURI("contacts", "people", PEOPLE);
        sURIMatcher.addURI("contacts", "people/#", PEOPLE_ID);
        sURIMatcher.addURI("contacts", "people/#/phones", PEOPLE_PHONES);
        sURIMatcher.addURI("contacts", "people/#/phones/#", PEOPLE_PHONES_ID);
        sURIMatcher.addURI("contacts", "people/#/contact_methods", PEOPLE_CONTACTMETHODS);
        sURIMatcher.addURI("contacts", "people/#/contact_methods/#", PEOPLE_CONTACTMETHODS_ID);
        sURIMatcher.addURI("contacts", "deleted_people", DELETED_PEOPLE);
        sURIMatcher.addURI("contacts", "phones", PHONES);
        sURIMatcher.addURI("contacts", "phones/filter/*", PHONES_FILTER);
        sURIMatcher.addURI("contacts", "phones/#", PHONES_ID);
        sURIMatcher.addURI("contacts", "contact_methods", CONTACTMETHODS);
        sURIMatcher.addURI("contacts", "contact_methods/#", CONTACTMETHODS_ID);
        sURIMatcher.addURI("call_log", "calls", CALLS);
        sURIMatcher.addURI("call_log", "calls/filter/*", CALLS_FILTER);
        sURIMatcher.addURI("call_log", "calls/#", CALLS_ID);
    }
 
```

Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), paths can start with a leading slash. For example: 

```kotlin
sURIMatcher.addURI("contacts", "/people", PEOPLE);
 
```

Then when you need to match against a URI, call [match](../android/content/UriMatcher.md)), providing the URL that you have been given. You can use the result to build a query, return a type, insert or delete a row, or whatever you need, without duplicating all of the if-else logic that you would otherwise need. For example: 

```kotlin
public String getType(Uri url)
    {
        int match = sURIMatcher.match(url);
        switch (match)
        {
            case PEOPLE:
                return "vnd.android.cursor.dir/person";
            case PEOPLE_ID:
                return "vnd.android.cursor.item/person";
 ... snip ...
                return "vnd.android.cursor.dir/snail-mail";
            case PEOPLE_ADDRESS_ID:
                return "vnd.android.cursor.item/snail-mail";
            default:
                return null;
        }
    }
 
```
instead of: 

```kotlin
public String getType(Uri url)
    {
        List<string>
  pathSegments = url.getPathSegments();
        if (pathSegments.size() &gt;= 2) {
            if ("people".equals(pathSegments.get(1))) {
                if (pathSegments.size() == 2) {
                    return "vnd.android.cursor.dir/person";
                } else if (pathSegments.size() == 3) {
                    return "vnd.android.cursor.item/person";
 ... snip ...
                    return "vnd.android.cursor.dir/snail-mail";
                } else if (pathSegments.size() == 3) {
                    return "vnd.android.cursor.item/snail-mail";
                }
            }
        }
        return null;
    }
 
</string>
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_MATCH](../android/content/UriMatcher.md) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UriMatcher](../android/content/UriMatcher.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates the root node of the URI tree. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addURI](../android/content/UriMatcher.md))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a URI to match, and the code to return when this URI is matched. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [match](../android/content/UriMatcher.md))`(`uri:` ` [Uri](../android/net/Uri.md)!`)` Try to match against the path in a url. |

## Constants

### NO_MATCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_MATCH: Int
```  

 Value: -1

## Public constructors

### UriMatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UriMatcher(code: Int)
```

Creates the root node of the URI tree.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code to match for the root URI |

## Public methods

### addURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addURI(
    authority: String!, 
    path: String!, 
    code: Int
): Unit
```

Add a URI to match, and the code to return when this URI is matched. URI nodes may be exact match string, the token "\*" that matches any text, or the token "#" that matches only numbers.

Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md), this method will accept a leading slash in the path.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the authority to match |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to match. \* may be used as a wild card for any text, and # may be used as a wild card for numbers. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code that is returned when a URI is matched against the given components. Must be positive. |
| --- | --- |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun match(uri: Uri!): Int
```

Try to match against the path in a url.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md)!:The url whose path we will match against. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The code for the matched node (added using addURI), or -1 if there is no matched node. |
