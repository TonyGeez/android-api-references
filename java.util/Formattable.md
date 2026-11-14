Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Formattable

```
interface Formattable
```

| [java.util.Formattable](Formattable.md) |

The `Formattable` interface must be implemented by any class that needs to perform custom formatting using the `'s'` conversion specifier of Formatter. This interface allows basic control for formatting arbitrary objects. For example, the following class prints out different representations of a stock's name depending on the flags and length constraints:

```kotlin
<code>import java.nio.CharBuffer;
    import java.util.Formatter;
    import java.util.Formattable;
    import java.util.Locale;
    import static java.util.FormattableFlags.*;
 
    ...
 
    public class StockName implements Formattable {
        private String symbol, companyName, frenchCompanyName;
        public StockName(String symbol, String companyName,
                         String frenchCompanyName) {
            ...
        }
 
        ...
 
        public void formatTo(Formatter fmt, int f, int width, int precision) {
            StringBuilder sb = new StringBuilder();
 
            // decide form of name
            String name = companyName;
            if (fmt.locale().equals(Locale.FRANCE))
                name = frenchCompanyName;
            boolean alternate = (f &amp; ALTERNATE) == ALTERNATE;
            boolean usesymbol = alternate || (precision != -1 &amp;&amp; precision &lt; 10);
            String out = (usesymbol ? symbol : name);
 
            // apply precision
            if (precision == -1 || out.length() &lt; precision) {
                // write it all
                sb.append(out);
            } else {
                sb.append(out.substring(0, precision - 1)).append('*');
            }
 
            // apply width and justification
            int len = sb.length();
            if (len &lt; width)
                for (int i = 0; i &lt; width - len; i++)
                    if ((f &amp; LEFT_JUSTIFY) == LEFT_JUSTIFY)
                        sb.append(' ');
                    else
                        sb.insert(0, ' ');
 
            fmt.format(sb.toString());
        }
 
        public String toString() {
            return String.format("%s - %s", symbol, companyName);
        }
    }
  </code>
```

<br />

When used in conjunction with the Formatter, the above class produces the following output for various format strings.

```kotlin
<code>Formatter fmt = new Formatter();
    StockName sn = new StockName("HUGE", "Huge Fruit, Inc.",
                                 "Fruit Titanesque, Inc.");
    fmt.format("%s", sn);                   //   -&gt; "Huge Fruit, Inc."
    fmt.format("%s", sn.toString());        //   -&gt; "HUGE - Huge Fruit, Inc."
    fmt.format("%#s", sn);                  //   -&gt; "HUGE"
    fmt.format("%-10.8s", sn);              //   -&gt; "HUGE      "
    fmt.format("%.12s", sn);                //   -&gt; "Huge Fruit,*"
    fmt.format(Locale.FRANCE, "%25s", sn);  //   -&gt; "   Fruit Titanesque, Inc."
  </code>
```

Formattables are not necessarily safe for multithreaded access. Thread safety is optional and may be enforced by classes that extend and implement this interface.

Unless otherwise specified, passing a `null` argument to any method in this interface will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` to be thrown.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | formatTo Formats the object using the provided Formatter. |

## Public methods

### formatTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun formatTo(
    formatter: Formatter!, 
    flags: Int, 
    width: Int, 
    precision: Int
): Unit
```

Formats the object using the provided Formatter.

| Parameters ||
|---|---|
| `formatter` | [Formatter](Formatter.md)!: The Formatter. Implementing classes may call out or locale to obtain the `https://developer.android.com/reference/kotlin/java/lang/Appendable.html#` or Locale used by this `formatter` respectively. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags modify the output format. The value is interpreted as a bitmask. Any combination of the following flags may be set: `https://developer.android.com/reference/kotlin/java/util/FormattableFlags#LEFT_JUSTIFY:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/FormattableFlags#UPPERCASE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/FormattableFlags#ALTERNATE:kotlin.Int`. If no flags are set, the default formatting of the implementing class will apply. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of characters to be written to the output. If the length of the converted value is less than the `width` then the output will be padded by `' '` until the total number of characters equals width. The padding is at the beginning by default. If the `https://developer.android.com/reference/kotlin/java/util/FormattableFlags#LEFT_JUSTIFY:kotlin.Int` flag is set then the padding will be at the end. If `width` is `-1` then there is no minimum. |
| --- | --- |
| `precision` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of characters to be written to the output. The precision is applied before the width, thus the output will be truncated to `precision` characters even if the `width` is greater than the `precision`. If `precision` is `-1` then there is no explicit limit on the number of characters. |

| Exceptions ||
|---|---|
| `java.util.IllegalFormatException` | If any of the parameters are invalid. For specification of all possible formatting errors, see the [Details](Formatter.md) section of the formatter class specification. |
