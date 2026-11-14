# Cloneable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cloneable

```
interface Cloneable
```

| [java.lang.Cloneable](../java/lang/Cloneable.md) |

A class implements the`Cloneable`interface to indicate to the [java.lang.Object#clone()](../java/lang/Object.md))method that it is legal for that method to make a field-for-field copy of instances of that class.

Invoking Object's clone method on an instance that does not implement the`Cloneable`interface results in the exception`CloneNotSupportedException`being thrown.

By convention, classes that implement this interface should override`Object.clone`(which is protected) with a public method. See [java.lang.Object#clone()](../java/lang/Object.md))for details on overriding this method.

Note that this interface does*not* contain the`clone`method. Therefore, it is not possible to clone an object merely by virtue of the fact that it implements this interface. Even if the clone method is invoked reflectively, there is no guarantee that it will succeed.

## Summary
