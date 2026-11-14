Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextShaper

```
open class TextShaper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.TextShaper](TextShaper.md) |

Provides text shaping for multi-styled text. Here is an example of animating text size and letter spacing for simple text.

```kotlin
<code>
  // In this example, shape the text once for start and end state, then animate between two shape
  // result without re-shaping in each frame.
  class SimpleAnimationView @JvmOverloads constructor(
          context: Context,
          attrs: AttributeSet? = null,
          defStyleAttr: Int = 0
  ) : View(context, attrs, defStyleAttr) {
      private val textDir = TextDirectionHeuristics.LOCALE
      private val text = "Hello, World."  // The text to be displayed
 
      // Class for keeping drawing parameters.
      data class DrawStyle(val textSize: Float, val alpha: Int)
 
      // The start and end text shaping result. This class will animate between these two.
      private val start = mutableListOf&lt;Pair&lt;PositionedGlyphs, DrawStyle&gt;&gt;()
      private val end = mutableListOf&lt;Pair&lt;PositionedGlyphs, DrawStyle&gt;&gt;()
 
      init {
          val startPaint = TextPaint().apply {
              alpha = 0 // Alpha only affect text drawing but not text shaping
              textSize = 36f // TextSize affect both text shaping and drawing.
              letterSpacing = 0f // Letter spacing only affect text shaping but not drawing.
          }
 
          val endPaint = TextPaint().apply {
              alpha = 255
              textSize =128f
              letterSpacing = 0.1f
          }
 
          TextShaper.shapeText(text, 0, text.length, textDir, startPaint) { _, _, glyphs, paint -&gt;
              start.add(Pair(glyphs, DrawStyle(paint.textSize, paint.alpha)))
          }
          TextShaper.shapeText(text, 0, text.length, textDir, endPaint) { _, _, glyphs, paint -&gt;
              end.add(Pair(glyphs, DrawStyle(paint.textSize, paint.alpha)))
          }
      }
 
      override fun onDraw(canvas: Canvas) {
          super.onDraw(canvas)
 
          // Set the baseline to the vertical center of the view.
          canvas.translate(0f, height / 2f)
 
          // Assume the number of PositionedGlyphs are the same. If different, you may want to
          // animate in a different way, e.g. cross fading.
          start.zip(end) { (startGlyphs, startDrawStyle), (endGlyphs, endDrawStyle) -&gt;
              // Tween the style and set to paint.
              paint.textSize = lerp(startDrawStyle.textSize, endDrawStyle.textSize, progress)
              paint.alpha = lerp(startDrawStyle.alpha, endDrawStyle.alpha, progress)
 
              // Assume the number of glyphs are the same. If different, you may want to animate in
              // a different way, e.g. cross fading.
              require(startGlyphs.glyphCount() == endGlyphs.glyphCount())
 
              if (startGlyphs.glyphCount() == 0) return@zip
 
              var curFont = startGlyphs.getFont(0)
              var drawStart = 0
              for (i in 1 until startGlyphs.glyphCount()) {
                  // Assume the pair of Glyph ID and font is the same. If different, you may want
                  // to animate in a different way, e.g. cross fading.
                  require(startGlyphs.getGlyphId(i) == endGlyphs.getGlyphId(i))
                  require(startGlyphs.getFont(i) === endGlyphs.getFont(i))
 
                  val font = startGlyphs.getFont(i)
                  if (curFont != font) {
                      drawGlyphs(canvas, startGlyphs, endGlyphs, drawStart, i, curFont, paint)
                      curFont = font
                      drawStart = i
                  }
              }
              if (drawStart != startGlyphs.glyphCount() - 1) {
                  drawGlyphs(canvas, startGlyphs, endGlyphs, drawStart, startGlyphs.glyphCount(),
                          curFont, paint)
              }
          }
      }
 
      // Draws Glyphs for the same font run.
      private fun drawGlyphs(canvas: Canvas, startGlyph: PositionedGlyphs,
                             endGlyph: PositionedGlyphs, start: Int, end: Int, font: Font,
                             paint: Paint) {
          var cacheIndex = 0
          for (i in start until end) {
              intArrayCache[cacheIndex] = startGlyph.getGlyphId(i)
              // The glyph positions are different from start to end since they are shaped
              // with different letter spacing. Use linear interpolation for positions
              // during animation.
              floatArrayCache[cacheIndex * 2] =
                      lerp(startGlyph.getGlyphX(i), endGlyph.getGlyphX(i), progress)
              floatArrayCache[cacheIndex * 2 + 1] =
                      lerp(startGlyph.getGlyphY(i), endGlyph.getGlyphY(i), progress)
              if (cacheIndex == CACHE_SIZE) {  // Cached int array is full. Flashing.
                  canvas.drawGlyphs(
                          intArrayCache, 0, // glyphID array and its starting offset
                          floatArrayCache, 0, // position array and its starting offset
                          cacheIndex, // glyph count
                          font,
                          paint
                  )
                  cacheIndex = 0
              }
              cacheIndex++
          }
          if (cacheIndex != 0) {
              canvas.drawGlyphs(
                      intArrayCache, 0, // glyphID array and its starting offset
                      floatArrayCache, 0, // position array and its starting offset
                      cacheIndex, // glyph count
                      font,
                      paint
              )
          }
      }
 
      // Linear Interpolator
      private fun lerp(start: Float, end: Float, t: Float) = start * (1f - t) + end * t
      private fun lerp(start: Int, end: Int, t: Float) = (start * (1f - t) + end * t).toInt()
 
      // The animation progress.
      var progress: Float = 0f
          set(value) {
              field = value
              invalidate()
          }
 
      // working copy of paint.
      private val paint = Paint()
 
      // Array cache for reducing allocation during drawing.
      private var intArrayCache = IntArray(CACHE_SIZE)
      private var floatArrayCache = FloatArray(CACHE_SIZE * 2)
  }
  </code>
```

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/text/TextShaper.GlyphsConsumer` A consumer interface for accepting text shape result. |

| Public methods ||
|---|---|
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | shapeText Shape multi-styled text. |

## Public methods

### shapeText

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun shapeText(
    text: CharSequence, 
    start: Int, 
    count: Int, 
    dir: TextDirectionHeuristic, 
    paint: TextPaint, 
    consumer: TextShaper.GlyphsConsumer
): Unit
```

Shape multi-styled text. In the LTR context, the shape result will go from left to right, thus you may want to draw glyphs from left most position of the canvas. In the RTL context, the shape result will go from right to left, thus you may want to draw glyphs from right most position of the canvas.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): a styled text. This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a start index of shaping target in the text. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a length of shaping target in the text. Value is 0 or greater |
| --- | --- |
| `dir` | [TextDirectionHeuristic](TextDirectionHeuristic.md): a text direction. This value cannot be `null`. |
| `paint` | [TextPaint](TextPaint.md): a paint. This value cannot be `null`. |
| `consumer` | [TextShaper.GlyphsConsumer](../android/text/TextShaper.GlyphsConsumer.md): a consumer of the shape result. This value cannot be `null`. |
| --- | --- |
